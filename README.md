# 🎯 GuessNumber Smart Contract
A simple and beginner-friendly Solidity project where users try to guess a hidden number stored inside the smart contract. If they guess correctly — they win!

---

## 📌 Project Description
GuessNumber is a straightforward learning project built to help beginners understand how smart contracts work in Solidity.  
The contract stores a secret number and allows anyone to guess it. If the guess is correct, the contract records the winner's address permanently.

This project is ideal for:

- Solidity beginners  
- Learning how functions, state variables, and conditions work  
- Understanding how blockchain apps can handle simple game logic  

---

## 🚀 What This Contract Does
- Stores a **secret number** internally (`7` by default)  
- Allows players to make a guess  
- Checks if the guess is correct  
- Saves the first person who guesses correctly as the **winner**  
- Prevents further guesses after a winner is declared  

---

## ✨ Features
✔ No deployment inputs required  
✔ Simple & easy-to-read code  
✔ Uses basic conditional logic  
✔ Publicly displays the winner’s address  
✔ Beginner-friendly and perfect for learning  
✔ Minimal gas usage  

---

## 🔗 Deployed Smart Contract
**Contract Address:** `XXX`  
*(Replace this with your actual deployed address)*

---

## 🧩 Smart Contract Code

```solidity
//paste your code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract GuessNumber {
    uint256 private secretNumber = 7; // fixed number, no input during deployment
    address public winner;

    function guess(uint256 _guess) public returns (string memory) {
        require(winner == address(0), "Game already won!");

        if (_guess == secretNumber) {
            winner = msg.sender;
            return "Correct! You won!";
        } else {
            return "Wrong guess. Try again!";
        }
    }
}
```
