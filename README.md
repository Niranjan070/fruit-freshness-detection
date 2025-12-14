# 🍎 Fruit Freshness Detection App

An AI-powered web application that detects whether a fruit is **fresh** or **rotten** using deep learning. Built with TensorFlow and Streamlit for an interactive user experience.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.20-orange.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.52-red.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Demo](#-demo)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Model Information](#-model-information)
- [Technologies Used](#-technologies-used)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

This application uses a **Convolutional Neural Network (CNN)** trained to classify fruit images as either fresh or rotten. Simply upload an image of a fruit, and the AI will analyze it and provide instant feedback on its freshness status.

### Use Cases
- 🏪 **Grocery stores** - Quick quality checks on produce
- 🏠 **Home use** - Check if your fruits are still good to eat
- 🚚 **Supply chain** - Quality control during distribution
- 📚 **Educational** - Learn about AI-based image classification

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🖼️ **Image Upload** | Support for JPG, JPEG, and PNG formats |
| 🧠 **AI Detection** | Deep learning-based freshness classification |
| ⚡ **Real-time Results** | Instant predictions with visual feedback |
| 🎨 **User-friendly UI** | Clean and intuitive Streamlit interface |
| 🔄 **Auto Image Conversion** | Handles RGBA, grayscale, and other formats |

---

## 🎬 Demo

1. Upload a fruit image (apple, banana, orange, etc.)
2. The AI analyzes the image
3. Get instant results:
   - ✅ **Fresh Fruit** - Safe to consume
   - ❌ **Rotten Fruit** - Not recommended for consumption

---

## 🚀 Installation

### Prerequisites

- Python 3.10 or higher
- pip (Python package manager)

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fruit_freshness_app.git
   cd fruit_freshness_app
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # Windows
   venv\Scripts\activate
   
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ensure the model file exists**
   
   Make sure `fruit_freshness_model.h5` is in the project root directory.

---

## 💻 Usage

### Running the Application

```bash
streamlit run app.py
```

The app will open in your default browser at `http://localhost:8501`

### How to Use

1. Click **"Browse files"** or drag and drop an image
2. Wait for the image to load
3. View the prediction result:
   - ✅ Green banner = Fresh fruit
   - ❌ Red banner = Rotten fruit

---

## 📁 Project Structure

```
fruit_freshness_app/
│
├── app.py                      # Main Streamlit application
├── fruit_freshness_model.h5    # Pre-trained CNN model (~134 MB)
├── requirements.txt            # Python dependencies
├── README.md                   # Project documentation
└── venv/                       # Virtual environment (not tracked in git)
```

---

## 🧠 Model Information

| Property | Value |
|----------|-------|
| **Architecture** | Convolutional Neural Network (CNN) |
| **Framework** | TensorFlow / Keras |
| **Input Size** | 224 x 224 pixels |
| **Input Channels** | 3 (RGB) |
| **Output** | Binary classification (Fresh / Rotten) |
| **File Format** | HDF5 (.h5) |

### Prediction Logic

```python
if prediction[0][0] > 0.5:
    result = "Rotten Fruit"
else:
    result = "Fresh Fruit"
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python 3.10+** | Programming language |
| **TensorFlow 2.20** | Deep learning framework |
| **Keras** | High-level neural networks API |
| **Streamlit 1.52** | Web application framework |
| **Pillow (PIL)** | Image processing |
| **NumPy** | Numerical computations |

---

## 🔧 Troubleshooting

### Common Issues

#### 1. "ValueError: expected axis -1 of input shape to have value 3"
**Cause:** Image has 4 channels (RGBA) instead of 3 (RGB)

**Solution:** The app automatically handles this, but ensure you're using the latest version of `app.py`

#### 2. Model file not found
**Cause:** `fruit_freshness_model.h5` is missing

**Solution:** Ensure the model file is in the same directory as `app.py`

#### 3. TensorFlow installation issues
**Solution:**
```bash
pip uninstall tensorflow
pip install tensorflow==2.20.0
```

#### 4. Streamlit not opening in browser
**Solution:** Manually navigate to `http://localhost:8501` in your browser

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 Fork the repository
2. 🌿 Create a feature branch (`git checkout -b feature/amazing-feature`)
3. 💾 Commit your changes (`git commit -m 'Add amazing feature'`)
4. 📤 Push to the branch (`git push origin feature/amazing-feature`)
5. 🔃 Open a Pull Request

### Ideas for Contribution
- [ ] Add support for more fruit types
- [ ] Improve model accuracy
- [ ] Add confidence score display
- [ ] Implement batch image processing
- [ ] Add dark/light theme toggle

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)

---

## 🙏 Acknowledgments

- TensorFlow team for the amazing deep learning framework
- Streamlit team for the intuitive web app framework
- The open-source community for continuous inspiration

---

<div align="center">

**⭐ If you found this project helpful, please give it a star! ⭐**

Made with ❤️ using Python, TensorFlow & Streamlit

</div>
