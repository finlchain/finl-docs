# Consensus Algorithm

## Consensus Group

A consensus group refers to a set of NNAs that participate in the process of creating, exchanging, storing, and confirming blocks between clusters, authenticating transactions and making them irreversible.

Each NNA belonging to the consensus group is logically composed of a P2P Network Layer and a Consensus Layer developed by itself on the TCP/IP Layer basis. The Security Layer supports the security functions of the P2P Network Layer and Consensus Layer such as ECIES, X25519, ECDSA, and EDDSA.

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption><p>Logical layer of NNA</p></figcaption></figure>

### P2P Network Layer

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption><p>P2P Header Description</p></figcaption></figure>

The P2P address system, which is the basis of the P2P network, consists of a total of 64 bits.

The upper 32 bits contain GPS information and consist of 16 bits of latitude and 16 bits of longitude, if latitude And if the longitude is "37.5207176, 127.0539982", use only “37.52, 127.05", which is the lower two digits of the decimal point. In decimal, it is “37 52 127 05" and in hexadecimal it is “25 34 7F 05". Therefore, it becomes possible to display as “0x25347F05”. At this time, the GPS maximum error range is 2.88 km, which is two multiples of 1.44 km.

The lower 32 bits are the chain code, continent code, country code, national hub network code, hub ne twork subnet code, subnet node address, etc. indicating whether this blockchain platform operates as a public or private blockchain, is used as.

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption><p>P2P Address System</p></figcaption></figure>

### Consensus Layer

Each local consensus group can independently generate a block, and in each round, the entire consensus group generates a block individually.

One round period is called Block Generation Interval (BGI) or Round Trip Time (RTT). One round minimum round period (BGI) is the minimum time required for the entire local consensus group to generate blocks in parallel and connect them in series. At this time, the minimum round period (BGI) of one round is affected according to the time taken for serial connection between the local consensus groups (t1) and the time between one round and the next round (t2).

The minimum delay time of t1 is 500 msecs. This is the minimum time to ensure that the block of one consensus group and all transaction/contract information accordingly are replicated to the other consensus group. Therefore, if a block is created in 4 clusters, a BGI of at least 2 sec must be guaranteed. In other words, the block generation cycle of one cluster is 2 sec.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Block Generation Period Vs. Number of Blocks</p></figcaption></figure>

### Security Layer



## Consensus Group Configuration

Each node in the system transmits hardware information, public key necessary for consensus, and vario us node information through ISA.

Send to The IS checks whether the node is a valid node based on information registered through DGOS and information collected during system startup.Based on this information, the IS creates a list for configuring the P2P main network and creates a list of P2P sub-networks within each P2P main network.

The IS transmits a P2P main network list and a P2P sub-network configuration list to each node according to the functions and roles of the nodes in the system. After receiving information for system operation , each node starts the system for each role. After confirming that all nodes are operating, the IS sends a block generation command to the P2P consensus group to generate a Genesis block. The P2P consensus group that has received the block generation command starts block generation.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>Control Sequence for Consensus Group Configuration</p></figcaption></figure>

