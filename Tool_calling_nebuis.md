AI Models Inference
Function calling & Tools
Learn how to make models select functions to extend their capabilities

Function calling allows you to enhance a model’s capabilities by integrating it with external code, services, or APIs. You can define a set of functions—also referred to as tools—that the model can call. Based on the context provided in the conversation, the model can intelligently decide which functions to invoke and suggest appropriate arguments.
This capability enables you to build more powerful agents that can:
Run custom code
Retrieve real-time data
Interact with third-party services
Connect to MCP servers
And perform other dynamic actions
Important: The model does not execute the functions itself. Instead, it outputs tool invocation instructions in an OpenAI-compatible function calling format. You are responsible for parsing these outputs and executing the corresponding functions on your backend or client side.
1
Define Available Tools

Start by specifying the tools (functions) the model can use. Each tool is described using a JSON Schema that defines its name, input parameters, and expected data types. This schema informs the model how each tool should be invoked.
2
Model Determines Intent

When the model receives a user query, it analyzes the intent and decides how to respond. Based on the context and the tools available, it may:
Respond conversationally, or
Propose a function call by selecting a relevant tool and filling in the required arguments according to the schema.
3
Execute and Iterate

If a function call is proposed, your system is responsible for executing the function with the provided arguments. You then pass the function’s output back to the model as part of the next prompt. This allows the conversation to continue seamlessly, with the model incorporating the function result into its response or triggering further tool use.API Example
​
Limitations
The tool_choice parameter controls how the model selects which function (tool) to use. It determines whether the model should choose a tool automatically or follow an explicit instruction. Supported values include:
"auto"
The model automatically selects the most appropriate function based on the context of the prompt. This is the default behavior and is useful for most use cases.
Explicit Function Call
You can instruct the model to call a specific function using the following structure:
{
  "type": "function",
  "function": {
    "name": "read_file"
  }
}
This forces the model to call the read_file function regardless of context, overriding its own tool selection logic.
​
API Example

Python

JavaScript

import json
import os

from pydantic import BaseModel, Field
from typing import Literal
from openai import OpenAI

client = OpenAI(
    base_url="https://api.tokenfactory.nebius.com/v1/",
    api_key=os.getenv("NEBIUS_API_KEY")
)

model = "meta-llama/Meta-Llama-3.1-8B-Instruct-fast"

class GetCurrentWeatherParams(BaseModel):
    city: str = Field(
        ...,
        description="The city to find the weather for, e.g. 'San Francisco'"
    )
    state: str = Field(
        ...,
        description=(
            "The two-letter abbreviation for the state that the city is in, "
            "e.g. 'CA' for California"
        )
    )
    unit: Literal['celsius', 'fahrenheit'] = Field(
        ...,
        description="The unit to fetch the temperature in"
    )

tools = [{
    "type": "function",
    "function": {
        "name": "get_current_weather",
        "description": "Get the current weather in a given location",
        "parameters": GetCurrentWeatherParams.model_json_schema()
    }
}]

messages = [
    {
        "role": "user",
        "content": "Hi! How are you doing today?"
    },
    {
        "role": "assistant",
        "content": "I'm doing well! How can I help you?"
    },
    {
        "role": "user",
        "content": (
            "Can you tell me what the temperature will be in Dallas, "
            "in Fahrenheit?"
        )
    }
]

chat_completion = client.chat.completions.create(
    messages=messages,
    model=model,
    tools=tools,
    tool_choice={
        "type": "function",
        "function": {
            "name": "get_current_weather"
        }
    }
)

messages.append({
    "role": "assistant",
    "tool_calls": chat_completion.choices[0].message.tool_calls
})

# Simulate a tool call
def get_current_weather(city: str, state: str, unit: 'str'):
    return (
      "The weather in Dallas, Texas is 85 degrees Fahrenheit. "
      "It is partly cloudy, with highs in the 90's."
    )


available_tools = {"get_current_weather": get_current_weather}

completion_tool_calls = chat_completion.choices[0].message.tool_calls
for call in completion_tool_calls:
    tool_to_call = available_tools[call.function.name]
    args = json.loads(call.function.arguments)
    result = tool_to_call(**args)
    print(result)
    messages.append({
        "role": "tool",
        "content": result,
        "tool_call_id": call.id,
        "name": call.function.name
    })
See all 98 lines
Messages array with response:
[
  {
    "role": "user",
    "content": "Hi! How are you doing today?"
  },
  {
    "role": "assistant",
    "content": "I'm doing well! How can I help you?"
  },
  {
    "role": "user",
    "content": "Can you tell me what the temperature will be in Dallas, in Fahrenheit?"
  },
  {
    "role": "assistant",
    "tool_calls": [
      {
        "id": "chatcmpl-tool-99a7259c139e4aa986549d07cde8df8f",
        "type": "function",
        "function": {
          "name": "get_current_weather",
          "arguments": "{ \"city\" : \"Dallas\" , \"state\": \"Texas\", \"unit\": \"fahrenheit\" }"
        }
      }
    ]
  },
  {
    "role": "tool",
    "content": "The weather in Dallas, Texas is 85 degrees fahrenheit. It is partly cloudy, with highs in the 90's.",
    "tool_call_id": "chatcmpl-tool-99a7259c139e4aa986549d07cde8df8f",
    "name": "get_current_weather"
  }
]
See all 33 lines
​
Try it in our Cookbook
Function & Tool Calling Cookbook
​
Function calling in Playground
You can explore Function Calling capabilities of models directly in the Playground:
Go to the “Model Parameters” section.
In the “Function calling” section add function description
Enter your prompt and run it to test whether the model returns the expected function selection for your use case.
