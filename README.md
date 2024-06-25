# Meta_ETHproject
Creating My first token

# Description
I have created this project on the platform (remix.ethereum.org) by using solidity. In this project I have created a my very own token.

# Getting Started

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

## Program Requirements

- Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
- Your contract will have a mapping of addresses to balances (address => uint)
- You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount.
- Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.
- Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.
  




## Program
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26 ;

contract MyToken {

    // public variables here
    string public tokenName="ABHINAV";
    string public tokenAbbrv="ABHI";
    uint public totalsupply=0 ;


    // mapping variable here
    mapping(address => uint) public balance ;



    // mint function
    function mint (address _address, uint _value) public {
        totalsupply= totalsupply +_value ;
        balance[_address] += _value ;

    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balance[_address ] >= _value) {
            totalsupply =totalsupply - _value;
            balance[_address] -= _value;

        }
        
    }

}
```


# How to run the program

- On the remix.ethereum.org, first go to the solidity image.
- Then in the deploy function ,click on deploy.
- Then copy the address from the address given in the address section.
- Paste that address to mint,burn, and balance sections.
- Now by entering token amount you can call your functions.

# Author
Abhinav Singh

# Lisence
This project is licensed under the MIT License - see the LICENSE.md file for details





