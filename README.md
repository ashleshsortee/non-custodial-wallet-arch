# Non-custodial cryptocurrency wallet

## Introduction

This is the high level overview of the non-custodial cryptocurrency wallet supporting multi assets and on multiple platforms like web, mobile and server.

## Architecture

A general non-custodian wallet comprises of following features: 
1. Key Management
    - Creation of a new key pair.
    - Storing of keys in secured local store.
    - Account recovery and restoration.
2. Asset Management
    - Support for multi-assets from multiple blockchain networks.
    - Add new netowrks or assets
    - List down the asset CMP and tokens owned by the account holder
3. Transaction signing and management
    - Transaction signing for various cryptocurrencies on relavant networks.
    - Transaction fees management
    - Transaction History

Based on the features mentioned above, below are the 3 key components for the non-custodian wallet:
1. Wallet Generator
    - Creation of a new key pair using BIP-39 for creating mnemonic code for generating keys and BIP-32 for the generating cryptographic keys from a single mnemonic code.
    - Encryption of keys using AES encryption to store it in local storage in web browser or keychain in ios or in Android keystore.
2. Asset Manager
    - Consume **Blockchain Explore APIs** to fetch the tokens owned by the wallet address with its respective value fetched through **CoinMarketCap** or **CoinGecko** APIs.
4. Data storage
    - Store the account information and transaction history in local storage of the device.
    - Use encrypted storage - keychain on ios and keystore on android for secuerly storing the keys with AES encryption.

### High Level Architecture
![Transaction Manager](https://github.com/user-attachments/assets/72ba4d81-751d-4c2b-a17f-ad06da1579c5)
