

[Page 1]
[BOX: Check for updates]

# A Layman's Guide to Bitcoin and Blockchain

Bhagwan Chowdhry and Seoyoung Kim

The recent, meteoric rise in crypto-activity has sparked widespread interest in this nascent asset class, which now comprises over 5000 distinct exchange-traded cryptocurrencies.¹ Worldwide google queries for the term "cryptocurrency" increased by more than fivefold in the final two months of 2017, during which time the search queries for “bitcoin” exceeded those for "trump" (see Fig. 1). There are now over 6000 Bitcoin ATMs across the world (Zmudzinski 2019),² and the average daily exchanged-traded dollar volume for Bitcoin (BTC) has tripled in the last year,³ with the latest daily activity averaging at $27.5 billion USD for January 2020. In comparison, the average daily dollar volume for MSFT stock was approximately $4.4 billion USD during this same timeframe.

---

¹ As per CoinMarketCap https://coinmarketcap.com on February 5, 2020.  
² See https://cointelegraph.com/news/bitcoin-atms-worldwide-hit-new-milestone-surpassing-6-000.  
³ Specifically, Bitcoin's average daily dollar volume in 2018 and 2019 was $16.7BN and $6.1BN (USD), respectively, as per historical data provided by CoinMarketCap.

---

B. Chowdhry (✉)  
Indian School of Business, Hyderabad, India  
e-mail: bhagwan@isb.edu

S. Kim  
Santa Clara University, Santa Clara, CA, USA  
e-mail: srkim@scu.edu

© The Author(s), under exclusive license to Springer Nature  
Switzerland AG 2021  
R. Rau et al. (eds.), *The Palgrave Handbook of Technological Finance*,  
https://doi.org/10.1007/978-3-030-65117-6_3

[Page 2]
62
B. Chowdhry and S. Kim

[CHART: A line graph titled "Weekly Google Trends" showing the relative search interest for "cryptocurrency", "bitcoin", and "trump" from January 2017 to January 2018. The y-axis is "Relative Search Interest" from 0 to 100. The x-axis shows dates. The "bitcoin" line shows a dramatic increase in late 2017, peaking at 100. The "cryptocurrency" line shows a smaller, similar increase. The "trump" line starts high and decreases over the year.]

**Fig. 1** Worldwide Interest in “Cryptocurrency” and “Bitcoin” (Source Google Trends). In this figure, we display the weekly, worldwide Google-search interest in the terms “cryptocurrency”, “bitcoin”, and “trump” over the period spanning January 1, 2017 through January 1, 2018. The relative search interest is scaled such that 100 represents the peak popularity for a term in the given time frame for provided search-term opportunity set: {“cryptocurrency”; “bitcoin”; “trump”}. See https://trends.google.com for further details

Despite the ongoing activity and interest in Bitcoin and the elusive "Satoshi Nakamoto," whose whitepaper has now been translated into almost 30 different languages,^4,^5 this digital asset remains widely misunderstood. Although many now recognize Bitcoin as a disintermediated medium of exchange, there remains confusion surrounding who "runs" Bitcoin and how we can be confident in the security of a permissionless shared ledger in the way that we place confidence in Bank of America, as a trusted third party, to keep a proper record of funds. That is, Bitcoin was designed to provide "an electronic payment system based on cryptographic proof instead of trust, allowing any two willing parties to transact without the need for a trusted third party" (Nakamoto 2008).^6 But what exactly does this mean and how is it implemented?

Furthermore, the possibility of creating "trust" without using an intermediary such as a bank, a regulatory body, or government suggests many

---
^4 The Github repository can be accessed on https://github.com/wbnns/bitcoinwhitepaper.

^5 "Nakamoto" was even nominated for the 2016 Nobel Prize in Economics (Chowdhry 2016).

^6 See page 1 of the original Bitcoin whitepaper, accessed on https://bitcoin.org/bitcoin.pdf.

[Page 3]
[CHART: A diagram showing three blocks in a chain, labeled Block N (time t), Block N+1 (time t + 10 min), and Block N+2 (time t + 20 min). Arrows link them sequentially from left to right. Each block contains the text 'Double SHA-256' with a formula, ellipses, and '[last record]'. The formulas are (Block$_{N-1}$ + nonce$_{N-1}$), (Block$_N$ + nonce$_N$), and (Block$_{N+1}$ + nonce$_{N+1}$) respectively.]

**Fig. 2 The Bitcoin Blockchain.** This figure graphically depicts a simplified version of the Bitcoin blockchain, which requires miners to find the winning “nonce” to close out a block of transactions records and to begin a new block. This nonce, when combined with the elements of the current block, must produce a double SHA-256 hash code with a minimum number of leading zeros. The first miner to find this nonce can close the current block and begin a new block, whose header will contain this nonce in addition to other pieces of information that link the new block to the prior one. Once this information is broadcast, other miners can easily verify that the new block was validly formed, and a new proof-of-work mining race begins

