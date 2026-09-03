conda install -y -c conda-forge gxx_linux-64 libgomp


# 1. Create a fresh environment named rag_env with Python 3.10
conda create -n rag_env python=3.10 -y

# 2. Activate the new environment sandbox
conda activate rag_env


pip install --upgrade pip
pip install docling langchain-text-splitters rank_bm25 sentence-transformers faiss-cpu ollama pandas tqdm ragas langchain-community python-dotenv notebook

# 1. Download and unpack the standalone Linux binary core helper
curl -L https://ollama.com -o ollama
chmod +x ollama

# 2. Start the Ollama background server execution worker
./ollama serve &

# 3. Pull down the lightweight 3B model parameters file inside a new task line
./ollama run llama3.2


jupyter notebook --ip=0.0.0.0 --no-browser


