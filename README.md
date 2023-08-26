# Degen ERC-20 Token Contract

The Degen ERC-20 Token Contract provides a foundational implementation of the ERC-20 token standard on the Ethereum blockchain. This contract enables users to seamlessly create, transfer, and manage tokens while adhering to the specifications outlined in the ERC-20 standard.

## Contract Overview

The primary features and functionalities of the contract include:

- **Token Information**: The contract maintains the name and symbol of the token, making it easily recognizable and differentiable from other tokens.

- **Token Balances**: Utilizing a mapping structure, the contract tracks the token balance of each address, granting anyone the ability to query an address's balance.

- **Token Allowances**: The contract facilitates delegated token transfers through a mapping of owner addresses to spender addresses, along with the associated allowance.

- **Events for Transparency**: To enhance transparency and accountability, the contract emits events for pivotal token-related actions such as transfers, minting, burning, and approvals.

## Functions

1. **Constructor**: The contract constructor initializes the token's name and symbol during deployment, maintaining these values throughout its lifecycle.

2. **Minting Tokens**: The `mint` function empowers authorized entities to generate new tokens and allocate them to designated accounts. The function enforces valid recipient addresses and updates token balances accordingly.

3. **Burning Tokens**: Through the `burn` function, token holders can permanently eliminate a specified quantity of their tokens. The function validates that the holder possesses enough tokens, deducts the amount, and emits a `TokensBurned` event.

4. **Transferring Tokens**: With the `transfer` function, account holders can transfer tokens to other recipients. The function verifies the recipient's address validity and the sender's balance before executing the transfer and emitting a `Transfer` event.

5. **Delegated Transfers**: The `transferFrom` function empowers approved third parties (spenders) to transfer tokens on behalf of token holders. It verifies the sender's balance and allowance, performs the transfer, reduces the allowance, and emits a `Transfer` event.

6. **Approving Spenders**: Through the `approve` function, token holders can grant spenders the permission to conduct token transfers on their behalf. The function sets the spender's allowance and emits an `Approval` event.

## Events

The contract emits the following events to facilitate tracking and transparency:

- `Transfer`: Emitted when tokens are transferred from one address to another.
- `TokensMinted`: Emitted when new tokens are created and assigned to an account.
- `TokensBurned`: Emitted when tokens are permanently destroyed (burned) by an account.
- `Approval`: Emitted when an account grants approval for a spender to conduct token transfers.

## Deployment
### The contract has been deployed on the Avalanche network for Degen Gaming.

For the deployment on your own pc follow the steps: 
- First write the contract on the remix.
- Add a network account on Metamask.
- Make sure that the required avax is present in your account.
- When the metamask has enough avax then select the environment as "Injected Provider" in remix.
- So finally at the last step deploy it.
- To verify copy the address of deployment and paste it into "Snowtrace Fauji Testnet".

## Loom Vidoe Link
https://www.loom.com/share/275d210f1f8e4bdb926a5fe27178614c?sid=004059b4-84fa-4182-92da-54c269e97122

## License

The code is released under the MIT License. For the complete license details, refer to the SPDX-License-Identifier comment at the beginning of the Solidity code.
