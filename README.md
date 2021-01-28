# data-DMRP
Data of paper J. Xie et al., Detecting and modelling real percolation and phase transitions of information on social media. 

This project provides the dataset of network structure, track of 253 information items and evolution dataset of Weibo, and evolution dataset of Twitter. In order to protect the privacy of users, the user’s ID are all reset in the dataset. By checking their IDs, one can rebuild the diffusion path of each cascade.

The file “weibo_activity.txt” provides the evolution dataset of 192,749 Weibo users. The first and second column are the users’ follower counts before and after a 198-days interval, respectively. The third and fourth column are the users’ tweet counts before and after the same interval, respectively.

The file “twitter_activity.txt” provides the evolution dataset of 184,095 Twitter users. The first to fourth column are similar to those in file “weibo_activity.txt”. The fifty column is the time interval of collection time, in days, for each user.

By decompressing the file “tracks.rar”, one will obtain the files “T1.txt” ~ “T253.txt” which provide the tracks of 253 information items. In each .txt file, the tweet users (including the poster) are listed by their reset ID. The file “cascade_size.txt” provides the numbers of retweet users (including the poster) of the information items. Note that some retweet users (including the poster) are missing when we collected the tracks data.

The code reads the file “kout_kin_count.txt”, which provides the degree distribution of our Weibo network 2014. The first to third column are the follower count, the followee count, and the number of users with both that follower count and followee count, respectively.

The files “k_each_user.txt”, “fan_table.sql” and “fo_table.sql” are too large to be upload here. The compressed files are available at website: https://pan.baidu.com/s/18XVJuzL4Umox9cF8kPUxmw, with code: 73ab

The file “k_each_user.txt” provides the degree of each user in our Weibo network 2014, which is used in the “simulating_dataDriven_percolation.py” file. The first to third column of the file are the users’ ID (reset), the followee counts and the follower counts.

The file “fan_table.sql” provides the database table “fan_table” for the topology structure of our Weibo network 2014. In the database file, the column “id” is the user’s ID (reset), the column “fans” is the user’s follower list. The network has 99,546,027 nodes, and the IDs of the nodes are set to be 1, 2, …, 99546027. When built the database, the column “id” was set to be the key. Note that the hottest user in our dataset had more than 10 million followers (with memory about 97M), please ensure that it does not exceed the memory when building the table. As a test, the file “fan_table_max.sql” (which can be obtained by decompressing file “fan_table_max.rar”) provides the row of the hottest user.

The file “fo_table.sql” provides the table “fo_table” for the topology structure of our Weibo network 2014. In the database file, the column “id” is the user’s ID (reset), the column “fo” is the user’s followee list. The “fo_table” is not used directly in this project. It is a redundant data which can be obtained by inversing the “fan_table” database. However, it is provided and we are looking forward to see your further applications.

