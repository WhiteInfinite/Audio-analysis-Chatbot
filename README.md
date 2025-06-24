# 🗣️ Voice Transcript using an AI-powered chatbot + PDF Export + Email

This project allows you to:

1. Upload an audio file and **transcribe it using Whisper**.
2. Ask questions about the transcript using an **AI assistant trained on the content**.
3. Automatically **save the chat history as a PDF**.
4. **Send the PDF to your email** via SMTP.

---

## 🚀 Features

✅ Audio-to-text transcription (MP3, WAV, etc.)

✅ Smart chatbot with context-aware Q&A based on transcript

✅ PDF export of conversation

✅ Email delivery via Gmail SMTP

---


## ⚙️ How to Run

### 1. Transcribe Audio

Use OpenAI Whisper to convert audio to text:

```python
import whisper
model = whisper.load_model("base")
result = model.transcribe("your_audio.mp3")
with open("transcript.txt", "w") as f:
    f.write(result["text"])
```

### 2. Start Chatbot with PDF & Email

```bash
python chatbot.py
```

You can:

* Ask questions about the transcript
* Type `exit` or `quit` to end the chat
* PDF will be generated and emailed to you automatically

---

## 📧 Email Sending Settings

Inside `chatbot.py`, update:

```python
sender_email = "your_email@gmail.com"
app_password = "your_16_char_app_password"
recipient_email = "recipient@example.com"
```

---

## 🧠 Example Chat

```
You: What did Tess do over the weekend?
Gemini: Tess visited her family and finished reading a novel.

You: Was it a productive weekend?
Gemini: Yes, she relaxed and completed a book she had been reading.

... [PDF generated + emailed]
```

---

## ✅ To-Do / Ideas

* Add Streamlit UI for uploading + chatting
* Add real-time token usage tracking
* Add audio chunking for long files

---

## 📃 License

MIT License – free to use, modify, and distribute.

---
