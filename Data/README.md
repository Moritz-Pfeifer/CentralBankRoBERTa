**Data**

This folder contains: 

1. *Raw Data*: The raw data for BIS, ECB, FED speeches in /BIS, /ECB, /FED. These speeches are publicly available and have been scraped from the [FED](https://www.federalreserve.gov/newsevents/speeches.htm), [BIS](https://www.bis.org/cbspeeches/index.htm), and [ECB](https://www.ecb.europa.eu/press/key/html/index.en.html) websites, respectively

2. *Pre-Processed Data*: The Pre_Processed files are the pre-processed Datasets. This means that the FED, BIS, ECB datasets were parsed into sentences, punctuation and common redundant strings (that stem from PDF scans) were removed. The script with which the first step of the pre-processing was done ('Pre_Processing.ipynb') is also in this folder. 

3. *Labeled Data*: For the FED, sentences were randomnized and manually labelled. For the BIS and ECB, the datasets were labelled using Pseudolabels, and include only the most confident predictions. This was done in the folder was done in the folder '[Meta_Labeling](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Meta_labelling)' Here are a couple of samples of the labels:

| Speaker           | Sentence                                                                                                            | Sentiment | Audience       |
|-------------------|---------------------------------------------------------------------------------------------------------------------|-----------|----------------|
| Michael H. Moskow | On a very practical level, we reestablished our competitiveness in financial services.                           | 1         | Financial Sector |
| Robert P. Forrestal | Continued success on the economic front depends largely on political reform namely constitutional reforms that will help restrain fiscal spending. | 0         | Government      |
| Richard W. Fisher | Our homeowners are thus less burdened with their housing predicament and better positioned as consumers.           | 1         | Households      |
| Paul A. Volcker   | Business investment has surged higher and productivity trends have shown sane signs of improvement from the poor record of the 1970s. | 1         | Firms           |
| Anthony M. Santomero | In fact, payments processing is the largest component of fed operations.                                           | NA        | Central Bank    |
