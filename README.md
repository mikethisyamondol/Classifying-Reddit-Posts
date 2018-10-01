## TL;DR (Executive Summary):

The idea of this project is to pull in posts from different sub-Reddits (LifeProTips vs. UnethicalLifeProTips) and build different classification models to be able to distinguish each post between subreddits.The classification models used in this project were: Multinomial Naive Bayes, Logistic Regression, Random Forest Classifier, Extra Trees Classifier, AdaBoost Classifier, and last but not least the Voting Classifier to tie everything together.
<br>
Initial thoughts: This will be extremely difficult to do. A lot of the posts contain sarcasm that even some humans (i.e. myself) have a hard time detecting, but I think it would be interesting to see what the results are.
<br>
Here are a few things we can look at:
<br>
- Checking the classifcation accuracy and sensitivity (False positives are more detrimental) scores. 
- Taking a look at the .predict_proba to see if the classifications are done close to the 50% probability mark, or if the classifications are more definitive on average (how confident is the model?). 
- Have the model predict results for the ShittyProLifeTips subreddit to see if it thinks these posts are closer to the LifeProTips or UnethicalLifeProTips subreddits

### Results:
<br>
The Voting Classifier that takes into account the "votes" of each model passed into it performed the best (but marginally). Wanted to note that the voting clasasifier does not include the Logistic Regressions.


<br>
*If you are looking to replicate this, I'd recommend selecting subreddits that are less similar in nature.
