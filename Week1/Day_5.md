## Day 5: Repeat Extraction for Multiple PDFs

### Bulk Extract and Save
```python
import os
import pdfplumber

pdf_files = [f for f in os.listdir('.') if f.endswith('.pdf')]
for pdf_file in pdf_files:
    with pdfplumber.open(pdf_file) as pdf:
        all_text = []
        for page in pdf.pages:
            all_text.append(page.extract_text())
        with open(pdf_file.replace('.pdf', '.txt'), 'w', encoding='utf-8') as f:
            f.write('\n'.join([t for t in all_text if t]))
```

- Review extracted `.txt` files in the VS Code Explorer.
