# Question-Answering System using FAQs
### Problem Statement:
Often websites have comprehensive FAQs, but manually searching and finding the answer to a specific 
question from these FAQs is not trivial. Examining main family of models is important in understanding 
what all things can be done to make the model better. Which model to implement for a smaller chatbot 
projects which could be more feasible in terms of space instead of loading heavy models.

### Approach:
In this project, I examined the task of automatically retrieving a suitable response to customer questions 
from FAQs. My basic strategy is as follows: For a given query, find the FAQ question that is closest in 
meaning to the user query and display it to the user. For this, we need to have an efficient way of 
computing semantic similarity between two sentences.
To compute semantic similarity between sentences, we will convert each sentence into a vector. I can 
then use cosine similarity between vectors to come up with a distance measure between sentences that 
indicates how similar they are in meaning. In this project, below models were used 
1) Bag of Words (BoW)
2) Pre-trained word embedding models : 
a) Word2Vec- SkipGram model
b) GloVe
3) BERT embeddings
The basic approach is to use **Different Embeddings + Cosine Similarity on different datasets.**

I have used different types of dataset for the four models. They are as follows:
1) Easy dataset with 10 FAQs: This was created by converting 10 FAQs using a paraphrasing tool called QuillBot.
2) Medium dataset with 10 FAQs: This was created by manually paraphrasing 10 FAQs keeping 3 to 4 words in common.
3) Hard dataset with 10 FAQs: This was created by manually paraphrasing 10 FAQs keeping 1 to 2 words in common.
The smaller datasets would help us study the accuracy of different models based on the level of 
paraphrasing. 

### Result:
We concluded that the Word2Vec model could be implemented if the processing power is low as its 
performance is similar to that of BERT model which requires GPU.

### References:

1) https://xplordat.com/2019/09/23/bow-to-bert/

2) https://towardsdatascience.com/from-pre-trained-word-embeddings-to-pre-trained-language-models-focus-on-bert-343815627598

3) https://towardsdatascience.com/cosine-similarity-how-does-it-measure-the-similarity-maths-behind-and-usage-in-python-50ad30aad7db

For Code taken help from youtube and stackoverflow

