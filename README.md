# EVQ Project (Fall 2021)

## Table of Contents
* [PART I: Data Profiling & Cleaning (using pyspark)](#part-i-data-profiling--cleaning-using-pyspark)
    * [About the Dataset](#about-the-dataset)
        * [Download Full Dataset (optional)](#download-full-dataset-optional)
    * [Profiling & Cleaning the Dataset](#profiling--cleaning-the-dataset)
        * [Profiling the Dataset](#profiling-the-dataset)
        * [Cleaning the Dataset](#cleaning-the-dataset)
* [Contact Information](#contact-information)

# PART I: Data Profiling & Cleaning (using pyspark)

For this assignment, we are assigned the [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9) dataset and is tasked to explore the dataset to identify data quality issues and then clean this data and create a new version of the dataset. In the following sections, we provide a brief overview of the dataset that is assigned to us and showcase our discoveries along with discussions of our approach to cleaning our dataset. 

To profile and clean our dataset, we chose to use [pyspark (v3.2.0)](https://spark.apache.org/docs/latest/api/python/getting_started/install.html), running on python version 3.6. We tested all of our codes using Google Colab (links to relevant notebooks are available in the corresponding sections below for easy testing and running). All notebooks are also uploaded onto this Github repo via the [notebooks/](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks) directory.

## About the Dataset

The dataset that we are assigned to profile and clean is [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9). This dataset contains 27.1 million rows and 41 columns, where each row is a 311 service request. It should also be noted that this dataset is automatically updated daily.

For profiling and cleaning, we randomly sampled ~5 million rows from the entire dataset. The compressed file containing the samples that we used is made available via Google Drive link: [erm2-nwe9_5M.csv.gz](https://drive.google.com/file/d/12pLI--cbQ-wTHjiDbiCdghYMDBUthQGf/view?usp=sharing) (599.5MB). 

The full dataset is available for download via the [Socrata Open Data API (SODA)](https://dev.socrata.com/). Note that OpenClean includes a SODA wrapper that provides access to all datasets available via the API using their unique identifier. The compressed full dataset is about 2.74GB in size. 

### Download Full Dataset (optional)

To download the full dataset, the [openclean](https://github.com/VIDA-NYU/openclean) tool is utilized. 

Use the notebook named "Download_Full_Dataset.ipynb" in the [notebooks/](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks) directory of this repo to download the entire dataset.

**Note:** This code is also available via [Google Colab](https://colab.research.google.com/drive/1Xy7rwx-p3Rjef4T5CoWoTGW2KKaVCBKP?usp=sharing).

## Profiling & Cleaning the Dataset

This section goes over the problems that we found while exploring the sample dataset (i.e. the sample dataset with ~5 million rows) as well as our solution to cleaning the data. 

We broke down the problems that we found into the following sub-sections: 
**Uniformity, Accuracy, Inconsistency, Completeness, and Outlier**

### Profiling the Dataset

Use the notebook named "Profiling_The_Dataset.ipynb" in the [notebooks/](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks) directory of this repo to view and explore our profiling procedure as well as our findings. 

**Note:** This code is also available via [Google Colab](https://colab.research.google.com/drive/1tk30gvS2qUptfBQTvsF68EuFWKPbwWY_?usp=sharing).

### Cleaning the Dataset

Use the notebook named "Cleaning_The_Dataset.ipynb" in the [notebooks/](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks) directory of this repo to view and go through our cleaning process and create a new version of the sample dataset ((i.e. the sample dataset with ~5 million rows).

**Note:** This code is also available via [Google Colab](https://colab.research.google.com/drive/1_EYqXb2oN889RPqRc8jwQaWygmpzKBiF?usp=sharing).

### Resulting Dataset

Our cleaned dataset can be found via and downloaded from [erm2-nwe9_5M_cleaned.csv.gz]().

# Contact Information

Erica Chou (emc689@nyu.edu), Varshitha Chennamsetti (vc2209@nyu.edu), and Qin Ying Chen (qyc206@nyu.edu)

Feel free to reach out to any of us if you run into any problems and/or have any questions.  
