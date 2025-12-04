
# 🔑 Keystractor: Intelligent Keyword & Entity Extraction Engine
### *Unlock the Hidden Value in Your Documents*

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Web-Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SpaCy](https://img.shields.io/badge/NLP-SpaCy-09A3D5?style=for-the-badge&logo=spacy&logoColor=white)
![Tesseract](https://img.shields.io/badge/OCR-Tesseract-green?style=for-the-badge)
![YAKE](https://img.shields.io/badge/Keyword-YAKE!-orange?style=for-the-badge)

---

## 🚀 Executive Summary

**Keystractor** is a powerful, multimodal document intelligence tool designed to bridge the gap between unstructured data and actionable insights. Whether dealing with scanned images or digital PDFs, Keystractor utilizes an advanced pipeline of **Optical Character Recognition (OCR)** and **Natural Language Processing (NLP)** to extract text, identify key entities (Names, Locations, Skills), and surface the most relevant keywords.

Wrapped in a playful, **kid-friendly "Blue Bubble" interface**, the complex backend processing is made accessible to everyone. From recruiters parsing resumes to researchers analyzing papers, Keystractor turns static documents into structured knowledge.

---

## 🔮 The Tech Stack

| Domain | Technology Stack | Role in Keystractor |
| :--- | :--- | :--- |
| **Backend Framework** | `Flask`, `Jinja2` | Orchestrates the application logic and serves the dynamic frontend. |
| **Optical Character Recognition** | `Tesseract OCR`, `Pytesseract` | Extracts raw text from image files (PNG, JPG, GIF). |
| **PDF Processing** | `PyMuPDF (fitz)` | High-fidelity text extraction from digital PDF documents. |
| **Natural Language Processing** | `SpaCy (en_core_web_sm)` | Performs Named Entity Recognition (NER) and linguistic analysis. |
| **Keyword Extraction** | `YAKE!` | Unsupervised statistical keyword extraction for identifying top topics. |
| **Frontend UI** | `HTML5`, `CSS3` | Provides a responsive, animated, and visually engaging user experience. |

---

## 🧠 System Architecture

```mermaid
graph TD
    subgraph "Frontend Layer"
    A["User Uploads File"] --> B("File Type Selection")
    end

    subgraph "Processing Core"
    B -->|Image| C["OCR Engine (Tesseract)"]
    B -->|PDF| D["PDF Extractor (PyMuPDF)"]
    C --> E["Raw Text"]
    D --> E
    end

    subgraph "Intelligence Layer"
    E --> F{"NLP Pipeline"}
    F -->|SpaCy| G["Entity Extraction"]
    F -->|YAKE| H["Keyword Extraction"]
    F -->|Regex| I["Pattern Matching"]
    end

    subgraph "Output Layer"
    G --> J["Structured Results"]
    H --> J
    I --> J
    J --> K["Web Dashboard"]
    end

---

## 🔬 The Methodology Matrix

Keystractor employs a multi-stage processing pipeline to ensure maximum accuracy and relevance in extraction.

| **Stage** | **Technique / Library** | **Implementation Details** | **Strategic Value** |
| :--- | :--- | :--- | :--- |
| **1. Ingestion** | **File Handling** | • Supports `image/*` and `application/pdf`.<br>• Secure filename sanitization via `werkzeug`. | Ensures safe and versatile file uploads for diverse use cases. |
| **2. OCR & Text** | **Tesseract & PyMuPDF** | • **Images:** Converts pixel data to text strings.<br>• **PDFs:** Iterates through pages to scrape text layers. | Transforms "dead" pixels into machine-readable text for downstream analysis. |
| **3. NLP Core** | **SpaCy NER** | • **Model:** `en_core_web_sm` transformer.<br>• **Tasks:** Identifies `PERSON`, `GPE` (Location), and Noun Chunks. | Provides semantic understanding of the document's content beyond simple words. |
| **4. Keyword Analysis** | **YAKE! Algorithm** | • **Settings:** N-gram size=3, Top-20 keywords.<br>• **Logic:** Statistical extraction based on text features (casing, position, frequency). | Surfaces the "main ideas" of a document without needing a training dataset. |
| **5. Pattern Matching** | **Regular Expressions** | • **Email:** `\S+@\S+`<br>• **Phone:** `\d{3}[-.\s]?\d{3}[-.\s]?\d{4}` | Precision extraction of critical contact information often missed by generic NLP models. |

---

## ⚡ Quick Start Guide

### Prerequisites
*   Python 3.10+
*   [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) installed on your system.

### 1. Clone the Repository
```bash
git clone https://github.com/SalmaTech-03/Keystractor.git
cd Keystractor
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

### 3. Run the Application
```bash
python app.py
```
*The application will launch at `http://127.0.0.1:5000/`*

---

## 📸 Visuals

### *The Dashboard*
A clean, animated interface featuring floating bubbles and clear call-to-action buttons. Users can toggle between Image and PDF processing modes effortlessly.

### *The Output*
Results are presented in distinct sections:
1.  **💡 Extracted Keywords:** A bulleted list of the most important terms.
2.  **📄 Extracted Text:** The full raw text recovered from the document.
3.  **🔍 Entities (Coming Soon):** Structured data for Names, Locations, and Contact Info.

---

## 📂 Project Structure

```text
Keystractor/
├── static/
│   └── styles.css          # The "Blue Bubble" visual theme
├── templates/
│   └── index.html          # Main application interface
├── uploads/                # Temporary storage for processed files
├── utils/
│   └── helper.py           # File safety utilities
├── app.py                  # Main Flask application entry point
├── ocr_engine.py           # Tesseract OCR wrapper
├── pdf_extractor.py        # PyMuPDF extraction logic
├── keyword_extract.py      # YAKE & SpaCy integration
├── extract_name_location.py # specialized entity extraction logic
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## 🔮 Future Roadmap

*   [ ] **Resume Parser Mode:** Specialized extraction for CVs (Skills, Experience, Education).
*   [ ] **Batch Processing:** Upload multiple files at once.
*   [ ] **API Endpoint:** Expose extraction logic via REST API for external integrations.
*   [ ] **Dark Mode:** A neon-cyberpunk visual theme alternative.

---

<p align="center">
  <sub>Built with 💙 by SalmaTech-03. Unlock your data.</sub>
</p>
