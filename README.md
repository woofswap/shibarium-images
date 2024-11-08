# Shibarium Token Bridge

This repository contains token images and details for the Shibarium bridge, supporting the **Ethereum**, **Sepolia**, **Shibarium**, and **Puppynet** networks.

## Folder Structure

```
assets/
├── ethereum/
│   └── {tokenSymbol}/
│       ├── token.json
│       └── {tokenAddress}.png
├── sepolia/
│   └── {tokenSymbol}/
│       ├── token.json
│       └── {tokenAddress}.png
├── shibarium/
│   └── {tokenSymbol}/
│       ├── token.json
│       └── {tokenAddress}.png
├── puppynet/
│   └── {tokenSymbol}/
│       ├── token.json
│       └── {tokenAddress}.png
```

### Network Directories

- **Ethereum Network**
  - **Path**: `assets/ethereum/`
  - **Description**: Contains images and details for tokens on the **Ethereum** network.

- **Sepolia Network**
  - **Path**: `assets/sepolia/`
  - **Description**: Contains images and details for tokens on the **Sepolia** test network.

- **Shibarium Network**
  - **Path**: `assets/shibarium/`
  - **Description**: Contains images and details for tokens on the **Shibarium** test network.

- **Puppynet Network**
  - **Path**: `assets/puppynet/`
  - **Description**: Contains images and details for tokens on the **Puppynet** test network.

---

## How to Add a New Token

### 1. Determine the Token Network

- Decide whether the token belongs to the **Ethereum**, **Sepolia**, **Shibarium**, or **Puppynet** network.

### 2. Create a Token Folder

- Under the appropriate network folder (`ethereum`, `sepolia`, `shibarium`, or `puppynet`), create a new folder named using the token's **symbol** in **capital letters** (e.g., `BONE`).

### 3. Add Token Image

- Place the token image inside the newly created folder.
- **File Naming**: Name the image file using the **token's address**, followed by `.png` (e.g., `0x1234567890abcdef.png`).
- **File Size**: Ensure the image size does not exceed **200 KB**.

### 4. Add `token.json` File

- In the same folder as the image, create a `token.json` file with the following structure:

```json
{
    "parentName": "BONE SHIBASWAP",          // Name of the parent token (e.g., BONE SHIBASWAP)
    "parentSymbol": "BONE",                  // Symbol of the parent token (e.g., BONE)
    "parentContract": "0x9813037ee2218799597d83D4a5B6F3b6778218d9", // Address of the parent token contract
    "childName": "Bone Token",               // Name of the child token (e.g., Bone Token)
    "childSymbol": "BONE",                   // Symbol of the child token (e.g., BONE)
    "childContract": "0x0000000000000000000000000000000000001010", // Address of the child token contract
    "bridgeType": "plasma"                   // Type of bridge (e.g., plasma, pos)
}
```

### 5. Create a Pull Request (PR)

- Once the image and `token.json` file are added, **create a pull request (PR)** to the main branch with your changes.

### 6. PR Review and Approval

- Wait for the PR to be reviewed and approved by the maintainers.

---

## Image URL Format

Once your PR is merged, the image for the token can be accessed via the following URL format:

```
https://cdn.shib.io/shibarium-bridge/${chain}/${symbol.toUpperCase()}/${contractAddress.toLowerCase()}.png
```

- `${chain}`: Replace with the network (either `ethereum`, `sepolia`, `shibarium`, or `puppynet`).

### For `${symbol}`:
- If **`parentSymbol`** is provided, use that as the symbol in the URL.
- If **`childSymbol`** is provided, use that as the symbol in the URL.

### For `${contractAddress}`:
- If **`parentContract`** is provided, use that as the contract address in the URL.
- If **`childContract`** is provided, use that as the contract address in the URL.

### Example URL:
If you added the `BONE` token for the **Ethereum** network, with the **parent contract address** of `0x9813037ee2218799597d83D4a5B6F3b6778218d9`, the image URL would be:

```
https://cdn.shib.io/shibarium-bridge/ethereum/BONE/0x9813037ee2218799597d83d4a5b6f3b6778218d9.png
```

If you added the same token but provided the **child contract address** as `0x0000000000000000000000000000000000001010`, the image URL would be:

```
https://cdn.shib.io/shibarium-bridge/ethereum/BONE/0x0000000000000000000000000000000000001010.png
```

---

## Contribution Guidelines

We welcome contributions! To ensure consistency and proper management of token images, please adhere to the following guidelines:

1. **Folder Naming**: Ensure the folder name is the token symbol in **capital letters** (e.g., `BONE`).
2. **Image Naming**: Name the image file using the **token address** followed by `.png` (e.g., `0x1234567890abcdef.png`).
3. **Image Size**: Ensure the token image does not exceed **200 KB** in size.
4. **File Format**: Use the specified structure for the `token.json` file.
5. **Contract Addresses**: Ensure that the contract addresses are accurate and in the correct format (all lowercase).

By following these instructions and ensuring the correctness of the files, your token addition will be quickly reviewed and integrated.

---

Let me know if you need any further updates or clarifications!