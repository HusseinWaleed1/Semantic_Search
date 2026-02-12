# 📌 Semantic Search & Text Embeddings Project

## 🚀 Overview
This project demonstrates how to build a **Simple Semantic Search Engine** using **Sentence Transformers** and **cosine similarity**.

Instead of searching by exact keywords, this system searches by **meaning (semantic similarity)** using **text embeddings**.

## 🧠 What This Project Covers
- Text Embeddings using `SentenceTransformer`
- Cosine Similarity
- Similarity Matrix Visualization
- t-SNE 2D Visualization
- Simple Semantic Search Engine
- Ranking top-k most relevant documents

## 📂 Project Structure
├── semantic_search.py  
├── similarity_matrix.py  
├── visualization_tsne.py  
├── requirements.txt  
└── README.md  

## 🔧 Installation
Clone the repository:  
`git clone https://github.com/HusseinWaleed1/Semantic_Search.git`  
`cd Semantic_Search`  

Install dependencies:  
`pip install -r requirements.txt`  

## 📦 Requirements
Main libraries used:  
- `sentence-transformers`  
- `scikit-learn`  
- `numpy`  
- `pandas`  
- `matplotlib`  

## 🔍 How It Works

### 1️⃣ Convert Text to Embeddings
Each sentence is converted into a vector representation using:  
`model = SentenceTransformer("all-MiniLM-L6-v2")`  
`embeddings = model.encode(sentences)`  

### 2️⃣ Compute Similarity Matrix
Compute similarity between sentences using cosine similarity:  
`similarity_matrix = cosine_similarity(embeddings)`  
- `1.0` = identical meaning  
- Close to `0` = unrelated  
- Negative = opposite meaning (rare)  

### 3️⃣ Visualization with t-SNE
Reduce embeddings to 2D for visualization:  
`tsne = TSNE(n_components=2)`  
`embeddings_2d = tsne.fit_transform(embeddings)`  

This helps visualize semantic clusters (e.g., Animals, Programming, Food, Sports).  

### 4️⃣ Simple Semantic Search Engine
Steps:  
1. Encode stored documents  
2. Encode query  
3. Compute similarity  
4. Return top-k most relevant documents  

Example:  
`search_engine.search("What is AI?", top_k=1)`  

Output:  
Rank: 1  
Score: 0.89  
Document: Machine learning is a subset of artificial intelligence  

## 🎯 Example Use Cases
- FAQ Systems  
- Chatbots  
- Search Engines  
- RAG Systems  
- Knowledge Retrieval  

## 📊 Sample Query Results
| Query | Best Match |
|-------|------------|
| What is AI? | Machine learning is a subset of artificial intelligence |
| How neural networks work? | Neural Networks are inspired by human brain |
| Best language for data science? | Python is a popular programming language for data science |

## 🏆 Key Learning Outcomes
- Understanding text embeddings  
- Measuring semantic similarity  
- Building basic vector search  
- Ranking documents by meaning  
- Visualizing embedding clusters  

## 📌 Future Improvements
- Integrate **FAISS** for large-scale search  
- Build a **web interface**  
- Connect to **LLM (RAG system)**  
- Store embeddings in a **vector database**  

## 👨‍💻 Author
**Hussien Waleed**  
AI & NLP Enthusiast 🚀
