# NFL-Fantasy-Helper
Cloud Computing Project - Data Analysis | Apache Spark Framework, Hadoop Distributed File System, Google Cloud Platform

Use the following commands on a VM. 

1. cd project (or you can call it whatever you would like to)
2. mkdir events
3. mkdir nbs
4. vim docker-compose.yml (Copy contents from my docker-compose.yml file)
5. vim hadoop.env (Copy contents from my hadoop.env file)
6. cd nbs
7. Upload data files - Career_Receiving_Stats.csv, Career_Stats_Rushing.csv, Career_Stats_Passing.csv.
8. sudo chmod -R 777 nbs/
9. docker-compose up -d
10. To upload the data files into HDFS run the following (Ensure to substitute <container_id> with the namenode container ID):
    docker ps
    docker exec <container_id> hdfs dfs -put /home/nbs/Career_Receiving_Stats.csv /Career_Receiving_Stats.csv
    docker exec <container_id> hdfs dfs -put /home/nbs/Career_Stats_Rushing.csv /Career_Stats_Rushing.csv
    docker exec <container_id> hdfs dfs -put /home/nbs/Career_Stats_Passing.csv /Career_Stats_Passing.csv

Now you can access HDFS web interface through: http://external_ip/explorer.html
Now you can access the project application on Jupyter Notebook via: http://external_ip:8888
