# 🎓 RAG-Based Teaching Assistant

This project implements a **Retrieval-Augmented Generation (RAG) powered AI Teaching Assistant**.  
It transforms lecture videos into structured knowledge and allows students to **ask questions and get context-aware answers** directly from the lecture content.

---

## 🚀 Features
- 🎥 **Video-to-Audio**: Extracts audio from lecture videos.  
- 🎙 **Audio-to-Transcript**: Converts `.mp3` lecture files into JSON-based transcripts.  
- 📝 **Preprocessing**: Cleans and structures transcript data for retrieval.  
- 🤖 **RAG Pipeline**: Uses transcripts to answer student queries in context.  
- 📂 **JSON Knowledge Base**: Stores processed lectures for efficient retrieval.  

---

## 🛠 Tech Stack
- **Python 3.9+**
- **LLMs** (OpenAI / Hugging Face, configurable)
- **Whisper / Speech-to-Text** (for audio transcription)
- **FAISS / Vector Store** (for retrieval)
- **JSON-based pipeline** for structured storage

---

## 📂 Project Structure
```

├── mp3\_to\_json.py        # Convert MP3 lectures to JSON transcripts
├── video\_to\_mp3.py       # Extract audio from videos
├── preprocess\_json.py    # Clean & preprocess transcripts
├── process\_incoming.py   # Handle student queries (RAG)
├── prompt.txt            # Base prompt for AI
├── response.txt          # Sample responses
├── jsons/                # Transcript knowledge base
└── Readme.md             # Documentation

````

---

## ⚙️ Installation

```bash
# Clone the repo
git clone https://github.com/<your-username>/RAG-Teaching-Assistant.git
cd RAG-Teaching-Assistant

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
````

*(If `requirements.txt` is not yet created, run `pip freeze > requirements.txt` after installing needed packages.)*

---

## ▶️ Usage

1. **Extract audio from lecture videos**:

   ```bash
   python video_to_mp3.py <path_to_video>
   ```

2. **Convert audio to JSON transcripts**:

   ```bash
   python mp3_to_json.py <path_to_mp3>
   ```

3. **Preprocess JSON transcripts**:

   ```bash
   python preprocess_json.py
   ```

4. **Ask questions via RAG**:

   ```bash
   python process_incoming.py "What is the difference between inline and block elements in HTML?"
   ```

---

## 📖 Example

**Input**:

```
What are semantic tags in HTML?
```

**Output**:

```
Semantic tags in HTML provide meaning to the structure of a webpage. 
Examples: <header>, <footer>, <article>, <section>.
They improve accessibility and SEO by clearly defining content roles.
```

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork the repo, open issues, or submit PRs.

---

## 📜 License

MIT License. See `LICENSE` file for details.

---

## 👨‍💻 Author

**Md Safwan**
B.Tech CSE, NIT Durgapur | Passionate about Data Science & AI

```

---

🔹 **Suggested GitHub Repo Description (for the repo settings):**  
> A Retrieval-Augmented Generation (RAG) powered AI Teaching Assistant that converts lecture videos into structured knowledge and answers student queries using contextual transcripts.  

---

Do you also want me to **auto-generate a `requirements.txt`** from your project so setup is easier for anyone cloning your repo?
```
