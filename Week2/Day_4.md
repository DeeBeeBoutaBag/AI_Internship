## Day 4: JSON Schema Validation

### Install Library

```sh
pip install jsonschema
```

### Create a Validation Script

```python
from jsonschema import validate, ValidationError
import json

schema = {
    "type": "object",
    "properties": {
        "title": {"type": "string"},
        "body": {"type": "string"},
    },
    "required": ["title", "body"]
}

# Test one file
with open('sample.json') as f:
    data = json.load(f)
try:
    validate(instance=data, schema=schema)
    print("Valid!")
except ValidationError as e:
    print("Invalid JSON:", e)
```

**Next:**  
Test the script on all JSON files.

---
