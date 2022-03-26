# WikiTalkEdit
A dataset of conversations from the Wikipedia Talk pages and Edit histories. For research in online cooperation and conversation modeling.


Jaidka, K., Ceolin, A., Singh, I., Chhaya, N., & Ungar L. (2021). WikiTalkEdit: A dataset for modeling editors’ behaviors on Wikipedia. In Proceedings of the North American Chapter of the Association for Computational Linguistics – Human Language Technologies (NAACL-HLT 2021). ACL.


Please also look at my gitrepo called "wikipedia_puller" for more information about how the talk page data and the edits data were collected.


Talk page data was collected in the following manner:


* We downloaded and had a look at the data of the Wikimedia Corpus (https://figshare.com/articles/Wikipedia_Talk_Corpus/4264973). 


* We created a python script to extract the interactions of the users that follow the scheme (wikireader.py in the wikipedia_puller gitrepo)

- UserA posts a comment

- UserB replies to the comment

- UserA answers to B's reply


This gives as a corpus of two-way interactions to study. The format of the conversations extracted (in the file 'filtered_wiki.tsv') is:


TIME   USER_A    TOPIC       COMMENT

TIME   USER_B    TOPIC       COMMENT

TIME   USER_A    TOPIC       COMMENT

Every three lines, there is a new interaction on a new topic. 


After checking the data, we decided to only keep the interactions of the wikipedia articles, and not those of the wikipedia users, since we found the latter less articulated and essentially redundant because of the presence of automatic messages. 


Examples of the kind of conversations collected are provided in the "resources" folder.
