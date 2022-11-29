# Security

## DSA Algorithm

FINL uses ED25519 by default. In addition, it supports secp256k1 used by most mainnets including Bitcoin, and supports secp256r1, which is officially recommended by NIST.

### EdDSA (ED25519)

EdDSA generates signatures using variants of Schnorr signatures based on SHA-512 and Curve25519, a Twisted Edward Curve. EdDSA is documented in the RFC 8032 standard and has better performance than RSA or DSA.

&#x20;The advantages of EdDSA are as follows.

* Fast single-signature verification
* Even faster batch verification
* Fast key generation&#x20;
* High security level&#x20;
* Foolproof session keys&#x20;
* Collision resilience&#x20;
* No secret array indices&#x20;
* No secret branch conditions&#x20;
* Small signatures&#x20;
* Small keys

In addition, the advantages described in the RFC 8032 standard are as follows.

* It provides high performance on various platforms.&#x20;
* The use of a unique random number for each signature is not required.&#x20;
* Against side channel attacks, it can be better protected.
* Small public key size and signature size (In case of Ed25519, public key size is 32 bytes (256-bits), signature size is 64 bytes)&#x20;
* For all points on the curve, the formulas are valid and no exceptions occur.&#x20;
* Collision resilience (no has-function collision)

| Protocol | Key length | Create AttrCert | Verify AttrCert |
| -------: | ---------: | --------------: | --------------: |
|      RSA |  1024 bits |                 |                 |
|      RSA |  2048 bits |                 |                 |
|      RSA |  4096 bits |                 |                 |
|      DSA |   512 bits |                 |                 |
|      DSA |  1024 bits |                 |                 |
|  ED25519 |   256 bits |                 |                 |

This mainnet uses ED25519 by default, and the length of both the private key and public key is 256 bits.

In the case of Public Key, 0x05 is defined and attached as a prefix by itself to confirm that it is ED25519.

_\[ Prefix (1 Byte : '0x05') + Public Key (32 Bytes) ]_

