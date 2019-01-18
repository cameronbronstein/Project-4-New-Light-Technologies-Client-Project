## Executive Summary

### Problem Statement
**How can we leverage social media messages to map natural disasters?**

Goal: Map specific areas that need assistance

- Identify people that need help
- Pinpoint their specific location

### Data & Modeling
**Steps:**

- We collected data from Twitter's API and third-party databases (Figure Eight and Kaggle)
- We examined the data and manufactured our own labels for classification
- We preprocessed our data (tokenize, lemmatize/stem) to prepare the data for NLP

**We built two models:**

- First model: Identify between people in urgent need of help after a natural disaster and those whose needs are not as urgent based on a social media message
- Second model: Given a time frame and a location's radius, predict whether a disaster occured based on tweet messages

### Findings
- Models do well at learning text data associated with labeled groups. They can be applied to unrelated data and mirror similar trends


### Recommendations & Next Steps
- Disaster response organizations should partner with social media to access geolocation data during natural disasters 
- Clustering and sentiment analysis on messages to train machines to learn sentiments and language context
