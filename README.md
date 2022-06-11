# Introduction-to-research-methods
# Final_Project_R-M
## 
#### Myrthe van der Veen S4977068


### The Repository
This repository consist of a python panda script which preprocessed the Data and make a graph with the average and standard deviation of the ammount of hashtags in a Tweet message on 22 July 2021. 

### Acces Data 

The data that is used is originating from **Karora** which is accessible with a RUG account
to access the data follow the folowing step (where s1234567 is of course your own student number):
```
ssh s1234567@karora.let.rug.nl
``` 

The in-house Twitter corpus can be found with: 
```
cd /net/corpora/twitter2/Tweets
``` 
The tool to extract information can be found with:
```
cd /net/corpora/twitter2/tools/tweet2tab
``` 

### The used Software 

The software that is used is **Python Panda** in Jupyter Notebook. The following versions of Python, Ubuntu and  Jupyter Notebook are used:
- **Python Panda**: 1.4.1 
- **Ubuntu**: 20.04.4 LTS
- **Jupyter Notebook**: 6.0.3 


###  Installation 
Use this steps to access the Jupyter notebook:  
```
git clone https://github.com/Myrthevdv/Final_Project_R-M
jupyter notebook code.ipynb
```

### Used Data

The data which is used for our project is comming from the in-house Twitter corpus
folow the steps of ``` Access Data ``` to Acess the data to use it
I used that data from July 22 2021 of each hour, with the metadeta date,place and hashtags.
to select the data for this project follow the following steps:

```
cd /net/corpora/twitter2/Tweets
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:23.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:22.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:21.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:20.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:19.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:18.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:17.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:16.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:15.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:14.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:13.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:12.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:11.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:10.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:09.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:08.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:07.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:06.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:05.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:04.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:03.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:02.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:01.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv
gunzip -c /net/corpora/twitter2/Tweets/2021/07/20210722:00.out.gz | /net/corpora/twitter2/tools/tweet2tab -i text date place hashtags > ~/user_text.tsv

scp -r s4977068@karora.let.rug.nl:/home/s4977068/Documents/user_text.tsv
``` 
It is also possible to select other data by adjusting the gunzip (all the data that is available is present in the tools directory)
**!** Use for scp -r s4977068@karora.let.rug.nl:/home/s4977068/Documents/user_text.tsv your own studentnumber. 

### Output

The output you get while running python panda script on the Data of 22 July 2021 (accesed on 29-3-2022 16:14)
contains o.a: 

| Place         | Mean          | std      |
| ------------- | ------------- | -------- |
| Belgie        | 0.293769      | 0.844004 |
| Nederland     | 0.453083      | 1.153761 |
