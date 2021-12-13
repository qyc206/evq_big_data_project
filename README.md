# EVQ Project (Fall 2021)

## Table of Contents
* [PART I: Data Profiling & Cleaning (using pyspark)](#part-i-data-profiling--cleaning-using-pyspark)
    * [About the Dataset](#about-the-dataset)
        * [Download Full Dataset (optional)](#download-full-dataset-optional)
    * [Profiling & Cleaning the Dataset](#profiling--cleaning-the-dataset)
        * [Profiling the Dataset](#profiling-the-dataset)
        * [Cleaning the Dataset](#cleaning-the-dataset)
* [PART II: Data Cleaning at Scale](#part-ii-data-cleaning-at-scale)
    * [Reference Datasets](#reference-datasets)
    * [Profiling & Cleaning Notebooks](#profiling--cleaning-notebooks)
    * [Final Paper](#final-paper)
* [Contact Information](#contact-information)


# PART I: Data Profiling & Cleaning (using pyspark)

For this assignment, we are assigned the [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9) dataset and is tasked to explore the dataset to identify data quality issues and then clean this data and create a new version of the dataset. In the following sections, we provide a brief overview of the dataset that is assigned to us and showcase our discoveries along with discussions of our approach to cleaning our dataset. 

To profile and clean our dataset, we chose to use [pyspark (v3.2.0)](https://spark.apache.org/docs/latest/api/python/getting_started/install.html), running on python version 3.6. We tested all of our codes using Google Colab (links to relevant notebooks are available in the corresponding sections below for easy testing and running). All notebooks are also uploaded onto this Github repo via the [notebooks/part1](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks/part1) directory.

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

Use the notebook named "Profiling_The_Dataset.ipynb" in the [notebooks/part1](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks/part1) directory of this repo to view and explore our profiling procedure as well as our findings. 

**Note:** This code is also available via [Google Colab](https://colab.research.google.com/drive/1tk30gvS2qUptfBQTvsF68EuFWKPbwWY_?usp=sharing).

### Cleaning the Dataset

Use the notebook named "Cleaning_The_Dataset.ipynb" in the [notebooks/part1](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks/part1) directory of this repo to view and go through our cleaning process and create a new version of the sample dataset ((i.e. the sample dataset with ~5 million rows).

**Note:** This code is also available via [Google Colab](https://colab.research.google.com/drive/1_EYqXb2oN889RPqRc8jwQaWygmpzKBiF?usp=sharing).


# PART II: Data Cleaning at Scale

## Reference Datasets

Two reference datasets are used during cleaning. One is a dataset with all the location information, i.e all cities, zip codes, latitude and longitudes of them. The second dataset is a custom-made dataset containing agency name and agency acronym. These reference datasets are available via [reference_datasets/](https://github.com/qyc206/evq_big_data_project/tree/main/reference_datasets).

## Profiling & Cleaning Notebooks

The notebooks provided for Part II are an extension and improvement of the notebooks from Part I. The code has been tested on the full [311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9) dataset, and the notebooks are also used to profile and clean ten similar datasets found on NYC Open Data.

### Profiling Notebook

To run the profiling code on Peel, download and upload the Zeppelin notebook named [Profiling_Dataset_peel.zpln](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Profiling_Dataset_peel.zpln). If you would only like to view the notebook, check out the notebook named [Profiling_Dataset_peel.ipynb](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Profiling_Dataset_peel.ipynb).

### Cleaning Notebooks

To Zeppelin notebooks that are used to clean the datasets are broken down into the following sub-sections: **Uniformity, Accuracy, Inconsistency, Completeness, and Outlier**

Since Zeppelin notebooks cannot be rendered on Github, we also provide a Jupyter notebook version that is **view only**. Please do not try to run the Jupyter  notebook versions as they will not work.

#### Uniformity

To run the cleaning code on Peel, download and upload the Zeppelin notebook named [Cleaning_Dataset_peel_Uniformity.zpln](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Uniformity.zpln). If you would only like to view the notebook, check out the notebook named [Cleaning_Dataset_peel_Uniformity.ipynb](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Uniformity.ipynb).

#### Accuracy

To run the cleaning code on Peel, download and upload the Zeppelin notebook named [Cleaning_Dataset_peel_Accuracy.zpln](). If you would only like to view the notebook, check out the notebook named [Cleaning_Dataset_peel_Accuracy.ipynb]().

#### Inconsistency

To run the cleaning code on Peel, download and upload the Zeppelin notebook named [Cleaning_Dataset_peel_Inconsistency.zpln](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Inconsistency.zpln). If you would only like to view the notebook, check out the notebook named [Cleaning_Dataset_peel_Inconsistency.ipynb](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Inconsistency.ipynb).

#### Completeness

To run the cleaning code on Peel, download and upload the Zeppelin notebook named [Cleaning_Dataset_peel_Completeness.zpln](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Completeness.zpln). If you would only like to view the notebook, check out the notebook named [Cleaning_Dataset_peel_Completeness.ipynb](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Completeness.ipynb).

#### Outlier

To run the cleaning code on Peel, download and upload the Zeppelin notebook named [Cleaning_Dataset_peel_Outlier.zpln](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Outlier.zpln). If you would only like to view the notebook, check out the notebook named [Cleaning_Dataset_peel_Outlier.ipynb](https://github.com/qyc206/evq_big_data_project/blob/main/notebooks/part2/Cleaning_Dataset_peel_Outlier.ipynb).


The notebooks for Part II are available via [notebooks/part2](https://github.com/qyc206/evq_big_data_project/tree/main/notebooks/part2).

## Final Paper


# Contact Information

Erica Chou (emc689@nyu.edu), Varshitha Chennamsetti (vc2209@nyu.edu), and Qin Ying Chen (qyc206@nyu.edu)

Feel free to reach out to any of us if you run into any problems and/or have any questions.  
