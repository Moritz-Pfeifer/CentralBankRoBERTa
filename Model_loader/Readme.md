Sure! Below is the step-by-step guide formatted for a GitHub README:

## Audience Classification and Sentiment Analysis with RoBERTa

This repository contains code to perform audience classification and sentiment analysis using a pre-trained RoBERTa model. The code is designed to work on Google Colab and assumes that you have the required data and models stored on your Google Drive.

### Setup

1. Mount Google Drive (optional, if you're running the code on Google Colab):

   Make sure you are running this code in a Google Colab environment or adjust the paths accordingly if running elsewhere. If you're not on Colab or don't want to mount Google Drive, skip this step.

2. Install required libraries:

   The code uses the Huggingface Transformers library. Run the following command to install the required dependencies:

   ```bash
   !pip install transformers[torch] accelerate>=0.20.1
   ```

### Code

The main code for audience classification and sentiment analysis can be found in the [main.py](main.py) file.

### Usage

Follow the steps below to use the code:

1. Make sure you have installed the required libraries mentioned in the Setup section.

2. If you are running the code on Google Colab, mount your Google Drive by following the steps mentioned in the Setup section.

3. Copy and paste the code from [main.py](main.py) into your Python environment.

4. Run the entire script.

### Functionality

The code performs the following tasks:

1. **Load Audience Classifier**

   The code loads the pre-trained Audience Classifier RoBERTa model along with its tokenizer. The Audience Classifier is used to classify text into specific categories (e.g., 'households', 'firms', 'financial sector', 'government', 'central bank').

2. **Load Sentiment Analysis**

   The code loads the pre-trained Sentiment Analysis RoBERTa model along with its tokenizer. The Sentiment Analysis model is used to predict the sentiment of the text (positive or negative).

3. **Define the `find_sentiment_audience` function**

   This function takes a list of sentences as input and performs audience classification and sentiment analysis on each sentence. The function returns a DataFrame containing the input sentences, their predicted audiences, audience probabilities, predicted sentiments, and sentiment probabilities.

4. **Sample Input and Output**

   After running the script, the code will prompt you to enter a sentence. Provide the sentence and press Enter. The script will then process the input sentence using the Audience Classifier and the Sentiment Analysis models. It will output the predicted audience category for the sentence and the sentiment prediction along with the probabilities.

