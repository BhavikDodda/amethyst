# Smart contracts

Self-executing code on the blockchain that automatically enforces agreements without intermediaries.

- Concept introduced by Nick Szabo in 1994 
- Popularized by Ethereum in 2015 
- Evolution with platforms like Cardano, Solana, and Hyperledger
# solidity sample code

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract HelloWorld {
    // A state variable to store a string
    string public message;

    // The constructor is executed once when the contract is deployed.
    constructor() {
        message = "Hello World";
    }

    // A public view function to retrieve the message.
    // 'view' indicates that it does not modify the contract's state.
    function getMessage() public view returns (string memory) {
        return message;
    }

    // A public function to set a new message.
    // This function modifies the contract's state.
    function setMessage(string memory _newMessage) public {
        message = _newMessage;
    }
}
```