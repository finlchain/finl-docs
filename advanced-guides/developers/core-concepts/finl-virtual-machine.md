# FINL Virtual Machine

As a core element of FINL, it is used everywhere, including User, Block Explorer, and Block Chain Core.

## FVM Structure

The core of FVM is implemented in C/C++. Core Function can be accessed through LUA Script, Node JS, or C/C++. Based on this structure, the same standard API can be applied anywhere.

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>FVM Structure</p></figcaption></figure>

## FVM Roles

### Wallet

It provides its own wallet that supports the Secp256r1 and Secp256k1 algorithms and applies the ED25519 algorithm with enhanced security. Key generation and recovery are possible using this wallet.

### Crypto SSL

By providing OpenSSL-based Crypto SSL, various Cryptography functions can be used. In particular, it supports Signature

Algorithms such as ECDSA and ED25519 and Encryption/Decryption Algorithms such as ECIES and X25519.

### Contract

It provides its own smart contract using a script language with excellent readability and extensibility.

### Fee/Reward Policy

Provides API to calculate Fee for Contract. In addition, it is possible to provide a reward policy of the node.

### Command Line Interface

Provides API to receive commands as Arguments and execute them. Through this API, LUA, Node JS, or Functions that can be executed with the C/C++ API can be directly executed.

### Web API

Provides a function that allows the client to communicate with the server using cURL (Client URL). In particular, HTTP GET and HTTP POST are mainly used.

### DB Connector

Provides API to access database.

### Validation

Provides API that can determine whether Contract and Transaction are valid.

## FVM Usages

### LUA Script

Currently, FVM is available for standalone operation using LUA Script on Linux and Windows systems. At this time, the Makefile automatically determines whether it is Windows-based or Linux-based and compiles, and the executable file can be linked with the LUA Script file.

#### &#x20;lua\_addon.cpp

It is a language based on C/C++ and includes a main function. The lua\_addon function implemented in this file binds various C/C++ functions that can be used in LUA Script and registers them in LUA. Also, the "luaConn" function of “main.lua” is executed, and if there is an argument value during execution, the argument value is transferred to the “luaConn” function.

#### main.lua

It is called from the FVM executable file and there is a “luaConn” function that can execute LUA Script.

#### init.lua

Register the LUA Core Script files and Configuration files used in FVM.

**NOTE :** Details related to interworking between LUA Script and FVM are provided in the manual.

### nodeJS Addon

FVM can be used as an Addon of nodeJS on Linux basis.

#### addon.cpp

It is a C/C++ based language and includes Initialize function for nodeJS addon. The Initialize function implemented in this file is registered by binding various C/C++ functions that can be used in nodeJS.

**NOTE :** Details related to interworking between nodeJS and FVM are provided in the manual.

