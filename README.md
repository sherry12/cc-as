# Comp5349 Assignment - Text Corpus Analysis
This assignment implement a spark application to analysis words in MultiNLI which contains 2 parts. One is vocabulary exploration and the other is sentence vector exploration. We implemented it by Python and pyspark and use AWS EMR and Jupyter notebook to run and test the results.

Here are the AWS environment setting instructions.
## Create EMR Cluster
- In Step1:  
  Release : emr-5.29.0;  
  Choose Hadoop2.8.5, spark2.4.4, Livy0.6.0, Tensorflow1.14.0  
  Enter configuration:  [{"classification":"spark","properties":{"maximizeResourceAllocation":"true"}}]
  
- In Step2:  
  Use either m4.large or m4.xlarge with at least 1 master node and 1 core node  

- In Step3: 
  Change cluster name to a readable name
  Bootstrapping Action:  
    sudo python3 -m nltk.downloader -d /usr/local/share/nltk_data all  
    sudo pip-3.6 install --quiet tensorflow-hub  
    sudo pip-3.6 install --quiet matplotlib  

- In Step4:
  Choose your own key value pair
  
## Create Jupyter Notebook  
- Choose the cluster that we create before and choose a location to store your notebook log

In our assignment, we use our own S3 storage path. Hence, if you would like to run it on your own environment, please change the path to your own path.
