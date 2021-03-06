# Sentiment-Analysis
## Analysis of parent comments clusters with an anomalous sarcastic response

The Sarcasm on Reddit dataset provides comments posted on Reddit labeled as sarcastic (1) or not sarcastic (0). The project goal is, given only the parent comment in a specific subreddit, identify parent comment clusters that receive an amount of sarcastic comments that deviate from the subreddit average. The project then focuses on document clustering, topic detection, and keyword ex- traction.

### References
• Dimo Angelov, Top2Vec: Distributed Representations of Topics, [link](https://arxiv.org/abs/2008.09470)

• Grootendorst Maarten, BERTopic, [link](https://github.com/MaartenGr/BERTopic)

• Grootendorst Maarten, Keyword Extraction with BERT, [link](https://towardsdatascience.com/keyword-extraction-with-bert-724efca412ea)

• L. McInnes, J. Healy, S. Astels, hdbscan: Hierarchical density based clus- tering In: Journal of Open Source Software, The Open Journal, volume 2, number 11. 2017, [link](https://www.theoj.org/joss-papers/joss.00205/10.21105.joss.00205.pdf)

• McInnes, L, Healy, J, UMAP: Uniform Manifold Approximation and Pro- jection for Dimension Reduction, [link](https://arxiv.org/abs/1802.03426)

• Universal Sentence Encoder, [link](https://arxiv.org/abs/1803.11175)

### Research question and methodology
The research question is whether it is possible to identify parent comment clus- ters in which the mean of sarcastic responses exceeds the subreddit mean. 
The methodology is based on the references cited. In order to work with textual data, parent comments are transformed into vectors using the Universal Sentence Encoder. Then with UMAP the dimensionality of the data is reduced from 512 dimensions to just 5 dimensions. The reason for the reduction is to be able to use HDBSCAN as a clustering algorithm. Once the clusters are identified, the intra-cluster mean of the label variable is calculated to identify the clusters with the most sarcastic responses and consequently the topics that attract the most sarcastic responses.
