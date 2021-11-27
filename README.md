# -Random-Forest-Based-Searching-Approach-for-RDF-

Search engines retrieve requested information based on the provided keywords which is not an efficient way for rich information retrieval. Consequently, the fetching of the required information is difficult without understanding the syntax and semantics of the content. The multiple existing approaches to resolve this problem by exploiting linked data and semanticWeb techniques. Such approaches serialize the content leveraging the Resource Description Framework (RDF) and process the queries using SPARQL to resolve the problem. However, an exact match between RDF content and query structure is required. Although it improves the keyword-based search, it does not provide probabilistic reasoning to
and the relationship accuracy between the query and results. In this perspective, we developed a machine learning (random forest) based approach to predict the fetching status of RDF by treating RDFs' requests as a classification problem. First, we preprocess the RDF to convert them into N-Triples format. Then, a feature vector is constructed for each RDF using the preprocessed RDF. After that, a random forest classifier is trained for the prediction of the fetching status of RDFs. The proposed approach is evaluated on
an open-source DBpedia dataset. 

The overview of RFSearch for fetching status prediction of documents using RDF data as follows:
 First, the W3C validation service is applied to documents for preprocessing.
 Then, the features are extracted from the preprocessed documents.
 After that, a feature vector is constructed for documents.
 Finally, a machine learning classifier is leveraged to anticipate the fetching status of documents. RFSearch takes the constructed feature vector to the classifier as input that predicts whether the requested documents is fetched or not.
