**Meta-Labelling**

This folder contains the script for the creation of pseudo-labels, with which we have created two additional datasets from the BIS and ECB datasets for each classifier. Pseudo-labelling is the process of adding confident predicted test data to training data (Riloff [1996](https://cdn.aaai.org/AAAI/1996/AAAI96-155.pdf); Lee [2013](https://github.com/emintham/Papers/blob/master/Lee-%20Pseudo-Label:%20The%20Simple%20and%20Efficient%20Semi-Supervised%20Learning%20Method%20for%20Deep%20Neural%20Networks.pdf)). 


1. To further fine-tune our economic agent classifier, we have created pseudo-labels for economic agents from LLM predictions with high confidence. A threshold of 77% for the BIS and 79% for the ECB was applied. As a result, 4,804 additional labels were created for the BIS and 4,051 for the ECB. Click here for the [BIS](Meta_labelling/BIS_meta_labels.ipynb) and [ECB](Meta_labelling/ECB_meta_labels.ipynb) script.

2. The training dataset for the sentiment classifier contains an 2,563 pseudo-labels generated from the ECB dataset and an additional 4,212 pseudo-labels generated from the BIS dataset, both with a threshold of 87% for confidence. [Click for the script](Meta_labelling/ECB_BIS_pseudo_sentiment.ipynb). 

