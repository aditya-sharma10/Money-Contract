# 💰Money Contract

A simple Solidity smart contract that demonstrates owner-controlled fund management on Ethereum. Users can deposit Ether into the contract, and only the owner can withdraw funds or transfer ownership. Ideal for learning Ether transfers, contract ownership, and secure withdrawals.



## 📜Features:

+ Owner Management: Tracks a single owner with exclusive rights to withdraw funds or assign a new owner.

+ Withdraw Specific Amount: Owner can withdraw a specified amount of Ether safely.

+ Withdraw All Funds: Convenient function to withdraw the entire balance of the contract.

+ Receive Ether: Contract can accept Ether sent directly using receive().

+ Secure Ownership Transfer: Only the current owner can transfer ownership; zero addresses are disallowed.




## ⚙️Functions
**Function	Description**
```

+ withdraw(uint256 _amount)	Owner can withdraw a specific amount of Ether.
+ withdrawAll()	Owner can withdraw the entire contract balance.
+ setOwner(address newOwner)	Owner can transfer ownership to a new address.
+ receive()	Enables the contract to accept Ether sent directly.
```

## 🚀 Usage

> Deploy the Contract
+ The deploying account becomes the initial owner.
+ Send Ether to the Contract
+ (bool success, ) = address(money).call{value: 1 ether}("");
+ require(success, "Transfer failed");





+ Withdraw Funds (Owner Only)

+ money.withdraw(0.5 ether); // Withdraw a specific amount
+ money.withdrawAll();       // Withdraw all funds


+ Change Ownership (Owner Only)

+ money.setOwner(newOwnerAddress);
---
## 🛡️ Security Notes
``` 
Only the owner can withdraw funds or change ownership.

Using call for transfers to avoid gas limit issues with transfer().

Ownership cannot be set to the zero address.

📚 Learning Benefits

Understanding payable addresses and Ether transfers.

Learning owner-restricted functions and access control.

Practicing receive() functions for direct Ether reception.

Writing secure Solidity contracts for real-world fund management.
```

📜 License

MIT License © 2025
