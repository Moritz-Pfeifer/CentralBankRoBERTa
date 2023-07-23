**Sentiment Classification**

This folder contains the [script](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/blob/main/Sentiment_classification/Sentiment_classification.ipynb) within which the different NLP models are trained for sentiment classification: 

1. BERT (Devlin et al., [2018](https://doi.org/10.48550/ARXIV.1810.04805))
2. RoBERTa (Liu et al., [2019](https://doi.org/10.48550/ARXIV.1907.11692))
3. XLNet (Yang et al., [2019](https://doi.org/10.48550/ARXIV.1906.08237))
4. FinBERT (Huang et al., [2022](https://doi.org/10.1111/1911-3846.12832))
5. TF-IDF + Naive Bayesian (Li, [2010](https://doi.org/10.1111/j.1475-679X.2010.00382.x))
6. Random Forest (Frankel et al., [2022](https://doi.org/10.1287/mnsc.2021.4156))
7. LSTM
8. Support Vector Machine (Mullen & Collier, [2004](https://aclanthology.org/W04-3253/))

These NLP models are trained to assign each sentence from our dataset a binary positive/negative label. As before, we fine-tune the LLM models by testing parameters for optimal batch size, learning rate and epochs. Warmup steps (n=500), gradient accumulation steps (n=2) and decay weight (0.01) are set equal, and dropout rates and parameter weights are on default settings. When applicable, we test for optimal parameters for the machine learning models via grid search. 
The sentiment dataset of 13,458 sentences is split into 80% (10,766) training and 20% (2,692) validation data.

The training data for these models is in the [data_input](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Sentiment_classification/data_input) subfolder. This data is identical to that in the [data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) folder. 

The fine-tuned models are saved to the [results](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Sentiment_classification/result) folder. Their accuracy scores are reported in the paper. 


