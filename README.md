🌍 Multilingual Text-to-Speech (TTS) using Hugging Face

A robust, echo-free, and slow-paced multilingual Text-to-Speech system built entirely with open-source Hugging Face models.
This project converts English text input into natural-sounding speech in:

🇬🇧 English

🇮🇳 Hindi

🇮🇳 Gujarati

The system is designed specifically to be stable in Google Colab (Python 3.12) and avoids common issues such as audio corruption, echo artifacts, and dependency conflicts.

✨ Highlights

✅ English → Hindi → Gujarati translation

✅ Clear and natural Text-to-Speech

✅ Slow speech without echo (sentence-level pause control)

✅ Uses only Hugging Face open-source models

✅ CPU-friendly (no GPU required)

✅ Colab-safe (no soundfile / scipy audio write failures)

✅ Full text spoken (no skipped or truncated sentences)

🧠 Models Used (Hugging Face)
🔹 Translation

facebook/nllb-200-distilled-600M

English → Hindi

English → Gujarati

🔹 Text-to-Speech (MMS – Massively Multilingual Speech)

facebook/mms-tts-eng – English

facebook/mms-tts-hin – Hindi

facebook/mms-tts-guj – Gujarati

All models are open-source and publicly available on Hugging Face 🤗

🛠️ Tech Stack

Python 3.12

Hugging Face Transformers

PyTorch

NumPy

Google Colab (recommended environment)

📂 Project Structure
multilingual-tts-huggingface/
│
├── Hugging_Face.ipynb
└── README.md

⚙️ How It Works (Pipeline)

User provides English text

Text is translated into Hindi and Gujarati using NLLB

Each language is converted into speech using MMS TTS models

Speech speed is controlled using natural pauses between sentences

Audio is played directly in Colab for maximum stability

⚠️ No audio time-stretching is used (prevents echo and metallic sound)

🧪 Installation (Google Colab)

Run once:

pip install -U transformers sentencepiece torch librosa


Then restart the runtime.

▶️ Example Usage
text = """
Hello, my name is Diaa.
I am an AI and Machine Learning enthusiast.
I enjoy building real world AI applications.
I am continuously learning new technologies.
"""

tts_play_clean(text, "facebook/mms-tts-eng")
tts_play_clean(hindi_text, "facebook/mms-tts-hin")
tts_play_clean(gujarati_text, "facebook/mms-tts-guj")

🎧 Output Characteristics

Natural pronunciation

Slow, human-like speech

No echo or hollow effect

Works fully on CPU

Stable playback in Google Colab

⚠️ Known Limitations

Audio is played directly in Colab for reliability

File saving (WAV/MP3) can be added if required, but playback is preferred for stability

🧩 Design Decisions (Important)

❌ No post-processing time-stretch (avoids echo)

✅ Sentence-level pause control for slow speech

❌ No Google TTS or paid APIs

✅ Hugging Face pipelines for stability in Python 3.12

This reflects real-world ML engineering practices, not just a demo script.

🎯 Use Cases

AI / ML portfolio project

Multilingual voice assistants

Accessibility & assistive tools

Hugging Face & NLP learning

Interview demonstration project



Diaa
AI & Machine Learning Enthusiast
Focused on building practical, production-ready AI systems 🚀
