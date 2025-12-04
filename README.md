# MyToken - ERC-20 Token Implementation

A simple ERC-20 token smart contract built for learning blockchain development fundamentals.

## Token Specifications

- **Name:** MyToken
- **Symbol:** MTK
- **Decimals:** 18
- **Total Supply:** 1,000,000 tokens (1,000,000,000,000,000,000,000,000 with 18 decimals)
- **Solidity Version:** ^0.8.0
- **License:** MIT

## Features

✅ Full ERC-20 standard compliance
✅ Token transfer functionality
✅ Approve and transferFrom for delegated transfers
✅ Balance tracking for all addresses
✅ Event emissions for Transfer and Approval
✅ Input validation and error handling
✅ Zero address protection

## Smart Contract Functions

### Read Functions
- `name()` - Returns token name
- `symbol()` - Returns token symbol
- `decimals()` - Returns decimal places
- `totalSupply()` - Returns total token supply
- `balanceOf(address)` - Returns balance of an address
- `allowance(address, address)` - Returns approved allowance

### Write Functions
- `transfer(address _to, uint256 _value)` - Transfer tokens
- `approve(address _spender, uint256 _value)` - Approve spending
- `transferFrom(address _from, address _to, uint256 _value)` - Delegated transfer

## Testing Results

### Deployment
- ✅ Successfully deployed on Remix VM (Prague)
- ✅ Contract Address: 0xD91...39138
- ✅ Initial supply correctly assigned to deployer

### Function Testing
- ✅ All metadata functions return correct values
- ✅ Transfer function successfully moved 100 tokens
- ✅ Sender balance decreased correctly (999,900 tokens)
- ✅ Recipient balance increased correctly (100 tokens)
- ✅ Events properly emitted
- ✅ Input validation working (zero address checks, balance checks)

## How to Deploy

1. Open [Remix IDE](https://remix.ethereum.org/)
2. Create a new file `MyToken.sol`
3. Copy the contract code
4. Compile with Solidity 0.8.0 or higher
5. Deploy using JavaScript VM
6. Enter total supply in constructor (e.g., 1000000000000000000000000)

## Usage Examples

### Check Balance
```solidity
balanceOf(0x5B38Da6a701c568545dCfcB03FcB875f56beddC4)
// Returns: 1000000000000000000000000
```

### Transfer Tokens
```solidity
transfer(0xAb8483F64d9C6d1EcF9b849Ae677dD3315835cb2, 100000000000000000000)
// Transfers 100 tokens
```

### Approve and TransferFrom
```solidity
// Account A approves Account B
approve(accountB, 50000000000000000000)

// Account B transfers from A to C
transferFrom(accountA, accountC, 50000000000000000000)
```

## Learning Outcomes

- Understanding ERC-20 token standard
- Implementing balance tracking with mappings
- Using events for transaction logging
- Input validation and error handling
- Testing smart contracts in Remix
- Deployment on Ethereum test networks

## Project Structure

```
erc20-mytoken/
├── contracts/
│   └── MyToken.sol          # Main token contract
├── README.md                # Project documentation
└── screenshots/             # Testing screenshots
```

## Technologies Used

- Solidity ^0.8.0
- Remix IDE
- Ethereum Virtual Machine (EVM)
- GitHub for version control

## Author

Created as part of Partnr Network blockchain learning task.

## License

MIT License - Feel free to use this code for learning purposes.
