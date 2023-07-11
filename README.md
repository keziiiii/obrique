ETHERIUM PROOF BEGGINER
The purpose of the module is to instruct us on the foundations of building a block chain.

Description
This training attempts to clarify the fundamentals and provide background information on block chains.

  Getting Started To be able to execute this application, you may use Remix, an online Solidity IDE, which can be found 
https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.18+commit.87f61d96.js

Create a new file on the Remix website by clicking the "+" symbol in the left-hand sidebar. Save the file as Phoenixtoken.sol . Insert the following code into the file: // SPDX-License-Identifier: MIT pragma solidity 0.8.18;

contract MyToken {
    // Public variables
    string public tokenName = "Boston";
    string public tokenAbbrv = "Bstn";
    uint256 public totalSupply = 0;
    mapping(address => uint256) public balances;

    // Mint function
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function
    function burn(address _address, uint256 _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}





Author:QUEZIE R. OBRIQUE
8210606@ntc.edu.ph


This project is licensed under the OBRIQUE.QUEZIE R. License - see the LICENSE.md file for details
