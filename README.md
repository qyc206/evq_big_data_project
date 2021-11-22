## EVQ Assignment 3
# PART I: Data Profiling & Cleaning (using openclean & pyspark)


## About the Dataset

The dataset that we are assigned to profile and clean is [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9). This dataset contains 27.1 million rows and 41 columns, where each row is a 311 service request. It should also be noted that this dataset is automatically updated daily.

For profiling and cleaning, we randomly sampled ~5 million rows from the entire dataset. The compressed file containing the samples that we used is made available via Google Drive link: [erm2-nwe9_5M.csv.gz](https://drive.google.com/file/d/12pLI--cbQ-wTHjiDbiCdghYMDBUthQGf/view?usp=sharing) (599.5MB). 

The full dataset is available for download via the [Socrata Open Data API (SODA)](https://dev.socrata.com/). Note that OpenClean includes a SODA wrapper that provides access to all datasets available via the API using their unique identifier. The compressed full dataset is about 2.74GB in size. 

## Download Full Dataset (optional)

Use the notebook named "Download_Full_Dataset.ipynb" in the [notebooks/](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks) directory of this repo to download the entire dataset.

This code is also available via [Google Colab](https://colab.research.google.com/drive/1Xy7rwx-p3Rjef4T5CoWoTGW2KKaVCBKP?usp=sharing).

## Profiling & Cleaning the Dataset

This section goes over the problems that we found while exploring the sample dataset (i.e. the sample dataset with ~5 million rows) as well as our solution to cleaning the data. 

We broke down the problems that we found into the following sub-sections: 
**Inconsistency, Uniformity, Completeness, Accuracy, and Outlier**. Each section will contain the problems that we found, along with the solution that we implemented.

(**Note:** profiling is completed using openclean & cleaning is completed using pyspark)

