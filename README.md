# REPORT
## Overview

The dataset [here](https://drive.google.com/file/d/1womRkJ-pf1XJyXtv-caGYH2jWMG0L_v3/view?usp=sharing) is contained a file called email_campaigns.pkl. I analysed the file to extract insights from this using NLP.

## Steps:

### 1. Data Analysis

- Load the .pkl data into a Pandas DataFrame.
- Performed basic EDA checks like df.head(), .info(), .describe(), .isnull().sum() for better understanding the dataset.
- Converted the .pkl file to .csv and .json for the convenience of performing operations and personally visualizing the data better.
- Load the JSON data into a Pandas DataFrame.
- Extract relevant features from the JSON structure (e.g., subject, body).
- Convert categorical variables (like boolean flags) into numerical values.

### 2. Machine Learning (NLP)

I used Natural Language Processing (NLP) techniques to analyze a collection of email subjects using the NLTK (Natural Language Toolkit) library in Python. The process can be dissected into several intricate steps:

- Stopword Removal:
Utilizes the NLTK library's stopwords module to download a set of common English stopwords.
Stopwords are linguistically inconsequential words (e.g., "the," "and," "is") that are often removed to focus on more meaningful content.

- Text Compilation:
Assembles all email subjects into a cohesive text string for further processing.

- Tokenization:
Employs the NLTK's word_tokenize function to break down the combined text into individual tokens (words). Tokenization is the foundational step in preparing text for analysis.

- Filtering:
Removes stopwords and non-alphabetic words from the tokenized list. Converts words to lowercase to ensure consistency.

- Frequency Distribution:
Constructs a frequency distribution of the filtered words. The frequency distribution captures the occurrences of each unique word in the dataset.

- Top Words Extraction:
Identifies and prints the top 10 words based on their frequency in the dataset. These top words offer insights into the most common and potentially significant terms within the email subjects.


# Note:
- I performed EDA only on the 'example1' column as a demonstration of how we can derive valuable insight.

Result:

![6b7cddae-a830-453e-b4d4-8be0b368c4a5](https://github.com/kevnantony/Email-Engagement-Analysis/assets/76067692/de6d6314-7b69-4878-b517-18246173f293)

- These are the top words used to get the ['Open'= True] with respect to the 'subject' in the above dataset. The exact similar process could be done for getting an analysis of what prompted the users to book a meeting (i.e. 'meeting link clicked': True) or (respond i.e. 'responded': True) by subsituting these for 'Open' in the above program and 'body' instead of 'subject' going by the logic that users tend to respond or click the meeting link only if they are interested.




