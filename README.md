# 🧠 WordTrace  
### PDF Keyword Spotter using Streamlit and OCR

**WordTrace** is a Streamlit-based application designed to analyze multi-page financial PDFs, detect important layout sections, and highlight word-level keywords using OCR. The tool focuses on extracting text only from relevant regions instead of processing the entire page, making it efficient and accurate for document analysis tasks.

---

## 🚀 Features

- 📄 Upload multi-page financial PDFs  
- 📦 Detect layout sections such as **Title** and **Tables** using layout-based cropping  
- 🔍 Perform OCR only on selected layout regions (not the full page)  
- 🧠 Extract text along with **word-level bounding box coordinates**  
- 💾 Store structured outputs in:
  - `layout.json` – section-level layout metadata  
  - `wordjson.json` – absolute word-level coordinates  
- 🔎 Real-time keyword search (up to 5 keywords)  
- 🟥 Highlight matching words using red bounding boxes  
- 🖥️ Side-by-side interface:
  - PDF viewer on the left  
  - Keyword search panel on the right  

---

## 🛠️ Tech Stack

| Tool / Library | Purpose |
|----------------|--------|
| Streamlit | Interactive web UI |
| PyMuPDF (fitz) | PDF rendering and page image generation |
| EasyOCR | Lightweight OCR engine |
| Pillow | Drawing word highlights |
| NumPy | Image processing |
| JSON | Structured storage for layout and word data |

---

## 📁 Project Structure
```
├── app.py # Main Streamlit application
├── textract_utils.py # OCR and layout detection logic
├── json_utils.py # Utilities for saving/loading JSON data
├── viewer_utils.py # PDF rendering and highlight utilities
├── requirements.txt # Project dependencies
├── output/ # Generated layout.json & wordjson.json
└── README.md
```

---

## ⚠️ Important Notes

- ❌ No external dependencies like **Tesseract CLI** or **Poppler**
- ✅ Fully based on pip-installable Python libraries
- 💻 Portable and works across Windows, macOS, and Linux
- ⚡ Optimized by applying OCR only on detected layout areas

---

## 🧪 Run Locally

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/wordtrace-pdf-keyword-spotter.git
cd wordtrace-pdf-keyword-spotter
```
2️⃣ Install dependencies
```
pip install -r requirements.txt
```

3️⃣ Run the Streamlit app
```
streamlit run app.py
```

## 🌐 Deploy on Streamlit Cloud (Optional)

- Push the project to GitHub  
- Visit https://streamlit.io/cloud  
- Connect your GitHub repository  
- Deploy the app with one click  

---

## 🎯 Use Cases

- Financial document analysis  
- Invoice and report keyword extraction  
- PDF search and highlight tools  
- OCR-based document automation  
- Word-level coordinate extraction  
