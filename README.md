# Spam-Detecting-Telegram-Bot
A Telegram Bot that predicts whether a message is "spam" or "ham".

The model was built with the aid of the online Udemy course, "Python for Data Science and Machine Learning Bootcamp". The construction of this model introduced me to basic NLP theory such as stopwords, bag-of-words, tokenization, TF-IDF and using NLTK to implement this. It also introducing me to a new classifier, the Mulitnomial Naive Bayes classifier (using keras). Finally, it introduced me to data pipelining - probably the biggest take away.

Once the model was trained, it was stored as a .joblib file,*pipelined_model.joblib*, where it could then be loaded into the python script running the telegram bot, *SpamDetectionBot.py*.

The *SpamDetectionBot.py* script (i.e. the Telegram Bot) receives message from the user, removes punctuation and stopwords and then passes the message into the loaded pipelined model. The prediction of *spam* or *ham* is then sent back to the user.

Here is a screenshot displaying the interaction of a user with the bot:

![alt text](https://github.com/ANDRYA005/Telegram_Digit_Recognition_Bot/blob/master/Screenshot_for_GitHub.PNG)

