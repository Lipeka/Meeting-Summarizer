# 🎙 Meeting Task Extractor

This **Meeting Task Extractor** converts **meeting recordings or manual transcripts into actionable task lists**.  
It performs two key operations:

✅ **Transcribes Audio** (using Whisper large)  
✅ **Extracts Actionable Tasks** (using Mistral-7B API)

The result is a neatly formatted **JSON summary of responsibilities**, ready for follow-up and delegation.

---

## 🌟 Features

- 🔉 Audio-to-Text Transcription (using Whisper large).
- 📝 Manual text fallback if you don't have audio.
- 🧑‍🏫 Actionable task extraction powered by **OpenRouter's Mistral-7B API**.
- 🔹 User-friendly **Gradio UI**.
- ✅ Ideal for meeting minutes, follow-up emails, and team task allocation.

---

## 🛠 Tech Stack

- **OpenAI Whisper:** Audio transcription
- **OpenRouter (Mistral-7B API):** Large Language Model for task extraction
- **Gradio:** User Interface for file upload or manual paste
- **pydub:** Audio format conversion (MP3 to WAV)

---

## 🔹 Installation

```bash
pip install -q gradio openai-whisper pydub ffmpeg-python
````

---

## 🔹 API Token

✅ Signup at [OpenRouter](https://openrouter.ai/) to generate your API key.
Save it to `OPENROUTER_API_KEY`.

```python
OPENROUTER_API_KEY = "your_api_key_here"
```

---

## 🔹 Run

```bash
python app.py
```

➥ The Gradio UI will launch in your browser.
➥ You can **upload an audio file or paste meeting minutes manually**.

---

## 🔹 File Format Support

✅ Audio: `.wav` or `.mp3`.
✅ Text: manually pasted into the textbox.

---

## 🔹 How It Works

1️⃣ If you **upload audio**, Whisper converts it into text.
2️⃣ If you **paste text manually**, it directly uses it.
3️⃣ The transcript is then fed into **OpenRouter's Mistral-7B API**, which parses it for actionable tasks.
4️⃣ The output is displayed in **JSON format**, with fields:

```json
[
  {
    "assigned_to": "Person's name",
    "department": "Team or department",
    "task_description": "Brief description of task",
    "deadline": "Due by (if available)"
  }
]
```

---

## 🔹 Run in Gradio UI

1️⃣ Open the link provided by Gradio in your terminal.
2️⃣ **Option 1:** Upload an audio file.
3️⃣ **Option 2:** Or paste your meeting's transcript manually.
4️⃣ Hit **Process** and view the results immediately.

---

## 🔹 Notes

➥ **OpenAI Whisper large** performs well but may be slow on weak machines.
➥ The **OpenRouter API key** must be kept private.
➥ The **model (Mistral-7B)** is lightweight, fast, and well-suited for this use case.

---

## 🔹 Possible Applications

✅ Automate meeting minutes
✅ Provide clear follow-up instructions
✅ Keep stakeholders informed about responsibilities
✅ Boost productivity and collaboration within your team

---

## 📝 License

This project is licensed under **MIT license** — feel free to reuse and modify it.
