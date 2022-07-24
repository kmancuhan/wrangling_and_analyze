# Date Created

July 24, 2022

# Project: Data Wrangling and Analysis

## Objective

The primary objective of this project is to provide a template for the data wrangling procedure, using multiple sources of data. Here, data wrangling means necessary steps to clean the data.

The secondary objective includes providing a basic analysis from the data to answer some of the questions, after completing the cleaning procedure:

  1.  Would rating, retweet and likes (favorites) change according to the age of the dogs in
  the tweets?
  2. How does the image classification performance for tweets with images change, with
  respect to the source of the tweet?
  3. Which class labels are confused most for misclassified images?
  4. Are there a relationship, or correlation, between favorite and retweet counts of tweets? Do people like the tweets they retweet, especially for WeRateDogs?

Here, WeRateDogs is a Twitter page giving ratings for various dog tweets. We use the tweet list of this page, giving more details in the subsequent parts of this README.

## Description

We will describe the data wrangling template here, which is initially provided by the Udacity platform. The template consists of three parts: data gathering, assessment, and cleaning.

Data gathering focuses on obtaining the data, in this example downloading from various sources to my local desktop. Some more complicated examples could include using API of Twitter to obtain the tweets directly from the platform.

Assessment focuses on identifying multiple issues related to dirtiness or messiness of the data. Depending on the nature of the issues, the problems could be related to data quality or tidiness issues. For example, one column could have missing values which puts it into data quality issue. Two separate tables could in fact belong to a single observational unit which requires merging two tables for a meaningful analysis. This could be put into a tidiness issue.

Cleaning part has a set of issues, each of which has the Define, Code and Test subsections. Each issue in the cleaning part is basically an issue in the assessment part, which is put into action in order to fix the problem.

Let's consider a simple data quality issue for a column named "X" in a DataFrame named "df". We need to change the data type of a column X from string to category. The assessment part could have an issue such as

  - Incorrect type for the column named X

and the cleaning part could have the respective task

  - Define: Change the type of the column named X from string to category
  - Code: Write the respective python code such as "pd.Categorical(...)"
  - Test: Test the necessary change calling something like df.info() assuming a DataFrame named df.

The template ends with a small section about analyzing and visualizing data. Udacity included this section in the template and I included some aggregates and plots to answer some of the basic questions. In real projects, this section would be more thorough but I kept it short here as this wasn't the primary objective of this project.

# Files

## Data Files

There are 4 data files in this project, 3 of which are actually raw data files that are downloaded from the Udacity servers:

  1. image-predictions.tsv has the predictions of an image classifier for object detection. The classifier aims to predict dog pictures here correctly and the file includes the classifier results. The classifier itself is not included in this project.
  2. twitter-archive-enhanced.csv has the tweet text, tweet source, dog name, dog age, dog ratings etc. from the WeRateDogs channel.
  3. tweet-json.txt has JSON records downloaded from the Twitter page using the Twitter API. Each record includes additional information not included in the former file such as retweet count, favorite count etc. The tweets are all from WeRateDogs channel.

The 4th file is a data file that I generated after cleaning various data quality and structural issues.

  - twitter-archive-master.csv includes all the features of the three different files above after cleaning the data quality issues on each file.

## Report files

There are two report files in the project:

  - wrangle_report.pdf explains all the steps to clean the data, including all the details about gathering, assessment and cleaning. This report explains the details of the primary objective of this project.
  - act_report.pdf explains all the insights derived from the cleaned data. It includes the answers for the questions in the secondary objective and a relevant plot.

## Source Code Files

  - wrangle_act.ipynb is a Jupyter notebook file including all the scripts for data wrangling and analysis.

Note that I didn't remove the comments and tips provided by the Udacity instructors for general audience. It makes it easier to follow and to generalize to other datasets and problems at hand.

# Running Instructions

As long as you have an installed Jupyter notebook server on your desktop with the required packages, you should be able to run the code. I am using the Anaconda virtual environment, although it is not necessary for running the project.

# Requirements

  - conda==4.12.0 (optional)
  - jupyter notebook==6.4.11
  - python==3.9.12
  - pandas==1.4.2
  - numpy==1.21.5
  - json==2.0.9
  - requests==2.27.1
