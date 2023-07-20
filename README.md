# ANKHWallet
multi-chain cold wallet generator

Instructions for usage:

Save the script in your secure environment as, for example, multi_chain_wallet_generator.py.

Transfer the script to the offline computer or set up an offline environment.

Run the script in the offline environment using a Python interpreter.

Add in terminal -> pip install Mnemonic bitcoinlib btclib

The script will generate a BIP39 mnemonic for you to securely write down.

Optionally, you can provide an additional passphrase to enhance security. Remember this passphrase along with the mnemonic.

The script will generate the BIP32 master key for Bitcoin and print it.

For each supported cryptocurrency in the CRYPTOCURRENCIES dictionary, the script will generate and print the BIP44 account extended key and the corresponding address.

Store the mnemonic and passphrase (if used) securely. Do not store them digitally or share them with anyone.

This script allows you to generate a single mnemonic and use it to derive different cryptocurrency addresses for various chains, all within a cold wallet environment. The address generation for Ethereum, Bitcoin, and Binance Smart Chain is a placeholder, as it requires additional libraries and external dependencies for full implementation. Ensure to use appropriate libraries and follow best practices for secure address generation when deploying this in a production environment.

How to properly use:
Generate the Cold Wallet: Use the script provided earlier to generate the cold wallet. Safely note down the mnemonic and passphrase (if used). This mnemonic will be used to create the "watch-only" wallet.

Set Up the Watch-Only Wallet: Create an online "watch-only" wallet using a wallet software or service. Import the extended public keys or individual public keys derived from the cold wallet's mnemonic seed. The "watch-only" wallet will monitor the cold wallet addresses' balances and transactions.

Set Up a Hot Wallet: Create a separate "hot" wallet using a wallet software or service that supports the cryptocurrencies and NFTs you want to send. Import the mnemonic seed and passphrase (if used) of the cold wallet into this "hot" wallet. This will give the "hot" wallet access to the private keys needed for transaction signing.

Transfer Funds or NFTs: Using the "hot" wallet, initiate the transfer of cryptocurrency or NFTs by specifying the recipient address and the amount or NFTs you want to send.

Sign the Transaction: The "hot" wallet will sign the transaction using the private keys derived from the cold wallet's mnemonic seed. The signed transaction will contain the necessary information to transfer the funds or NFTs.

Broadcast the Transaction: After the transaction is signed, the "hot" wallet will broadcast it to the blockchain network. This action initiates the transfer of funds or NFTs from the cold wallet address to the recipient's address.

Confirmation: Once the transaction is confirmed by the blockchain network, the funds or NFTs will be sent from the cold wallet address to the recipient address.

It's important to keep the "hot" wallet secure and protected from potential threats. Use it only in a secure and trusted environment. The "hot" wallet is responsible for transaction signing and is the only component that needs to be online. The cold wallet remains offline at all times, keeping your private keys secure.
