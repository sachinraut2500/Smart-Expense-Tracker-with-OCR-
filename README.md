# Smart Expense Tracker (with OCR)
-----
Scan receipts, parse totals/dates/vendors, auto-categorize spending, and store everything in a local SQLite database.  
Uses **Tesseract OCR** + **scikit-learn** (when training data exists) with a rule-based fallback.
---
## ✨ Features
- 🧾 **OCR**: Extract text from PNG/JPG/TIFF/WebP with Tesseract.
- 🔍 **Parsing**: Heuristics to find **date**, **amount**, **currency**, and **vendor**.
- **Categorization**:
  - ML model (**TF-IDF + MultinomialNB**) trained from your labeled data (rows with categories).
  - Falls back to keyword rules when no training data exists.
- 💾 **Storage**: Local **SQLite** DB (`expenses.db` by default).
- 📊 **Reports**: Totals by category for a period (YYYY or YYYY-MM).
- 📤 **Export**: Dump everything to CSV.
----------------------------
## 🧰 Tech Stack
- Python 3.9+
- pytesseract, opencv-python
- scikit-learn
- python-dateutil
- pandas
- SQLite (built-in)
--------------------------
## 📦 Install
```bash
pip install pytesseract opencv-python scikit-learn python-dateutil pandas
# Also install Tesseract OCR engine:
# macOS:   brew install tesseract
# Ubuntu:  sudo apt-get install tesseract-ocr
# Windows: https://tesseract-ocr.github.io/tessdoc/Installation.html