[Page 4]
64
B. Chowdhry and S. Kim

interesting use cases beyond financial transactions. This trustless security is
the promise of distributed ledger technology in general. A public blockchain
is a mechanism by which to store data, distributed across vast, peer-to-peer
networks. Transactions or records are grouped into blocks that are chained
to each other using cryptographic links. Blocks are verified and synchro-
nized across many nodes only through agreement across various nodes of the
network, a mechanism known as distributed consensus. Blockchain delivers
immutability (i.e., it is impossible to modify past blocks of data unless a
majority of nodes in the network collude, which is an unlikely and expensive
situation as the network scales), and a reliable provenance of the transaction
paths.

The focus of this chapter is to provide a layman's guide to Bitcoin and to
explain the basic underpinnings of the consensus protocol (also known as the
Nakamoto Consensus) that secures transactions on the Bitcoin blockchain.⁷,⁸

# 1 An Intuitive Introduction

## 1.1 Numbers

Numbers are everywhere. We use numbers to count. Humans, because they
have ten fingers, started using a decimal system that requires ten symbols: 0,
1, 2, 3, 4, 5, 6, 7, 8, and 9. When we need to represent a number larger than
9, we begin using a second digit (i.e., 10, 11, 12 to 99) and then proceed to
a third digit (i.e., 100, 101, 102) and so on.

Computers employ a binary system that uses only two symbols: 0 and 1.
The counting in a binary system proceeds as 0, 1, 10, 11, 100, 101, and so
on. Thus, 10 in binary is equivalent to 2 in the decimal system.

The binary system has a big advantage in that it is easy to make hard-
ware that can be represented by 0s and 1s (e.g., OFF and ON). So, it is
easy to build computers that only require switches that can be turned off
and on. Furthermore, 0 and 1 can also represent False and True, or No and
Yes, allowing us to represent any logical statement as a sequence of 0s and
1s. This was the remarkable insight by one of the greatest mathematicians,
Claude Shannon, who founded information theory in the 1930s and 1940s.

---
⁷ See Kim et al. (2018) for a generalized overview of cryptocurrencies, including but not limited to
Bitcoin.

⁸ For examples of other blockchain-based platforms and additional use cases, “Blockchain for
Dummies, 2nd Edition" (Laurence 2019).

[Page 5]
Alan Turing around the same time also showed that any computer language could be reduced to a sequence of 0s and 1s.

In the late 1950s, it was discovered that the basic building block of life itself only required four molecules (A, T, G, C) that makes the DNA molecule, and thus, the genome of any living being could also be represented by a number with four symbols, which could be 0 (A), 1 (T), 2 (G), and 3 (C). Of course, any number in a system of base 4 could equivalently be represented as a binary number. It is easy to see that any language with a finite set of letters in the alphabet could also be equivalently represented as a number in a binary system. For example, the English language would require 52 symbols to represent all 26 letters of the alphabet in lower and upper case, plus a few additional symbols to denote punctuation marks such as the period and the comma. In fact, our experience with fossil records has indicated that DNA can be preserved for hundreds of thousands of years without requiring any energy sources. Recent exciting advances are, in fact, exploring the use of information preservation using DNA (Lee 2019).[^9]

So then, a binary sequence could represent a (i) number, (ii) any message in any language or any document that could be represented as a digital file, (iii) a person identified by her genomic sequence, or (iv) any set of logical instructions—e.g., if X then Y else Z—or even any detailed algorithm or a computer program.

In order to economize on the number of digits, a hexadecimal system is often used instead of a binary system. Since a hexadecimal system requires sixteen symbols, “0” to “9” plus “a” to “f” are typically used. So “e3b,” for example, is a number in the hexadecimal system which is equivalent to $(14 \times 16^2) + (3 \times 16^1) + (11 \times 16^0) = 3643$ in the decimal system and 111000111011 in the binary system.

## 1.2 A Unique “Fingerprint” Number for Everything Interesting (SHA256 Hash)

We have now established that almost every interesting thing that exists (e.g., a document, a transaction, a computer program, a person, a book, the first edition of Encyclopedia Britannica, a movie, all of Wikipedia at the current moment, and so on) can be represented as a number. Suppose that each one of these things could be assigned an ID or a unique number (i.e., a *fingerprint*). How many binary digits would be sufficient to represent all such objects? The

[^9]: See, for instance, https://www.scientificamerican.com/article/dna-data-storage-is-closer-than-you-think/.

[Page 6]
number of interesting objects for which we need IDs might be a very large number, say a trillion x trillion x trillion (i.e., $10^{12} \times 10^{12} \times 10^{12}$, since $10^{12}$ in the decimal system is one trillion). This sequence can also be written as $(10 \times 10 \times 10)^{12}$. Since $2^{10} = 1024$, which is approximately equal to $10 \times 10 \times 10$, a trillion x trillion x trillion can also be expressed as $(2^{10})^{12}$ or $2^{120}$. That is, 120 binary digits would be enough to represent all IDs required to uniquely identify one trillion x trillion x trillion objects.

