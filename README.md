# 数据集：Russo Ukrainian War Collection of Tweet IDs
 
The repository contains an ongoing collection of tweets IDs associated with the current war between Russia and Ukraine, which we commenced collecting on Februrary 24, 2022. We leveraged Twitter's search API to extract historical tweets, leading our dataset to contain tweets from February 22, 2022. We utilize Twitter’s streaming API to collect dataset based on selected popular hashtags corelated to particullar topic. The list of selected hashtags is presented in "hashtags.txt" file. To comply with Twitter’s [Terms of Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy), we are only publicly releasing the Tweet IDs of the collected Tweets. The data is released for non-commercial research use. 

The associated paper to this repository can be found here: [Twitter Dataset on the Russo-Ukrainian War](https://arxiv.org/abs/2204.08530)



## Data Organization
The Tweet-IDs are organized as follows:
* Tweet-ID files are stored in folders that indicate the year and month of the collection (YEAR-MONTH). 
* Individual Tweet-ID files contain a collection of Tweet IDs, and the file names all follow the same structure, with a prefix “tweet_ids_day_” followed by the YEAR_MONTH_DATE. 
* Note that Twitter returns Tweets in UTC, and thus all Tweet ID folders and file names are all in UTC as well. 


## Data Statistics and Analysis
We are manage to perform multiple statistical measurments in daily basis over the described dataset such as:
* User Activity (Traffic volume)
* Active users
* Volume of suspended and deactivated accounts
* Traffic volume based on text language
* Traffic of hashtags
* Sentiment analysis between entities of Russia and Ukraine
* Sentiment analysis between entities of Putin and Zelensky

All described analytics are published in [Parasecurity Group webpage](https://alexdrk14.github.io/RussiaUkraineWar/). 

## Data Usage Agreement / How to Cite
By using this dataset, you agree to abide by the stipulations in the license, remain in compliance with Twitter’s [Terms of Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy), and cite the following manuscript: 

Authors and Paper title with arxiv_id
BibTeX:
```bibtex
@misc{shevtsov2022twitter,
  title={Twitter Dataset on the Russo-Ukrainian War},
  author={Shevtsov, Alexander and Tzagkarakis, Christos and Antonakaki, Despoina and Pratikakis, Polyvios and Ioannidis, Sotiris},
  journal={arXiv preprint arXiv:2204.08530},
  year={2022}
}
```


## Statistics Summary (v1.0)
Number of Tweets : **66,128,912**


## Inquiries

Please read through the README and the closed issues to see if your question has already been addressed first. 

If you have any  questions about this dataset/analysis, please contact Alexander Shevtsov at **shevtsov[at]ics[dot]forth[dot]gr**.

## VIINA
https://github.com/zhukovyuri/VIINA

# 代码：01~09
01_Tweet_Scraper:使用多线程和Snscrape将数据集中的Tweet_id抓取并存储到相应的文件中

02_Data_Clean:将爬取到的数据初步清洗

03_Cleand_Data_Rename:重命名文件，便于下一步读取

04_Data_Description:使用Dask同时统计并汇总多个文件中的信息，完成描述性统计工作

05_Data_Analysis_Moral&Hate:完成道德基础赋值和仇恨言论检测工作，并进行统计检验

06~08_Panel_Data_Analysis:构建并对面板数据进行各项分析

09_Vinna_and_Hate&Moral:时间序列数据的格兰杰因果检验及因果图发现
