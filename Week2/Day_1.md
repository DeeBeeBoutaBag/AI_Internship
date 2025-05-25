## Day 1: JSON Basics

### Python-JSON Refresher

```python
import json
data = {'title': 'My Doc', 'content': 'Sample text here'}
with open('output.json', 'w') as f:
    json.dump(data, f, indent=2)
```

**Task:**  
Create a sample JSON object using fields from the extracted text.

---
