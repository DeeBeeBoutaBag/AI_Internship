## Day 3: Downloading PDFs from Google Drive

### Python Code Sample to Download PDFs
```python
for file in file_list:
    if file['title'].endswith('.pdf'):
        print(f"Downloading {file['title']}...")
        file.GetContentFile(file['title'])
```

- Check your working directory to confirm files are downloaded (use `os.listdir()` or browse files in the VS Code Explorer tab).

### Version Control
1. Initialize Git:
    ```sh
    git init
    ```
2. Add code:
    ```sh
    git add .
    ```
3. Commit:
    ```sh
    git commit -m "initial commit"
    ```
