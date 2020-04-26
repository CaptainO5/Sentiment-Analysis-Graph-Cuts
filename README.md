# Sentiment Analysis - Graph Cuts
Based on **_A Sentimental Education: Sentiment Analysis Using Subjectivity  Summarization Based on Minimum Cuts_** by  Bo Pang and Lillian Lee

### Approach
##### Part 1
- Trained a MultinomialNB model on subjectivity dataset 
  - The dataset has 5000 + 5000 sentences of classes objective and subjective: sentences extracted from IMDB and Rottentomatoes respectively
- Used this Classifier to extract subjective sentences from the polarity review dataset
- Trained Naive bayes models on the extracted data and 3-fold cross validation accuracies are plotted (is in NB-NB.png)

> Code and results are in `/Subjectivity.ipynb`

##### Part 2
Instead of using a Naive bayes model to extract Subjective sentences, Graph cut based algorithm, mentioned in the paper, is used.

Values considered are 
 - T = 2
 - c = 0.5
 - f(d) = 1 / d ** 2
 
All the subjetive sentences are trained and tested on a Naive Bayes model.

###### Result...
Naive Bayes Avg. Accuracy (10-fold): __85.60__

> Code is in `/Graph_cut.ipynb`
