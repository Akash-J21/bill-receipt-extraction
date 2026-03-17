# 🧾 Bill Receipt Information Extraction

## 📌 Overview

This project extracts structured information from **bill/receipt images** using a combination of **NLP (spaCy)** and **computer vision (Detectron2)**.

It identifies key entities such as:

* Bill To
* Ship To
* Billing Address
* Shipping Address
* Other relevant invoice fields

The pipeline processes input images and converts unstructured receipt data into structured outputs for further analysis.

---

## ⚙️ Features

* 🧠 Named Entity Recognition using spaCy
* 👁️ Object detection using Detectron2
* 🧾 Extracts key invoice fields (Bill To, Ship To, Addresses, etc.)
* 📂 Supports batch processing of receipt images
* 📊 Structured output for downstream use

---

## 🏗️ Project Structure

```
.
├── main.ipynb                 # Main notebook for processing
├── D@_new/
│   └── images/               # Sample input receipt images
├── output/                   # Extracted results (optional)
├── requirements.txt          # Dependencies
└── README.md
```

---

## 📋 Prerequisites

* Python 3.8+
* GPU (recommended for Detectron2)
* PyTorch installed (compatible with Detectron2)

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/bill-receipt-extraction.git
cd bill-receipt-extraction
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Install Detectron2 (based on your system):

```bash
pip install detectron2 -f https://dl.fbaipublicfiles.com/detectron2/wheels/cu118/torch2.0/index.html
```

---

## 📂 Input Data

Sample images are available in:

```
D@_new/images/
```

You can add your own receipt images in this folder for processing.

---

## ▶️ Usage

Open and run the notebook:

```bash
jupyter notebook main.ipynb
```

Steps inside notebook:

1. Load models (spaCy + Detectron2)
2. Read input images
3. Perform detection and text extraction
4. Extract structured fields
5. View/export results

---

## 🔄 Workflow

1. Detect regions of interest using Detectron2
2. Extract text from detected regions (OCR assumed if integrated)
3. Apply spaCy NER to identify entities
4. Map extracted entities into structured format

---

## 📚 Dependencies

Example `requirements.txt`:

```
spacy
torch
torchvision
detectron2
opencv-python
pandas
numpy
pytesseract
```

---

## ⚠️ Notes

* OCR (e.g., Tesseract) may be required if working with raw images
* Model accuracy depends on training data quality
* GPU improves performance significantly for Detectron2

---

## 🚀 Future Improvements

* Improve model accuracy with custom training
* Add support for more invoice fields
* Export results to JSON / CSV / database
* Build API for real-time processing
* Add UI for uploading receipts

---

## 👨‍💻 Author

**Akash J**
📧 [jakash2105@gmail.com](mailto:jakash2105@gmail.com)

##
