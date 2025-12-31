# SMS-Spam-Detection
An NLP-driven security engine designed to identify and mitigate mobile messaging threats. By leveraging Multinomial Naive Bayes and TF-IDF vectorization, this system classifies incoming SMS data into "Ham" or "Spam" with high precision, protecting users from phishing and unsolicited marketing.

Why this is different
Most basic tutorials just throw a model at the data and call it a day. In this repo, I focused heavily on the text cleaning pipeline. SMS data is messy—it has slang, abbreviations, and weird punctuation. I spent a lot of time on the preprocessing stage to make sure the model wasn't just memorizing words but actually picking up on spam patterns.

The Tech Stack
Language: Python 3.x

Libraries: Scikit-learn, Pandas, NLTK (for the heavy lifting on text)

Algorithm: Multinomial Naive Bayes (chosen for its speed and efficiency with text counts)

Vectorization: TF-IDF (because some words like "the" are useless, while "win" or "urgent" are huge red flags)

How it works

The Math: I used a TF-IDF Vectorizer to turn the text into a matrix of numbers that the computer can actually understand.

The Prediction: The Naive Bayes model calculates the probability of a message being spam based on the word frequencies it saw during training.

Results
The model hits an accuracy of about 98%. However, I focused more on the Confusion Matrix to ensure I wasn't accidentally marking "Ham" as "Spam"—because missing a text from your mom is worse than seeing one ad for a fake cruise.
