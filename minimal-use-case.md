# Minimal Use Case

Minimal use case enables a user to send Ether through the state oracles infrastructure.

## Dapp (Client)
Dapp itself has not functionalities other that interpreting (rendering) state messages coming from State Oracles.

Upcoming steps describe procedure of creation and submission of Ethereum transaction that transfers Ethers.

## First step
When making an Ethereum payment, we need to fill out a form with payment details (address from/to, amount etc.) For this purpose, the dapp gets the html code of the form from “TransferProposalView” State Oracle. ([github](https://github.com/yiedl/htmlview-erc20-transfer-from-proposal-oracle))

![Step 1](/docs/images/eth-tx1.png?raw=true "Step 1")

## Second step
In the second step, the dapp obtains Ethereum raw transaction for intended token transfer. For this purpose, the dapp calls the UnsignedRawTransaction State Oracle with necessary attributes. ([github](https://github.com/yiedl/ethereum-unsigned-raw-transaction-oracle))

![Step 2](/docs/images/eth-tx2.png?raw=true "Step 2")

## Third step
In the third step, the dapp obtains and renders TransactionSigning View.

![Step 3](/docs/images/eth-tx3.png?raw=true "Step 3")

## Forth step
Finally the dapp submits the signed raw transaction to the State Oracle and gets a confirmation of the transaction in return.

![Step 4](/docs/images/eth-tx4.png?raw=true "Step 4")