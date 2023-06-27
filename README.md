# Creating a Token 
The token has the name "META" and the initials "MTA." The project permits the creation and destruction of tokens.

Depending on your particular objectives and intents, the project's goal may change:
1. Building a Custom Token: On the Ethereum network, we are building a custom token with the name "META" and the symbol "MTA." This token might represent ownership, value, or participation rights inside a certain ecosystem or enterprise, among other things.
   
2. Token Creation and Destruction: The project offers the ability to mint (produce) and burn (destroy) tokens. You can raise the total number of tokens available and assign them to a particular address using the mint function. The supply of tokens can be reduced by removing them from a particular address using the burn function.This feature can be used for controlling token distribution, rewards, or modifying token supply in accordance with predetermined guidelines or requirements.

3. Token Management and Balances: The project comes with a mapping variable named "balances," which enables you to keep track of the token balances held by various addresses. The "public" keyword indicates that the balances are available to the whole public. This feature makes token balances transparent and enables users or outside systems to check them.

   
## Description

In this project, a token with the name "META" and the symbol "MTA" will be created on the Ethereum network. The goal of this project is to create a digital asset with multiple uses inside a certain ecosystem or project. The mint function enables the production of fresh tokens, boosting the available quantity, and assigning them to a certain address. This can be used to distribute tokens, give out awards, or raise money. On the other hand, the burn function allows you to remove tokens from a particular address, so lowering the total supply. This functionality is useful for controlling the supply of tokens according to predetermined guidelines or needs. Also included in the project is a mapping variable named "balances," which keeps track of the token balances of various addresses. As a result, token holdings may be verified by users or other external systems and transparency is provided. Overall, your project gives you the ability to design, oversee, and disseminate a unique token on the Ethereum blockchain. This opens up the door for a variety of potential uses, including loyalty schemes, decentralised finance (DeFi) platforms, or in-app currencies inside a particular ecosystem.

## Getting Started

### Installing

Installing an Ethereum development environment - The Remix Ethereum IDE can be used to set up an Ethereum development environment.
The files don't require any special adjustments. However, it's crucial to check that our development environment and required dependencies are correctly configured.


### Executing program

To run the provided smart contract code, we can follow these step-by-step instructions:

1. Set up the Ethereum Development Environment:

Install Remix IDE, a web-based Ethereum development environment, or use another development environment of your choice.
2. Creating  a New Solidity File:

Open the Remix IDE .
Create a new Solidity file and name it "MyToken.sol".
Write the required code into the "MyToken.sol" file.
Compile the Smart Contract:

In the Remix IDE, navigate to the "Solidity Compiler" section.
Select the "MyToken.sol" file.
Click the "Compile" button to compile the smart contract.

3. Deploy the Smart Contract:

In the Remix IDE, navigate to the "Deploy & Run Transactions" section.
Select the "MyToken" contract from the dropdown.
Click the "Deploy" button to deploy the smart contract to the selected network.
Take note of the deployed contract's address for future interactions.

4. Interact with the Smart Contract:

In the Remix IDE, navigate to the "Deployed Contracts" section.
Select the deployed "MyToken" contract from the list.
We will see the contract's public variables (tokenName, tokenAbbrv, totalSupply) and the "balances" mapping.
To interact with the contract, you can use the provided functions:
To mint new tokens, call the "mint" function and provide an address and the amount to mint as parameters.
To burn tokens, call the "burn" function and provide an address and the amount to burn as parameters.
After executing a function, you can check the updated state variables and balances.

Code Block :
```
function mint (address _address, uint _value) public{
    totalSupply += _value;
    balances[_address] += _value;
}
```
```
function burn (address _address, uint _value) public{
    if(balances[_address] >= _value){
        totalSupply -= _value;
        balances[_address] -= _value;
    }
```



## Authors
Avinash


## License

This project is licensed under the [Avinash] License - see the LICENSE.md file for details
