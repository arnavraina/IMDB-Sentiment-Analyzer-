# IMDB-Sentiment-Analyzer-
It is a a project which deals with classification of IMDB movie reviews and classifies it to be positive or negative
With the widespread use of social media, the need to analyze the sentiment of content that people share over social media is increasing day by day. Considering the volume of data coming through diffrent social media such as Facebook,twitter,Imdb,Amazon , it is quite difficult to do this with human power. Therefore, the need for applications that can quickly detect and respond to the positive or negative comments that people write is increasing day by day.









In information retrieval or text mining, the TfidVectorizer (also called tf-idf), is a well know method to evaluate how important is a word in a document.In this Project we use tf-idf  to convert the textual representation of information into a Vector Space Model (VSM), or we can say a sparse matrix.It is an algebraic model representing textual information as a vector, the components of this vector could represent the importance of a term (tf–idf) or even the absence or presence  of it in a document.Text is represented as a vector of numbers instead of its original string textual representation.

Process of transforming data into numeric vectors



The first step is to select the data which needs to be modelled for training the analyser.
stop words that are present in almost all documents such as a,an,the,is etc,must be removed from training data.Since they occur in almost every sentence they won't be useful at all for extracting sentiment information from the text
Further Data Preprocessing is done using regex by removing special characters, digits from our documents.
We use term-frequency to represent each term in our vector space. We determine term-frequency which is nothing more than a measure of how many times the terms present in our vocabulary.We can specify many parametrs in Tf-Idf such as Max_df(maximum Document frequency),Lowercase(for converting all characters to lowercase),max_features(specifies No of terms used in building vocabulary).
 		5.we can define the term-frequency as a couting function:

			   \mathrm{tf}(t,d) = \sum\limits_{x\in d} \mathrm{fr}(x, t)   





About Machine Learning Algorithim Used:

The machine Learning algorithim used is:

 Stochastic Gradient Descent Classifier from Scikit-Learn

Why this Particular Algorithim ? why not other commonly used algorithims such Naive-bayes,Decision tree or Logistic Regression.?

The main reason for using SGD Classifier for training our data model is that our traininind data is very large hence it is  sparse, the classifiers in this module easily scale to problems with more than 10^5 training examples and more than 10^5 features..

The estimator implements regularized linear models with stochastic gradient descent (SGD) learning: the gradient of the loss is estimated each sample at a time and the model is updated along the way with a decreasing strength schedule (aka learning rate).

This results in a better accuracy as the data backpropogates to reduce error.



Testing our Data Model:

We use scikit-learn library and calculate accuracy precision recall and f1 results for the testing data which is the other 25000 reviews

This helps us in determing how good our model has trained for Sentimental Analysis.

Also we print the confusion Matrix to determine True Positive,False Positive,True Negative and False Negative.

We can Visualize our Confusion Matrix using Matplotlib Library of Python for better Analytics of our results. 



Program:

The Program is written in Jupyter Notebook for better understanding of output linewise and is attached  in the attachment along with CSV file for Refrence.

For any Doubts/Queries regarding the program feel free to comment down and ask it.
