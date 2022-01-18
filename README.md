# Sentiment analysis on OnePlus Nord 2 reviews extracted from amazon

### Sentiment analysis:

[<img width = "450px" height = "450px" src = "https://user-images.githubusercontent.com/71897685/149979701-c9c881fb-a0cc-4793-99d9-f2b83fd31ae3.jpg"/>](https://www.amazon.in/OnePlus-Nord-Sierra-128GB-Storage/dp/B097RDVDL2/ref=cm_cr_arp_d_product_top?ie=UTF8)



Sentiment analysis is used to find out what peoples thinks about product and to find out their emotions toward that product. 

It also helps to find out what kind of problems people are facing with product, because the negative review is almost full with those things and this also make useful for that company to make or consider those factors in their new products.

#### Reviews Extraction:

**BeautifulSoup** 🥣 is used for extraction of reviews from amazon websites alone with **urllib and request** library.
The reviews are extracted and saved in text file at interval of 50 review, so that even if the program get crashed or something happened, The extraction will begin from the point where it is stopped. so it will save time. The extraction program is saved in [web_scrapping_text_file_writing.py](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/c2d0106704487353044ff85627e1fb9f774a2032/web_scrapping_text_file_writing.py) and The extracted text file is [reviews_cleaned.txt](https://github.com/piyumaha12/Sentiment_analysis_on_amazon_review/blob/c2d0106704487353044ff85627e1fb9f774a2032/reviews_cleaned.txt). The 5100 reviews get extracted but after cleaning there are 4813 reviews.

#### Data Cleaning:

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
