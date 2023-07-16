# Error Handling
This Solidity program is a simple Error handling program that demonstrates the essential condition which must be checked before a function is executed in the Solidity programming language. The primary purpose of this program is to handle errors in the function or code encountered while running and executing the code.

# Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has 4 functions to handle the error in a different manner or by using different functions require(), revert(), assert() and the one function is just to set the age. In this Eligible Criteria contract basically, it will check whether your age limit is eligible or not for the vote through this 3 error handling function. This program serves as a simple and straightforward introduction to Error handling and can be used as a stepping stone for more complex projects in the future for handling error in the contract.

# Getting Started
# Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol).

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.17;

contract ErrorHandling {
    
    uint public b = 4;

    function testAssert(uint num) public pure {
        assert(num != 0);
    }

    function divide(uint _numerator, uint _denominator) public pure returns (uint) {
        require(_numerator >= _denominator, "Please provide a numerator greater than or equal to the denominator");
        return _numerator / _denominator;
    }

    function mult(uint a) public view returns (uint) {
        require(a > 0, "Value of 'a' is zero. The result should not be zero.");
        return a * b;
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. testAssert(uint num) This function demonstrates the usage of the assert function. divide(uint _numerator, uint _denominator) This function demonstrates the usage of the revert function. It takes _numerator and _denominator parameters and performs division. If the _numerator is less than _denominator, it reverts the transaction with a custom error message stating that the numerator should be greater than the denominator. mult(uint a) This function demonstrates the usage of the require statement with a custom error message. It takes a parameter 'a' and checks if it is greater than zero using the require statement. If the condition fails, the function reverts with the provided error message. Otherwise, it performs the multiplication'a * b'and returns the result.

# Authors
Metacrafter Chris @metacraftersio

# License
This project is licensed under the MIT License - see the LICENSE.md file for details
