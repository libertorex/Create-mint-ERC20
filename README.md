# Create-and-Mint-ERC20-Tokens
**MyToken - ERC-20 Token Smart Contract**

**Overview:**

MyToken is an ERC-20 token smart contract deployed on the Ethereum blockchain. It represents a fungible digital asset with the symbol "MTK" and is compliant with the ERC-20 standard. This contract allows the token owner to mint new tokens and transfer them to specified addresses.

**Prerequisites:**

- Truffle Suite: v5.3.6 or higher
- Solidity: v0.8.9
- OpenZeppelin Contracts: v4.3.2 (already imported via npm)

**Installation:**

1. Clone the repository:
   ```
   git clone https://github.com/your-username/MyToken.git
   cd MyToken
   ```

2. Install dependencies:
   ```
   npm install
   ```

**Usage:**

1. Deployment:
   Before deploying the smart contract, you need to configure your preferred Ethereum network and set the deployment parameters in the `truffle-config.js` file.

   ```
   truffle migrate --network <network-name>
   ```

2. Interacting with the Smart Contract:
   - To interact with the smart contract, you can use the Truffle console or deploy the contract on an Ethereum wallet like MetaMask and interact with it through the user interface.

   - The owner of the contract can mint new tokens to a specific address using the `mint` function. Only the owner has permission to perform this action.

**Smart Contract Details:**

The `MyToken` contract inherits from three OpenZeppelin contracts:

1. `ERC20`: This provides the core functionality of the ERC-20 token, including transferring tokens between addresses.

2. `ERC20Burnable`: This extends the ERC-20 token by adding the capability to burn (destroy) tokens.

3. `Ownable`: This contract allows for a single owner of the token contract, and certain functions can only be executed by the owner.

The contract constructor initializes the token with the name "MyToken" and the symbol "MTK," and it mints 1000 tokens to the address that deploys the contract.

