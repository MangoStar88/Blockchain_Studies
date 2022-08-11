## What is blockchain?

### Introduction
I have seen people defining blockchain in all kinds of fashion. But personally, I prefer the one on Wikipedia:

A blockchain is a type of Digital Ledger Technology (DLT) that consists of growing list of records, called blocks, that are securely linked together using cryptography.

#### 1. DLT
What is a DLT? This is probably the most important concept to grasp for someone to truly understand blockchain. According to Wikipedia, DLT is:

A distributed ledger (also called a shared ledger or distributed ledger technology or DLT) is a consensus of replicated, shared, and synchronized digital data geographically spread across multiple sites, countries, or institutions. Unlike with a centralized database, there is no central administrator。

The concept of a distributed ledger is also not a brand new one; in fact, it can arguably be traced back as far as the times of the Roman Empire, which hosted a banking system allowing people to participate in monetary transactions across different regions of the empire. 

It is important to note that not all DLTs are blockchains, meaning that not all distributed ledgers are built on blockchain technology and not all blockchains need to be distributed. For example, there are some decentralized cryptocurrency project, such as IOTA, that is not blockchain-based. 

#### 2.overview of bc history。
1982 Chaum
1982 cryptographer -david chaum first prposed a blockchain-liked protocol in his dissertation<computer system established,maintained,and trusted by mutually suspicious groups>(Ph.D Thesis
University of California, Berkeley, CA, USA (1982)）

1991 Haber & Stornetta
S. Haber, W.S. Stornetta
How to time-stamp a digital document
(J. Cryptol., 3 (2) (1991), pp. 99-111)

1993 Bayer
D. Bayer, S. Haber, W.S. Stornetta
Improving the efficiency and reliability of digital time-stamping
(R. Capocelli, A. De Santis, U. Vaccaro (Eds.), Sequences II, Springer, New York, NY, USA (1993))

1998 Szabo
R. Sharma
Bit gold

2008 Satoshi

2013 ethereum

2015 hyper ledger

2020-2022 ethereum 2.0

#### 3. What is a block?
So, “Blockchain”, what is actually a “block”. A block is a container of data structure. 

#### 4.How to identify a block?
Block header hash
How can we identify a block? The primary way to identify a block is using its cryptographic hash, basically a form of digital fingerprint, created by hashing the block header twice via the SHA256 algorithm.

However, the block hash is not technically included inside the data structure of a block. It’s not there when the block is being transmitted on the network, it’s also not there when the block is being stored as a node on the blockchain. Instead, the computation of block’s hash happens when the block is received by the network. In order to facilitate indexing and retrivel of blocks from a disk, the block hash can also be stored as part of “metadata” of a block. 

Block height
What if you don’t have any info on a block’s cryptographic hash? In that case, you can also identify a block by its position in the blockchain, aka the block height. Let’s put it this way, xxx. The first block ever created will be found at block height 0. 
But different from the block hash, the block height is not “unique”. A block will always have a specific block height, but you can’t always use the block height to identify a block. Because, multiple blocks can have the same block height, as if they are fighting for the same position in the blockchain.

#### 5. Merkle tree
Within each block, the transactions are recorded in a structure called “merkle tree” or “binary hash”. 

For each merkle tree, the node on top is referred to as “the root”. Transactions are summarized in each block through storing information regarding the root in the block header. It’s also important to note that no matter how many transaction are contained in a block, they will always be summarized by a 32 bytes hash. 

#### 6. Blockchain
The blockchain data structure is an ordered, back-linked list of blocks of transactions. It can be stored as a flat file, or in a simple database. It is linked by references in the previous block hash field.

Imagine yourself as a passenger on an “Interstellar Express”. Everyone on the train has the same destination (consensus), and as the number of passengers (transaction) increased, they have to build more carriages (blocks) to accomodate these passengers; hence, the train (blockchain) will get longer andlonger.

