<H3>ENTER YOUR NAME: NIVETHA.K</H3>
<H3>ENTER YOUR REGISTER NO.212222230102</H3>

<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.

<H3>Program:</H3>
```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)
```

<H3>Output:</H3>

![image](https://github.com/NivethaKumar30/Project-Based-Experiment-AAI/assets/119559844/afe15368-bcc4-4905-a7c7-89636031987f)

<H3>Inference:</H3>
Thus, the sentiment analysis using your Facebook data is done and filtering the data that has only negative feedback for the code is done.
