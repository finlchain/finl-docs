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

| Protocol | Create AttrCert | Verify AttrCert | Key length |
| -------: | --------------: | --------------: | ---------: |
|      RSA |          4.85 s |         1.91 ms |  1024 bits |
|      RSA |         24.06 s |         8.33 ms |  2048 bits |
|      RSA |        189.07 s |        30.91 ms |  4096 bits |
|      DSA |          1.01 s |         7.86 ms |   512 bits |
|      DSA |          1.34 s |        10.36 ms |  1024 bits |
|  ED25519 |        25.79 ms |        29.34 ms |   256 bits |

This mainnet uses ED25519 by default, and the length of both the private key and public key is 256 bits.

In the case of Public Key, 0x05 is defined and attached as a prefix by itself to confirm that it is ED25519.

_\[ Prefix (1 Byte : '0x05') + Public Key (32 Bytes) ]_

### ECDSA (Secp 256k1 and Secp 256r1)

This mainnet ECDSA is provided as an option. The length of the private key is 256 bits, and the compressed public key is used for the public key.

In case of public key, there is a standard prefix, and the contents are as follows.

\[ Prefix 1 Byte ('0x02' or '0x03') + Compressed (32 Bytes) ] or

\[ Prefix 1 Byte ('0x04') + Uncompressed (64 Bytes) ]

## Encryption or decryption

The extension name of the standard key file is 'pem'. Among them, the private key is an important file and should not be exposed to anyone other than the creator. This private key file is encrypted with 'key seed' and the extension name is 'fin'. In this case, 'key seed' is the password created by the creator himself.

This encrypted private key file can be used by decrypting it with 'key seed'. Encrypted Private Key Files must be safely isolated from external factors such as hacking and stored.

## Wallet Address

After encoding the public key value with base58, prefix is added. Prefixes are "FINL" for mainnet, "FINT" for testNet, and "FIND" for devNet.
