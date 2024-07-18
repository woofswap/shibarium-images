# Shibarium Images

This repository contains token images for the Shibarium bridge, supporting both mainnet and testnet networks.

## Folder Structure

assets/
├── mainnet/
│ └── ethereum/
│ └── {tokenAddress}.png
├── testnet/
│ └── ethereum/
│ └── {tokenAddress}.png


### Mainnet

- **Path**: `assets/mainnet/ethereum/`
- **Description**: This folder contains images for tokens on the mainnet network. Each token image is named using its token address.

### Testnet

- **Path**: `assets/testnet/ethereum/`
- **Description**: This folder contains images for tokens on the testnet network. Each token image is named using its token address.

## How to Add a New Token Image

1. Determine if the token is for the mainnet or testnet.
2. Place the token image in the appropriate folder (`mainnet` or `testnet`) under the `ethereum` directory.
3. Name the image file using the token's address, followed by `.png` (e.g., `0x1234567890abcdef.png`).

## Contribution

Contributions are welcome! Please ensure that any token images you add are named correctly and placed in the appropriate directory.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
