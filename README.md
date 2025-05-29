# multiModal-Rag
references : 
https://openreview.net/pdf?id=6ewsi4xi1L

This project is a Multimodal Retrieval-Augmented Generation (RAG) system that allows users to ask questions about Flipkart products, and it answers by retrieving relevant product information using both text and image embeddings.Project Overview


Pipeline 
1. Extract data from flipkart on iphones less tha 50,000 using beautiful soup and requests module  
1. Data Format
Each product contains:

name
description
specifications (list)
reviews (list)
qna (list)
price
category
rating
link
image_path (for loading product image later) 



2. Store those embeddings in a Chroma vector database.
I used a  techqinue that uses text embeddings , images embeddings and caption(generated from the image ) embeddings . 
I thought of using a hybrid technique for iamge embeddings as well. 

3. Use LangChain's RetrievalQA with Gemini 1.5 Pro LLM.


4. Allows users to ask natural language queries like:
“What is the cheapest iPhone?”# multi-modal-ragchatbot
