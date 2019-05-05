+++
title = "Video Game Recommender System   Final Report"
date = 2019-03-26

# List format.
#   0 = Simple
#   1 = Detailed
#   2 = Stream
list_format = 2

+++

Website: http://discorn.pythonanywhere.com/

#Hosting, Framework, Language
Hosting: PythonAnywhere  
Framework: Flask  
Languages: Python 3.6, SQLite, HTML, CSS  

#Search

# 1.	Functionality
The website is to take the user input and return a list of games in according to the relevancy of the input. Information returned would include the title, release date, metacritic score, price, and description.
To save space and reduce load time several unused data columns in the dataset were left out. Data such as the publisher count, achievement count, and linux requirement.
# 2.	Algorithm
The search function will use TF-IDF (Term Frequency – Inverse Document Frequency) by taking in every word on the input and calculates the frequency of the term among the documents then multiplied by the inverted frequency of term occurrences in each document. This repeats for every word and return a score to be outputted in the results page.

#Classifier

# 1.	Functionality  
After the user enters the query, the program would run MNB by running NB for every individual tag (Action, Adventure, Strategy, RPG, Sport, Racing). Returning to the user would be the total amount of words for each tag, probability of every tag, number of unique words overall in the dataset, probability of every query word given every tag, and the final probability of every tag given the query.  
# 2.	Algorithm  
Multinomial Naive Bayes by finding the best tag through P(tag | query) = P(tag)*P(word_1 | tag)*...*P(ward_n | tag)  

#Recommender

# 1.	Functionality  
Takes up to the past 3 search queries from the user and displays the top 10 recommended games.
# 2.	Algorithm  
A context based algorithm that applies the TF-IDF algorithm coupled with Multinomial Naive Bayes [P(tag | query) = P(tag)*P(word_1 | tag)*...*P(ward_n | tag)] by computing the TF-IDF score for each game per query multiply by a weight calculated by the Multinomial Naive Bayes then sort the score desending. 

# Source Code: 
https://github.com/KRT0335/RecSystem  
# Dataset: 
https://data.world/craigkelly/steam-game-data 
# References:
Basic flask tutorial  
http://www.blog.pythonlibrary.org/2017/12/12/flask-101-getting-started/  
Video tutorial of Python Flask by Corey Schafer  
https://www.youtube.com/watch?v=MwZwr5Tvyxo  
Blog describing TF-IDF integration into Python  
https://towardsdatascience.com/tf-idf-for-document-ranking-from-scratch-in-python-on-real-world-dataset-796d339a4089  
Multinomial Naive Bayes from textbook:  
https://nlp.stanford.edu/IR-book/pdf/13bayes.pdf  
Multinomial Naive Bayes article by John Michael Kovachi  
https://medium.com/@johnm.kovachi/implementing-a-multinomial-naive-bayes-classifier-from-scratch-with-python-e70de6a3b92e  
Multinomial Naive Bayes Classifier for Text Analysis (Python)  
https://towardsdatascience.com/multinomial-naive-bayes-classifier-for-text-analysis-python-8dd6825ece67  
Basic concepts of recommendation systems
https://www.analyticsvidhya.com/blog/2016/03/exploring-building-banks-recommendation-system/
Paper over using Multinomial Naive Bayes for recommender system (by Koji Miyahara and Michael J. Pazzani)
https://www.ics.uci.edu/~pazzani/Publications/IPSJ.pdf
Forum post over the use of Multinomial Naive Bayes in recommendation system
https://www.quora.com/How-do-I-implement-a-recommendation-engine-using-Naive-Bayes-Method
