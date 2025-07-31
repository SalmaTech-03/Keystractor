# 🧠 Keystractor

A Flask-based web application that extracts text and identifies key information such as names, locations, and skills from uploaded images or PDF documents using OCR and NLP techniques.

## 🚀 Features

- 📄 Upload *PDFs* or *image files*
- 🧾 Extract *text* using pytesseract (OCR) and PyMuPDF
- 🧠 Use spaCy NLP to identify:
  - Names
  - Locations
  - Skills / Keywords
- 🌐 Web interface built with *Flask*
- 🎨 Simple, responsive frontend with HTML/CSS


## 🛠 Tech Stack

| Area           | Tools / Libraries                     |
|----------------|---------------------------------------|
| Backend        | Flask                                 |
| OCR            | pytesseract                           |
| PDF Extraction | PyMuPDF (fitz)                        |
| NLP            | spaCy (en_core_web_sm)                |
| Frontend       | HTML, CSS                             |
| Deployment     | GitHub (for version control)          |


## 📁 Project Structure

project/ ├── app.py ├── extract_name_location.py ├── keyword_extract.py ├── ocr_engine.py ├── pdf_extractor.py ├── requirements.txt ├── templates/ │   └── index.html ├── static/ │   └── style.css ├── upload/ │   └── (uploaded files) ├── utils/ │   ├── i_catch.py │   └── helper.py


## 🔧 Setup Instructions

1. *Clone the repository*

git clone https://github.com/yourusername/keystractor.git
cd keystractor
2. Create and activate virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
python -m spacy download en_core_web_sm
4. Run the application
python app.py

📄 License

This project is licensed under the MIT License — see the LICENSE file for details.

🙌 Acknowledgements

pytesseract
spaCy
PyMuPDF
Flask

💡 Future Improvements

Add resume ranking system
Use skill-matching database
Deploy on Render or Railway
Add user authentication

⭐ If you found this project useful, give it a star and follow for updates!

Let me know if you want help customizing it with your GitHub username, adding badges, or writing a README specifically for showcasing on LinkedIn or your portfolio!
