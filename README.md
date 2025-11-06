🧠 MediBot — Your Personal Medical Chat Assistant
<p align="center"> <img src="https://img.shields.io/badge/Python-3.10+-blue.svg?style=for-the-badge&logo=python" /> <img src="https://img.shields.io/badge/Framework-LangChain-orange.svg?style=for-the-badge&logo=chainlink" /> <img src="https://img.shields.io/badge/Database-FAISS-green.svg?style=for-the-badge&logo=vectorworks" /> <img src="https://img.shields.io/badge/LLM-OpenAI-brightgreen.svg?style=for-the-badge&logo=openai" /> <img src="https://img.shields.io/badge/UI-Streamlit-red.svg?style=for-the-badge&logo=streamlit" /> </p>

🩺 MediBot is an intelligent AI-powered Medical Chatbot built using LangChain, OpenAI, and FAISS, capable of answering complex medical questions using trusted data sources like The Gale Encyclopedia of Medicine.

✨ Features

✅ Extracts and processes content from large medical PDFs.
✅ Understands and answers user queries using LLMs (OpenAI GPT models).
✅ Uses FAISS Vector Search for lightning-fast retrieval.
✅ Built with modular, scalable architecture.
✅ Keeps your OpenAI API key secure via .env.
✅ Interactive and user-friendly Streamlit UI.

🧩 Tech Stack
Component	Technology Used
🧠 LLM Model	OpenAI GPT
🔗 Framework	LangChain
🗃️ Vector Database	FAISS
🌐 Frontend	Streamlit
🧰 Language	Python
🔒 Environment Management	dotenv
🗂️ Project Structure
Medical_Chatbot/
│
├── data/                     # Medical PDFs
│   └── The_GALE_ENCYCLOPEDIA_of_MEDICINE_SECOND.pdf
│
├── vectorstore/              # FAISS database (ignored in git)
│   ├── index.faiss
│   └── index.pkl
│
├── .env                      # Contains API Key (ignored)
├── .gitignore
├── createMemoryForLLM.py     # Creates FAISS memory from PDFs
├── connectMemoryWithLLM.py   # Connects FAISS memory with OpenAI model
├── medibot.py                # Streamlit chatbot application
└── README.md

⚙️ Setup Instructions
1️⃣ Clone the Repository
git clone https://github.com/<your-username>/Medical_Chatbot.git
cd Medical_Chatbot

2️⃣ Create a Virtual Environment
python -m venv venv
source venv/Scripts/activate     # Windows
# or
source venv/bin/activate         # macOS/Linux

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Add Your OpenAI API Key

Create a .env file in the project root:

OPENAI_API_KEY=your_openai_api_key_here

5️⃣ Generate Vector Memory
python createMemoryForLLM.py

6️⃣ Run MediBot 🧠
streamlit run medibot.py


Then open your browser at 👉 http://localhost:8501

💬 Example Query

User: What is a pimple in teenagers?
MediBot: A pimple in teenagers is most likely folliculitis, which is inflammation or infection of one or more hair follicles.

🔐 Security Note

⚠️ The .env file (containing your API key) is safely excluded via .gitignore.
Never commit it to public repositories!

🤝 Contributing

Contributions are always welcome 💡

Fork the repo

Create a new branch

Make your improvements

Submit a Pull Request 🚀

👨‍💻 Author

👋 Ankita Raj
🎓 B.Tech CSE @ JIIT Noida
📧 rajankita098@gmail.com

📜 License

This project is licensed under the MIT License — you’re free to use, modify, and distribute it.

⭐ Support

If you like this project, please give it a ⭐ on GitHub — it helps others find it too!
