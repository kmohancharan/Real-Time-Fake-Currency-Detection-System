# 💵 Real-Time Fake Currency Detection System Using Deep Learning

This repository contains the source code, model training pipeline, system architecture, and supporting materials for the project **"Real-Time Fake Currency Detection System Using Deep Learning"**, developed as part of the Bachelor of Technology degree in Computer Science and Engineering (IoT specialization) at SRM Institute of Science and Technology.

---

## 🧠 Abstract

Counterfeit currency is a growing threat to global financial systems. Traditional detection techniques like UV scanning or manual verification are slow, error-prone, and costly. This project proposes a **deep learning-based real-time fake currency detection system**, using **Convolutional Neural Networks (CNNs)** trained on a large dataset of genuine and counterfeit banknotes. It also integrates **blockchain technology** for secure and tamper-proof recording of detection events.

The system is built with a modular architecture comprising data preprocessing, model training, a real-time prediction interface, and a blockchain-backed logging mechanism.

---

## 👨‍💻 Authors

- K. Mohan Charan (RA2111032010020)
- K. Sri Siva Hari Kishore (RA2111032010043)
- D. Venkata Jagadeesh (RA2111032010063)

Project Guide: **Dr. S. Sivamohan**, Assistant Professor, Department of Networking and Communications

---

## 🚀 Features

- ✅ Real-time image-based detection of counterfeit currency
- 🧠 CNN-based classification using **AlexNet**
- 🔒 Integration with **blockchain** for secure logging of detections
- 🌍 Scalable architecture for global use across banks and retailers
- 📊 Admin dashboard for viewing analytics and system performance
- 🧩 Modular microservice components for flexibility and upgradability

---

## 🔧 Tech Stack

| Technology      | Description                             |
|-----------------|-----------------------------------------|
| Python          | Core programming language               |
| PyTorch         | Deep learning framework                 |
| TensorFlow/Keras| Model experimentation (optional phases) |
| OpenCV / PIL    | Image preprocessing and enhancement     |
| Flask / Django  | Web application backend (TBD)           |
| HTML/CSS/JS     | Web interface for uploading and results |
| Hyperledger / Ethereum | Blockchain logging (conceptual demo) |
| Google Colab    | Model training and GPU support          |

---

## 🧪 How It Works

1. **Dataset Preparation**  
   - Collect high-resolution images of real and counterfeit banknotes.
   - Apply preprocessing: resizing, normalization, noise removal, grayscale conversion.

2. **Model Training (AlexNet)**  
   - Implemented in PyTorch.
   - 80/20 train-test split with image augmentation.
   - Achieved high classification accuracy on validation set.

3. **Prediction System**  
   - Upload currency note images via web interface.
   - Predict authenticity and classify as real or fake.
   - Optionally log result to blockchain.

4. **Blockchain Integration**  
   - Detection result + timestamp are stored as immutable logs.
   - Enhances transparency and trust for auditing.

---

## 💻 Usage Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/fake-currency-detector.git
cd fake-currency-detector

## 📈 Results

- **Model Used**: AlexNet (Modified)
- **Accuracy**: ~97.5%
- **Precision**: 96%
- **Recall**: 98%
- **Real-time Feedback**: < 1 second
- **Security Logging**: Blockchain (Proof of Concept)

---

## 🌍 Use Cases

- 🏦 Bank teller systems
- 🛒 Retail checkout verification
- 🚓 Law enforcement analysis
- 💱 Currency exchange validation

---

## 🎯 Sustainable Development Goals (SDG)

This project aligns with **UN SDG 16: Peace, Justice, and Strong Institutions** by promoting financial security, reducing fraudulent activities, and supporting transparent record-keeping via blockchain.

---

## 🔮 Future Enhancements

- 📱 Mobile app for field detection
- 💾 Integration with ATM/Cash Deposit Machines
- 🌐 Cloud-based detection API
- 🧩 Transfer learning with VGG-16, ResNet
- 🔁 Automatic model retraining with new data

---

## 📜 License

This project is for academic and non-commercial research purposes. Please contact the authors for permission to reuse or modify.

---

## 📧 Contact

For any questions, reach out to:

**Dr. S. Sivamohan** – [sivamohs2@srmist.edu.in](mailto:sivamohs2@srmist.edu.in)  
**SRM Institute of Science and Technology**, Department of Networking and Communications

