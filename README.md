# Spam-Detecting-Telegram-Bot
A Telegram Bot that predicts whether a message is "spam" or "ham".

The model was built with the aid of the online Udemy course, "Python for Data Science and Machine Learning Bootcamp". The construction of this model introduced me to basic NLP theory such as stopwords, bag-of-words, tokenization, TF-IDF and using NLTK to implement this. It also introduced me to a new classifier, the Multinomial Naive Bayes classifier (using keras). Finally, I was reminded of the use of data pipelining with Scikit-learn - probably the biggest take away.

Once the model was trained, it was stored as a .joblib file, *pipelined_model.joblib*, where it could then be loaded into the python script running the Telegram bot, *SpamDetectionBot.py*.

The *SpamDetectionBot.py* script (i.e. the Telegram bot) receives a message from the user, removes punctuation and stopwords and then passes the message into the loaded pipelined model. The prediction of *spam* or *ham* is then sent back to the user.

Here is a screenshot displaying the interaction of a user with the bot:

![alt text](https://github.com/ANDRYA005/Spam-Detecting-Telegram-Bot/blob/master/Screenshots/Display.jpeg)

