


# **Lingo Bot**


## **Introduction**

Translation plays a crucial role in spreading new information, knowledge, and ideas worldwide. It enables effective communication among different cultures, shaping history and expanding people's understanding of the world. To facilitate seamless communication, we have developed the Lingo Bot, a language translator and detector. This project aims to bridge language barriers in various domains such as chat apps and multiplayer games, enabling users to interact in their native languages for better strategic decision-making.


## **Existing Systems**

Despite the availability of translation systems like Google Translate and Duolingo, challenges still exist in language complexity and dialects. Miscommunication, frustration, and the inability to accurately share important information are common issues. Our research revealed that many existing systems rely on the Natural Language Toolkit (NLTK) library [1] for their implementation. Other projects have explored the use of Recurrent Neural Networks (RNN) with the Keras library [2]. There was also a project that attempted language identification from short strings using LID networking [3]. However, our project focuses on developing a language detector and translator that combines global and Indian regional languages without relying on the NLTK library.


## **Drawbacks of Existing Systems**

During our analysis of existing systems, we identified several drawbacks:



* RNN models were slow due to the scraping process, resulting in decreased efficiency.
* NLTK-based projects exhibited lower accuracy in language detection and translation.
* The language support models (LSMs) used in the LID project were shallow, simple, and outdated.
* Some projects focused only on English and a few additional languages, limiting their language coverage and overall accuracy.


## **Module-Wise Description**

Our project utilizes the following tools and libraries:



1. **CountVectorizer tool** (from scikit-learn library): This tool breaks down the input text into words and converts them into vectors based on their frequency.
2. **LabelEncoder tool** (from scikit-learn library): This tool encodes categorical features, such as language labels, into numeric values for unique identification.
3. **train_test_split tool** (from scikit-learn library): This tool splits the dataset into random train and test subsets, with a test size of 20% and a train size of 80%.
4. **MultiNomialNB model** (from scikit-learn library): This model, suitable for classification with discrete features, is chosen for language detection and works in conjunction with the CountVectorizer tool.
5. **sklearn.metrics library**: This library provides functions for calculating accuracy scores, generating confusion matrices, and producing classification reports.


## **Design**


### **Dataset Used**

We utilized the **Language_Detection dataset** obtained from Kaggle, comprising 15+ languages and over 10,000 entries.


### **Tools Used**

Our project employs the following tools and libraries:



* **Google Colaboratory Notebook**: This platform is used for development and execution of the project.
* **Excel**: The dataset is managed and manipulated using Excel for data preprocessing.
* **pandas**: This library is utilized for efficient data manipulation and analysis.
* **NumPy**: It provides support for handling large, multi-dimensional arrays and performs various mathematical functions.
* **re**: Regular expression functions are used for text preprocessing and cleaning.
* **seaborn and matplotlib**: These libraries are used to create visually appealing statistical graphics.
* **deep_translator**: We incorporated the `google_translator` API through the `deep_translator` package for the translation process.


## **Implementation**
The implementation of our project involved training the model on a dataset containing 17 languages. The unique words associated with each language were extracted for prediction. The accuracy achieved in language prediction was found to be high.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/d53274f8-4e80-417a-a004-703101c29cdd)

We have trained our model with 17 languages and their corresponding unique words. The accuracy achieved in predicting the languages is 97.4855%.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/b4715887-3b45-404a-86e5-ebbdd568e7ba)

The confusion matrix provides insights into the similarity between languages, where English, Italian, and Portuguese share higher similarities.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/a70d334c-5b3f-47b3-842d-679f76724456)

To visualize the confusion matrix, we created a heat map using the spectral colormap, indicating the degrees of similarity between languages.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/5bb3ff5d-6dd1-449c-829c-66cf04e238ab)

The classification report presents precision, recall, f1-score, and other metrics for each language, demonstrating the overall accuracy of the model.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/ccd30dee-bd07-48d9-a748-1fcc33160617)

By utilizing the Lingo Bot, users can overcome language barriers and engage in effective cross-cultural communication.

![image](https://github.com/Shubhdeepdsa/Appi/assets/90149745/031e1517-78a4-4cfa-aabb-2d9850c62390)

Feel free to explore the code and datasets to gain a deeper understanding of the project's implementation.
