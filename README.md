# Project Title  
Solidity Error Handling

## Problem Statement
write a smart contract that implements the require(), assert() and revert() statements.

## Description  
The UniqueContract is a simple Solidity contract that demonstrates the use of require(), assert(), and revert() statements. It allows updating a positive data value and restricts certain functions to the contract owner. The updateData function ensures the new value is positive using require(), while ownerOnlyFunction restricts access using revert(). The verifyCondition function uses assert() to ensure data remains positive. The contract is initialized with the deployer as the contractOwner.

## Getting Started

### Installing  
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract UniqueContract {
    uint256 public data;
    address public contractOwner;

    constructor() {
        contractOwner = msg.sender; // Set the deployer as the initial contract owner
    }

    function updateData(uint256 newData) public {
        // Ensure the new data is positive
        require(newData > 0, "Data must be greater than zero");
        data = newData;
    }

    function ownerOnlyFunction() public view {
        // Custom error handling for restricted access
        if (msg.sender != contractOwner) {
            revert("Access denied: Only the contract owner can call this function");
        }
    }

    function verifyCondition() public view {
        // Use assert to check for conditions that must always be true
        assert(data > 0);
    }
}

```

## Executing program    
### How to Run the Program      
Navigate to the project directory  
Compile the Solidity contract  
Deploy the contract using your preferred Ethereum development environment   

#### For Remix:    
Open Remix IDE.  
Upload MyToken.sol.  
Compile and deploy the contract.  


## Authors  
Sandeep Kaur @Sandeep1925

## License  
This project is licensed under the MIT License - see the LICENSE.md file for details.  

We have established a solidity contract with this code. 
