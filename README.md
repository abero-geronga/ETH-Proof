# Solidity Ethereum Proof

This smart contract defines a basic token called "META" with the symbol "MTA" that includes both minting and burning capabilities.

## Description

This smart contract offers a simple token implementation with features to mint new tokens and burn existing ones. It's designed to be user-friendly and easy to understand, serving as a great introduction to Ethereum smart contracts.

## Getting Started

### Installing

* Open [Remix IDE](https://remix.ethereum.org/).
* Once you are on the Remix website, create a new file by clicking on the `+` icon in the left-hand sidebar. Save the file with a `.sol` extension (e.g., `myToken.sol`). Copy and paste the following code into the file:


`contract MyToken {

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


}`
  
### Executing program

To mint tokens, go to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and select the "MyToken" contract. Click on the "mint" function, then enter the account address in the _address text field and the token amount in the _value text field. Finally, click the "transact" button to mint tokens to the specified account.

To burn tokens, navigate to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and choose the "MyToken" contract. Click on the "burn" function, then input the account address in the _address text field and the token amount in the _value text field. Click the "transact" button to burn tokens from the specified account.

To check an account's token balance, go to the "Deployed/Unpinned Contracts" section in the left-hand sidebar and select the "MyToken" contract. Click on the "balances" function, then enter the account address in the address text field. Click the "call" button to display the token balance for the specified account.

## Help
For any issues, please create an issue

## Authors

Abero Isaiah D. Geronga

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
