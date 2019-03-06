# NLP With GCP Natrual Language Processing API and AWS Comprehend API

By: William Gao
Colab Kernel: https://colab.research.google.com/drive/13uP__xufuhc2Fd1gSn-x8SlQHzYqIHnE

A Jupyter Notebook in my Github: https://github.com/Barneybean/NLP_natrual_language_process_GCP_AWS_textblob 

## Overview
Natural language processing (NLP) is a hot topic in machine learning. More and more use case has been developed to machine learning model to make entity identification and sentiment analysis and so on. With help from AWS and GCP, companies no longer require a developer to write complex models on NLP, instead, we can simply call the APIs and get the job done with reasonably low cost. In this report, I am going to show how to start using NLP API with AWS and GCP. 
Highlights and Procedures
Highlight: 
1.	Set up environment for API in command line can be difficult. The process involves some tweak. 
2.	The syntax in GCP NLP API for command line set up in environment does not always work so it requires some engineering. 
I had to use following code to set GCP credentials
os.environ["GOOGLE_APPLICATION_CREDENTIALS"]="/content/gdrive/MyDrive/Colab Notebooks/Credentials/flowerautoml-df46bea0c0ef.json" 
 
## Procedures
1.	Install boto3 and google-cloud-language
2.	Set up NLP API in AWS accounts and GCP accounts then download credentials 
3.	Set up AWS and GCP functions that calls for NLP APIs
4.	Ingest Google Review data and perform sentiment analysis. There are other services available but I am going with sentiment analysis for now because it is useful in operation. 
 
5.	Then I compared the sentiment analysis from the two cloud-services and the original sentiment analysis done by textblob library and I personally think is more accurate for this dataset. The identical ratio in (number of identical result/total results)
GCP sentiment vs. original sentiment = 66%
AWS sentiment vs. original sentiment = 66%
GCP vs. AWS = 66%

## Conclusions
1.	AWS and GCP natural language API are fairly fast and easy to use. But the set up can be tough. One set up process is handled correctly, a business will greatly benefit from it. 
2.	There is still room for improvement on the accuracy in sentiment analysis form the two cloud-services but I might be wrong. An accuracy audit is recommended if the API is used in mass production. 
