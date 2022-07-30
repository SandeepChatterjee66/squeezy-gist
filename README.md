### Squeezy-Gist
A tool to analyze the amount of content in long text using NLP.

Suppose you are in a test, you have been asked a question to write in 2000 words, and you don't know the answer! So what do you do? You write as much you know, then use filling words to extend it, and then paraphrase the same sentences again and again, repeatedly. So that if the examiner is in hurry and if he is marking your answers based on superficial overview and length of the paragraph written, he can mark you well based on that.

So, we are going to detect the same thing here, if you have a long paragraph of text blabbering about same thing again and again. This tool will allow you to analyze , how much is the actual content after squeezing it though the magic of NLP algorithms.

##So How are we going to do it ?

Well here are the steps:
1. First take the large input text, and pre-process it            
2. Now we will tokenize the text, into sentences and then tokenize each sentences into words.            
3. The count of words we have is the initial count.
4. Now, we will remove the stop words - to do this we can use the NLTK stop dictionary
5. Then do stemming of words and check the count of new vocabulary, this will tell how rich the vocabulary is.
6. Now we will take each sentences from step 4, and using word2vec, calculate the average vector for all words in every sentence and use cosine similarity between vectors:
7. Then take each sentences, and compare this sentence with all other remaining sentences. If two sentences are semantically similar, we only treat them as single sentence and count them as 1.
8. 

Exact methods:
1. for 1 we will convert all words into lower case remove irrelevant punctuations and correct the spellings if possible.
