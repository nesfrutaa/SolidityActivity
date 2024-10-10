# SolidityActivity
# Solidity Creating Token

This project mints and burn token.

## Description

This is an assessment given by MetaCrafters under the ETH PROOF: Beginner EVM Course

## Getting Started

### Executing program

* Open [Remix](https://remix.ethereum.org/).
* Create a new solidity file (.sol).
* Copy and paste the code to the created file.
```
contract MyToken {

    // public variables here
    string public tokenName = "Nesfruta";
    string public tokenAbbrv = "nes";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public{
        if(balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
* Compile the project and select ^0.8.26 as the version of the compiler.
* Deploy the project
  
## Help

### Common Problems
* MIT license not specified.
```
// SPDX-License-Identifier: MIT
```
* Incorrect solidity version.
```
pragma solidity ^0.8.26;
```

## Authors

Contributors names and contact info
[@nesfrutaa](https://github.com/nesfrutaa)
