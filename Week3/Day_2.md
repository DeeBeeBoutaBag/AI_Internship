## Day 2: Preparing Training Data

- **Review OpenAI fine-tune data format ([docs](https://platform.openai.com/docs/guides/fine-tuning)).**
- **Convert JSONs into training pairs.**  
  Example:
    ```python
    # Create training.jsonl: each line '{"prompt": "...", "completion": "..."}'
    import glob, json
    for json_file in glob.glob('*.json'):
        with open(json_file, 'r') as jf:
            data = json.load(jf)
            prompt = data['title'] + "\n" + data.get('body', '')
            completion = "<END>"  # Or whatever you want model to predict
            with open('training.jsonl', 'a', encoding='utf-8') as tf:
                tf.write(json.dumps({"prompt": prompt, "completion": completion}) + '\n')
    ```

---
