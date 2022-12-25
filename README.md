

**NLP Final Term Project**

**Tex t Summarizer Tool**

Team 1:

Gregorio Losa | Frederick Tantowi | Laurensia Gono





Executive Summary

**Business Use Case**

**Dataset Specifications**

● Create a text summarizer tool

● For executives, professionals, or

individuals interested in the financial

industry

● Provide a condensed version of a full

article or report in 4 succinct

sentences

●

●

●

●

**Dataset:** webhose\_citigroup

**Source:** webz.io

**Format:** JSON file

**Specifications:**

○ 11,358 articles

○ Details of companies’ activities,

stock market performances and

financial reports related to

Citibank

● Example:

○ Earnings call every quarter has

lots of notes and reports. These

can be summarized to save

time and focus on the main

points.

○ Variables include source, author,

title, and url

2





**Implementation Roadmap**

01

02

03

04

Data Preprocessing

Topic Modeling

Text Summarizer

Taxonomy

● **Data Reduction**

● **Gensim**

● **LexRank**

● **Semantic Similarity**

○ Deduplication (LSH

MinHash):

○ Transform data to

bigrams and trigrams

○ Id2word and corpus

○ Evaluated using

perplexity and

○ Summarized into 4

**Classifier**

sentences

○ Take keywords and

11,358 → 9,277 articles

● **Data Cleaning**

put it into a

taxonomy category

under an umbrella

topic

○ Remove stopwords, emails,

white space, punctuations

(incl. single quotation

marks), and new line

characters

coherence

○

Use the taxonomy to

● **Scikit-Learn**

○ Vectorization

○ Evaluated using

perplexity

classify the

summarized text into

a labeled topic

● **Data Transformation**

○ Tokenization

○ Lemmatization (SpaCy)

3





**Gensim Topic Modeling Results**

4





**Scikit-Learn Topic Modeling Results**

5





**Final Results**

Scikit Learn was the

best performing model

25 Topics

15 Keywords / Topic

6





**Final Results**

**Text Summarizer**

**LexRank**

● A graph-based unsupervised method for

automatically summarizing text

● Computes sentence importance based on the

concept of eigenvector centrality in a graph

representation of sentences

● It uses similarity metrics in addition to the

pageRank method (TextRank)

● Considers where sentences go and how long

they are

● Use for Multi-document summarization

● Maintains redundancy

● Improves coherency

**Graphical Approach**

●

●

Based on Eigen Vector Centrality.

Sentences are placed at the vertexes of the

Graphs

The weight on the Edges are calculated using

cosine similarity metric.

●

●

Where S are the sentences at the vertices

i

respectively and W are weights on the edges.

ij

7

*LexRank method for Text Summarization*. (2019, December 5). OpenGenus IQ: Computing Expertise & Legacy. <https://iq.opengenus.org/lexrank-text-summarization/>





**Final Results**

**Text Summarizer**

8





**Final Results**

**Taxonomy**

**Sklearn**

9





**Evaluation Metrics**

**Eyeballing Methods:**

**Intrinsic Evaluation Metrics:**

**Perplexity**

**Clusters**

● Gensim: -5.799

● First Scikit Learn: 317.98

● Second Scikit Learn: 262.49

● Eyeballed the clusters

of our LDA models

**Top N words**

● Read the top 15

keywords

**Coherence**

● Gensim: 0.44

● Scikit Learn: Not built in

1

0





**Future Considerations**

**Taxonomy**

Add more relevant keywords see if there's

better classification terms

1

**Scikit Learn**

2

3

Develop coherence score for sklearn lda

model

**Gensim**

Optimise gensim to have the same no. of

clusters as Sklearn and compare the results

based on evaluation criteria

11





**Thank You**

**Any Questions?**

Team 1:

Gregorio Losa | Frederick Tantowi | Laurensia Gono

