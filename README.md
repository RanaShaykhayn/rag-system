# RAG System with LLM-as-a-Judge Evaluation

A Retrieval-Augmented Generation (RAG) system I built to retrieve relevant document chunks and evaluate retrieval quality with high precision.

## 🎯 The Problem I Solved
Large Language Models (LLMs) don't know about private company documents. RAG solves this by retrieving relevant chunks before generating an answer.

## 💡 My Solution
1. **Retriever**: I built a system that splits documents into chunks, converts them to embeddings, and searches using Cosine Similarity.
2. **Evaluator**: I created an evaluation framework using an LLM-as-a-Judge to validate if the retrieved chunks contain the correct answer.
3. **Precision**: I achieved **100% precision** on a custom golden dataset.

## 📊 Results
- **Precision**: 100% (5/5 queries correct)
- **Retrieval Method**: Cosine Similarity (threshold > 0.60)
- **Evaluation**: LLM-as-a-Judge (using Gemini Flash)

## 🚀 How to Run It
```bash
pip install -r requirements.txt
python -m test.test_evaluator