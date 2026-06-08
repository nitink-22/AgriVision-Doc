# AgriVision Doctor

Production-ready AI system with automated background removal and Grad-CAM visual diagnostics.

AgriVision Doctor is an enterprise-grade Streamlit application designed for rapid, field-level botanical diagnostics. Powered by a custom-trained ResNet-50 Convolutional Neural Network, the system can accurately identify 38 distinct plant pathogens and healthy states across 14 different crop species.

## Live Demo
[Launch AgriVision Doctor Web App]
 https://nitink-22-agrivision-doc-app-2bozjv.streamlit.app/


---

## Core Features

* Deep Learning Diagnostics: Utilizes a fine-tuned ResNet-50 model to classify images into 38 distinct categories with high confidence.
* Auto-Isolate Leaf (Alpha Matting): Integrates rembg with advanced alpha matting to automatically strip complex backgrounds, allowing the AI to focus purely on the botanical structure.
* AI Focus X-Ray (Grad-CAM): Generates Gradient-weighted Class Activation Mapping (Grad-CAM) heatmaps in real-time, overlaying a visual representation of the exact cellular structures that triggered the AI's diagnosis.
* Actionable Protocols: Maps identified pathogens directly to an internal database of recommended agricultural treatments and mitigation strategies.
* Dual-Input Processing: Supports both local file uploads and live device-camera capture streams.
* Enterprise UI/UX: Features a responsive, dark-mode CSS dashboard optimized for both desktop analysis and mobile field-use.

---

## Supported Crops
The model is currently trained to process leaves from the following 14 species:
Apple | Blueberry | Cherry | Corn | Grape | Orange | Peach | Pepper (Bell) | Potato | Raspberry | Soybean | Squash | Strawberry | Tomato

---

## Local Installation & Setup

If you wish to run AgriVision Doctor locally on your own machine, follow these steps:

1. Clone the repository
git clone https://github.com/nitink-22/AgriVision-Doc.git
cd AgriVision-Doc

2. Create and activate a virtual environment

Windows:
python -m venv env
.\env\Scripts\activate

Mac/Linux:
python3 -m venv env
source env/bin/activate

3. Install dependencies
pip install -r requirements.txt

4. Add the Model Weights
Ensure your trained weights file (enterprise_plant_model.pth) is placed directly in the root directory of the project.

5. Launch the Application
streamlit run app.py

---

## Project Structure

AgriVision-Doc/
├── app.py                         # Main Streamlit application script
├── requirements.txt               # Python dependencies for deployment
├── .gitignore                     # Git exclusion rules
├── enterprise_plant_model.pth     # Trained ResNet-50 weights (Local requirement)
└── README.md                      # Project documentation

---

## Technology Stack
* Frontend/Deployment: Streamlit
* Deep Learning Framework: PyTorch
* Computer Vision: OpenCV
* Background Removal: Rembg
* Data Processing: NumPy & Pillow