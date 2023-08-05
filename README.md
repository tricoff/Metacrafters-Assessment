# Metacrafters_Challenge
# Creating My First Token 

This Solidity program is a simple program about creating a ERC20 token and deploying it to diffrent testnets.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has mainly 2 function:-

--> To mint tokens

--> To burn tokens





### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

javascript
pragma solidity ^0.8.4;

contract MyToken {

    // public variables here
    string public tokenname = "TRICO"; 
    string public tokenAbbrv = "FF"; 
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value; 
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address, uint _value) public { 
        if (balances[_address] >= _value) {
            totalSupply -= _value; 
            balances[_address] -= _value;
        }
    }
}


