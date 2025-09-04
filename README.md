# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on "The Basics of Blockchain Technology" using multiple AI platforms and prompting strategies.

Your goal is to determine which combination of prompting technique + platform provides the best summary in terms of:

Accuracy

Coherence

Simplicity

Speed

User experience

## claude:
What is Blockchain?
Blockchain is a distributed digital ledger that records transactions across multiple computers in a network, making it virtually impossible to change, hack, or manipulate the system. Think of it as a shared notebook where everyone has a copy, and all copies must match for the information to be valid.

Key Features
Decentralization: No single authority controls the blockchain network. Instead, control is distributed among all participants, reducing the need for trust between parties.

Immutability: Once information is recorded in a block, it cannot be changed or deleted. Any errors require adding a new transaction to correct the mistake, with both visible to the network.

Transparency: All network participants can view the complete transaction history, creating an open and verifiable system.

Consensus: New transactions are only recorded when the majority of network participants agree they are valid.

How Blockchain Works
1. Transaction Recording
When a transaction occurs, it's recorded as a data block containing details like who was involved, what happened, when it occurred, and how much was exchanged.

2. Block Structure
Each block contains three main components:

Header: Metadata including timestamp and hash of the previous block

Data: Actual transaction information

Hash: A unique cryptographic fingerprint representing the entire block

3. Chain Formation
Blocks are linked together using cryptographic hashes. Each block's hash includes data from the previous block, creating a secure chain where altering any block would require changing all subsequent blocks.

4. Network Validation
Multiple computers (nodes) in the network maintain copies of the blockchain and use consensus algorithms like Proof of Work or Proof of Stake to validate new transactions.

Key Components
Distributed Ledger: A shared database spread across many computers, with each participant having an identical copy.

Nodes: Individual computers in the network that store the blockchain and validate transactions through peer-to-peer communication.

Cryptography: Mathematical algorithms using public and private keys to secure data and verify participant identities.

Smart Contracts: Automated programs that execute predefined actions when specific conditions are met, eliminating the need for intermediaries.

Why It Matters
Blockchain technology provides security through cryptographic protection, builds trust without central authorities, ensures reliability through distributed storage, and enables transparency while maintaining data integrity. The most famous application is Bitcoin, but blockchain is increasingly used in supply chains, healthcare, and digital identity systems.

## gemini:
Introduction to Blockchain Technology
Blockchain technology is a revolutionary system for recording information in a way that makes it difficult or impossible to change, hack, or cheat the system. At its core, a blockchain is a decentralized, distributed, and immutable digital ledger used to record transactions across a network of computers. Think of it as a shared digital notebook that everyone in a network can see, but no one can alter once an entry is made.

How Does It Work?
The process of adding a transaction to a blockchain involves several key steps:

Transaction Creation When a transaction occurs, it is bundled into a "block" along with other transactions happening at the same time. This block includes details such as the transaction data, a timestamp, and other relevant information.

Hashing and Chaining Each block is given a unique identifier called a hash, which is a cryptographic fingerprint. Crucially, each new block also contains the hash of the previous block. This creates a secure, chronological chain, linking the blocks together. If anyone tries to alter a block, its hash will change, effectively breaking the chain and alerting the network to the tampering.

Consensus and Validation Before a new block can be added to the chain, a majority of the computers (or "nodes") in the network must agree that the transaction is valid. This agreement process is known as a consensus mechanism. Common methods include Proof-of-Work (used by Bitcoin) and Proof-of-Stake.

Distribution Once validated, the new block is added to the chain, and the updated version of the ledger is distributed to all participants in the network. This ensures that everyone has an identical and up-to-date copy.

Core Components of Blockchain
Distributed Ledger This is the shared database that is duplicated and spread across the entire network of computers. Because there is no single point of failure, the system is highly resilient.

Blocks These are the individual records in the chain that hold batches of transaction data. Each block is securely linked to the one before and after it.

Nodes These are the computers connected to the blockchain network that store, spread, and preserve the blockchain data. They work to validate transactions and maintain the integrity of the ledger.

Cryptography Blockchain relies on advanced cryptographic techniques, such as hash functions and digital signatures, to ensure security, authenticity, and data integrity. Public and private keys are used to prove ownership and sign off on transactions.

Smart Contracts These are self-executing contracts with the terms of the agreement directly written into code. They automatically execute transactions and enforce rules when predetermined conditions are met, removing the need for intermediaries.

Key Features of Blockchain
Decentralization Control and decision-making are transferred from a central entity to a distributed network. This reduces the need for trust among participants.

