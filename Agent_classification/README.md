**Audience Classification**

This folder contains the [script](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/blob/main/Audience_classification/Audience_classification.ipynb) within which the different NLP models are trained for audience classification: 

1. BERT (Devlin et al., [2018](https://doi.org/10.48550/ARXIV.1810.04805))
2. RoBERTa (Liu et al., [2019](https://doi.org/10.48550/ARXIV.1907.11692))
3. XLNet (Yang et al., [2019](https://doi.org/10.48550/ARXIV.1906.08237)) 

These LLMs are trained to assign each sentence from our dataset to one of five economic groups: *Households, Firms, Financial Sector, Government* and *Central Bank*. We fine-tune these models by testing parameters for batch size, learning rate (LR) and epochs. Manual testing has yielded the hyperparameters in Fig. 2 to be optimal. Warmup steps (n=500), gradient accumulation steps (n=2) and decay weight (0.01) parameters are set equal for all models. To increase the batch size and still be able to fit higher batch sizes into memory, we add gradient accumulation steps (GAS) to our model. Dropout rates and parameter weights are left at the default settings.
The economic agent dataset of 15,060 sentences is split into 80% (12,048) training and 20% (3,012) validation data. 

The training data for these models is in the [data_input](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Audience_classification/data_input) subfolder. This data is identical to that in the [data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) folder. 

The fine-tuned models are saved to the [results](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Audience_classification/result) folder. Their accuracy scores are reported in the paper. 