Suppose that, rather than using just 120 digits, we allow each ID to be represented by a 256-digit binary number. This extension allows an incredibly large number of IDs, approximately equal to the number of atoms in one trillion solar systems. Surely, if we were to distribute one trillion x trillion x trillion IDs using a 256-digit binary number, the number of IDs issued would be a vanishingly small fraction of the total potential IDs available. Furthermore, if IDs were issued randomly from the available pool of $2^{256}$ IDs, knowing the ID would provide no indication as to which object (which itself is represented by a number) it represents. The SHA-256 hash, where SHA refers to Secure Hash Algorithm, provides such an ID.

For each object, the SHA-256 hash code is fixed. That is, hash functions are deterministic, and the same input always yields the same hash code. However, because there are $2^{256}$ possible SHA-256 codes, it would be incredibly difficult to guess which object(s) generated a given SHA-256. Furthermore, given the complex nonlinear nature of the SHA-256 hash function, two seemingly similar inputs can yield SHA-256 hash codes that are completely different, which further complicates the guesswork in finding the original object that matches a provided SHA-256 hash code.

In cryptography, numbers are often expressed in a hexadecimal system, which requires sixteen symbols. Thus, a SHA-256 hash that requires 256 binary digits can be represented in a hexadecimal system using only 64 digits, where each digit is represented by one of the numbers 0 to 9 or letters “a” to “f.”

For example, the SHA-256 hash$^{10}$ of the message “Prof. Bhagwan Chowdhry can explain Blockchain” is

8f8d3f14177bf664e9748cc790d739a71a7d06b2907844a309b43478e45c7124

If the original message, instead, were “Prof Bhagwan Chowdhry can explain Blockchain" its SHA256 hash is

db5bebb9f82d1040e96486b8573d91f7e205a025f41b8c7733dfa229c649b121

---
$^{10}$ A SHA-256 hash calculator can be accessed on https://andersbrownworth.com/blockchain/hash.

[Page 7]
Notice that the two hash codes are completely different even though the only difference between the first and second messages is that the word “Prof” is followed by a period in the former but not in the latter. Similarly, if the message were “Prof Bhagwan Chowdhry can explain blockchain” (where the only difference now is that the word “blockchain” is spelt with a lower case “b”), the SHA-256 hash is again completely different from the two hash codes shown above:

127b89ac962afc11e4c79fa265789633de209abac7400fd220c1268462ebde6c

Thus, if some original document’s SHA-256 hash were presented along-side a tampered version of the original document, the SHA-256 hash of the tampered document would not match the hash code of the original document, signaling immediately that the document has been altered. This is the fundamental mathematical insight that many blockchain-based use cases exploit, whereby the authenticity of documents, such as birth certifi-cates, transcripts, records of property ownership, etc., must be proven quickly (sometimes, nearly instantly) and efficiently without relying on cumbersome and expensive notary services, which often take a long time.

Hash codes are also referred to as checksums, since they allow you to prove access to or knowledge of the contents of a particular document without revealing any information contained in the document. That is, because it is nearly impossible to produce the correct SHA-256 hash without knowing the contents of the document, producing the SHA-256 hash code provides credible evidence that one indeed has the document in question.

For instance, consider the following tweet posted by Julian Assange of Wikileaks on October 16, 2016:

pre-commitment 1: John Kerry
4bb96075acadc3d80b5ac872874c3037a386f4f595fe99e687439aabd0219809

Specifically, Julian Assange was sending a message to John Kerry (the, then, Secretary of State to President Barack Obama of the United States) to convey that he had successfully hacked into the State Department’s documents, the proof of which was the SHA-256 hash. After seeing this message, Secretary Kerry could easily compute the SHA-256 hash code himself and would be able to confirm whether Julian Assange has access to the secret document in question.

Furthermore, the Twitter message is public for anyone to see and yet, no contents of the secret document are revealed by posting the SHA-256

[Page 8]
hash. Thus, the SHA-256 hash code provides what is termed a zero-knowledge
proof.

## 1.3 Digital Signatures Using Cryptography

There is often a need to transmit complete contents of messages as opposed to
just its SHA-256 hash, from which the original message cannot be recovered.
To do so electronically, without the contents of the message being intercepted
by a third party, requires that the message be encrypted. Encryption refers to
a two-way process whereby the original message is transformed using some
one-to-one deterministic algorithm. For example, “I love you, Chris" could
be encrypted as "J mpwf zpv Disjt” using a simple substitution in which each
letter of the original message is substituted by the next letter in the alphabet.
Anyone intercepting the message would either have to guess or know how
the original message was transformed (i.e., the encryption key). An attempt
to transmit the key electronically runs the risk that not only the message but
also the key may be intercepted by a rogue third party.

