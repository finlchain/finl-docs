# Wallet

## FINL Key Generation

FIP39 provides two ways to create and restore wallets.

In both methods, you can create a wallet by preparing a single sentence and password.

For the first method, the password must be at least 10 bytes in length. Each sentence must have a mini mum length of 20 bytes or more and a maximum length of 500 bytes or less. Each password and sentence are converted into Multi-bytes. At this time, in the case of a sentence, it is hashed.

The converted password and hash values are subjected to XOR processing using randomly generated 2bytes unsigned integer values. The output value obtained through XOR processing is hashed in PBKDF2, and the password is used as the password argument value, and the password is used as the salt argument input value. PBKDF2 is password and Hash the salt 2048 times to generate a seed value of 512 bits.

Optionally, the sentence part may use a mnemonic word of BIP39. However, because Hash Processing and XOR Processing are used internally, the value is different from the value of BIP39.

<figure><img src="../../../.gitbook/assets/image (2) (2).png" alt=""><figcaption><p>FIP 39 Method 1 and FIP 32</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (2) (5).png" alt=""><figcaption><p>XOR Processing of Password and Salt used by PBKDF2 for FIP 39 Method 1</p></figcaption></figure>

The second method provides the same method as BIP39. Mnemonic derived from entropy can be listed in one sentence. In this case, Passphrase is optional. Each sentence and passphrase are converted into Multi bytes.

FIP32 can be regarded as the same as actual BIP32. The Random Number and Master Node Keys values generated during the wallet creation process are provided as outputs. At thistime, the Hash Left 256 bit s value of the Master Node Keys is used asthe Master Private Key, and the Master Public Key is derived. At thistime, the key standard uses ed25519 instead of secp256k1 for signature. In addition, X25519 sta ndard is used for encryption/decryption.

Password, Sentences 1, and Sentences 2 used as inputs when creating a wallet, and Random Number values provided as outputs are used when recovering the wallet. When recovering a wallet, after under going multi-bytes conversion and HASH concatenation as in the wallet creation step, the key value of the wallet can be recovered by using the random number provided by the wallet user instead of creating a new random number.

<figure><img src="../../../.gitbook/assets/image (3) (2).png" alt=""><figcaption><p>FIP 39 Method 2 and FIP 32</p></figcaption></figure>
