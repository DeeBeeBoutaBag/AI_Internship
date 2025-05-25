## Day 3: Validating Data with OpenAI

- **Send some examples for validation:**
    ```python
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[{"role":"user", "content": prompt}]
    )
    print(response.choices[0].message['content'])
    ```
- **Document observations.**

---