A solution to this problem was proposed by Diffie and Hellman and
further refined by Merkle in the mid-1970s (Levy 2002).[^11] The basic idea
is to generate a pair of keys, termed Public and Private keys. One of the keys
is used to encrypt a message, and the other key is used to decrypt it back to
its original form. For example, in order to make sure that the message “I love
you, Chris" is not intercepted by a rogue third party, such as a spouse, Chris
generates a pair of Public and Private keys. Chris publishes the Public key,
making it available to everyone (including her secret lover), but keeps the
Private key private by not revealing it to anyone (including her secret lover).
Using Chris's Public key, the message "I love you, Chris" is transformed into
unintelligible gibberish which can be converted back to the original message
only by using Chris's corresponding private key, which only Chris knows.
Thus, we avoid the problem of transmitting the key required for decryption.

However, another potential problem is that Chris cannot be sure who
actually sent the encrypted message because the Public key is available to
everyone. For example, the unhappy spouse could transmit a message, “Never
talk to me again, Chris." Although only Chris would be able to decrypt the
message, she would not know whether the message was sent by her lover or
the unhappy spouse, who is trying to sabotage the illicit love affair.

[^11]: See, for instance, “Crypto: How the Code Rebels Beat the Government Saving Privacy in the
Digital Age" (Levy 2002).

[Page 9]
To get around this issue, we can encrypt the message twice, first with Chris's Public key and then again with a different Private key, which also has a corresponding Public key that can be published publicly. Thus, the message has now been encrypted twice. Chris and her secret lover keep their respective Private keys private, while publicly publishing their respective Public keys.
When Chris receives a twice encrypted message, first she decrypts it using her lover's Public key-which is public-and then again using her own Private key. The unhappy spouse can no longer meddle because he does not know the Private key with which to first encrypt the original message.
In essence, any message can be digitally signed by encrypting the message with one's Private key. The encrypted message itself, which can only be decrypted by the corresponding Public key, can confirm that it must have been sent only by the person who knows the Private key. For example, one could prepend the message with the statement: "This message has been signed by Your Name." By adding this sentence to the beginning of the secret message "I love you, Chris" and, in addition, announcing publicly that all valid messages will begin with "This message has been signed by Your Name," Chris can easily verify the provenance of the message.

# 2 Bitcoin: A Bird's-Eye View

Bitcoin transactions are recorded and secured on a public, blockchain-based distributed ledger.¹² In this system, transaction records in the ledger are grouped into blocks, whereby a new block is formed approximately every ten minutes and is cryptographically linked to the prior block using hashed information from the prior block. The ledger is then replicated and maintained across numerous participants and systems, referred to as nodes, who do not need permission from a central authority to access these records.¹³ In contrast, random users cannot gain read/write access to Bank of America's ledger without permission. With a sufficient number of distinct nodes in the Bitcoin network, a dishonest node's attempts to alter transaction records or to validate faulty transactions will be overridden by the majority consensus of honest nodes.
Given the lack of central leadership in such networks, where participants can freely enter and exit in a permissionless and leaderless fashion,

---
¹² See Kim and Sarin (2018) for a generalized overview of distributed ledger technology, including but not limited to blockchain-based ledgers.
¹³ In fact, we (the authors) maintain a node on the Ethereum network, which is another public, blockchain-based distributed ledger

[Page 10]
these systems are also often called decentralized autonomous organizations (i.e.,
DAOs). However, to date, Bitcoin is the only cryptocurrency that comes
closest to being a true DAO. That is, not only is participation in the Bitcoin
network leaderless and permissionless (i.e., anyone can choose to maintain a
replicated copy of the ledger or even choose to participate as a validator/miner
who can add new blocks of records to the ledger), the ongoing upkeep of
the underlying protocol is also managed in a leaderless and permissionless
fashion. Specifically, anyone can submit Bitcoin Improvement Proposals (i.e.,
BIPs) to propose updates or changes to the network protocol, which will
be implemented in the mining software once it has been accepted by the
community of active Bitcoin miners.¹⁴

These updates to the network protocol, upon agreement by active miners,
are known as *soft forks*. For instance, one proposal (BIP-0098)¹⁵ led to the
adoption of a more efficient Merkle hash tree to summarize transactions in
each new block header. Another proposal (BIP-0065)¹⁶ led to the implemen-
tation of an additional security feature to specify a time lock on transactions.
Not all BIPs reach consensus across miners, which can lead to what is known
as a *hard fork*, whereby a new cryptocurrency is created with the desired
feature that was not accepted by the Bitcoin mining community as a whole.
For instance, BIPs to adjust block sizes in the Bitcoin blockchain were not
generally accepted by Bitcoin miners, which ultimately led to the creation of
Bitcoin Cash (BCH),¹⁷ the first of many hard forks on Bitcoin.

