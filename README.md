# Shibarium Token

This repository contains token images, token details for the Shibarium bridge, supporting both ethereum and sepolia networks.

## Folder Structure

```
assets/
├── ethereum/
│ └── {tokenSymbol}/
| └── token.json
│ └── {tokenAddress}.png
├── sepolia/
│ └── {tokenSymbol}/
| └── token.json
│ └── {tokenAddress}.png
```


### Ethereum

- **Path**: `assets/ethereum/`
- **Description**: This folder contains images and detail for tokens on the ethereum network.

### Sepolia

- **Path**: `assets/sepolia/`
- **Description**: This folder contains images and detail for tokens on the sepolia network.

## How to Add a New Token Image

1. Determine if the token is for the ethereum or sepolia.
2. Create a folder named by the token symbol in CAPITAL letters under the appropriate directory (ethereum or sepolia).
3. Place the token image in this folder. Name the image file using the token's address, followed by .png (e.g., 0x1234567890abcdef.png).
4. Add a token.json file in the same folder with the following structure:
```
{
    "parentName": "BONE SHIBASWAP",
    "parentSymbol": "BONE",
    "parentContract": "0x9813037ee2218799597d83D4a5B6F3b6778218d9",
    "childName": "Bone Token",
    "childSymbol": "BONE",
    "childContract": "0x0000000000000000000000000000000000001010",
    "bridgeType": "plasma"
}
```
5. Create a pull request (PR) to the main branch with the token image and token.json file added in the respective mainnet or testnet folder.
6. Wait for the PR approval.
7. The URL for the token image will be:

   ```
   https://cdn.shib.io/shibarium-bridge/ethereum/BONE/0x9813037ee2218799597d83d4a5b6f3b6778218d9.png
   ```

   The general format is:

   ```
   https://cdn.shib.io/shibarium-bridge/${chain}/${parentSymbol}/${parentContract.toLowerCase()}.png
   ```

## Contribution

Contributions are welcome! Please ensure that any token images you add are named correctly and placed in the appropriate directory.