## Introduction
Wrangling is a process that covers the steps of gathering data, assessing the data for quality and tidiness issues, and cleaning the data. This project is about the process of wrangling data. The project makes use of the data from WeRateDogs' Twitter account.

WeRateDogs (@dog_rates) is a Twitter account that gives ratings to people's dogs along with a lighthearted comment. The denominator of these scores is almost always 10. however, the numerators? frequently more than 10. 13/10, 14/10, 15/10,etc. Over 4 million people follow WeRateDogs, and it has been featured in international media.
I will be using three datasets to achieve this objective. The datasets are:

## Data Gathering
### WeRateDogs Twitter archive data (twitter_archive_enhanced.csv)
I manually downladed the Twitter archive csv-format file using my web browser, then I uploaded it to the Jupyter Notebook I was working with. Then, I read it into a dataframe by using Pandas read csv method to red csv files directly.

### Tweet image prediction file (image_predictions.tsv)
I made use of the Python Request library to download the file through the URL Udacity supplied. Afterwards, I wrote the fetched content to a file named image_predictions.tsv as it is a tsv file using Python Context Manager. Finally, I loaded the written file into Pandas using Pandas read csv method, and specifying the separator as tab because the contents are delimited by tab.

### Tweet additional data (tweet-json.txt)
I obtained the additional information associated with each tweet using the file (tweet-json.txt) provided by Udacity because Twitter is showing an error message whenever I try to register for a Twitter developer account. After acquiring the file (tweet-json.txt), I leveraged glob library, json library and Python Context Manager to locate, read and parse the file into a json. On parsing into json, I extracted the needed fields into a dictionary and appended each record into a list. I concluded the process by using Pandas method to turn the list into a dataframe.

## Assessing Data
After the data gathering stage was completed, I assessed three dataframes produced during the data gathering stage:

#### twitter_archive_enhanced_df - Twitter archive enhanced dataframe
#### tweet_image_prediction_df - Tweet image prediction dataframe
#### tweet_add_df - Tweet additional data dataframe
I implemented both visual and programmatic assessments during the process of assessing the data

## Visual Assessments
I visually assessed the data by displaying the whole dataframe in my Jupyter lab, and I also used notebook on my PC to also visually assessed the data

## Programmatic Assessments
I programmatically assessed the data using the various Pandas methods available. Some of the methods I used are:

head()
info()
describe()
value_counts()
contains()
After the end of the assessment, I detected some quality and tidiness related issues

## Quality Issues detected
### twitter_archive_enhanced_df
source column is a combination of the platform used and a link
timestamp column datatype is object (string)
retweeted_status_timestamp datatype is object (string)
some tweets are replies
some tweet are quote tweets
some tweets are re-tweets
some tweets have wrong ratings
name column has values that are not possible
stage of dog in some tweets is incorrect
## Tidiness Issues detected
### Tweet image prediction dataframe
some of the columns names are not self-explanatory
Twitter archive enhanced dataframe
the different dog stages (doggo, floofer, pupper, puppo) have different column names for each stage
column for combined rating is absent
dataframe lacks additional information about each tweet
information about the predictions associated with each tweet is missing
## Cleaning Data
After assessing the data for quality and tidiness issues, I cleaned the data by correcting the issues identified using the define, code and test framework. Note: I made a copy of the dataframes before cleaning