# AI_Internship

# **WEEK 1: Environment Setup & Data Extraction**

## **Day 1 (Monday): VS Code & Python Environment Setup**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:30 | **Meet & Project Intro via Zoom/Slack**<br>- Welcome & orientation.                   |
| 00:30–01:15 | **Install VS Code**<br>- Download/install [VS Code](https://code.visualstudio.com/).  |
| 01:15–01:45 | **Install Python 3.x**<br>- Download from [python.org](https://python.org/).          |
| 01:45–02:15 | **Configure VS Code for Python**<br>- Open VS Code, install Python extension.         |
| 02:15–03:00 | **Hello World Script**<br>- Open VS Code, create `hello.py`, write:<br>`print("Hello, AI World!")`.<br>- Run in terminal: `python hello.py`<br>- Troubleshoot as needed.|
| 03:00–03:45 | **GitHub Setup**<br>- Create account, install Git if needed, `git init` in project.   |
| 03:45–04:00 | **Recap/Write journal**<br>- Summit: List of what you learned, any blocking issues.   |


---

## **Day 2 (Tuesday): Google Drive Integration**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:30 | **Meet & Sync/Share Journal**<br>- Discuss previous day, answer questions.            |
| 00:30–01:00 | **Install PyDrive2**<br>- In terminal: `pip install pydrive2`                         |
| 01:00–01:30 | **Google API Setup (with mentor help):**<br>- Generate credentials, save as `credentials.json` in root.<br>- Follow [PyDrive2 Quickstart](https://docs.iterative.ai/PyDrive2/quickstart/).|
| 01:30–02:15 | **List Files in Drive**<br>- Open VS Code, create `list_files.py`:<br>See previous code.<br>- Run and verify output.|
| 02:15–02:45 | **Store Folder ID**<br>- Identify team folder ID in Google Drive.<br>- Update code accordingly.|
| 02:45–03:30 | **Explore Drive Data**<br>- Tweak script to find all PDF files.<br>- Print file names and IDs.|
| 03:30–04:00 | **Document steps & blockers**.                                                        |


---

## **Day 3 (Wednesday): Download PDFs from Google Drive**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily sync/check-in**                                                               |
| 00:15–00:45 | **Use PyDrive2 to Download PDFs:**<br>- Update `list_files.py` to download each PDF to project folder.|
| 00:45–01:30 | **Verify File Downloads:**<br>- Check VS Code Explorer for files.<br>- Use `os.listdir()` to programmatically check.|
| 01:30–02:15 | **Basic Python For/While Loops Practice:**<br>- Write a script that prints all filenames ending in `.pdf`.|
| 02:15–03:00 | **Intro to Version Control:**<br>- `git add .`, `git commit -m "download script"`      |
| 03:00–03:30 | **Write down today’s learnings and issues.**                                           |
| 03:30–04:00 | **Peer Review:**<br>- Share code snippets with teammate, get feedback.                 |


---

## **Day 4 (Thursday): PDF Extraction**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in: Plan for the day.**                                                       |
| 00:15–00:30 | **Install `pdfplumber` in VS Code terminal:**<br>`pip install pdfplumber`              |
| 00:30–01:00 | **Extract First Page Text:**<br>- Open `pdf_extract.py`, use:       |
|             | ```python<br>import pdfplumber<br>with pdfplumber.open('sample.pdf') as pdf:<br>  page = pdf.pages[0]<br>  print(page.extract_text())<br>```|
| 01:00–01:30 | **Save Output to Text File:**<br>- Write code to save result as `sample.txt`           |
| 01:30–02:15 | **Extract All Pages:**<br>- Loop for full document extraction, save all text to file.  |
| 02:15–03:00 | **Batch Extraction:**<br>- For all PDFs in folder, repeat extraction.<br>- Save .txt files.|
| 03:00–03:30 | **Review files in VS Code (explorer/text editor).**<br>- Confirm all .txt look as expected.|
| 03:30–04:00 | **Update GitHub repo; peer code review.**                                             |


---

## **Day 5 (Friday): Review & Documentation**

| Time        | Activity                                                                                                    |
|-------------|------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily check-in: Problems, questions**.                                                                   |
| 00:15–01:00 | **Summarize Week’s Work**<br>- Write Markdown doc summarizing steps/scripts learned.                        |
| 01:00–01:45 | **Clean & Comment All Scripts**<br>- Add `# comments` for each function, logic section.                     |
| 01:45–02:30 | **Troubleshoot Each Other’s Scripts**<br>- Try switching/test teammate’s scripts on your machine.           |
| 02:30–03:00 | **Push work to GitHub** (no credentials, just code and sample outputs).                                     |
| 03:00–03:30 | **Mentor Meeting:**<br>- Present week’s outcome, get feedback, clarify next week plan.                      |
| 03:30–04:00 | **Recap:**<br>- Plan improvements or homework (e.g., Python or JSON tutorial videos for weekend).           |


---

# **WEEK 2: Data Structuring & Validation**

## **Day 1 (Monday): JSON Basics**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Kickoff & review**                                                                  |
| 00:15–00:45 | **Intro to Python Dicts/JSON:**<br>Practice with:<br>```python<br>import json<br>data = {"a": 1}<br>with open("test.json", "w") as f:<br>    json.dump(data, f)<br>```|
| 00:45–01:15 | **Open & Edit Output:**<br>- Change/test values in .json, re-read into Python.         |
| 01:15–01:45 | **Manual Mapping:**<br>- Open one .txt, decide key fields: Title, Date, Body.          |
| 01:45–02:30 | **Write Script for One File:**<br>- Turn .txt (split by first newline) to JSON fields. |
| 02:30–03:00 | **Save as .json, print result, repeat for 2-3 files.**                                |
| 03:00–03:45 | **Document mapping assumptions in markdown (e.g., "first line is title...").**         |
| 03:45–04:00 | **Commit code to GitHub, note issues/questions.**                                      |

---

## **Day 2 (Tuesday): Automate Text-to-JSON**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Meet, recap mapping logic.**                                                        |
| 00:15–01:00 | **Write Function:**<br>- Automate from yesterday’s manual work:                                            |
|             | ```python<br>def txt_to_json(txt):<br>    lines = txt.splitlines()<br>    return {"title": lines[0], "body": "".join(lines[1:])}<br>```|
| 01:00–01:45 | **Batch Processing:**<br>- For all .txt, use above function and write output to .json.|
| 01:45–02:30 | **Check Outputs:**<br>- Open outputs, confirm correct fields.                        |
| 02:30–03:15 | **Write Error Handling** (if file is empty, missing title, etc.).                    |
| 03:15–03:45 | **Peer Test:**<br>- Partner runs your code, you run theirs.                          |
| 03:45–04:00 | **Document & Commit.**                                                               |

---

## **Day 3 (Wednesday): JSON Schema Validation**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Catch-up/Review**                                                                   |
| 00:15–00:45 | **Intro to JSON Schema:** ([Tutorial](https://json-schema.org/learn/getting-started-step-by-step.html))|
| 00:45–01:15 | **Install validator:**<br>`pip install jsonschema`                                    |
| 01:15–01:45 | **Write First Schema:** For `{title: string, body: string}`.                          |
| 01:45–02:30 | **Validation Script:**<br>- For each .json, validate.<br>- Print valid/invalid files. |
| 02:30–03:15 | **Faulty Case Testing:**<br>- Make intentionally broken .json and check error reporting.|
| 03:15–03:45 | **Document error types, common fixes.**                                               |
| 03:45–04:00 | **Summary & push code.**                                                              |

---

## **Day 4 (Thursday): Bulk Validation, Review**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily sync**                                                                        |
| 00:15–01:00 | **Automate: Validate All**<br>- Loop over directory, check every .json, log errors.   |
| 01:00–01:45 | **Output Error Log:**<br>- Write one error log file for batch run.                    |
| 01:45–02:30 | **Partner Audit:**<br>- Run each other’s validator, try to break it.                  |
| 02:30–03:15 | **Document lessons/issues.**                                                          |
| 03:15–04:00 | **Mentor meeting: Present validator, debug live.**                                    |

---

## **Day 5 (Friday): Review, Clean, Document**

| Time        | Activity                                                                              |
|-------------|---------------------------------------------------------------------------------------|
| 00:00–00:30 | **Check-in: Lessons, blockers.**                                                      |
| 00:30–01:00 | **Document Full Workflow:**<br>- Markdown step-by-step of .pdf → .txt → .json → validated.|
| 01:00–01:30 | **Combine all core code snippets into “main.py”.**                                    |
| 01:30–02:30 | **Full Run-Through:**<br>- Try pipeline on 5 new test PDFs through to validated .json.|
| 02:30–03:15 | **Code Review:**<br>- Each intern checks the other's master script.                   |
| 03:15–03:45 | **Prepare for Week 3: Read OpenAI API docs ([Quickstart](https://platform.openai.com/docs/quickstart)).**|
| 03:45–04:00 | **Finalize/Submit week’s code, notes, and questions in Git/Slack.**                   |

---

## Week 3: OpenAI Integration & Preparing Training Data

### **Day 1: OpenAI API Setup and Testing**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily Sync:**<br>- Recap JSON scripts.<br>- Set goal: run OpenAI API call from VS Code.                        |
| 00:15–00:45 | **OpenAI Account:**<br>- Sign up [at OpenAI](https://platform.openai.com/).<br>- Find API Key, store safely.      |
| 00:45–01:15 | **Install OpenAI Python library:**<br>```pip install openai```                                                    |
| 01:15–01:45 | **Test a Simple API Call:**<br>In `openai_test.py`:<br>```python<br>import openai<br>openai.api_key = "YOUR_API_KEY"<br>response = openai.ChatCompletion.create(<br>  model="gpt-3.5-turbo",<br>  messages=[{"role":"user", "content":"Hello, how are you?"}]<br>)<br>print(response.choices[0].message.content)<br>```<br>- If error, check API key, API usage limit.|
| 01:45–02:15 | **Error Handling/Debugging**<br>- Try passing in empty key.<br>- Document common problems.                       |
| 02:15–03:15 | **Read OpenAI Docs:**<br>- [Prompt Engineering guide](https://platform.openai.com/docs/guides/prompting).        |
| 03:15–03:45 | **Peer Review & Journal:**<br>- Share API test output.                                                           |
| 03:45–04:00 | **Push to GitHub, write summary in journal.**                                                                    |

---

### **Day 2: Formatting Training Data for Fine-Tuning**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily Sync:**<br>- Set today's task: convert `.json` data to OpenAI training format (`.jsonl`).                |
| 00:15–00:45 | **Review OpenAI Fine-Tuning Format:**<br>- Docs: https://platform.openai.com/docs/guides/fine-tuning/preparing-your-dataset|
| 00:45–01:30 | **Write Format Script:**<br>- `json_to_jsonl.py`:<br>```python<br>import json, glob<br>with open("train.jsonl","w",encoding="utf-8") as out:<br>  for jf in glob.glob("*.json"):<br>    with open(jf,"r",encoding="utf-8") as f:<br>      d=json.load(f)<br>      prompt = f"Title: {d.get('title','')}\n\nBody: {d.get('body','')}\n" <br>      completion = "<END>"    # replace with appropriate output<br>      out.write(json.dumps({"prompt":prompt,"completion":completion})+"\\n")<br>```|
| 01:30–02:00 | **Examine Output:**<br>- Open `train.jsonl` in VS Code.<br>- Ensure each line is valid JSON, formatted as OpenAI expects.|
| 02:00–02:45 | **Check Sample Data:**<br>- Try small samples for mistakes or weird output.<br>- Log any irregular files.        |
| 02:45–03:15 | **Add Comments and Docstrings to Scripts.**                                                                      |
| 03:15–03:45 | **Peer Testing:**<br>- Partner reviews script for clarity.                                                       |
| 03:45–04:00 | **Commit to GitHub / Journal.**                                                                                  |

---

### **Day 3: Validate Training Data Quality**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Daily Standup:**<br>- Clarify valid/invalid `.jsonl` data.                                                     |
| 00:15–01:00 | **Write Validation Script:**<br>Check: both fields present, line is valid JSON, prompt not too long.             |
| 01:00–02:00 | **Test Validation:**<br>- Run over all `.jsonl` lines.<br>- Log errors and filenames to `data_quality.log`.      |
| 02:00–02:30 | **Review Results:**<br>- Report: How many lines succeed? Which JSONs cause invalid data?                         |
| 02:30–03:15 | **Document Requirements for “good” data samples in Markdown file.**                                              |
| 03:15–03:45 | **Mentor Check-in:**<br>- Demo scripts, get bugfix advice.                                                       |
| 03:45–04:00 | **Push scripts and outputs to GitHub.**                                                                         |

---

### **Day 4: OpenAI API Trial Inference**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in:**<br>- Share data issues/fixes.                                                                      |
| 00:15–01:00 | **Call OpenAI API on Your Data:**<br>- In `try_gpt_prompt.py`:<br>```python<br>import openai<br>openai.api_key = "YOUR-API-KEY"<br>train_ex = "Title: Example\n\nBody: Example text."\nresponse = openai.ChatCompletion.create(<br>  model="gpt-3.5-turbo",<br>  messages=[{"role":"user", "content": train_ex}]<br>)<br>print(response.choices[0].message.content)<br>```|
| 01:00–01:30 | **Try with Multiple Prompts:**<br>- Test your actual prompts.<br>- Compare outputs with “expected” answers.      |
| 01:30–02:00 | **Log Success/Failure:**<br>- Which prompts yield good completions? Any weird quirks?                            |
| 02:00–03:00 | **Document Prompt Patterns:**<br>- What formulation gets best result? Try rewording for improvement.<br>- Use Markdown. |
| 03:00–03:45 | **Share learnings with team (Slack or meeting).**                                                                |
| 03:45–04:00 | **GitHub Push.**                                                                                                |

---

### **Day 5: Peer Review & Retrospective**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in / Set review plan.**                                                                                  |
| 00:15–01:00 | **Swap Scripts:**<br>- Peer reviews and runs each other’s `.jsonl` creation and validation scripts.              |
| 01:00–02:00 | **Debugging:**<br>- Fix each other’s bugs, merge codebases where needed.                                         |
| 02:00–03:00 | **Write Documentation:**<br>- Full workflow for `.json` → `.jsonl` → validated for fine-tuning.                  |
| 03:00–03:30 | **Feedback with Mentor:**<br>- Screenshare, discuss challenges, reflections.                                     |
| 03:30–04:00 | **Plan for Fine-tuning next week.**                                                                             |

---

## Week 4: Fine-Tuning, Validation, and Pipeline Automation

### **Day 1: Fine-Tune Prep & Upload**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in / Objective: Prepare for fine-tune.**                                                                 |
| 00:15–01:15 | **Check Data Against OpenAI Validation Tool:**<br>- Clean up `train.jsonl` as needed.                            |
| 01:15–01:45 | **Upload Data for Fine-Tuning:**<br>- OpenAI CLI or dashboard.<br>- Docs: https://platform.openai.com/docs/guides/fine-tuning |
| 01:45–02:45 | **Start Fine-Tune Job:**<br>- Wait for results.<br>- While waiting, review what fine-tuning means and expected outcomes.|
| 02:45–03:30 | **Document Fine-Tuning Process:**<br>- Write steps and command-line args you used for reference.<br>- Journal questions for followup.|
| 03:30–04:00 | **Daily Wrap-up & Peer Review.**                                                                                 |

---

### **Day 2: Fine-Tune Analysis and Result Evaluation**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Team Check-in.**                                                                                               |
| 00:15–01:15 | **Fetch Fine-Tuned Model Details:**<br>- Model name, settings used, training log.                                |
| 01:15–02:00 | **Run Validation Prompts:**<br>- Take set of test prompts, call the fine-tuned model for inference.<br>```python<br>response = openai.ChatCompletion.create(<br>  model="your-finetuned-model-id",<br>  messages=[{"role":"user", "content":"PROMPT HERE"}]<br>)<br>print(response.choices[0].message.content)<br>```|
| 02:00–03:00 | **Compare Base vs. Fine-Tuned**<br>- How does the fine-tuned model’s output compare to the basic model?<br>- Note strengths and weakness in a table.|
| 03:00–03:30 | **Write Evaluation Notes:**<br>- Markdown summary, screenshots, comments for each example.                       |
| 03:30–04:00 | **Team Share-out:**<br>- Synchronous sync, discuss findings.                                                     |

---

### **Day 3: Full Pipeline Script (Automate Everything)**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:15 | **Plan: Outline Functions Needed**<br>- Download → Extract → .json → .jsonl → Validate → Fine-tune upload.       |
| 01:15–02:15 | **Start Scripting:**<br>- Break into reusable functions or main `pipeline.py`.                                   |
| 02:15–03:15 | **Error Handling:**<br>- Make script robust to missing files, format errors, API failures.<br>- Add basic logging.|
| 03:15–03:45 | **Peer Test:**<br>- Test script as a team, run on new samples.                                                   |
| 03:45–04:00 | **Update GitHub, write run instructions/README.**                                                                |

---

### **Day 4: API Wrapper & Validation Endpoints**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:00 | **Intro: Flask API**<br>- Install: `pip install flask`.<br>- Docs: https://flask.palletsprojects.com/            |
| 01:00–02:30 | **Write Simple Flask Endpoint:**<br>- Example:<br>```python<br>from flask import Flask, request, jsonify<br>app = Flask(__name__)<br>@app.route('/validate', methods=['POST'])<br>def validate_data():<br>    data = request.json<br>    # Run your JSON validation logic from earlier<br>    return jsonify({"valid": True})<br>if __name__ == "__main__":<br>    app.run()<br>```|
| 02:30–03:30 | **Test with curl or Postman:**<br>- Send POST requests, validate response.                                       |
| 03:30–04:00 | **Comment, document code, commit to GitHub.**                                                                    |

---

### **Day 5: Security Review & End-of-Week Wrap Up**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:00 | **Simple Security/Privacy Review:**<br>- How do you store API keys? Is any sensitive info logged? Document.      |
| 01:00–01:45 | **Add .gitignore**<br>- Ensure creds aren’t committed.<br>- Practice removing secrets from repo if needed.        |
| 01:45–02:30 | **Peer Code Review:**<br>- Each intern runs the other’s Flask app and main pipeline.                            |
| 02:30–03:30 | **Document Week’s Progress in Markdown.**                                                                       |
| 03:30–04:00 | **Mentor Feedback Session.**                                                                                    |

---

## Week 5: System Integration, API Improvements, and Stress Testing

### **Day 1: Integrate and Refactor Pipeline**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:30 | **Integrate pipeline and Flask API:**<br>- Endpoint for file upload, then pipeline runs automatically.           |
| 01:30–02:15 | **Write/Update Tests:**<br>- For pipeline and API (can be manual test scripts if not familiar with pytest).       |
| 02:15–03:15 | **Run Full Integration Test:**<br>- Upload → extract → validate → (dummy) fine-tune.                            |
| 03:15–03:45 | **Peer Review:**<br>- Test each other's integration.                                                             |
| 03:45–04:00 | **Update GitHub, journal findings.**                                                                             |

---

### **Day 2: Build in Error Logging and Notification**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:00 | **Add Error Logs:**<br>- Write to `pipeline.log` on failure.                                                     |
| 01:00–02:00 | **Notification (Optional):**<br>- Add email/SMS/logging if pipeline fails.<br>- Use logs for mentor review.      |
| 02:00–03:00 | **Test Error Handling:**<br>- Deliberate failures: missing files, API errors, server crash.                      |
| 03:00–03:45 | **Document Error Paths for Users:**<br>- Markdown or README section.                                             |
| 03:45–04:00 | **Commit to GitHub.**                                                                                            |

---

### **Day 3: Security Practice**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Brief on security basics.**                                                                                    |
| 00:15–01:30 | **API Key Security:**<br>- Store keys in `.env` or environment variables.<br>- Use `python-dotenv`.              |
| 01:30–02:15 | **Test Private Endpoint:**<br>- Protect Flask route with a simple token check.                                   |
| 02:15–03:00 | **Try Basic Attack Vectors:**<br>- Send invalid/broken JSON.<br>- Try huge file.<br>- See what happens, log problems.|
| 03:00–03:45 | **Document Security Findings.**                                                                                  |
| 03:45–04:00 | **Push to GitHub.**                                                                                              |

---

### **Day 4: Improve User Documentation**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Check-in.**                                                                                                    |
| 00:15–01:45 | **Work on README.md:**<br>- Document: Setup<br>- Running locally<br>- API usage<br>- Common errors and fixes.     |
| 01:45–02:45 | **Add Code Comments Throughout.**                                                                                |
| 02:45–03:45 | **Peer Edit README/docs.**                                                                                       |
| 03:45–04:00 | **Commit and distribute doc link to team.**                                                                      |

---

### **Day 5: Peer Demo Day**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:30 | **Prep for demo:**<br>- Rehearse pipeline, screenshots, support files.                                            |
| 00:30–02:00 | **Demo to peer(s):**<br>- Live walk-through of full process in VS Code.                                          |
| 02:00–03:00 | **Peer Feedback:**<br>- Take notes, identify usability issues.<br>- Update code if there's time.                  |
| 03:00–03:45 | **Reflect: Weekly review in Google Doc.**                                                                        |
| 03:45–04:00 | **Mentor Sync:**<br>- End-of-week feedback.                                                                      |

---

## Week 6: Stress Testing, Documentation, Final Review, and Presentation

### **Day 1: Stress Testing (Functionality & Robustness)**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Define stress test plan with mentor.**                                                                         |
| 00:15–01:30 | **Run pipeline with large/edge case files.**                                                                    |
| 01:30–02:30 | **Log results:**<br>- Document all failures, outputs, and fixes/patches attempted.                               |
| 02:30–03:30 | **Fix Vulnerabilities:**<br>- Patch any crash bugs.<br>- Retest after fixes.                                     |
| 03:30–04:00 | **Summarize findings in Markdown, push to repo.**                                                                |

---

### **Day 2: Security & Privacy Final Checks**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–00:15 | **Review Security Practices:**<br>- .env for keys, blacklisting bad inputs, info leaks.                           |
| 00:15–01:45 | **Try Known Attacks:**<br>- Send SQL, shell, etc. as text.<br>- Confirm no leaking info or dangerous behavior.   |
| 01:45–02:45 | **Write-up: Security Practices for Final Doc.**                                                                  |
| 02:45–03:45 | **Peer Review all code and documentation.**                                                                      |
| 03:45–04:00 | **Commit per security checklist.**                                                                               |

---

### **Day 3: Final Documentation & Packaging**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–01:00 | **Re-read code and README, update as needed.**                                                                   |
| 01:00–01:45 | **Check sample inputs/outputs for clarity.**                                                                     |
| 01:45–02:30 | **Produce short video/written “Getting Started” guide.**                                                         |
| 02:30–03:30 | **Add/fix code comments and Markdown examples.**                                                                 |
| 03:30–04:00 | **Mentor check-in, feedback before presentation.**                                                               |

---

### **Day 4: Final Presentation Practice**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–01:00 | **Review presentation outline with peer/mentor (live walkthrough of your process).**                             |
| 01:00–03:00 | **Solo practice: Run through every script using sample data with commentary.**                                   |
| 03:00–03:45 | **Ask for peer/mentor feedback, make improvements.**                                                             |
| 03:45–04:00 | **Prep files for demo/hand-in.**                                                                                 |

---

### **Day 5: Final Presentation & Wrap-up**

| Time        | Task                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------|
| 00:00–01:00 | **Final Demo to Mentor/Team:**<br>- 20 min VS Code walkthrough + Q&A.                                            |
| 01:00–02:00 | **Show documentation, take live feedback.**                                                                      |
| 02:00–03:00 | **Hand-off:**<br>- Archive repo, share install/run docs, submit all deliverables.                                 |
| 03:00–03:45 | **1:1 reflection:**<br>- Review what you learned, what you’d do differently.                                     |
| 03:45–04:00 | **Celebration & Next Steps!**                                                                                    |

---
