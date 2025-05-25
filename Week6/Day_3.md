## Day 3: Stress Test & Security Review

**Goal:** Try to “break” the system and identify weaknesses.

### Tasks:
- Each intern gets a checklist:
    - Test with huge PDFs (tens of megabytes), corrupt files, empty files, files with non-standard encoding.
    - Simulate floods of uploads, concurrent API use (try `curl` in a loop or browser tabs).
    - Try uploading files with tricky filenames (spaces, unicode, long names, etc.).
    - Attempt invalid/unsupported file types and permission edge cases.
    - Try to inject bad data into API (malformed JSON, extra fields, missing required fields).
    - Encrypt/decrypt loops—does repeated processing change output, or create errors?
- Log all failures and odd/error logs in a shared spreadsheet (Bug Bash!).
- Each intern picks at least one found vulnerability (code crash, confusing error, poor validation, etc.) and writes a suggested fix.

---
