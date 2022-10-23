# Implentation of TF-IDF Vectorizer without using scikit-learn library.

Tf-idf stands for term frequency-inverse document frequency, and the TF-IDF weight is a weight often used in information retrieval and text mining. 
This weight is a statistical measure used to evaluate how important a word is to a document in a collection or corpus. 
The importance increases proportionally to the number of times a word appears in the document but is offset by the frequency of the word in the corpus. 

TF-IDF can be successfully used for stop-words filtering in various subject fields including text summarization and classification.


TF: Term Frequency, which measures how frequently a term occurs in a document. Since every document is different in length, it is possible that a term 
would appear much more times in long documents than shorter ones. Thus, the term frequency is often divided by the document length 
(aka. the total number of terms/words in the document) as a way of normalization:

𝑇𝐹 = Number of times a term or word appears in a document/Total number of terms or words in the document.

IDF: Inverse Document Frequency, which measures how important a term or word is. While computing TF, all terms are considered equally important. 
However it is known that certain terms, such as "is", "of", and "that", may appear a lot of times but have little importance. 
Thus we need to weigh down the frequent terms while scale up the rare ones, by computing the following:

𝐼𝐷𝐹 = log𝑒(Total number of documents/Number of documents with term or word in it) 
For numerical stabiltiy we will be changing this formula little bit : 𝐼𝐷𝐹 = log𝑒(Total number of documents/(Number of documents with term or word in it + 1)).


To better understand what TF-IDF does, in the .ipynb I've implemented the TF-IDF Vectorizer from scratch without using sckit-learn. And to further check
my results I've compared the values of my custom function with scikit-learn's implementation. 
