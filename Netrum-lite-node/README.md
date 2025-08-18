# NETRUM-LITE-NODE

## Hardware & Network Requirements 

|  Component	|         Minimum           |       Recommended         |
| :---------: | :-----------------------: |:-----------------------:  |    
|   **CPU**   |         2 Cores           |        ≥ 4 Cores          |
|   **RAM**   |         4 GB              |        ≥ 6 GB             |
| **Storage** |         50 GB SSD         |        ≥ 100 GB SSD       |
| **NETWORK** |         10 Mbps           |        ≥ 10 Mbps          |

- SSD storage is highly recommended for faster performance and node stability.
- A stable and fast internet connection is important for uptime sync, mining tasks, and daily reward claims.

## Netrum Lite Node – Setup Guide

```
git clone https://github.com/NetrumLabs/netrum-lite-node.git
cd netrum-lite-node
sudo apt update && sudo apt install -y curl bc jq speedtest-cli nodejs npm
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt install -y nodejs
npm install
npm link
```

### Test the CLI
```
netrum
```

> You should see the Netrum Lite Node CLI interface.
```
Netrum CLI  Version v2.0.0
       Light-weight node & wallet toolkit for the Netrum network.

       Available Commands:
       netrum-update          Cli Update
       netrum-system          System status & logs
       netrum-new-wallet      Create / new a wallet
       netrum-import-wallet   Create / import a wallet
       netrum-wallet          Create / inspect a wallet
       netrum-wallet-key      Export private key
       netrum-wallet-remove   Delete wallet files
       netrum-check-basename  Check basename conflicts
       netrum-node-id         Show current Node ID
       netrum-node-id-remove  Clear Node ID
       netrum-node-sign       Sign a message with node key
       netrum-node-register   Register node on-chain
       netrum-sync            Sync blockchain data
       netrum-sync-log        Node sync logs
       netrum-mining          Start mining
       netrum-mining-log      Node mining logs
       netrum-claim           Claim rewards

       Run netrum <command> --help for command-specific options.
```

> Register a domain here: https://www.base.org/names

## Please run the following commands one by one to proceed with registering the node.
> If you already have an EVM wallet, choose option 2; if not, start with step 1
### Option 1: Creates a new EVM

```
netrum-system
netrum-new-wallet
netrum-check-basename
netrum-node-id
netrum-node-sign
netrum-node-register
```
### Option 2: Import an existing wallet by entering your private key

```
netrum-system
netrum-new-wallet
netrum-check-basename
netrum-node-id
netrum-node-sign
netrum-node-register
```

### Run Node 
```
netrum-mining
```
> Mining Logs: 
```
netrum-mining-log
```
> Claim rewards every 24 hours: 
```
netrum-claim
```

# How to Use Netrum CLI Commands

- **`netrum-system` :** This command checks your VPS system status, including CPU, RAM, and internet speed. Use it to make sure your machine meets the basic requirements before setup.


- **`netrum-new-wallet` :** Creates a new EVM-compatible wallet directly from the CLI. It will generate your public address and private key, all of which you should store securely.


- **`netrum-import-wallet` :** Allows you to import an existing wallet by entering your private key. This is useful if you already have a Base domain tied to a wallet you control.


- **`netrum-check-basename` :** Checks whether your current wallet has a registered Base domain name. Your Base name will also become your Netrum Node ID.


- **`netrum-node-id` :** Displays the current Node ID associated with your wallet. This is your official node identity on the Netrum network.


- **`netrum-node-sign` :** Generates a signed identity message using your wallet's private key. This signature verifies that you own the node and wallet.


- **`netrum-node-register` :** Registers your node on-chain and with the backend system. This step requires a small amount of BASE for gas (typically between 0.0002 and 0.0005 BASE).


- **`netrum-sync` :** Starts the syncing process between your node and the Netrum network. This keeps your node active and eligible to earn mining rewards.


- **`netrum-sync-log` :** Displays real-time logs showing your sync status, heartbeat signals, and activity tracking. Use this to confirm your node is working correctly.


- **`netrum-mining` :** Begins the mining process for NPT tokens. Your node will now start earning rewards based on uptime and active sync.


- **`netrum-mining-log` :** Shows live mining logs and confirms whether your node is earning tokens correctly. This is useful for monitoring daily activity


- **`netrum-claim` :** Lets you claim your mined NPT tokens after 24 hours of uptime. Once claimed, mining will automatically restart. This step requires a small amount of BASE for gas (around 0.00002 to 0.00003 BASE).


- **`netrum-wallet` :** Displays wallet information including your public address and NPT balance. Use this to check if your mined rewards have been received.


- **`netrum-wallet-key` :** Reveals both the public and private keys of your wallet. Only use this in a secure environment and never share your private key.


- **`netrum-wallet-remove` :** Deletes your wallet from the local VPS. Make sure to back up your private key or seed phrase before running this command, as this action cannot be undone.
