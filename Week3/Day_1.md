## Day 1: OpenAI API Setup

- **Create/OpenAI account:** [https://platform.openai.com/](https://platform.openai.com/)
- **Install OpenAI package:**
    ```sh
    pip install openai
    ```
- **Test API Key Usage:**
    ```python
    import openai
    openai.api_key = "YOUR-API-KEY"
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[{"role":"user", "content":"Hello!"}]
    )
    print(response.choices[0].message['content'])
    ```

---
