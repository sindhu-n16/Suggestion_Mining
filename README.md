In this Project, I am implementing a transformer model for Suggestion Mining from opinion reviews.

The project mainly having the following components:

The Dataset Embedding Creation Squence to Sequence Model Building Training Evaluation Output

** Dataset: **

The dataset consists of reviews given by customers for a hotel named Berlin which is a set of train and test data collected from Kaggle. The goal is to extract the suggestion phrases from given reviews.

** Embedding Creation: ** Embedding is the process of representing a word or text in vector or number format with specific dimension.

As, the python code consisting on various special characters, generating embedding for each character will improve the model performance, than assigning a random values.

For generating embedding for Python code, gensim with Word2Vec model has be utilized and created a embedding with the same dimension ie 256.

** Squence to Sequence Model Building: **

The model built for achieving the desired result with the reference of Attention is all you need, a transformer model by Google in 2017.

The transformer model consists of Encoder and Decoder block with varying number of blocks in each part. Here we experimented with various number of blocks in Encoder and Decoder also. Finally we used Three Encoder blocks and 3 Decode blocks.

Each Enoder block consisting of same architecture as Attention All you need paper with Mutlihead Attention and FUlly Connected Network Each Decode block also having similar structure with Masked Attention, Mutli-head Attention and fully connected network.

** Training & Evaluation: **

The Complete sequence to Sequence model created and Trained it for best valid loss and ran the model for 100 Epochs.

** Output: **

User Interface is built using streamlit. The review number representing the customer review taken from the dataset is given in the text box and tranformer model is checked. Then the output will be displayed as the suggestion extracted from the given review. Visualization is represented for the review and the suggestion in the form of attention weights matrix.
