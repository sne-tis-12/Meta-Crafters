## Creating a Token in Solidity

The myToken.sol program provided in this repository demonstrates the creation, minting, and burning of a simple token on a blockchain using Solidity.


## Description

**This program showcases a basic smart contract written in Solidity, which is a programming language used for developing smart contracts on the Ethereum blockchain.** 

The contract defines several state variables to manage the token information, including the token's name, abbreviation, total supply of tokens in the network, and a balances mapping that associates addresses with the amount of tokens they hold. Additionally, it implements two functions: mint and burn, which allow for the modification of token amounts in the network.

 
```javascript

function mint(address _address, uint _value) public {

    totalSupply += _value;

    balances[_address] += _value;

}

```

The mint function is responsible for increasing the token supply. It takes an address _address and a value _value as parameters, and it adds the _value to both the total supply and the balance of the specified address.

```javascript

function burn(address _address, uint _value) public {

    if (balances[_address] >= _value) {

        totalSupply -= _value;

        balances[_address] -= _value;

    }

}

```

On the other hand, the burn function decreases the token supply. It verifies if the specified address has a balance greater than or equal to the value to be burned, and if so, it subtracts the value from both the total supply and the balance of the given address.

> This program serves as a simple and straightforward introduction to token creation and management in Solidity, providing a foundation for more complex token-based applications on the Ethereum blockchain.


## Authors
[Metacrafter](https://twitter.com/metacraftersio) Student   
[Sneha](https://www.linkedin.com/in/snetis/)