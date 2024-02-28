## Audience Classification and Sentiment Analysis with CentralBankRoBERTa

This repository contains code to perform economic agent classification and sentiment analysis using a pretrained RoBERTa model. The code is designed to work on Google Colab and assumes that you have the required [data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) and models ([Economic Agent Model](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Agent_classification/result/RoBERTa) and [Sentiment Model](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Sentiment_classification/result/RoBERTa/checkpoint-500)) stored on your Google Drive.

### Setup

1. Mount Google Drive (if you're running the code on Google Colab):

   Make sure you are running this code in a Google Colab environment or adjust the paths accordingly if running elsewhere. If you're not on Colab or don't want to mount Google Drive, skip this step.

2. Install required libraries:

   The code uses the Huggingface Transformers library. Run the following command to install the required dependencies:

   ```bash
   !pip install transformers[torch] accelerate>=0.20.1
   ```

### Usage

   Follow the steps below to use the code:

1. Make sure you have installed the required libraries mentioned in the Setup section.

2. If you are running the code on Google Colab, mount your Google Drive by following the steps mentioned in the Setup section.

3. Copy and paste the code from [model_loader.ipynb]([model_loader.ipynb](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/blob/main/Model_loader/Model_loader.ipynb)) into your Python environment.

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

