# Working with Solidity

This Solidity repository is a folder that contains four program files - variables, conditional_statements, arithematic_functions, Token_assesment. 



## Description

These programs are  simple contracts written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. Each program has its own contracts with different functions.
The variables files contains a contract which contains diffrent types of variables and some get and set functions for these variavbles.
The conditional_statements file contains a contract which contains functions that shows the use of conditional statements in solidity. It also has the use of ternary operator.
The arithematic_functions file contains a contract which has four arithematic functions that is addition, subtraction, multiplication and division.
The last and the main file which is the Token_assesment is the file which contains the project for creating a token and implementing mint and burn function for the token.

## Getting Started

### Executing program

//(Here I  am showing execution only for the Token_assesment file, which is the main project. The rest you can execute in a similar way.)

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token_assesment.sol). Copy and paste the following code into the file:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public token_name = "ZEN";
    string public token_abbrv = "ZN";
    uint public total_supply=0;

    // mapping variable here
    mapping(address => uint) public balances; 
    // mint function
    function mint(address _address, uint _value) public{
        total_supply+= _value;
        balances[_address]+= _value;
    }
    // burn function
    function burn(address _address, uint _value) public{
        if(balances[_address]>=_value){
            total_supply-= _value;
            balances[_address]-= _value;
        }
    }
        

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Token_assesment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token_assessment" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint and burn functions and minting and burnig some tokens in any address. 


