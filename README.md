# avax_module4
#  create a ERC20 token and deploy it on the Avalanche network for Degen Gaming
This repository is made for my ethereum intermediate avax mod 4 project which is used to create ERC20 token and test it on Avalanche fuji test network.

## Problem Statement
The smart contract should have the following functionality:
1.Minting new tokens: The platform should be able to create new tokens and distribute them to players as rewards. Only the owner can mint tokens.
2.Transferring tokens: Players should be able to transfer their tokens to others.
3.Redeeming tokens: Players should be able to redeem their tokens for items in the in-game store.
4.Checking token balance: Players should be able to check their token balance at any time.
5.Burning tokens: Anyone should be able to burn tokens, that they own, that are no longer needed.


## Description
1) The contract is named DegenToken and inherits from both ERC20 and Ownable. This means it includes the functionalities provided by these parent contracts.
2) The constructor function is executed when the contract is deployed. It initializes the ERC-20 token's name as "Degen" and symbol as "DGN" using the constructor of the parent ERC20 contract.
3) The contract defines three events:
TokenRedeem: Emitted when tokens are redeemed by an account.
TokenBurn: Emitted when tokens are burned (destroyed).
TokenTransfer: Emitted when tokens are transferred between addresses.
4) The mint function allows the owner of the contract to create new tokens and assign them to a specified address.
5)  The transfer function overrides the standard transfer function from the ERC20 contract. It transfers tokens from the sender to the specified recipient and then approves the sender to spend that amount of tokens.
6) The redeem function allows users to redeem tokens by burning a specific amount of tokens (10 times the chosen option). The function checks if the caller's balance is sufficient and then burns the required tokens. It emits the TokenRedeem event.
7) The decimals function is overridden to return a fixed value of 0. This means that the token will have zero decimal places, making it a whole number token.
8) The checkBalance function is an external view function that returns the balance of the caller's address.
9) An external view function that returns the token balance of a specified account.
10) The burn function allows any address to burn (destroy) a certain amount of their own tokens. It emits the TokenBurn event when tokens are burned.

## Getting Started

### Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at (https://remix.ethereum.org/.)

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., error.sol). Copy and paste the following code written by me into the file.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set heigher to "0.8.1" (or another compatible version), and then click on the "Compile error.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyContract" contract from the dropdown menu, and then click on the "Deploy" button.

After deployment of  the contract call the function Mint(), Transfer() , Burn() , checkBalance() , and test it on #SnowTrace network using Avalanche fuji test network. 


## Author

SHRESHTHA PAL

## License

This project is licensed under the MIT License - see the LICENSE file for details
