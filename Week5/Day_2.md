## Day 2: Add Encryption & Logging

**Main Goal:** Secure sensitive data and create robust error tracking.

**Tasks:**
- Extend Day 1’s script to:
  - Encrypt the validated JSON output using the `cryptography` package.
  - Save both encrypted and original JSONs in separate folders.
  - Log all validation and encryption actions, errors, and file names to a daily log file.
- Bonus:  
  - Add CLI arguments so users can process a single file or a directory.
- Each intern:
  - Tests the entire pipeline on new and edge-case files (corrupted PDFs, missing fields).
  - Documents and screenshots bugs or exceptions encountered.
- Review log files and error cases as a team on Slack/Discord.

---
