# Sentiment analysis on OnePlus Nord 2 reviews extracted from amazon

### **Sentiment analysis:**

[<img width = "450px" height = "450px" src = "https://user-images.githubusercontent.com/71897685/149979701-c9c881fb-a0cc-4793-99d9-f2b83fd31ae3.jpg"/>](https://www.amazon.in/OnePlus-Nord-Sierra-128GB-Storage/dp/B097RDVDL2/ref=cm_cr_arp_d_product_top?ie=UTF8)



Sentiment analysis is used to find out what people thinks about product? and to find out their emotions toward that product. 

It also helps to find out what kind of problems people are facing with product, because the negative review is almost full with those things and this is useful for company to make changes or consider those factors in their new products.

### Reviews Extraction:

**BeautifulSoup** 🥣 is used for extraction of reviews from amazon websites alone with **urllib and request** library.
The reviews are extracted and saved in text file at interval of 50 review, so that even if the program get crashed or something happened. The extraction will begin from the point where it is stopped. so it will save time. The extraction program is saved in [web_scrapping_text_file_writing.py](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/c2d0106704487353044ff85627e1fb9f774a2032/web_scrapping_text_file_writing.py) and The extracted text file is [reviews_cleaned.txt](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/c2d0106704487353044ff85627e1fb9f774a2032/reviews_cleaned.txt). 

The 5100 reviews get extracted but after cleaning there are 4813 reviews.

### Data Cleaning:

The data cleannning process involves :
- Removing Extra whitespaces and tabs and newlines
- Correcting the format i.e adding space if necessary.
- Removing emojis
- Removing websites and hashtags.
- Removing reviews that are in other languages.
- Removing Media files. 
- Removing blanck lines or blank reviews
- etc etc.

I used the **Regular expression, nltk and spacy** for cleanning the data and for further text analysis

After all cleaning and The Lemmatization is applied

So we have unlabeled data i used sentiment lexicons, that assign the numerical values based on presence of positive and negative words in the review and the i encode those numerical values as **Positive, Neutral and Negative** 

After all these processes the dataset looks like ([oneplus_labeled_data_oversampled.csv](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/8a0b3ede3f1a025e1d527e67af383c3bd82310d2/oneplus_labeled_data_oversampled.csv)): 
> <img width = "480px" height = "400px" src = "https://user-images.githubusercontent.com/71897685/149990796-7ba11cbc-4528-4cd5-8962-996aef8be4c9.png"/>

### Exploratory Data analysis:
Various techniques and method are used to get more insides about dataset like:
1. WordCloud
2. Word Counts
3. N-gram methods 

![2](https://user-images.githubusercontent.com/71897685/149992233-ced8ac50-a419-4beb-9442-2c776974f02a.png)

and Word Count plot

![6](https://user-images.githubusercontent.com/71897685/149992370-0528d72e-e4d6-4a6b-892c-21cb3630f7c0.png)



The dataset is unbalanced, so I tried one model to see how it behaves but i found that i need to apply balancing method. So i used ***RandomOverSampling***. This method created duplicates to balance the dataset. 

**For More detail about EDA and Data Cleanning please refer [Sentiment_analysis_EDA.ipynb](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/9e47d8d852c3885dd3812cdb490dde13954811a7/Sentiment_analysis_EDA.ipynb)**

### Model Creation:

Atlast this is classification problem, so I used different classifiers with different Embedding techniques.

Embedding Techniques used in Models:
1. Bag of Words.
2. CountVectorizer
3. TF-IDF
4. Word Embedding (Neural network)

Models used:
1. Logistic Regression
2. Naive Bayes.
3. Support Vector Machine
4. Decision tree based Models
5. RNN
6. LSTM


For More info please refer to:

> [Sentiment_analysis_Logistic.ipynb](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/b18a61575c0c44978cf8e6023ba1d1cd06afbe50/Sentiment_analysis_Logistic.ipynb)

> [Sentiment_analysis_neural_models.ipynb](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/b18a61575c0c44978cf8e6023ba1d1cd06afbe50/Sentiment_analysis_neural_models.ipynb)

> **NOTE - I am currently working on this project, so Neural Network models are Incomplete except those are mentioned here**


