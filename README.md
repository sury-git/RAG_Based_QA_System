# RAG_Based_QA_System
Question 1: Retrieval-Augmented Generation (RAG) Based QA System
Objective
Build a simple question-answering system using document retrieval and a pre-trained language
model.
1. Document Selection: 
    * Total 5 docs has beed used in above project. Which are given below with Number of 
        Aritficial Intelligence: 13140 words 
        Artificial Organs      : 2540 Words
        Great Pyramid Giza     : 12305 Words
        Psycological effect of Internet: 3252 Words
        List of dates for apoclyptic events: 7124 Words
    All the documents data has been taken from wikipedia

    * Read all the documents and concatenate all the document to make a single large document

    * Preprocess the data by removing all the square brackets data and new line specifiers with the help of RegEx.

2. Embedding Generation & Storage:
    * From the Sentence Transformer the pre trained model all-MiniLM-L6-v2 has been loaded. This model is used to generate vector embeddings for the document.

    * As the generated embedded vector is dense. So we use FAISS to store this vector. FAISS is used for efficient similiarity search and fast retrieval of user Query.

3. Query Processing & Retrieval:
    * Took the user query as Input and preprocess the same.
    * Encode it with sentence transform to make vector embedding
    * Pass it to cosine similiarity with document's embedding which compare both the embeddings and retrieve the most similar.

4. Answer Generation:
    * For the answer generation based on the retrieved document' chunk and the user query we use flan-t5-small.

Dependencies for the above projects are:
Numpy
Pandas
Sentence Transformers
FAISS
Transformers
Sklearn 
matplotlib
RegEx