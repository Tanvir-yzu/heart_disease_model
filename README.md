# 🫀 Heart Disease Prediction Model

<div align="center">

<!-- Project Badges Placeholder -->
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.6.1-orange.svg)
![Gradio](https://img.shields.io/badge/gradio-6.3.0-green.svg)
![Accuracy](https://img.shields.io/badge/accuracy-88.65%25-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**🚀 AI-Powered Heart Disease Prediction System**

</div>

---

## 📋 Project Description

### 🎯 Core Value Proposition
This project is an advanced heart disease prediction web application built with Gradient Boosting algorithms, achieving high-precision predictions (88.65% accuracy). Through an intuitive Gradio interface, medical professionals and general users can quickly assess patients' cardiovascular risk, providing data-driven support for early prevention and timely intervention.

### 💡 Project Mission
Utilize artificial intelligence technology to democratize heart disease risk assessment, making high-quality medical prediction tools easily accessible and usable, contributing to global cardiovascular disease prevention efforts.

---

## ✨ Key Features

### 🔬 **Machine Learning Capabilities**
- ⚡ **High-Precision Prediction**: 88.65% accuracy model based on Gradient Boosting algorithm
- 🧠 **Intelligent Feature Engineering**: Automatic calculation of blood pressure/heart rate ratio, cholesterol/age ratio, and other critical indicators
- 📊 **Probabilistic Output**: Provides both disease probability and no-disease probability for dual reference

### 🖥️ **User Experience**
- 🎨 **Modern Interface**: Utilizes Gradio Soft theme with beautiful and intuitive design
- 📱 **Responsive Design**: Supports desktop and mobile device access
- 🎛️ **Interactive Controls**: Multiple input methods including sliders, radio buttons, dropdown menus
- 💡 **Sample Data**: Built-in typical case quick test functionality

### 🛠️ **Technical Highlights**
- 🐍 **Python Ecosystem**: Based on mature Python ML ecosystem
- 🔄 **Real-time Prediction**: Instant results without waiting
- 🌐 **Web Deployment**: Supports local and public network access (share mode)
- 🔧 **Proxy Optimization**: Built-in Windows proxy issue solutions

### 📈 **Data Science**
- 🎯 **15-Dimensional Feature Analysis**: Comprehensive indicators covering age, gender, chest pain type, etc.
- 🔍 **Multi-dimensional Assessment**: Combines physiological indicators and lifestyle factors
- 📋 **Medical Mapping**: Standardized medical terminology encoding system

---

## 🚀 Installation Guide

### 📋 System Requirements
- **Operating System**: Windows 10/11, macOS, Linux
- **Python Version**: 3.8 or higher
- **Memory Requirement**: Minimum 4GB RAM (8GB+ recommended)
- **Network Environment**: Internet connection needed for initial dependency installation

### 🔧 Quick Start

#### 1️⃣ Clone Project
```bash
git clone <your-repository-url>
cd heart_disease_model
```

#### 2️⃣ Create Virtual Environment (Recommended)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

#### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

#### 4️⃣ Verify Installation
```bash
python -c "import gradio, sklearn, pandas, numpy; print('✅ All dependencies installed successfully!')"
```

### 📦 Core Dependencies
- `gradio==6.3.0` - Web interface framework
- `scikit-learn==1.6.1` - Machine learning library
- `pandas==2.3.3` - Data processing
- `numpy==2.4.1` - Numerical computing
- `joblib==1.5.3` - Model serialization

---

## 💻 Usage Instructions

### 🎮 Launch Application

#### Method 1: Direct Run (Recommended)
```bash
python app.py
```

#### Method 2: Run with Custom Port
```bash
python app.py --port 8080  # Modify port number
```

### 🌐 Access Application
- **Local Access**: http://127.0.0.1:7860
- **Network Access**: http://localhost:7860
- **Public Sharing**: Temporary public link generated on startup (share=True)

### 📝 Usage Examples

#### Example 1: Typical Middle-aged Male Patient
```python
# Enter the following values in the web interface:
Age: 45
Sex: Male
ChestPainType: ATA (Atypical Angina)
RestingBP: 130 mm Hg
Cholesterol: 250 mg/dl
FastingBS: 0 (Fasting blood sugar ≤ 120 mg/dl)
RestingECG: Normal
MaxHR: 165 bpm
ExerciseAngina: No
Oldpeak: 1.0 mm
ST_Slope: Up
```

#### Example 2: High-risk Female Patient
```python
# High-risk configuration example:
Age: 60
Sex: Female
ChestPainType: ASY (Asymptomatic)
RestingBP: 140 mm Hg
Cholesterol: 300 mg/dl
FastingBS: 1 (Fasting blood sugar > 120 mg/dl)
RestingECG: LVH (Left Ventricular Hypertrophy)
MaxHR: 140 bpm
ExerciseAngina: Yes
Oldpeak: 2.5 mm
ST_Slope: Flat
```

#### Example 3: Low-risk Young Patient
```python
# Low-risk configuration example:
Age: 35
Sex: Male
ChestPainType: NAP (Non-Anginal Pain)
RestingBP: 120 mm Hg
Cholesterol: 180 mg/dl
FastingBS: 0
RestingECG: Normal
MaxHR: 180 bpm
ExerciseAngina: No
Oldpeak: 0.0 mm
ST_Slope: Up
```

### 📊 Interpreting Prediction Results
Application returns JSON formatted results:
```json
{
  "Prediction": "Heart Disease Detected", // or "No Heart Disease"
  "Confidence": "85.32%",               // Prediction confidence
  "Probability of Disease": "85.32%",   // Disease probability
  "Probability of No Disease": "14.68%" // No-disease probability
}
```

---

## ⚙️ Configuration

### 🔧 Environment Variables
Application automatically sets the following environment variables to avoid proxy issues:
```bash
NO_PROXY=localhost,127.0.0.1,::1,0.0.0.0
HTTP_PROXY=(cleared)
HTTPS_PROXY=(cleared)
```

### 🎛️ Application Parameters
In `app.py`, the `demo.launch()` function accepts these configurable parameters:

| Parameter | Default | Description |
|-----------|---------|-------------|
| `server_name` | `127.0.0.1` | Server address |
| `server_port` | `7860` | Service port |
| `share` | `True` | Generate public link |
| `debug` | `True` | Debug mode |
| `theme` | `gr.themes.Soft()` | UI theme |

### 📁 File Path Configuration
- **Model File**: `heart_disease_model.pkl` (must be in same directory as app.py)
- **Log Output**: Real-time console display
- **Temporary Files**: System temp directory

---

## 📚 API Reference

### 🔌 Core Function Interfaces

#### `load_model(model_path='heart_disease_model.pkl')`
Loads the pre-trained cardiovascular disease prediction model.

**Parameters:**
- `model_path` (str): Model file path, defaults to 'heart_disease_model.pkl'

**Returns:**
- Deserialized scikit-learn model object

**Exceptions:**
- `FileNotFoundError`: Model file not found
- `RuntimeError`: Model loading failed

#### `predict_heart_disease(...)`
Core function for performing heart disease risk prediction.

**Input Parameters:**
| Parameter | Type | Range/Options | Description |
|-----------|------|---------------|-------------|
| `Age` | float | 20-100 | Patient age (years) |
| `Sex` | str | 'Female', 'Male' | Gender |
| `ChestPainType` | str | 'ASY', 'ATA', 'NAP', 'TA' | Chest pain type |
| `RestingBP` | float | 80-200 | Resting blood pressure (mmHg) |
| `Cholesterol` | float | 100-600 | Serum cholesterol (mg/dl) |
| `FastingBS` | int | 0, 1 | Fasting blood sugar > 120mg/dl (1=Yes) |
| `RestingECG` | str | 'LVH', 'Normal', 'ST' | Resting electrocardiogram results |
| `MaxHR` | float | 60-220 | Maximum heart rate (bpm) |
| `ExerciseAngina` | str | 'No', 'Yes' | Exercise-induced angina |
| `Oldpeak` | float | 0.0-6.0 | ST depression induced by exercise |
| `ST_Slope` | str | 'Down', 'Flat', 'Up' | ST segment slope |

**Return Value:**
```python
{
    "Prediction": str,           # Prediction result
    "Confidence": str,           # Confidence percentage
    "Probability of Disease": str, # Disease probability
    "Probability of No Disease": str # No-disease probability
}
```

**Error Return:**
```python
{"Error": "Error description message"}
```

---

## 👥 Contributing Guidelines

### 🤝 How to Contribute
We welcome all forms of contributions! Please follow these steps:

#### 1️⃣ Fork & Clone
```bash
git clone https://github.com/yourusername/heart_disease_model.git
cd heart_disease_model
git checkout -b feature/your-feature-name
```

#### 2️⃣ Development Standards
- 🐍 **Code Style**: Follow PEP 8 Python code standards
- 📝 **Documentation**: All functions must include docstrings
- 🧪 **Test Coverage**: New features require unit tests
- 🔍 **Code Review**: Self-review before submission

#### 3️⃣ Commit Standards
```bash
# Commit message format: <type>(<scope>): <subject>
git commit -m "feat(model): Add new feature engineering method"
git commit -m "fix(ui): Fix mobile display issues"
git commit -m "docs(readme): Update installation instructions"
```

**Commit Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation updates
- `style`: Code formatting adjustments
- `refactor`: Refactoring
- `test`: Testing related
- `chore`: Build process or auxiliary tool changes

#### 4️⃣ Pull Request
- 📋 Detailed description of changes and motivation
- 🔗 Link related Issues (if any)
- ✅ Ensure all tests pass
- 📸 Provide screenshots or demos if applicable

### 🐛 Bug Reports
Please use GitHub Issues template including:
- 🖥️ Operating system and environment information
- 📋 Reproduction steps
- 📷 Error screenshots or logs
- 🔍 Expected vs actual behavior

### 💡 Feature Suggestions
We particularly welcome suggestions for:
- 🎨 UI/UX improvements
- 🤖 New algorithm integration
- 📊 Visualization enhancements
- 🔧 Performance optimizations
- 🌐 Multi-language support

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### 📄 License Terms Summary
- ✅ **Permitted**: Commercial use, modification, distribution, private use
- ⚠️ **Conditions**: Must include license and copyright notice in copies
- ❌ **Limitations**: Cannot use author/copyright holder names for endorsement

**In short**: You can freely use this code, just retain the copyright notice.

---

## 📞 Contact Information

### 👤 Project Maintainer
- **Name**: AI/ML Expert Team
- **Organization**: AI/ML WEB TESTING
- **Email**: ai.ml.expert@example.com
- **GitHub**: [@ai-ml-expert](https://github.com/ai-ml-expert)

### 🌟 Technical Support
- 📚 **Documentation**: Check this README and code comments
- 🐛 **Bug Reports**: [GitHub Issues](https://github.com/ai-ml-expert/heart_disease_model/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/ai-ml-expert/heart_disease_model/discussions)
- 📧 **Email**: ai.ml.expert@example.com

### 🤝 Collaboration Opportunities
If you are:
- 🏥 **Healthcare Institutions**: Seeking customized deployment solutions
- 🔬 **Researchers**: Wanting to collaborate on model improvements
- 💼 **Enterprise Clients**: Needing commercial solutions
- 🎓 **Educational Institutions**: Using for teaching and research purposes

Welcome to contact us for deep collaboration!

---

## 🙏 Acknowledgments

### 📚 Technology Stack Thanks
- 🤖 **Scikit-Learn Team**: Providing excellent machine learning framework
- 🎨 **Gradio Team**: Creating simple yet powerful web ML interfaces
- 🐍 **Python Community**: Continuously advancing open-source AI development
- 📊 **Medical Dataset Providers**: Providing valuable data for model training

### 🌟 Special Thanks
Thanks to all researchers, developers, and healthcare workers contributing to cardiovascular health!

---

<div align="center">

**⭐ If this project helps you, please give us a star!**

Made with ❤️ by Tanvir Islam

</div>