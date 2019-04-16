+++
title = "Video Game Recommender System   Part 2: Classifier"
date = 2019-03-26

# List format.
#   0 = Simple
#   1 = Detailed
#   2 = Stream
list_format = 2

+++

# Video Game Recommender System   Part 2: Classifier

Website: http://discorn.pythonanywhere.com/

# 1.	Hosting, Framework, Language
Hosting: PythonAnywhere  
Framework: Flask  
Languages: Python 3.6, SQLite, HTML, CSS  
Classifier: Multinomial Naive Bayes
# 2.	Functionality
After the user enters the query, the program would run MNB by running NB for every individual tag (Action, Adventure, Strategy, RPG, Sport, Racing). Returning to the user would be the total amount of words for each tag, probability of every tag, number of unique words overall in the dataset, probability of every query word given every tag, and the final probability of every tag given the query. 
# 3.	Algorithm
Multinomial Naive Bayes by finding the best tag through P(tag | query) = P(tag)*P(word_1 | tag)*...*P(ward_n | tag)

# Challenges:
•	Choosing between SVM and MNB for the classifier
•	Deciding which tags to use to build the classifier
# Improvements to be Made:
- [ ] CSS visual aesthetics  
- [ ] Add proper accuracy with training and testing data
- [ ] Add stemming function  
- [ ] Exclude stop words  
- [ ] Expand to more untouched tags such as Indie





# Source Code: 
https://github.com/KRT0335/RecSystem  
# Dataset: 
https://data.world/craigkelly/steam-game-data 
# References:
Multinomial Naive Bayes from textbook:
https://nlp.stanford.edu/IR-book/pdf/13bayes.pdf
Multinomial Naive Bayes article by John Michael Kovachi
https://medium.com/@johnm.kovachi/implementing-a-multinomial-naive-bayes-classifier-from-scratch-with-python-e70de6a3b92e
Multinomial Naive Bayes Classifier for Text Analysis (Python)
https://towardsdatascience.com/multinomial-naive-bayes-classifier-for-text-analysis-python-8dd6825ece67
