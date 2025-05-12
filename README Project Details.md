# Real-Time Fake Currency Detection System Using Deep Learning and Blockchain

## Overview

This system enables banks, law enforcement, and retail stakeholders to detect counterfeit currency in real time using deep learning algorithms and blockchain-based transparency. The project integrates Convolutional Neural Networks (CNNs) for image classification and Ethereum smart contracts for immutable logging of results. It aims to enhance public confidence in currency systems through accurate, secure, and scalable detection methods.

## Project Instructions

### Prerequisites

Install the following tools:

- **Python 3.8+**
- **Anaconda Navigator** (optional but recommended)
- **PyTorch & torchvision** (for CNN models)
- **OpenCV** (image preprocessing)
- **Web3.py** (for blockchain interaction)
- **MetaMask** (for Ethereum testnet)
- **Ganache or Infura** (optional local/test network)

#### Python Dependencies

```bash
pip install torch torchvision web3 opencv-python numpy pandas matplotlib
```

### Setup Instructions

#### 1. Dataset Preparation

1. Collect real and counterfeit currency images from trusted sources.
2. Apply preprocessing: grayscale, normalization, noise removal, resizing (e.g., 227x227).
3. Structure dataset:
   ```
   dataset/
   ├── real/
   └── fake/
   ```

#### 2. Train CNN Model (AlexNet)

```python
# Pseudocode snippet
alexnet = models.alexnet(pretrained=True)
alexnet.classifier[6] = nn.Linear(...)
# Train model with PyTorch
```

#### 3. Deploy Smart Contract

Smart contract: `CurrencyValidation.sol`

```solidity
pragma solidity ^0.8.0;

contract CurrencyValidation {
    struct Detection {
        bool isFake;
        uint256 timestamp;
        address validator;
    }

    mapping(bytes32 => Detection) public detections;

    event CurrencyScanned(bytes32 imageHash, bool isFake, uint256 timestamp);

    function logDetection(bytes32 imageHash, bool isFake) public {
        detections[imageHash] = Detection(isFake, block.timestamp, msg.sender);
        emit CurrencyScanned(imageHash, isFake, block.timestamp);
    }

    function getDetection(bytes32 imageHash) public view returns (bool, uint256, address) {
        Detection memory det = detections[imageHash];
        return (det.isFake, det.timestamp, det.validator);
    }
}
```

1. Compile and deploy using Remix IDE.
2. Connect MetaMask and use Sepolia testnet.
3. Save contract address and ABI.

#### 4. Integrate Blockchain with Python

```python
from web3 import Web3
w3 = Web3(Web3.HTTPProvider("https://sepolia.infura.io/v3/YOUR_PROJECT_ID"))
contract = w3.eth.contract(address='0xYourContract', abi=abi)
```

#### 5. Run Real-Time System

1. Use webcam or image upload.
2. Apply preprocessing.
3. Predict with CNN.
4. Log result to blockchain.
5. Display result to user.

### Usage Flow

- **Admin:** Configure system, view all logs
- **Teller/Staff:** Scan currency and validate
- **Public User:** Use mobile app to verify notes via QR/scan

### Directory Structure

```
├── main.py               # App entry point
├── model.py              # CNN model logic
├── blockchain.py         # Contract interaction
├── utils/
│   ├── preprocess.py     # Image enhancement functions
│   └── qr_generator.py   # Optional QR output
├── dataset/              # Real/Fake images
├── templates/
│   └── ui.html           # Web UI
├── contracts/
│   └── CurrencyValidation.sol
├── static/
│   ├── style.css
│   └── script.js
└── README.md
```

### Acknowledgements

- Dr. S. Sivamohan, Project Guide
- SRM Institute of Science and Technology
- Research credits to referenced authors (Appendix)