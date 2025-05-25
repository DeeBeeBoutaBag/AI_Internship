## Day 3: Bulk TXT to JSON

### Bulk Convert all TXT to JSON

```python
import glob
import json

txt_files = glob.glob("*.txt")
for txt_file in txt_files:
    with open(txt_file, 'r', encoding='utf-8') as f:
        lines = f.readlines()
        data = {
            "title": lines[0].strip(),
            "body": ''.join(lines[1:])
        }
        with open(txt_file.replace('.txt', '.json'), 'w', encoding='utf-8') as jf:
            json.dump(data, jf, indent=2)
```

---