Immutability Once a transaction is recorded on the blockchain, it cannot be altered or deleted. If a correction is needed, a new transaction must be created, and both are visible.

Transparency While the identity of participants can be anonymous, all transactions on the ledger are visible to anyone with access to the network.

Security The decentralized and cryptographic nature of blockchain makes it extremely secure. Altering any record would require changing every subsequent block and gaining control of a majority of the network, which is practically impossible.


## chatgpt :
Direct answer: A blockchain is a decentralized, immutable ledger that records transactions in linked blocks validated by network consensus, enabling trustless, transparent data sharing and programmable automation via smart contracts.

Overview
Blockchain is a distributed database that maintains a shared, append-only ledger across many computers, removing reliance on a central authority. Data is grouped into blocks, each referencing the previous block via a cryptographic hash, forming an ordered chain. This structure, combined with consensus protocols and public-key cryptography, makes past records tamper-evident and highly resistant to modification.

Core concepts

Ledger: A synchronized, shared record of transactions replicated across nodes. Every honest node stores and verifies the same state.

Blocks and chain: Each block contains a header (previous block hash, timestamp, nonce/metadata) and a body (transactions or state changes). Linking via hashes ensures that altering a past block breaks all subsequent links.

Cryptography: Hash functions provide tamper evidence; digital signatures (public/private keys) authenticate senders and enable non-repudiation.

Consensus: Network participants agree on the canonical chain. Common mechanisms include Proof of Work (PoW), where miners solve computational puzzles, and Proof of Stake (PoS), where validators attest blocks proportional to stake.

Decentralization: Authority and validation are distributed, reducing single points of failure and the need for trusted intermediaries.

Immutability: Finalized blocks are practically unchangeable; corrections occur through new transactions, preserving a transparent audit trail.

Smart contracts: On programmable chains (e.g., Ethereum), code deployed on-chain executes deterministically when conditions are met, automating agreements and workflows.

How it works (transaction lifecycle)

Create: A user crafts a transaction, signs it with a private key, and broadcasts it.

Propagate: Nodes validate basic rules (signatures, balances, format) and relay it peer-to-peer.

Package: A proposer (miner/validator) assembles valid transactions into a candidate block.

Validate: The network runs the consensus protocol (e.g., mining in PoW, attestations in PoS) to select and verify the next block.

Finalize: The accepted block is appended; nodes update their state and replicate the new ledger view. Reorg risk decreases with more confirmations.

Security properties

Tamper resistance via hash chaining and economic/cryptographic difficulty of rewriting history.

Sybil resistance and fork choice through consensus incentives and penalties.

Data integrity through signatures and deterministic validation rules.

Availability via replication across many independent nodes.

Types of blockchains

Public (permissionless): Open participation, strong censorship resistance, transparent state (e.g., Bitcoin, Ethereum).

Permissioned (consortium/private): Restricted validators, higher throughput, governance-controlled access; often used in enterprise contexts.

Layered designs: Base layer ensures security; Layer-2s (rollups, payment channels) increase throughput and reduce costs while inheriting security from the base chain.

Benefits and trade-offs

Benefits: Trust minimization, auditability, fault tolerance, programmable coordination, reduced intermediary costs.

Trade-offs: Throughput and latency limits, energy use (PoW), governance complexity, key management risks, and privacy challenges on transparent ledgers.

Key use cases

Payments and remittances, tokenized assets, decentralized finance (DEXs, lending), supply chain traceability, identity and credentialing, provenance, and automated compliance via smart contracts.

Mental model
Treat blockchain as a shared, time-stamped log where every entry is verified by many, locked by math and incentives, and extended only by consensus—turning distributed systems into a ledger everyone can trust without trusting each other.

If desired, this can be adapted into multiple AI prompting styles (zero-shot, few-shot with examples and analogies, role-based “explain like a TA,” or stepwise reasoning prompts) and aligned to learning outcomes like definitions, mechanics, components, benefits, limitations, and applications.

## copilot:


## Result
Criteria	Claude	ChatGPT	Gemini	Copilot
Accuracy	High (4.5/5)	Very High (5/5)	High (4/5)	Medium (3/5)
Coherence	High (4.5/5)	Very High (5/5)	High (4/5)	Low-Medium (2.5/5)
Simplicity	High (4.5/5)	Medium-High (4/5)	Medium (3.5/5)	Very High (5/5)
Speed	Fast (4.5/5)	Fast (4.5/5)	Fast (4/5)	Very Fast (5/5)
User Experience	Excellent (5/5)	Excellent (4.5/5)	Good (4/5)	Poor (2/5)


