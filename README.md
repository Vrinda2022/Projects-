# Token Project- (Metacrafter Projects Assessment)

Learn the fundamental concepts of blockchain technology, including decentralization, consensus mechanisms, and cryptographic principles.

## Description

Develop and deploy a simple token on a blockchain platform, such as creating an ERC-20 token on Ethereum. This involves writing a smart contract that defines the token’s behavior, supply, and other properties. Understand how tokens are transferred between addresses, including the underlying mechanisms of token transactions on the blockchain. Learn to interact with the blockchain using tools like web3.js, ethers.js, or Truffle, enabling activities such as token transfers, balance checks, and smart contract interactions.

## Getting Started

### Installing

You can download the content of this code through the copy raw file option on github or download the whole repository through the Download ZIP file option.

### Executing program

* The Program can be executed by copying the code and paste it in the remix workspace at https://remix.ethereum.org/.
* After pasteing the code you can go to the solidity symbol on the left hand side tool bar and click on compile code.
* Click on the ethereum sign and there you have to click on deploy.
* Then the code will be ready for tansactions.
```
pragma solidity ^0.8.7;

contract Together {

    string public tokenName = "EvoCoin";
    string public tokenAbbrv = "EVC";
    uint public totalSupply = 0;

    mapping (address => uint) public balances;

    function mint (address ID, uint value) public {
        totalSupply += value;
        balances[ID] += value;
    }

    function burn (address id, uint _value) public {
        if (balances[id] >= _value) {
            totalSupply -= _value;
            balances[id] -= _value;
        }
    }

}
```
* Click on the mint function to mint some amount into any address provided my you.
* Click on transact to see your changes.

## Authors

Vrinda

https://www.linkedin.com/in/vrinda-mittal-415595265/

## License

This project is licensed under the MIT License - see the LICENSE.md file for details 
