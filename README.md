## Executive Summary

### Problem Statement
**How can we leverage natural language processing of social media posts to map natural disasters?**

Goal: Flag specific social media messages that have "Urgent Help" content and map their location.
- Identify people that need help from the urgency of their social media posts.
- Pinpoint their specific location and alert emergency response agencies.

### Data & Modeling
**Steps:**
- We collected data from Twitter's API and third-party databases (Figure Eight and Kaggle)
    - Twitter API: Data accessed within 50 miles of Mexico Beach within the week surrounding landfall of Hurricane Michael.
    - Only geolocated tweets were used for this portion of the project.
- We examined the data and manufactured our own labels for classification, based on prevelance of urgent, traumatic language. These labels were proxies for "Urgent" and "Non-Urgent". The original data was not labeled in this manner. Non-urgent language in this dataset typically came from transcribed and translated phone-calls from impoverished, developing areas after natural disasters. 
- We preprocessed our data (tokenize, lemmatize/stem) to prepare the data for classification using Bag-of-Words Natural Language Processing and Logistic Regression Classification models.

**Modeling**
- First model: Identify social media messages in urgent need of help after a natural disaster. The model could be applied to a specific location based on current maps or information regarding location of natural disaster impact. Geolocation must be enabled for flagged posts to be mapped.
- Second model: Given a time frame and radius, predict whether a disaster occured based on prevelance of "urgent help" type language. This model could provide an initial scan of broader geographic ranges for more selective deploymet of a robust natural language processing model, like model 1.

### Findings
- Social media is full of reposted, news-type or informational messages regarding natural disasters.
- Urgent messages often do not include descriptive details about the natural disaster in question.
- Models do well at learning text data associated with labeled groups. They can be applied to unrelated data and mirror similar trends. However, effectively creating proxy labels is very difficult. This results in extensive noise and decreases model effectiveness and generalizability. 


### Recommendations & Next Steps
- Disaster response organizations should partner with social media to access geolocation data during natural disasters. Without access to large geolocated datasets, models will lack the geospatial data necessary for improved model performance.
- Clustering and sentiment analyses could be used to train models to learn sentiments and language context.
- More complex NLP tools, like Neural Networks or Word2Vec, could better learn words associated with survivors in urgent need of help.
