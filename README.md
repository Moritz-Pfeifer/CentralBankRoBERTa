<table>
  <tr>
    <td><img src="https://i.postimg.cc/63NfP4jK/Central-Bank-Ro-BERTa-logos-black.png" width="250" height="250"> </td>
    <td>
      <h1 style="font-size: 36px; font-weight: bold; margin: 0;">CentralBankRoBERTA</h1>
      <p style="font-size: 18px; margin: 0;">A large language model for analyzing central bank communications</p>
    </td>
  </tr>
</table>

Central bank communications are an important tool for guiding the economy and fulfilling monetary policy goals. Natural language pro-cessing (NLP) algorithms have been used to analyze central bank com-munications, but they often ignore context. Recent research has introduced deep-learning-based NLP algorithms, also known as large language models (LLMs), which take context into account. This study applies LLMs to central bank communications and constructs CentralBankRoBERTa, a state-of-the-art economic agent classifier that distinguishes five basic macroeconomic agents (households, firms, banks, the government and the central bank itself) and binary sentiment classifier that identifies the emotional content of sentences in central bank communications. Here we release our data, models, and code.

Data

● [Data](https://github.com/Moritz-Pfeifer/CentralBankRoBERTa/tree/main/Data) 

The tra data (sector-specific interest rate differentials, productivity and Taylor rules) are in this folder.

● [Data Analysis](https://github.com/Moritz-Pfeifer/FED-Communications-Project/tree/main/Data_analysis)

The tools for analyising the data including the tone analysis and econometric model can be found in this folder. 

● [Data Mining](https://github.com/Moritz-Pfeifer/FED-Communications-Project/tree/main/Data_mining)

The tools for collecting the data and setting up the databse itself can be found in the Data Mining folder.
