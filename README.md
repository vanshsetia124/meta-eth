# Create a Token

This program is a simple contract that demonstrates how a smart contract works and behaves on a blockchain network.

## Description

This is a simple contract written using the Solidity programming language. It demonstrates how an actual contract works and behaves on a blockchain network. First, I have created multiple state variables that will store the basic information of the tokens, such as their name, abbreviation, total supply, and map the balance of the account to their address.

It has two functions:

* `mint()` function increases and stores the total supply of tokens and the balance of an account.
* `burn()` function decreases and updates the total supply of tokens and the balance of an account.

## Getting Started

### Executing program

To run this program, you have to use a Solidity IDE.

* To get started, Open [Remix](https://remix.ethereum.org/ "https://remix.ethereum.org/") an online Solidity IDE.
* Create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol).
* Copy-paste the code provided below.

  ```solidity
    pragma solidity >=0.8.20;
    
    contract MyToken {
    
        // public variables here
        string public tokenName = "META";
        string public tokenAbbrv = "MTA";
        uint public totalSupply = 0;
    
        // mapping variable here
        mapping(address => uint) public balances;
    
        // mint function
        function mint (address _address,uint _value) public {
          totalSupply += _value;
          balances[_address] += _value;
        }
    
        // burn function
        function burn (address _address, uint _value) public {
          if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
          }
        }
    }
  ```
* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile myToken.sol" button.

* After successful compilation of code, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

* Once the contract is deployed, you can interact with it by calling its various functions and state variables. Provide the address of the account and the number of tokens you want to mint or burn, and click the function name to execute the function.

## Authors

Vansh setia

## Additional

[Link](#add your link) to my video explanation.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