In contrast, updates to Ethereum’s network protocol are ultimately decided
upon by a consolidated team of developers, known as *Ethereum Core Devs*.
Although anyone in the general community can submit an Ethereum
Improvement Proposal (EIP), the decision to implement the proposed
updates does not rest on the general consensus of the Ethereum mining
community. Thus, although participation as a node on the Ethereum network
is leaderless and permissionless, the upkeep of the underlying protocol that
determines the rules of the network is not. Other cryptocurrencies are even
more centralized in the upkeep of their underlying protocol, lacking the open
discussions and invitation of improvement proposals from their respective
communities.

---
¹⁴ For instance, see BIP-0001, accessed on https://github.com/bitcoin/bips/blob/master/bip-0001.mediawiki, which established the concept and guidelines for all subsequent BIPs.

¹⁵ Accessed on https://github.com/bitcoin/bips/blob/master/bip-0098.mediawiki.

¹⁶ Accessed on https://github.com/bitcoin/bips/blob/master/bip-0065.mediawiki.

¹⁷ See https://www.bitcoincash.org/.

[Page 11]
# 3 The Bitcoin Blockchain

The Bitcoin blockchain is secured by a hashcash-based proof-of-work (PoW) protocol,¹⁸ which requires solving a computationally difficult puzzle to close out the current block of records and begin a new one.

Hashing is a critical part of the Bitcoin protocol. Hashing is used in the generation of *private keys*, which are used as part of a *digital signature* to verify a user's legitimate access to Bitcoin funds. It is also an important part of the proof-of-work puzzle that miners must solve to close out one block and begin another.

Specifically, the Bitcoin blockchain uses the double SHA-256 hash function (also known as SHA-256$^2$). As we discussed earlier in Sect. 1.2, the SHA-256 function is a *secure hash algorithm* that generates a 256-bit hash code (also known as the checksum), which is typically expressed as a 64-digit number in base 16. Double SHA-256 repeats the hash process by entering the SHA-256 hash code from the first iteration into the SHA-256 hash function once more, thereby producing a double SHA-256 hash code. Inputs to the SHA-256 hash function can be of any length, but the resulting hash code is always a 256-bit number.

Overall, the safety of the Bitcoin network, which allows anyone read/write access to its distributed ledger of transaction records, hinges critically on forcing validators in the network to solve computationally taxing cryptographic puzzles that would be nearly impossible for any single node (or colluding group of nodes) to resolve in a reasonable timeframe. We now proceed to explain the role of Bitcoin miners in validating transactions and maintaining the integrity of this permissionless, trustless system.

## 3.1 Nonces and Miners

Miners work to validate transactions requests, which are checked against past transaction records on the Bitcoin blockchain. Once verified, valid transactions wait in a memory pool (a.k.a., *mempool*) until they are added to a block that has been closed by a miner and confirmed by the network.

To successfully close a block and begin a new one, miners search for an arbitrary value called a *nonce*, that, when combined with the elements of the current block, must produce a double SHA-256 hash code with a minimum

---
¹⁸ See, for instance, “Hashcash-A Denial of Service Counter-Measure" (Back 2002), accessed on http://www.hashcash.org/papers/hashcash.pdf.

[Page 12]
number of leading zeros. Thus, this nonce is difficult to find, but simple to
verify once a solution is offered.

The first miner to find a winning nonce can close the current block, and
“mine” a new block, whose header will contain this nonce in addition to
other pieces of information that cryptographically chain the new block to
the prior one.19 The header also contains code to generate a *block reward*
to compensate the miner for forging this new block.20 Once this new block
is broadcast to the network, other miners can easily verify that the nonce
is valid, and a new proof-of-work mining race begins. The Bitcoin protocol
is designed to dynamically adjust the difficulty level based on rolling average
block times such that a new block is formed approximately every ten minutes.

The design choice in setting a ten-minute block time is specific, though
not limited, to Bitcoin. For instance, Ethereum block times typically average
around 15s.21 The block-time choice entails a tradeoff between achieving a
faster first confirmation (i.e., the time required for a pending transaction to
first be included in a valid block) and dealing with the ensuing chain splits,
whether accidental or intentional. That is, faster block times allow pending
transactions to be added to the blockchain more quickly. However, since the
proof-of-work puzzle is less computationally taxing, there is a greater likeli-
hood that multiple miners will find winning nonces close to simultaneously,
thereby causing a temporary split in the chain which must be resolved.

Overall, the inherent difficulty in solving for the proof-of-work nonce we
described above is what secures the integrity of this trustless, permissionless
ledger, since a group of malicious nodes is unlikely to have the computing
power to resolve a series of nonces to successfully alter transaction records that
are multiple blocks deep. Thus, a dishonest node’s attempts to validate faulty
transactions or to alter the contents of a prior block would be overridden by
the majority consensus of properly functioning nodes.

## 3.2 Network Congestion and Wait Times

Although Bitcoin blocks, on average, close every ten minutes, transactions
in a closed block are typically not considered “confirmed" for about an hour
after being added. The reason is that, for added security measures, Bitcoin

---
19 Figure 2 provides a graphical representation of this process. Additional visual representations can
be accessed on https://andersbrownworth.com/blockchain/.

