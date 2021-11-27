# -Random-Forest-Based-Searching-Approach-for-RDF-

Search engines retrieve requested information based on the provided keywords which is not an efcient way for rich information retrieval. Consequently, the fetching of the required information is difficult without understanding the syntax and semantics of the content. The multiple existing approaches to resolve this problem by exploiting linked data and semanticWeb techniques. Such approaches serialize the content leveraging the Resource Description Framework (RDF) and process the queries using SPARQL to resolve the problem. However, an exact match between RDF content and query structure is required. Although it improves the keyword-based search, it does not provide probabilistic reasoning to
and the relationship accuracy between the query and results. In this perspective, this paper proposes a machine learning (random forest) based approach to predict the fetching status of RDF by treating RDFs' requests as a classication problem. First, we preprocess the RDF to convert them into N-Triples format. Then, a feature vector is constructed for each RDF using the preprocessed RDF. After that, a random forest classier is trained for the prediction of the fetching status of RDFs. The proposed approach is evaluated on
an open-source DBpedia dataset. The 10-fold cross-validation results indicate that the performance of the proposed approach is accurate and surpasses the state-of-the-art.
