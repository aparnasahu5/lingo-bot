#lingo bot
Lingo Bot
Introduction
Translation plays a crucial role in spreading new information, knowledge, and ideas worldwide. It enables effective communication among different cultures, shaping history and expanding people's understanding of the world. To facilitate seamless communication, we have developed the Lingo Bot, a language translator and detector. This project aims to bridge language barriers in various domains such as chat apps and multiplayer games, enabling users to interact in their native languages for better strategic decision-making.

Existing Systems
Despite the availability of translation systems like Google Translate and Duolingo, challenges still exist in language complexity and dialects. Miscommunication, frustration, and the inability to accurately share important information are common issues. Our research revealed that many existing systems rely on the Natural Language Toolkit (NLTK) library [1] for their implementation. Other projects have explored the use of Recurrent Neural Networks (RNN) with the Keras library [2]. There was also a project that attempted language identification from short strings using LID networking [3]. However, our project focuses on developing a language detector and translator that combines global and Indian regional languages without relying on the NLTK library.

Drawbacks of Existing Systems
During our analysis of existing systems, we identified several drawbacks:

RNN models were slow due to the scraping process, resulting in decreased efficiency.
NLTK-based projects exhibited lower accuracy in language detection and translation.
The language support models (LSMs) used in the LID project were shallow, simple, and outdated.
Some projects focused only on English and a few additional languages, limiting their language coverage and overall accuracy.
Module-Wise Description
Our project utilizes the following tools and libraries:

CountVectorizer tool (from scikit-learn library): This tool breaks down the input text into words and converts them into vectors based on their frequency.
LabelEncoder tool (from scikit-learn library): This tool encodes categorical features, such as language labels, into numeric values for unique identification.
train_test_split tool (from scikit-learn library): This tool splits the dataset into random train and test subsets, with a test size of 20% and a train size of 80%.
MultiNomialNB model (from scikit-learn library): This model, suitable for classification with discrete features, is chosen for language detection and works in conjunction with the CountVectorizer tool.
sklearn.metrics library: This library provides functions for calculating accuracy scores, generating confusion matrices, and producing classification reports.
Design
Dataset Used
We utilized the Language_Detection dataset obtained from Kaggle, comprising 15+ languages and over 10,000 entries.

Tools Used
Our project employs the following tools and libraries:

Google Colaboratory Notebook: This platform is used for development and execution of the project.
Excel: The dataset is managed and manipulated using Excel for data preprocessing.
pandas: This library is utilized for efficient data manipulation and analysis.
NumPy: It provides support for handling large, multi-dimensional arrays and performs various mathematical functions.
re: Regular expression functions are used for text preprocessing and cleaning.
seaborn and matplotlib: These libraries are used to create visually appealing statistical graphics.
deep_translator: We incorporated the google_translator API through the deep_translator package for the translation process.
Implementation
The implementation of our project involved training the model on a dataset containing 17 languages. The unique words associated with each language were extracted for prediction. The accuracy achieved in language prediction was found to be high.
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