20 The current block reward, as of February 5, 2020, is 12.5 BTC, and is estimated to reduce to 6.25
BTC by May 2020. See “Countdown to the Bitcoin Halving”, which can be accessed on https://bra
venewcoin.com/insights/countdown-to-the-bitcoin-halving.

21 See https://etherscan.io/chart/blocktime.

[Page 13]
clients (i.e., end-user software to facilitate sending and receiving Bitcoin) typi-
cally set their thresholds such that a transaction is not officially “confirmed”
until it is six blocks deep.²²

However, during times of high network volume, transactions may take
hours to be added and officially confirmed. Specifically, the Bitcoin protocol
limits block sizes to one megabyte. As Bitcoin usage has increased, average
block sizes have grown dramatically over time, and in recent years, we observe
that blocks often reach their maximum size limit.²³ If the collective size of
pending transactions in the memory pool exceeds the one megabyte block-
size limit, then unchosen transactions must inevitably wait to be added to a
subsequent block. Based on an average transaction size of 570 bytes (Moos
2019),²⁴ an influx of 100,000 network messages would result in wait times
in excess of five hours to clear and confirm all transactions in the memory
pool.

Because miners also collect transaction fees attached to each transaction
record, they are incentivized to gather the transactions with the highest fee-
to-size ratios. Bitcoin clients tend to dynamically adjust fees for end-users
based on the size of the transaction and extant network conditions. They
also allow users the option to pay an enhanced priority fee, which makes
a miner more likely to select that particular transaction from the memory
pool when forming the latest block. Thus, pending transactions with lower
fees risk sitting in the memory pool for long periods of time when network
volume is high.

Finally, we note the vast differences in speed and confirmation times when
transacting via a peer-to-peer Bitcoin client versus on a crypto-exchange.
Because of the frustration and intractability inherent in maintaining an
evolving limit order book when traders are forced to wait in excess of an hour
to know whether they have the funds to bid or the assets to offer, exchanges
simply maintain a centralized ledger of so-called *off-chain* transactions (as
distinct from *on-chain* transactions). That is, transactions to move BTC to
and from an exchange are recorded on the Bitcoin blockchain, and thus, are
not instantaneously confirmed. However, transactions *within* an exchange

---
²² As of November 8, 2019, Coinbase has lowered this threshold to three blocks, which suggests that
many Bitcoin clients may follow suit. See https://blog.coinbase.com/announcing-new-confirmation-
requirements-4a5504ba8d81. In comparison, Coinbase requires an Ethereum transaction to be 35
blocks deep before considering it confirmed. See https://help.coinbase.com/en/coinbase/trading-and-
funding/sending-or-receiving-cryptocurrency/why-is-my-transaction-pending.html.

²³ See, for instance, https://bitinfocharts.com/comparison/bitcoin-size.html.

²⁴ See https://cryptoslate.com/bitcoin-transactions-per-block-at-all-time-highs/ for a discussion on
average transaction sizes and average number of transactions per block.

[Page 14]
occur off chain, and can be confirmed swiftly since the exchange's permissioned ledger does not require a computationally taxing proof-of-work puzzle to be solved to add a transaction.

Overall, scalability remains a challenge to the widespread adoption of Bitcoin as a medium of exchange. In the following section, we describe other design choices intended to increase the throughput of transactions while maintaining the integrity of transactions records.

# 4 Ledger Design

Introduced by Bitcoin and popularized by its success, the most widely used choice in public-ledger design is currently a blockchain-based ledger predicated on a proof-of-work consensus protocol. However, there are other types of ledgers and consensus protocols, which differ in their efficacy and propriety based on whether the ledger is intended to be public or private. We now proceed to a brief overview of these various design choices.

## 4.1 Which Consensus Protocol?

A key issue in a distributed record-keeping system is how to reach consensus across nodes without halting the system in the presence of a few faulty or malicious nodes. This property, known as Byzantine fault tolerance (BFT),²⁵ strives to achieve a balance between what is known as *liveness* (i.e., allowing transactions to occur) and *safety* (i.e., preventing faulty transactions from occurring). A proof-of-work based consensus mechanism is one commonly used choice in designing a Byzantine fault-tolerant network.

As we discussed, the Bitcoin blockchain is secured by a proof-of-work consensus protocol, whereby miners work to solve a computationally intense puzzle to add new blocks of transaction records to the existing chain. Proof of work, by design, is a slow and laborious process, and more recent algorithms are moving to alternative consensus mechanisms in an attempt to achieve greater scalability in light of the bottlenecks occurring during times of high network volume.

For instance, the proof-of-stake (PoS) consensus protocol has been a popular alternative, whereby a node or subgroup of nodes is selected to validate the next set of transactions to be added to the ledger. That is, rather

---
²⁵ See Lamport et al. (1982) for a discussion of the Byzantine generals problem and its applications to reliable distributed computing.

