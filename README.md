# Clustering_topic_modeling

This was for a homework assignment for my Unstructed Data Analytics class at Carnegie Mellon. 

Objective: This project consists of two sections. 
1.)Perform clustering of emails from Enron Email dataset to determine groups of emails that appear to be spam or non-spam. 
2.)Perform topic modeling for android apps based on type of permissions they require (gps location, camera access, sound, etc.)

Method: For part 1, I loaded 5,000 emails and cleaned the data using a TF-ID vectorizer to tokenize the words and return a document matrix. Gaussian Mixture Model (GMM) was used to peform clustering on the emails and predict which cluster emails should be placed in. To check if the clusters made sense, I choose some words I thought would appear in spam emails, such as, "click", "free", "www." and saw the probability of those words appearing in each cluster. For 1 cluster, the probabilities of these words appearing were high, which indicates that cluster was for spam emails. 

For part 2, I loaded data from 180,000 android apps and the phone permissions they required (173 types of permissions). Latent Dirichlet Allocation (LDA) was used to under the latent topics that appear based on permissions. After running LDA, I displayed the permission names that had the highest probability of appearing in each topic to qualitatively assess the topics. I saw that distinct topics were formed that grouped together apps with permissions for camera and modify storage, while other topics had apps with permissions for phone call and network communications. 

