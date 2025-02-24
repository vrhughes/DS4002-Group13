# DS4002-Group13 Project 1

#### Avery Donmoyer (leader), Viv Hughes, Vishal Kamalakrishnan, Dana Pham

## Goal

14.8% of Americans deny that climate change is real, a belief that researchers found evidence was influenced by social media use [^fn1]. With 59% of Twitter users getting news from the platform in 2020, we are motivated to analyze Twitter users’ sentiments about climate change to better understand the media landscape that has the potential to create social and political implications on climate [^fn2]. 

Our goal is utilize BERT [^fn3] to analyze the sentiment of Twitter users’ posts [^fn4], with the goal of categorizing the users’ sentiment based on one of the following 3 categories
1. User agrees with climate change
2. User disagrees with climate change
3. User is neutral towards climate change

## Software / Platform

We are using Jupter Notebooks for this program that run on Python 3 (prefferably 3.10+). Our code can be run on **Google Colab** by importing our notebooks. The following files require access to a GPU (or else will be very slow):

1. bert_sentiment_analysis.ipynb

For this file, a **Windows** or **Linux** environment is needed with `Pytorch`, `Tensorflow`, and `Transformers` packages and access to a Nvidia GPU and respective drivers. Additonal packages will be included in the files themselves as a runtime dependency. These files can alternatively be run on **Google Colab** or **Rivanna**. 

All additional files will need a Python environment with the packages `Pandas`, `Numpy`, `Matplotlib`, `Seaborn` and with support for `Jupyter Notebooks` and can be run on **Windows**, **Linux**, or **Mac**

## Documentation

The files and folders are broken down into this structure

```
- root
  -- DATA
    -- twitter_sentiment_data.csv
    -- random_sample.csv
  -- SCRIPTS
    -- script files for data analysis
  -- OUTPUT
    -- generated data files
    -- charts
  -- README.md
  -- License.md
```

The DATA folder contains the datasets which we used in our project. The tweet dataset (twitter_sentiment_data.csv) and a random sample of the data (random_sample.csv) is found there. The SCRIPTS folder contains multiple `Jupyter Notebooks` that have been used to analyse the data, run BERT, create graphs, and do error analysis. The OUTPUT folder contains generated datasets from SCRIPTS. These generated datasets are also used in SCRIPTS to reference trained BERT data, manual labels, etc... with the baseline data. The OUTPUT folder also contains images of charts that are present in the SCRIPTS.


## Steps To Reproduce

To reproduce the results of the project first clone the repository the following command in your terminal 
```
git clone https://github.com/vrhughes/DS4002-Group13.git
```

You can run the individual files locally (provided you follow the specifications listed in - [Software / Platform](##Software%20/%20Platform)) or can run them in **Rivanna** or **Google Colab**. All data files are provided and all outputs will overwrite the output images or files will overwrite previously existing output files.

The scripts can be run in the order shown by their filenames. While this is not a strict requirements, note that some files need to be run before others in the order shown below

1. twitterccdata.ipynb, twitter_cc_data_frequencies.ipynb, EDA.ipynb, bert_sentiment_analysis.ipynb
2. random_data_subset.ipynb
3. bert_error_analysis.ipynb, bert_graphs.ipynb

## References

[^fn1]: “AI study finds nearly 15% of Americans deny climate change is real, shaped by social media influencers: Public figures such as Trump play outsized role in influencing beliefs,” School for Environment and Stability at the University of Michigan, https://seas.umich.edu/news/ai-study-finds-nearly-15-americans-deny-climate-change-real-shaped-social-media-influencers [accessed January 31, 2025). 

[^fn2]: “Social Media and News Fact Sheet,” Pew Research Center September, 2024 https://www.pewresearch.org/journalism/fact-sheet/social-media-and-news-fact-sheet/ [accessed January 31, 2025). 

[^fn3]: “Twitter Climate Change Sentiment Dataset,” www.kaggle.com. https://www.kaggle.com/datasets/edqian/twitter-climate-change-sentiment-dataset 

[^fn4]: J. Devlin, M.-W. Chang, K. Lee, and K. Toutanova, “BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding,” arXiv.org, Oct. 11, 2018. https://arxiv.org/abs/1810.04805 
