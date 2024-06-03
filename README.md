# MyToken.sol

This Solidity code defines a smart contract called MyToken that implements a basic token system on the Ethereum blockchain. This contract outlines a simple token management system, suitable for learning and basic applications on the Ethereum blockchain.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract provides basic functionality to mint and burn tokens. The total supply of tokens and individual balances are tracked and updated accordingly. The burn function includes a safeguard to prevent burning more tokens than are available in an address's balance.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g Mytoken.sol). Copy and paste the following code into the file:
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {

    // public variables here
  string public TokenName = "Rusty";
  string public TokenAbbrv = "RTY";
  uint public TotalSupply = 0;

    // mapping variable here
  mapping (address => uint) public balances;

    // mint function
  function mint (address _address, uint _value) public {
    TotalSupply += _value;
    balances[_address] += _value;
  }

    // burn function
  function burn (address _address, uint _value) public {
    if (balances[_address] >= _value){
      TotalSupply -= _value;
      balances[_address] -= _value;
    }
  }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Mytoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by burning and minting tokens. Click on the "MyToken" contract in the left-hand sidebar, there you could try to use the functions of burning and minting tokens.

## Authors
Rusty L. Palubon
8215442@ntc.edu.ph
