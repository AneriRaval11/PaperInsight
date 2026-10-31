# PaperInsight

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.10+" />
  <img src="https://img.shields.io/badge/Streamlit-1.x-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
  <img src="https://img.shields.io/badge/LangChain-FAISS-000000?style=for-the-badge" alt="LangChain + FAISS" />
  <img src="https://img.shields.io/badge/Gemini-AI-8A2BE2?style=for-the-badge" alt="Gemini AI" />
</p>

PaperInsight is an AI-powered research companion that helps you upload academic PDFs, extract meaningful knowledge, and ask context-aware questions using Gemini and vector search. Built for students, researchers, and knowledge workers who want fast understanding without manually reading every page.

From dense journal articles to technical reports, PaperInsight turns PDFs into an interactive Q&A workspace with semantic retrieval and natural-language answers.

## 🎬 Demo

<p align="center">
  <video src="https://github.com/AneriRaval11/PaperInsight/raw/main/demo.mp4" width="900" controls autoplay muted loop></video>
</p>

[Download the demo video](https://github.com/AneriRaval11/PaperInsight/raw/main/demo.mp4)

## ✨ Features

- Upload one or more PDF files
- Extract text from academic papers and documents
- Split long content into manageable chunks
- Generate embeddings using Google Generative AI
- Store and query vector data with FAISS
- Ask questions in plain English and get context-based answers
- Built as a lightweight and interactive local web app

## 🧠 Tech Stack

- Python
- Streamlit
- PyPDF2
- LangChain
- FAISS
- Google Generative AI / Gemini

## 📁 Project Structure

```text
PaperInsight/
├── PaperInsight.ipynb
├── my_app.py
├── app.py
├── faiss_index/          # generated after processing PDFs
├── README.md
└── requirements.txt      # optional if added later
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/PaperInsight.git
cd PaperInsight
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set your Google API key

Create a `.env` file or export your API key before running the app:

```bash
setx GOOGLE_API_KEY "your_google_api_key_here"
```

Or in a shell:

```bash
export GOOGLE_API_KEY="your_google_api_key_here"
```

> In a production project, avoid hardcoding secrets directly in source files.

## ▶️ Run the App

```bash
streamlit run my_app.py
```

Then open the local URL shown in the terminal, typically:

```text
http://localhost:8501
```

## 📝 How It Works

1. Upload one or more PDF documents.
2. The app extracts raw text from the PDF pages.
3. The text is split into chunks using a recursive text splitter.
4. Embeddings are generated from the chunks.
5. FAISS stores the vector index locally.
6. You ask a question and the app retrieves the most relevant chunks.
7. Gemini responds using the retrieved context.

## 🧪 Example Use Case

- Upload a research paper related to machine learning
- Ask: "What are the key findings of this paper?"
- Ask: "Summarize the experiment setup and evaluation metrics"
- Ask: "What limitations are mentioned in the document?"

## ⚠️ Notes

- This app depends on a valid Google API key for Gemini and embeddings.
- Performance depends on the size and number of uploaded PDFs.
- Large documents may take longer to process due to chunking and embedding generation.

## 🤝 Contributing

Contributions are welcome. If you’d like to improve the app, open a pull request or suggest useful enhancements such as:

- PDF drag-and-drop improvements
- Better citation support
- Multi-file session persistence
- Better UI/UX refinements
- Model selection options

## 📄 License

This project is currently unlicensed. If you'd like to publish it publicly, consider adding a license such as MIT.

## 👤 Author

Built as a personal research assistant project for analyzing academic papers and extracting insights efficiently.
