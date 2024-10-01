# Solidity Creating Token

This project mint and burn token.

## Description

This is an assesment given by MetaCrafters under the ETH PROOF: Beginner EVM Course

## Getting Started

### Executing program

* Open [Remix](https://remix.ethereum.org/).
* Create a new file with an extension of .sol.
* Copy and paste the code to the created file.
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.26;

contract MyToken {

    // public variables here
    string public tokenName = "YukiCone";
    string public tokenAbbrv = "YC";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```
* Compile the project and make sure to select 0.8.26 as the version of the compiler.
* Deploy the project
  
## Help

###Common Problems
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

[@angelosmbn](https://github.com/angelosmbn)

