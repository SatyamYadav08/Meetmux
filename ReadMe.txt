ChatRec_Model - Conversational Response Prediction System
==========================================================

This project implements an offline GPT-2 Transformer model to predict User A's next reply based on conversational context. [cite: 63]
----------------------------------------------------------
Directory Structure
----------------------------------------------------------
ChatRec_Model/
│── ChatRec_Model.ipynb      : Jupyter notebook containing code execution
│── Report.pdf               : Technical report summarizing model design & evaluation
│── Model.joblib             : Serialized fine-tuned GPT-2 model and tokenizer
│── ReadMe.txt               : Documentation file (this one)

----------------------------------------------------------
Steps to Run
----------------------------------------------------------
1. Install dependencies: [cite: 64]
   pip install torch transformers datasets nltk rouge-score sacrebleu pandas scikit-learn joblib tqdm [cite: 64]

2. Place your conversation dataset (conversationfile.xlsx [cite: 64] 
or .csv) in the working directory. [cite: 65]

3. Run ChatRec_Model.ipynb to preprocess, train, and evaluate the model. [cite: 65]
4. After training: [cite: 66]
   - The model will be saved as ./final_model/ (Hugging Face format) [cite: 66]
   - It will also be serialized as ChatRec_Model/Model.joblib [cite: 66]

----------------------------------------------------------
Evaluation Summary
----------------------------------------------------------
BLEU Score : 0.0102 [cite: 66]
ROUGE-1    : 0.1500 [cite: 66]
ROUGE-2    : 0.0000 [cite: 66]
ROUGE-L    : 0.1000 [cite: 66]
Perplexity : 53.9670 [cite: 66]

----------------------------------------------------------
Model Justification
----------------------------------------------------------
Model  : GPT-2 (autoregressive Transformer) [cite: 66]
Reason : Efficient for small datasets, capable of context-aware text generation. [cite: 66]
Deployment : Joblib serialization allows fast loading in production (Flask/FastAPI). [cite: 67]

----------------------------------------------------------
Author's Note
----------------------------------------------------------
This model serves as a prototype. [cite: 67] For production, train with more data and consider
larger models (GPT-2 Medium, T5, or Longformer) for better context understanding. [cite: 68]