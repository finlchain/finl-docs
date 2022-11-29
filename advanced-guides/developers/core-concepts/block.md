# Block

## Block Description

<figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Block Contents</p></figcaption></figure>

Blocks are created in the consensus layer of the NNA. Block Fields are Block Number, NNA's P2P Address that creates Block, Block Generation Time (BGT), Previous Block Hash (PBH), Transaction Count, Block Hash, Signature, Public Key matching the Private Key used for Signature, and It consists of Block Confirm Time (BCT).

#### Block Number

Block Number starts with 1 in Genesis Block and increases by 1 for each Block.

#### P2P Address

This is the P2P address of the NN that creates the block.

#### Block Generation Time

Block Generation Time is the time when a block is created and is expressed in UTC milliseconds time.

#### Previous Block Hash

Previous Block Hash is the Block Hash of the previous block, and in the case of Genesis Block, Previous B lock Hash Field is set to 0x0.

#### Transaction Count

It is the total of new transactions entered into the cluster when the block is created.

#### Block Hash

Block Number, P2P Address, Block Generation Time, Previous Block Hash, Transaction Count, and the value obtained by concatenating the XOR values of Transactions are input values to SHA256 and outputted.

#### Signature

Issue the signature for the previously derived Block Hash value. At this time, to generate the signature, t he ed25519 private key of the NN that creates the block is used.

#### Public key

It is NN's ed25519 public key to verify the signature for the previously issued Block Hash.

#### Block Confirm time

Block Confirm Time is the time to confirm that the created block is irreversible.

