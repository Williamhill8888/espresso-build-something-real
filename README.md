# Espresso Hackathon - Arbitrum Sepolia Nitro Rollup Node

This repository contains the configuration and setup for an Arbitrum Sepolia Nitro Rollup node as part of the Espresso Hackathon.

## Overview

The goal of this project is to deploy and configure an Arbitrum Nitro Rollup node on the Sepolia testnet. This node will be used to demonstrate the capabilities of the Arbitrum Nitro stack and participate in the Espresso Hackathon.

## Prerequisites

- **Docker**: Ensure Docker is installed on your system.
- **Docker Compose**: Ensure Docker Compose is installed.
- **Git**: Ensure Git is installed for cloning the repository.

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/Williamhill8888/espresso-build-something-real.git

2.Navigate to the project directory:
```bash
cd espresso-build-something-real

3.Create a .env file and set the required environment variables:
```bash
nano .env

Example .env file:
```bash
WEBSOCKET_ARBITRUM_SEPOLIA_RPC_URL=wss://arbitrum-sepolia-rpc.publicnode.com
VALIDATOR_PRIVATE_KEY=Your staker private key.
BATCH_POSTER_PRIVATE_KEY=Your BATCH_POSTER private key

4.Start the Nitro Rollup node:
```bash
docker compose up -d

Configuration
The main configuration file is located at config/full_node.json.

Environment variables are used to manage sensitive data (e.g., private keys).


Usage
Once the node is running, you can interact with it via the following endpoints:

HTTP JSON-RPC: http://localhost:8547

WebSocket JSON-RPC: ws://localhost:8549

Example: Get Chain ID
```bash
curl -X POST \
  -H "Content-Type: application/json" \
  --data '{"jsonrpc":"2.0","method":"eth_chainId","params":[],"id":1}' \
  http://localhost:8547

Tasks for Espresso Hackathon
As part of the Espresso Hackathon, the following tasks have been completed:

Deployed an Arbitrum Nitro Rollup node on Sepolia testnet.

Configured the node to use a custom chain ID and environment variables.

Set up a validation node for block validation.

Tested the node's functionality using JSON-RPC endpoints.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Note: This project is part of the Espresso Hackathon. For more information, visit the Espresso Systems website.
