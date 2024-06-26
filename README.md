# Project Title  
Solidity Error Handling

## Problem Statement
write a smart contract that implements the require(), assert() and revert() statements.

## Description  
The SimpleAddition contract in Solidity facilitates adding two positive integers with error handling:
require: Ensures both inputs are positive before updating the sum.
revert: Checks if the stored sum matches a provided value; reverts if not, with an error.
assert: Verifies that the addition result is greater than both inputs for correctness before updating the sum.

## Getting Started

### Installing  
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleAddition {
    uint256 public sum;

    // Function to add two positive integers using require
    function addWithRequire(uint256 a, uint256 b) public {
        // Ensure both numbers are positive
        require(a > 0 && b > 0, "Both numbers must be positive");

        // Perform the addition and update the sum state variable
        sum = a + b;
    }

    // Function to demonstrate revert
    function checkSumWithRevert(uint256 value) public view {
        // Check if the sum is equal to the provided value
        if (sum != value) {
            revert("Sum does not match the provided value");
        }
    }

    // Function to perform addition and ensure conditions using assert
    function addWithAssert(uint256 a, uint256 b) public {
        // Perform the addition
        uint256 result = a + b;

        // Ensure the result is greater than both inputs
        assert(result > a && result > b);

        // Update the sum state variable
        sum = result;
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
