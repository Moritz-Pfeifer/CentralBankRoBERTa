<table>
  <tr>
    <td><img src="https://i.postimg.cc/HLqPqkyk/Central-Bank-Ro-BERTa-logos-black.png" width="250" height="250"> </td> 
    <td>
      <h1 style="font-size: 36px; font-weight: bold; margin: 0;">CentralBankRoBERTa</h1>
      <p style="font-size: 18px; margin: 0;">A Fine-Tuned Large Language Model for Central Bank Communications</p>
    </td>
  </tr>  
</table>

Central bank communications are an important tool for guiding the economy and fulfilling monetary policy goals. Natural language pro-cessing (NLP) algorithms have been used to analyze central bank communications, but they often ignore context. Recent research has introduced deep-learning-based NLP algorithms, also known as large language models (LLMs), which take context into account. We apply LLMs to central bank communications and construct **CentralBankRoBERTa**, a state-of-the-art economic agent classifier that distinguishes five basic macroeconomic agents (households, firms, banks, the government and the central bank itself) and binary sentiment classifier that identifies the emotional content of sentences in central bank communications. A detailed discussion on the motivations and results for this model can be found in Pfeifer, M. and Marohl, V.P. (2023) "CentralBankRoBERTa: A Fine-Tuned Large Language Model for Central Bank Communications" ADD SOURCE/LINK. Here we release our data, models, and code. 

● [Data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) 

The training data of speeches from the Fed, the ECB and the BIS are in this folder. Overall, we have collected 19,381 speeches. To train our economic agents classifier, we have labeled we labeled 6,205 randomized sentences from the Fed database as speaking either about households, firms, the financial sector, the government, or the central bank itself. To train our sentiment classifier, we have labelled 6,683 sentences from the Fed database, which are either labeled as being positive (1) or negative (0). 

* 🤗 The Huggingface 🤗 dataset card for the pre-labeled datasets can be found [here](https://huggingface.co/datasets/Moritz-Pfeifer/CentralBankCommunication)

● [Meta-labelling](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Meta_labelling)

The scripts and methodology for generating additional meta-labels. 

● [Economic agent classification](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/agent_classification)

This folder contains the script testing different large language models such as BERT (Devlin et al., [2018](https://doi.org/10.48550/arXiv.1810.04805)), XLNET (Yang et al., [2019](https://doi.org/10.48550/ARXIV.1906.08237)), FinBERT (Huang et al. [2022](https://doi.org/10.1111/1911-3846.12832)) and RoBERTa (Liu et al., [2019](
https://doi.org/10.48550/arXiv.1907.11692)) for our economic agents classification task. 

● [Sentiment classification](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Sentiment_classification)

The script testing different large language models (BERT, FinBERT, XLNET and RoBERTa) and and machine learning models such as Support Vector Machine (SVM), Random Forest, and a two-step TF-IDF and Naïve Bayes (NB) model on our sentiment classification task are in this folder. 

● [Model loader](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Model_loader)

Go to this folder if you want to use CentralBankRoBERTA for your own analysis of central bank communications. Both the economic agents classifier and the sentiment classifier and a step-by-step guide for implementation are in here.

* 🤗 The Huggingface 🤗 pipeline for both models can be found here:
  * [AgentClassifier](https://huggingface.co/Moritz-Pfeifer/CentralBankRoBERTa-agent-classifier)
  * [SentimentClassifier](https://huggingface.co/Moritz-Pfeifer/CentralBankRoBERTa-sentiment-classifier)


<p align="center">☆☆☆</p>


<table>
  <tr>
    <td colspan="2" style="border-top: 1px solid #ccc; padding: 5px; text-align: center;">
      Please cite this model as Pfeifer, M. and Marohl, V.P. (2023) "CentralBankRoBERTa: A Fine-Tuned Large Language Model for Central Bank Communications". <em>Journal of Finance and Data Science </em> (forthcoming) https://doi.org/10.1016/j.jfds.2023.100114
    </td>
  </tr>
  <tr>
    <td style="padding: 5px;">
      Moritz Pfeifer<br>
      Institute for Economic Policy, University of Leipzig<br>
      04109 Leipzig, Germany<br>
      <a href="mailto:pfeifer@wifa.uni-leipzig.de">pfeifer@wifa.uni-leipzig.de</a>
    </td>
    <td style="padding: 5px;">
      Vincent P. Marohl<br>
      Department of Mathematics, Columbia University<br>
      New York NY 10027, USA<br>
      <a href="mailto:vincent.marohl@columbia.edu">vincent.marohl@columbia.edu</a>
    </td>
  </tr>
</table>