[Page 15]
than having an entire pool of miners racing to solve a computationally taxing puzzle to win the right to add transactions to the existing ledger, a proof-of-stake system selects the next validator(s), typically with a randomized component, based on some relative stake in the system. For instance, the stake may be measured by the sheer size of a node's stake (i.e., wealth in native tokens),²⁶ or by a combination of the node's stake and age of stake (i.e., how long the node has held these native tokens).²⁷

Some modifications allow for lightweight nodes (i.e., nodes that don't maintain full copies of the blockchain database) with relatively little stake to lease their stake to full nodes on the network (known as *leased proof of stake*),²⁸ or use their stake to vote for the delegates to represent them (known as *delegated proof of stake*).²⁹ Others have begun to implement punitive elements to their proof-of-stake protocol (known as *punitive proof of stake*), whereby validators are not only rewarded for producing valid blocks but also punished for producing invalid ones.³⁰

## 4.2 Public Versus Private Ledgers

Our discussions on various considerations in ledger design and consensus protocol were predominantly fashioned with public (permissionless) ledgers in mind. However, with the rising popularity of Bitcoin, it has become in vogue to seek out blockchain solutions in a variety of settings, and firms have begun to consider private blockchain-based ledgers as well as other types of shared ledger designs for use within a group of permissioned entities.

For instance, Hyperledger,³¹ started by the Linux Foundation in 2015, provides private blockchain solutions that do not require a native token to operate. This should allay the fears of many regulators, such as those in India, who welcome the potential of blockchain technology but want to discourage

---
²⁶ See, for instance, the BlackCoin whitepaper (Vasin, n.d.), accessed on https://blackcoin.org/blackcoin-pos-protocol-v2-whitepaper.pdf.

²⁷ See, for instance, the Peercoin whitepaper (King and Nadal 2012), accessed on https://www.peercoin.net/whitepapers/peercoin-paper.pdf.

²⁸ See, for instance, the WAVES whitepaper (2016), accessed on https://medium.com/wavesprotocol/waves-whitepaper-164dd6ca6a23.

²⁹ See, for instance, the Steem whitepaper (2018), accessed on https://steem.com/steem-whitepaper.pdf.

³⁰ For an early discussion of a punitive proof-of-stake protocol, see Slasher: A Punitive Proof-of-Stake Algorithm Buterin (2014), accessed on https://blog.ethereum.org/2014/01/15/slasher-a-punitive-proof-of-stake-algorithm/.

³¹ https://www.hyperledger.org/.

[Page 16]
the proliferation and use of cryptocurrencies. Depending on the permis-
sion settings and selected consensus mechanism, the corresponding network
may be categorized as public (e.g., Bitcoin) or private (e.g., one built on
Hyperledger Fabric).

Naturally, some features used in distributed ledger design can be imple-
mented in a practical and sensible manner for use in a private ledger. For
instance, the simple act of grouping transactions into blocks, which are
chained in sequence, is not a particularly novel idea and has been imple-
mented by many in their own private ledgers. For instance, in our finance
records, we often create blocks (perhaps one for each year). Then, at the end
of the calendar year, we close out the 2019 block and form a new 2020 block
whereby the first element is chained to the last element of the prior block,
thereby forming the simplest of blockchains.

However, some design features used in many public distributed ledgers,
such as the proof-of-work consensus protocol, are clearly inappropriate in a
private ledger design.

## 4.3 Blockchain-Based Ledgers Versus Directed Acrylic Graphs

Although, blockchain-based ledgers are still currently the most widespread
design choice, not all distributed ledgers are blockchain-based, and more
recently, other implementations are being explored in an attempt to
achieve greater scalability. Specifically, a blockchain-based design requires
synchronous consensus, such that blocks are agreed upon and added linearly
in a chronological fashion. In an effort to mitigate bottlenecks inherent in
such a design, some recent projects are moving away from a blockchain-
based structure and toward a design that allows for asynchronous agreement
to validate pending transactions.

For instance, one structure makes use of a Unique Node List,³² whereby
overlapping subsets of nodes asynchronously reach consensus until the entire
network reaches agreement. Another such structure makes use of a directed
acyclic graph (DAG),³³ whereby each transaction must select other trans-
actions to validate. A pending transaction is ultimately confirmed as it is
repeatedly selected for verification and is nestled more deeply in the DAG.

---
³² See, for instance, Chase and MacBrough (2018) for an analysis of Ripple’s XRP protocol, accessed
on https://arxiv.org/pdf/1802.07242.pdf.

³³ See, for instance, the Byteball whitepaper (Churyumov, year unknown), accessed on https://obyte.
org/Byteball.pdf.

[Page 17]
Some nascent projects have also been researching the ability of this DAG-
based structure to handle the throughput required of an IoT (Internet
of Things) network, which would be impossible to handle with current
blockchain-based designs.34

# 5 Concluding Remarks

Now, more than ten years following its arrival, “Bitcoin” has quickly become
a natural part of colloquial speech. Its widespread popularity has also brought
to prominence terms such as "blockchain" and "distributed ledgers." But the
rapid adoption of these terms by the general public has also been fraught
with many misunderstandings and ill-conceived use cases. Our hope, with
this chapter, is to provide a layman's guide to Bitcoin and to shed light on the
basic mechanisms underlying the Bitcoin blockchain and other more general
considerations in distributed ledger design.

# References

Back, Adam. 2002. Hashcash—A Denial of service counter-measure, August 1.
Accessed on http://www.hashcash.org/papers/hashcash.pdf.
BraveNewCoin.com. 2020. Countdown to the Bitcoin Halving, February 5. Accessed
on https://bravenewcoin.com/insights/countdown-to-the-bitcoin-halving.
Buterin, Vitalik. 2014. Slasher: A punitive proof-of-stake algorithm, January 15.
Accessed on https://blog.ethereum.org/2014/01/15/slasher-a-punitive-proof-of-
stake-algorithm/.
Chase, Brad, and Ethan MacBrough. 2018. Analysis of the XRP ledger consensus
protocol, February 21. Accessed on https://arxiv.org/pdf/1802.07242.pdf.
Chowdhry, Bhagwan. 2016. *I (Shall Happily) accept the 2016 nobel prize in economics
on behalf of Satoshi Nakamoto*, November 6. Accessed on https://www.huffpost.
com/entry/i-shall-happily-accept-th_b_8462028.
Churyuomv, Anton. *Byteball: A decentralized system for storage and transfer of value*.
Accessed on https://obyte.org/Byteball.pdf.
Coinbase. 2019. Announcing new confirmation requirements, November 8.
Accessed on https://blog.coinbase.com/announcing-new-confirmation-requireme
nts-4a5504ba8d81.

---
34 See, for instance, an earlier IOTA whitepaper (Popov 2018), accessed on https://www.iota.org/fou
ndation/research-papers.

[Page 18]
Friedenback, Mark, Kalle Alm, and BtcDrak. 2017. *BIP 98: Fast Merkle trees*, August 24. Accessed on https://github.com/bitcoin/bips/blob/master/bip-0098.mediawiki.

Kim, Seoyoung, and Atulya Sarin. 2018. Distributed ledger and blockchain technology: Framework and use cases. *Journal of Investment Management* 16 (3): 90–101.

Kim, Seoyoung, Atulya Sarin, and Daljeet Virdi. 2018. Crypto-assets unencrypted. *Journal of Investment Management* 16 (2): 1–31.

King, Sunny, and Scott Nadal. 2012. *PPCoin: Peer-to-Peer crypto-currency with proof-of-stake*, August 19. Accessed on https://www.peercoin.net/whitepapers/peercoin-paper.pdf.

Lamport, Leslie, Robert Shostak, and Marshall Pease. 1982. The Byzantine generals problem. *ACM Transactions on Programming Languages and Systems* 4 (3): 382–401.

Laurence, Tiana. 2019. *Blockchain for dummies*, 2nd edn, May 7.

Lee, Sang Yup. 2019. *DNA data storage is closer than you think*, July 1. Accessed on https://www.scientificamerican.com/article/dna-data-storage-is-closer-than-you-think/.

Levy, Steven. 2002. *Crypto: How the code rebels beat the government saving privacy in the digital age*, January 15.

Moos, Mitchell. 2019. *Bitcoin transactions per block at all-time highs*, April 8. Accessed on https://cryptoslate.com/bitcoin-transactions-per-block-at-all-time-highs/.

Nakamoto, Satoshi. 2008. *Bitcoin: Peer-to-peer electronic cash system*, October 31. Accessed on https://bitcoin.org/bitcoin.pdf.

Popov, Serguei. 2018. *The Tangle*, April 30. Accessed on https://www.iota.org/foundation/research-papers.

Steem. 2018. *An incentivized, blockchain-based, public content platform*, June. Accessed on https://steem.com/steem-whitepaper.pdf.

Taaki, Amir. 2011. *BIP 1: BIP purpose and guidelines*, August 19. Accessed on https://github.com/bitcoin/bips/blob/master/bip-0001.mediawiki.

Todd, Peter. 2014. *BIP 65: OP_CHECKLOCKTIMEVERIFY*, October 1. Accessed on https://github.com/bitcoin/bips/blob/master/bip-0065.mediawiki.

Vasin, Pavel. n.d. *BlackCoin's proof-of-stake protocol V2*. Accessed on https://blackcoin.org/blackcoin-pos-protocol-v2-whitepaper.pdf.

Waves Protocol. 2016. *WAVES Whitepaper*, April 1. Accessed on https://medium.com/wavesprotocol/waves-whitepaper-164dd6ca6a23.

Zmudzinski, Adrian. 2019. *Bitcoin ATMs worldwide hit new milestone, surpassing 6,000*, November 17. Accessed on https://cointelegraph.com/news/bitcoin-atms-worldwide-hit-new-milestone-surpassing-6-000.