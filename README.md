# SMS-Spam-Detection

I built this project to tackle the classic problem of mobile spam. We’ve all gotten those annoying "winner" texts; this is my attempt at using Machine Learning to filter them out before they even reach a user.

Why I built it this way:
I used the Multinomial Naive Bayes algorithm because it’s a powerhouse for text classification. It’s fast, efficient, and handles word counts much better than more complex models for this specific task.

One thing I realized during the process is that data cleaning is 90% of the work. I had to drop unnecessary columns (like those 'Unnamed' ones in the CSV) and map the labels to numbers so the computer could actually process them.

The Technical Workflow:
Exploratory Data Analysis (EDA): I visualized the distribution of 'ham' vs 'spam' using Seaborn to understand the class imbalance.

Text Processing: I used TfidfVectorizer to convert raw text into a numerical format. This is better than simple word counting because it penalizes common words (like "the") and rewards "signature" words that actually identify spam.

Modeling: Split the data (70/30) and trained the classifier.

Evaluation: I didn't just look at accuracy. I generated a full Classification Report and a Confusion Matrix to see exactly where the model was getting confused.

Key Stats
Accuracy: ~96%
Unique Words in Corpus: 15,585
Average Message Length: 15 words

How to use this:
Open the .ipynb file in Google Colab.

Make sure you have your spam.csv file ready (I loaded mine via Google Drive).

Run the cells to see the visualizations and the final performance metrics.

Lessons Learned
The model is great at catching "ham," but it’s interesting to see where it misses spam. In the future, I might try adding "Stemming" or "Lemmatization" to see if reducing words to their roots helps the model generalize even better.


