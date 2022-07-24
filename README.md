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

## Source Code Files

# Running Instructions

# Requirements
