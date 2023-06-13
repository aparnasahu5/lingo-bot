#lingo bot
Translation is necessary for the spreading of new information, knowledge, and ideas
across the world. It is absolutely necessary to achieve effective communication
between different cultures. In the process of spreading new information, translation is
something that can change history. It is the only medium by which certain people can
know different works that will expand their knowledge of the world.
For this reason, we decided to build a language translator and also a detector with
which the user can detect and translate their desired language. With our project, it can
be implemented in areas like chat apps where two people can communicate with each
other using their native languages. We can also use them for multiplayer games where
players from different countries will be able to chat with each other using their native
language for better strategic decisions on how to beat the other players in the game.
Our project has a wide array of applications it can be embedded into.

Existing Systems:
With advancements in communications and different dialects, it is common to be lost in
translation. When people aren’t able to understand each other, it leads to miscommunication,
irritability and the inability to share important information if needed. As social beings, it’s a
lot of take in. Trying to go for a universal language effectively results in the loss of culture.
Current systems like Google Translate or Duolingo are useful in detecting and translating
global languages. By just researching a bit on the existing systems, we were able to see that
most systems used NLTK for their implementation.[1] Another project followed the
Recurrent neural network while using the Keras library.[2] One project attempted to identify
language from very short strings by using LID networking. [3] Another project that used
NLTK for english-to-local language.
In this project, we have focused on building a language detector and translator. This project
will combine global as well as Indian regional languages. This is done without using the
NLTK library and with the use of the MultiNominalNB model.



Drawbacks of the existing systems:
The drawback for the RNN model was the slowness because of the scraping. While the
NLTK project was observed to have low accuracy. In the LID project, the LSM systems were
shallow, simple and outdated. The final project that we reviewed had only used English and
Efik because of which the accuracy in the training and testing was high.

Module Wise Description:
This program is constructed with the use of:
• CountVectorizer tool from the scikit-learn library to break down the given text into
words and then modify it into vectors on the basis of its frequency.
• LabelEncoder tool from the sklearn library is used to encode the levels of categorical
features into numeric values i.e. in this project to give unique records in the language
column and count of its corresponding records from the text column.
• train_test_split tool from the sklearn library split arrays or matrices into random train
and test subsets
• test_size has been initialized as 0.20 ( size of the test set is 20% and the train set is 80%
of the Lang_new_version_2.0 dataset)
• The model chosen for this project is MultiNomialNB from the sklearn.naive_bayes
library ,The multinomial Naive Bayes classifier is suitable for classification with
discrete features (e.g., word counts for text classification) which makes it an apt
combination with the CountVectorizer tool.
• The accuracy score, confusion matrix and classification report has been classified from
the sklearn.metrics library



Design:

Dataset used:
The dataset used for this project, Language_Detection, comprises 15+ languages and
comprises 10,000+ entries. This dataset was obtained from kaggle.

Tools used:
1. Google Colaboratory Notebook
2. Excel for the dataset
3. pandas for data manipulation and analysis.
4. numpy for adding support for large, multi-dimensional arrays and matrices, along
with a large collection of high-level mathematical functions to operate on these
arrays.
5. re for using regular expression functions
6. seaborn and matplotlib for drawing attractive and informative statistical graphics.
deep_translator to import the google_translator api for the translation process


Implementation:
We have 17 languages and their corresponding unique words are shown below:
![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/0a5e991c-bd09-4fe8-91c2-292793608a63)


The accuracy found out while predicting the languages is found to be 97.4855%
![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/7f458b30-2211-4ac1-a432-75c2c1ef1a4d)


The confusion matrix depicted below provides information on how the languages are
compared as well as the degree of similarity between them.
For example, when compared to any other language, the characters in the English language
are the most similar to those in English, followed by Italian and Portuguese.
![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/8977ae08-89b7-49d7-aca0-0e493fa83c7f)


The confusion matrix has been mapped into a heat map using the spectral colormap, with the
block with the highest similarity to a language being marked with a shade of blue ((3,3),253)
and the block with the least similarity to a language being marked with a shade of dark red.
(0)
![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/2703f2c8-2fe3-4bce-9ed1-7f303cecf2cb)


The classification report is given here, from which we can learn about the precision, recall,
f1-score and its accompanying macro average, weighted average, support value, and total
accuracy. As a result, we may deduce that 20 percent of the dataset (20% of 10,337 records =
2,068) has been used as the test set entries.
![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/c37a3b64-f807-4414-9843-cef88293fb9f)

![image](https://github.com/aparnasahu5/lingo-bot/assets/95071662/7fbbcdc3-78ed-4893-8006-7be027bf03b6)
