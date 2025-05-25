## Day 2: Mapping PDF to JSON

### Manual Mapping

1. Open a `.txt` file.
2. Decide on a simple schema, e.g.:

    ```python
    data = {
        "title": first_line,
        "date": find_date_in_text(text),
        "body": rest_of_text
    }
    ```

3. Write a function to automate mapping.

---
