## Day 2: Google Drive Integration

### 1. Install Dependencies
In the VS Code terminal, run:
```sh
pip install pydrive2
```

### 2. Set Up Google Drive Access
> **One-time admin/mentor assistance may be needed for API keys.

- Follow the [PyDrive2 Quickstart](https://docs.iterative.ai/PyDrive2/quickstart/).
- Save your credentials JSON in your project root as `credentials.json`.

### 3. List Files in a Google Drive Folder

Sample Python script:
```python
from pydrive2.auth import GoogleAuth
from pydrive2.drive import GoogleDrive

gauth = GoogleAuth()
gauth.LocalWebserverAuth()
drive = GoogleDrive(gauth)
folder_id = 'YOUR_AI_INTERNSHIP_FOLDER_ID'  # Replace

file_list = drive.ListFile({'q': f"'{folder_id}' in parents and trashed=false"}).GetList()
for file in file_list:
    print(f'{file["title"]} ({file["id"]})')
```
- Replace `folder_id` with your given team folder ID.
