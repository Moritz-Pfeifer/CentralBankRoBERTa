<table>
  <tr>
    <td><img src="https://i.postimg.cc/8cTxrBYX/Central-Bank-Ro-BERTa-logos-black.png" width="250" height="250"> </td>
    <td>
      <h1 style="font-size: 36px; font-weight: bold; margin: 0;">CentralBankRoBERTA</h1>
      <p style="font-size: 18px; margin: 0;">A large language model for analyzing central bank communications</p>
    </td>
  </tr> 
</table>

Central bank communications are an important tool for guiding the economy and fulfilling monetary policy goals. Natural language pro-cessing (NLP) algorithms have been used to analyze central bank communications, but they often ignore context. Recent research has introduced deep-learning-based NLP algorithms, also known as large language models (LLMs), which take context into account. This study applies LLMs to central bank communications and constructs CentralBankRoBERTa, a state-of-the-art economic agent classifier that distinguishes five basic macroeconomic agents (households, firms, banks, the government and the central bank itself) and binary sentiment classifier that identifies the emotional content of sentences in central bank communications. Here we release our data, models, and code.


● [Data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) 

The training data of speeches from the Fed, the ECB and the BIS are in this folder. Overall we have collected 19,381 speeches. To train our audience classifier, we have labelled we labeled 6,205 randomized sentences from the Fed database as speaking either about households, firms, the financial sector, the government, or the central bank itself. To train our sentiment classifier, we have labelled 6,683 sentences from the Fed database, which are either labeled as being positive (1) or negative (0). 

● [Meta-labelling](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Meta_labelling)

The scripts and methodology for generating additional meta-labels. 

● [Audience classification](https://github.com/Moritz-Pfeifer/FED-Communications-Project/tree/main/Data_mining)

The script testing different large language such as BERT (Liu et al., [2019](https://github.com/your-username/CentralBankRoBERTA)), XLNET (Yang et al., [2019](https://doi.org/10.48550/ARXIV.1906.08237)) and FinBERT (Huang et al. [2022](https://doi.org/10.1111/1911-3846.12832)) for our economic agents classification task. 

● [Sentiment classification](https://github.com/Moritz-Pfeifer/FED-Communications-Project/tree/main/Data_mining)

The tools for collecting the data and setting up the databse itself can be found in the Data Mining folder. Support Vector Machine (SVM), Random Forest, and a two-step TF-IDF and Naïve Bayes (NB)

