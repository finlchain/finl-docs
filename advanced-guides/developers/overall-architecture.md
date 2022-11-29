# Overall Architecture

## Network Architectures

The FINL network is largely divided into Main Chain and Sub Chain. The Main Chain acts as a Public Network, and the Sub Chain can be used as a Private Network. It is used as Globalization, and Sub Chain is used as Localization. Main Chain and Sub Chain actually function the same and are connected by Net Connector.

<figure><img src="../../.gitbook/assets/image (4) (4).png" alt=""><figcaption><p>Overall flow of Main Chain</p></figcaption></figure>

Net Connector or User uses Kafka/Zookeeper messaging cloud system to send transaction to chain.&#x20;

The chain that receives the transaction through the messaging cloud system checks the validation of the transaction, turns it into a smart contract, gives a unique ID along with the hashed value of the contra ct, and stores it in the DB through the DB contractor.

Block Producer (BP) is composed of odd numbers, and each BP composes its own Cluster, that is, a P2P Sub Network. This BP records the contract's unique ID and hash value in its own block through the DB Connector, and stores the block information in the DB through the DB Blocker.

Block Explorer can search all information such as Transaction information, Contract information, and Block information stored in the Chain DB through DB Explorer.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Overall flow of Sub Chain</p></figcaption></figure>

The core functions of Chain can be divided into Control Path and Data Path. Control Path consists of IS, I SAG, and ISA. IS and ISAG act as independent nodes, and ISA operates as an application in Network Nod e (NN). Data Path consists of SCA and NNA, and both operate as applications in NN.&#x20;

In addition, for the purpose of providing information to users, a Node with Block Explorer or similar functions can be operated, and these Nodes can request information necessary for a Full Block Node (FBN).

The DGOS Foundation operates the Index Server (IS), collects information on nodes that want to participate in the chain ecosystem, and can form a cluster based on this information. ISAG replicates and store s IS information and plays a role in distributing the information. In addition, ISAG replicates all information stored in NN of each cluster. The ISA serves as a medium for various control information transmitted From the IS to the NN.

Chain is a set of Clusters with BPs as the main axis. Each BP operates NN for each cluster and plays a rol e in collecting transactions, making smart contracts, and creating blocks. Blocks created in parallel in thi s way are serially connected between clusters. At this time, replication occurs for all information stored i n each cluster between NNs. In addition, the generated block is transmitted to the NN that will generate the next block through a network frame.

The SCA in the NN subscribes to the transaction through the messaging cloud system, and there are mu ltiple SCAs in each NN. Therefore, it can be seen that the number of transactionsthat can be processed in one NN is proportional to the number of SCAsin the NN.

Users can receive their account information and various public information through Block Explorer or a similar Node Application. In addition, a user can create a transaction, and the created transaction information is published in the messaging cloud system.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Overall flow of Clusters</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Replication flow</p></figcaption></figure>

