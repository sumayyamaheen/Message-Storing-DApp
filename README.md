# 📩 Simple Message Storing DApp

A basic decentralized application (DApp) built with **HTML**, **CSS**, **JavaScript**, **Ethers.js**, and **MetaMask**, allowing users to **write and read messages** from an Ethereum smart contract.

---

## 🚀 Features
- ✔ Connects automatically to MetaMask  
- ✔ Writes a message to the blockchain  
- ✔ Reads all messages stored in your smart contract  
- ✔ Clean glass-morphism UI  
- ✔ Uses Ethers.js for blockchain interaction  

---

## 🛠️ Tech Stack
- **HTML + CSS + JavaScript**
- **Ethers.js**
- **MetaMask**
- **Solidity Smart Contract (deployed via Remix)**

---

## 📦 File Structure
```
simple-dapp/
│── index.html
│── style.css
│── README.md
```

---

## 🔧 Smart Contract Used
Make sure you deploy this contract in Remix:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract MessageStore {
    string[] public messages;

    function setMessage(string memory _message) public {
        messages.push(_message);
    }

    function getAllMessages() public view returns (string[] memory) {
        return messages;
    }

    function getLatestMessage() public view returns (string memory) {
        if (messages.length == 0) return "No messages yet";
        return messages[messages.length - 1];
    }
}
```

After deploying, copy the contract address and paste it in `index.html`:

```js
const contractAddress = "YOUR_DEPLOYED_CONTRACT_ADDRESS";
```

---

## 🖥 How to Run Locally
### **1. Download or Clone the Repo**
```
git clone https://github.com/YOUR-USERNAME/simple-dapp.git
```

### **2. Open the App**
Just open **index.html** in any browser.

### **3. Connect MetaMask**
- Install MetaMask  
- Connect to the appropriate network (your testnet)

### **4. Interact with Your DApp**
- Type a message  
- Click **Set Message** to save it  
- Click **Get Message** to read messages  

---

## 🧪 Requirements
- MetaMask installed  
- Ethereum Test Network (Sepolia, Holesky, Local Ganache, etc.)  
- ABI + Contract Address updated

---

## 📸 Screenshot (UI)
*(Add your screenshot here)*  
Example:
```
![DApp Screenshot](screenshot.png)
```

---

## 📝 Author
**Your Name (Optional)**  
Built for learning Web3 & Smart Contract integration.

---

## ⭐ Star this repo if you found it helpful!
