# filename: README.md
# 🤖 AI Research Agent — Agentic AI Capstone Project

> **My first step into the world of Agentic AI.**
> An end-to-end autonomous research pipeline that takes a topic,
> fetches real papers, reasons over them, and produces a full
> research paper + PowerPoint presentation — fully automated.

---

## 🚀 What This Does

You type a topic. The agent does everything else:
Topic Input
│
├── 📡  Fetches papers from arXiv
├── 🧠  Chunks + indexes them into a vector store (RAG)
├── 💡  Extracts key ideas via semantic search
├── 🧪  Generates a research hypothesis
├── ✍️   Writes 8 full paper sections (LLM)
├── 🎯  Quality-scores the output (clarity, novelty, etc.)
├── 💾  Saves → .txt + .docx (Word document)
└── 📊  Builds → .pptx (PowerPoint presentation)

🗂️ Project Structure
research_agent/
│
├── agent_core.py               # Core utilities, LLM setup, embedder
│
├── 01_hello_langchain.ipynb    # Week 1 — LangChain fundamentals
├── 02a_arxiv_search.ipynb      # Week 2a — arXiv paper fetching
├── 02b_pdf_parser.ipynb        # Week 2b — PDF parsing
├── 02c_quality_checker.ipynb   # Week 2c — Quality scoring
├── 02d_full_week2_agent.ipynb  # Week 2 — Full mini-agent
├── 03a_vector_store.ipynb      # Week 3a — FAISS vector store
├── 03b_semantic_search.ipynb   # Week 3b — Semantic search
├── 03c_rag_agent.ipynb         # Week 3c — RAG pipeline
├── 04a_interactive_agent.ipynb # Week 4a — Interactive agent
├── 04b_multi_topic_compare.ipynb # Week 4b — Multi-topic comparison
├── 04c_master_agent.ipynb      # Week 4 Capstone — Master agent
├── 05_paper_draft.ipynb        # Week 5 — Full paper writer
├── 06_presentation.ipynb       # Week 6 — PowerPoint generator
├── 07_run_agent.ipynb          # 🎯 MAIN INTERFACE — run this
│
├── outputs/                    # All generated files land here
│   ├── *.txt
│   ├── *.docx
│   └── *.pptx
│
└── data/
└── vector_db/              # FAISS index (auto-created)

🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **LLM** | Groq API — `llama-3.1-8b-instant` |
| **Orchestration** | LangChain |
| **Embeddings** | `all-MiniLM-L6-v2` (HuggingFace) |
| **Vector Store** | FAISS |
| **Paper Source** | arXiv API |
| **Output — Word** | `python-docx` |
| **Output — PPT** | `python-pptx` |
| **Interface** | Jupyter + `ipywidgets` |

⚡ Quick Start
1. Clone the repo
git clone https://github.com/YOUR_USERNAME/research-agent.git
cd research-agent
2. Install dependencies
pip install langchain langchain-groq langchain-community
pip install faiss-cpu sentence-transformers
pip install arxiv pymupdf python-docx python-pptx
pip install ipywidgets jupyter
3. Set your Groq API key
Create a .env file:
 GROQ_API_KEY=your_key_here
Get a free key at → https://console.groq.com
4. Run the agent
Open 07_run_agent.ipynb in Jupyter, run all cells,
type your topic and click ▶ RUN AGENT.

📸 Sample Output
Input topic: Reinforcement learning from human feedback
Generated in one run:

📝 Full research paper (~1,800 words across 8 sections)
📊 PowerPoint presentation (auto-styled slides)
🎯 Quality scorecard (clarity, novelty, feasibility scores)


🧠 What I Learned Building This

How RAG (Retrieval-Augmented Generation) works end-to-end
How to build LangChain pipelines that chain prompts + models
How vector stores enable semantic search over documents
How to orchestrate multi-step LLM workflows (agentic loops)
Real-world challenges: rate limits, prompt engineering,
error handling, output parsing


🗺️ What's Next

[ ] Add memory so the agent can refine across multiple runs
[ ] Web UI with Streamlit or Gradio
[ ] Support more paper sources (Semantic Scholar, PubMed)
[ ] Multi-agent collaboration (research agent + critic agent)


👤 Author
Mah Rathod
First agentic AI project — June 2026
Built with curiosity, LangChain, and a lot of rate limit errors 😄





