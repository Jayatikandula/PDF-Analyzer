A lightweight and intelligent GenAI-powered application that allows users to upload PDF documents and ask natural language questions. It uses Gemini Flash 1.5 through LangChain to understand, process, and respond to queries quickly and accurately.

🚀 Features
📤 PDF Upload & Processing – Supports uploading and analyzing any PDF document.

🧠 LLM-Powered Q&A – Uses Gemini Flash 1.5 for fast, intelligent question-answering.

🧩 Document Chunking & Embedding – Splits and embeds PDF content for semantic search.

🗃️ FAISS Vector Store – Efficient retrieval of relevant document parts.

🎛️ Streamlit Interface – Simple, clean, and interactive UI for users.

🛠️ Tech Stack
Frontend: Streamlit

LLM: Gemini Flash 1.5 (via LangChain)

Vector Store: FAISS

Embeddings: Google's embedding models or OpenAI embeddings

Python Libraries: LangChain, PyMuPDF (fitz), FAISS, dotenv, etc.

📁 Project Structure
bash
Copy
Edit
.
├── app.py                  # Main Streamlit app
├── requirements.txt        # Required Python packages
├── utils/                  # Utility modules
│   ├── pdf_loader.py       # Loads and chunks PDF content
│   └── llm_query.py        # Handles LLM querying logic
├── .env                    # Contains your Gemini API key (not pushed to GitHub)
└── README.md               # Project documentation
⚙️ Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/pdf-analyzer-gemini.git
cd pdf-analyzer-gemini
2. Set Up Virtual Environment
bash
Copy
Edit
python -m venv venv
# Activate it
source venv/bin/activate         # macOS/Linux
venv\Scripts\activate            # Windows
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
🔧 Configuration
Create a .env file in the root folder and add your Gemini API key:

ini
Copy
Edit
GEMINI_API_KEY=your_gemini_flash_key
▶️ Run the App
Launch the application with:

bash
Copy
Edit
streamlit run app.py
🧠 How It Works
The user uploads a PDF through the Streamlit interface.

The app splits the PDF into manageable chunks using PyMuPDF.

Each chunk is embedded and stored in a FAISS vector database.

When a user asks a question, the app retrieves relevant chunks and queries Gemini Flash 1.5 via LangChain.

The model provides a precise answer based on the retrieved document content.

📌 Use Cases
Academic paper summarization and Q&A

Business reports and financial document analysis

Contract understanding and legal document querying

Personal note/document search using natural language

🔒 Security Tips
For production use:

Secure your .env file and API keys

Use authentication for user access

Log usage and implement rate limiting if hosted publicly

🤝 Contributions
Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to improve.

