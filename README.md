# 🦜🔗 LangChain Fundamentals & RAG Tutorial

A comprehensive hands-on tutorial for learning **LangChain** and **RAG (Retrieval Augmented Generation)** using the **free Groq API**.

## 📚 What You'll Learn

| Notebook | Topics |
|----------|--------|
| `langchain_start.ipynb` | LangChain basics: LLM, Messages, Prompts, Chains, Output Parsers, Tools |
| `rag_fundamental_langchain.ipynb` | RAG pipeline: Document Loaders, Text Splitters, Embeddings, Vector Stores, Retrievers |

---

## 🛠️ Prerequisites Setup

### Step 1: Install VS Code

Download and install Visual Studio Code:

🔗 **Download:** [https://code.visualstudio.com/download](https://code.visualstudio.com/download)

After installation, install the **Python extension**:
1. Open VS Code
2. Go to Extensions (`Cmd+Shift+X` on Mac / `Ctrl+Shift+X` on Windows)
3. Search for "Python" and install the Microsoft Python extension
4. Also install "Jupyter" extension for notebook support

---

### Step 2: Install UV (Python Package Manager)

UV is a fast Python package manager. Install it based on your OS:

🔗 **Documentation:** [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/)

#### macOS / Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Windows (PowerShell)
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### Verify Installation
```bash
uv --version
```

---

### Step 3: Get Groq API Key (Free)

1. Go to Groq Console: [https://console.groq.com/keys](https://console.groq.com/keys)
2. Sign up for a free account
3. Create a new API key
4. Copy the key (starts with `gsk_...`)

---

## 🚀 Project Setup

### Step 1: Clone or Download the Project

```bash
# If using git
git clone <repository-url>
cd Rag_basic_test_langchain

# Or download and extract the zip file
```

### Step 2: Create Virtual Environment & Install Dependencies

```bash
# Create virtual environment with Python 3.12
uv venv --python 3.12

# Activate the virtual environment
# macOS/Linux:
source .venv/bin/activate

# Windows (PowerShell):
.venv\Scripts\Activate.ps1

# Windows (Command Prompt):
.venv\Scripts\activate.bat
```

### Step 3: Install Project Dependencies

```bash
# Install all dependencies from requirements.txt
uv pip install -r requirements.txt

# Or using uv add (recommended)
uv add -r requirements.txt
```

### Step 4: Configure API Key

Create a `.env` file in the project root:

```bash
# macOS/Linux
echo 'GROQ_API_KEY=your-api-key-here' > .env

# Or manually create .env file with:
GROQ_API_KEY=gsk_your_actual_api_key_here
```

⚠️ **Important:** Never commit your `.env` file to git!

---

## 📂 Project Structure

```
Rag_basic_test_langchain/
├── .env                              # Your API keys (create this)
├── .venv/                            # Virtual environment (auto-created)
├── data/
│   └── 6.LANDMARK JUDGMENTS...pdf    # PDF for RAG tutorial
├── langchain_start.ipynb             # LangChain Fundamentals
├── rag_fundamental_langchain.ipynb   # RAG Fundamentals
├── requirements.txt                  # Python dependencies
├── pyproject.toml                    # Project configuration
└── README.md                         # This file
```

---

## 🎯 Running the Notebooks

### Option 1: VS Code (Recommended)

1. Open the project folder in VS Code
2. Open `langchain_start.ipynb`
3. Select Python interpreter: Click "Select Kernel" → Choose `.venv` environment
4. Run cells with `Shift+Enter`

### Option 2: Jupyter Lab

```bash
# Install Jupyter
uv pip install jupyterlab

# Start Jupyter
jupyter lab
```

---

## 📦 Dependencies

| Package | Purpose |
|---------|---------|
| `langchain` | Core LangChain framework |
| `langchain-groq` | Groq LLM integration |
| `langchain-community` | Community integrations (FAISS, etc.) |
| `langchain-huggingface` | HuggingFace embeddings |
| `python-dotenv` | Environment variable management |
| `pypdf` | PDF document loading |
| `faiss-cpu` | Vector similarity search |
| `sentence-transformers` | Text embeddings |

---

## 🔧 Troubleshooting

### Issue: "ModuleNotFoundError"
```bash
# Make sure virtual environment is activated
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows

# Reinstall dependencies
uv pip install -r requirements.txt
```

### Issue: "API Key not found"
```bash
# Check if .env file exists
cat .env

# Make sure the key is set correctly
echo 'GROQ_API_KEY=gsk_your_key_here' > .env
```

### Issue: "Kernel not found" in VS Code
1. Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)
2. Type "Python: Select Interpreter"
3. Choose the `.venv` environment from the list

### Issue: UV command not found
```bash
# Add UV to PATH (macOS/Linux)
export PATH="$HOME/.cargo/bin:$PATH"

# Or reinstall UV
curl -LsSf https://astral.sh/uv/install.sh | sh
```

---

## 📖 Learning Path

1. **Start with:** `langchain_start.ipynb`
   - Learn LangChain basics
   - Understand LLMs, prompts, and chains

2. **Then move to:** `rag_fundamental_langchain.ipynb`
   - Build a RAG pipeline
   - Create a legal Q&A system

---

## 🔗 Useful Links

| Resource | Link |
|----------|------|
| VS Code Download | [https://code.visualstudio.com/download](https://code.visualstudio.com/download) |
| UV Installation | [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/) |
| Groq Console | [https://console.groq.com/keys](https://console.groq.com/keys) |
| LangChain Docs | [https://python.langchain.com/docs/](https://python.langchain.com/docs/) |
| LangChain Groq | [https://python.langchain.com/docs/integrations/chat/groq/](https://python.langchain.com/docs/integrations/chat/groq/) |
| FAISS Docs | [https://faiss.ai/](https://faiss.ai/) |
| HuggingFace | [https://huggingface.co/](https://huggingface.co/) |

---

## 📝 Quick Start Commands

```bash
# Complete setup in one go (macOS/Linux)
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv --python 3.12
source .venv/bin/activate
uv add -r requirements.txt
echo 'GROQ_API_KEY=your-key-here' > .env
```

```powershell
# Complete setup in one go (Windows PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
uv venv --python 3.12
.venv\Scripts\Activate.ps1
uv add -r requirements.txt
echo 'GROQ_API_KEY=your-key-here' > .env
```

---

## 🎓 About

This tutorial is designed for students learning:
- Large Language Models (LLMs)
- LangChain framework
- RAG (Retrieval Augmented Generation)
- Vector databases and embeddings

**Happy Learning! 🚀**
