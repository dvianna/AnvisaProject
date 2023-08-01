# AnvisaProject

Building a retrieval system for the Anvisa dataset. The anvisa dataset contains 1238 documents from Anvisa, the Brazilian Health Regulatory Agency, until February 2021.

# Requirements

```pip install -r requirements.txt```


# The Anvisa Dataset

The Anvisa dataset is composed of data about irregular products recorded by Anvisa until February 2021. To build the dataset we have used the initial file ExportPortalAntigo.xlsx that, besides having details about each product, it also contains the links to the complete data on the Anvisa website. Using the links, the data was retrieved (scraper.ipnyb) using the urlib library. Then, the html was parsed (parsehtml.ipnyb) using the BeautifulSoup library. 


# Document Retrieval

To experiment with LangChain, we built a small retrieval system using the language model pucpr/biobertpt-all to generate the embeddings for each item in our dataset. Then, FAISS indexes are created using LangChain vectorestores. Now, we can use LangChain similarity_search or max_marginal_relevance_search to retrieval documents from our dataset using a customized query.
