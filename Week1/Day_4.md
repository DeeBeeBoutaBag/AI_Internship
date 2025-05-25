## Day 4: PDF Text Extraction Basics

### 1. Install Library
```sh
pip install pdfplumber
```

### 2. Practice Text Extraction
```python
import pdfplumber

with pdfplumber.open('sample.pdf') as pdf:
    first_page = pdf.pages[0]
    print(first_page.extract_text())
```

### 3. Save Extracted Text
```python
with open('sample.txt', 'w', encoding='utf-8') as f:
    f.write(first_page.extract_text())
```
