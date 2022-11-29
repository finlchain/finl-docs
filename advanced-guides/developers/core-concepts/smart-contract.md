# Smart Contract

## Contract Description

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>Contract fields</p></figcaption></figure>

### Contract fields

#### Create Time

Indicates the time when the Contract was created in the past or when it will be executed in the future. UTC milliseconds are used.

#### Fintech

Indicates whether it is a financial transaction. The status value has true / false.

#### Privacy

Indicates whether the contract is public or private. The status value has true / false.

#### Fee

Network fee for contract transmission.

#### From Account

This is the account that sends the contract. Value is Default Account (0x00000000), Token Account, or U ser. It can be an Account.

#### To Account

This is the account that receives the contract. Value is Default Account (0x00000000), Token Account, or User. It can be an Account.

#### Action

It is a unique value for the actual operation. Token Action value, Action value according to contract type, and It is divided into Smart Contract Action values.

#### Contents (Blob)

These are the detailed items included in the contract. Each contract has different details.

#### Memo

A contract can optionally make a memo about the contract.

#### Signature

It is the signature of the contract sender.

#### Signed Public Key

It is the public key used as the wallet of the contract sender.



## NFT

This mainnet supports non-fungible tokens through smart contracts.
