# Solidity Ethereum Proof

This Solidity program focuses on minting and burning tokens. Its purpose is to provide an understanding of tokens and demonstrate how they function in Solidity.

## Description

This Solidity-based smart contract is designed for minting and burning tokens on the Ethereum blockchain. It features functions to create new tokens (mint) and destroy existing ones (burn), enabling dynamic management of the token supply. This contract serves as a fundamental example for developers who want to grasp the basics of token supply control in Solidity, offering a foundation for more sophisticated token management systems in the future.

## Getting Started

### Installing

* Open [Remix IDE](https://remix.ethereum.org/).
* Once you are on the Remix website, create a new file by clicking on the `+` icon in the left-hand sidebar. Save the file with a `.sol` extension (e.g., `myToken.sol`). Copy and paste the following code into the file:

```javascript
contract MyToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
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

        if (balances[_address] >= _value){

        totalSupply -= _value;
        balances[_address] -= _value;
        }

    }


}
```
  
### Executing program

To mint tokens, go to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and select the "MyToken" contract. Click on the "mint" function, then enter the account address in the _address text field and the token amount in the _value text field. Finally, click the "transact" button to mint tokens to the specified account.

To burn tokens, navigate to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and choose the "MyToken" contract. Click on the "burn" function, then input the account address in the _address text field and the token amount in the _value text field. Click the "transact" button to burn tokens from the specified account.

To check an account's token balance, go to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and select the "MyToken" contract. Click on the "balances" function, then enter the account address in the address text field. Click the "call" button to display the token balance for the specified account.

## Help
For any issues, please create an issue

## Authors

Abero Isaiah D. Geronga

## License

This project is licensed under the MIT License - see the LICENSE file for details
