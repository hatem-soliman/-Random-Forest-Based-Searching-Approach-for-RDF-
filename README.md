# -Random-Forest-Based-Searching-Approach-for-RDF-

Search engines retrieve requested information based on the provided keywords which is not an efficient way for rich information retrieval. Consequently, the fetching of the required information is difficult without understanding the syntax and semantics of the content. The multiple existing approaches to resolve this problem by exploiting linked data and semanticWeb techniques. Such approaches serialize the content leveraging the Resource Description Framework (RDF) and process the queries using SPARQL to resolve the problem. However, an exact match between RDF content and query structure is required. Although it improves the keyword-based search, it does not provide probabilistic reasoning to and the relationship accuracy between the query and results. In this perspective, we developed a machine learning (random forest) based approach to predict the fetching status of RDF by treating RDFs' requests as a classification problem. First, we preprocess the RDF to convert them into N-Triples format. Then, a feature vector is constructed for each RDF using the preprocessed RDF. After that, a random forest classifier is trained for the prediction of the fetching status of RDFs. The proposed approach is evaluated on an open-source DBpedia dataset. 

Overview

The overview of RFSearch for fetching status prediction of documents using RDF data as follows:
1) First, the W3C validation service is applied to documents for preprocessing.
2) Then, the features are extracted from the preprocessed documents.
3) After that, a feature vector is constructed for documents.
4) Finally, a machine learning classifier is leveraged to anticipate the fetching status of documents. RFSearch takes the constructed feature vector to the classifier as input that predicts whether the requested documents is fetched or not.

Preprocessing Steps

The each of document is preprocessed using the W3C Validation Service. To this end, collected documents are loaded by leveraging Apache Jena API (http://jena.apache.org/) to validate its syntax. After
that, the validated document is loaded into the model for the conversion of RDF serialization into RDF N-Triples format.

Feature Extraction

In a classification problem, features (predicates in our case) are usually extracted from the given dataset that can be effective in their characterization. In order to build a prediction model for a retrieval of a document, we first analyze all the given documents and extract the features (predicates) from them. After that, natural language preprocessing techniques (e.g., lemmatization) are exploited for preprocessing. Note that we leverage Python Natural Language Toolkit (NLTK - http://www.nltk.org/) for the preprocessing. lemmatization shapes the superlative and comparative words into their base-form, and Word inflection shapes the words into their singular form. Finally, we constructed a n-dimension matrix. Each row of the matrix represents a document, whereas columns of the matrix represent the features (predicates) of the document.

Training and Prediction

RFSearch leverages the random forest (RF) classification algorithm to predict the fetching status of documents. Random forest is an algorithm that builds several trees (decision
trees) for the decision. It combines the outputs decision trees to improve the abstraction ability of the model. All the decision trees are combined using the ensemble method. It integrates the weak learners (i.e., individual decision trees) to generate a strong learner.

Dataset

To evaluate RFSearch, we collect the DBpedia dataset (https://wiki.dbpedia.org/data-set-30). DBpedia 2016-10 release contains 13 billion records of information. This release contains 1.7 billion records that are extracted from the English edition of Wikipedia. We use only 1.7 billion RDF triples (English version) for the evaluation of RFSearch. Note that, we ignore all syntactically invalid triples. Moreover, we divide the data into four different search categories: triple-pattern queries having multiple results (e.g., mystery novelists and their birth addresses), extended triple-pattern queries having multiple results (e.g., novels written by famous British authors), triple-pattern queries with zero results (e.g., Hull graduates born in Agatha Christie's death place), and extended triple pattern queries with zero results (e.g., people who influenced Egyptian writers) for the evaluation of RFSearch.
