
# README FILE - MIDTERM

# QUESTION 1:

# Using Enron data-set, perform 3 analysis.

## ANALYSIS 1 - Retriving email message text content

- All the emails in ENRON dataset are traversed using os.walk()
- Each email JSON file is loaded into another data structure.
- This loaded file is analysed to find message text content and printing the email in tree format.

##RESULT

##We get the body of every email in an organised way.

## ANALYSIS 2 - Retriving all emailIds and their email subjects involved in Enron Dataset with their frequency

- Using os.walk() we traverse through uneven hierarchy and read each JSON file in the dataset.
- While analysing a file we store data in string 'b' and then parse the data using an email parser.
- With the help of parser we find all the to and from emailids and append it to a list 'list_tofrom'.
- Then we use a funtion 'mainlist' to convert the 'list_tofrom' into dictionary 'Main' with counts of occurence of - -- each emailids
- Also we track the various subject of these mails and their frequency.
- All the retrieved data is stored in a csv file.

## ANALYSIS 2 - Determining the sent mails, inbox, sent_items for each individual

- By traversng through each folder and then respectively into it's files 
- we get the count of all the types of mails in a person's folder.

# QUESTION 2: 
# Use NYT API to collect NYT data. Perform 3 analysis on the collected data.

## COLLECTING AND STORING DATA:

- Generate key from the NYT API site
- On console exported the key and assigned it to a variable
- Using they generated, type of data is chosen from NYT API and filtered according to our requirements.
- The url generated is copied from the site and assigned to a variable ‘url’  in jupiter notebook.
- The data is requested and stored in list ‘response_data’ depending on the hits.
- Then the data from the list in stored in JSON files. 

## ANALYSIS 1 - Find out 100 most frequent words in the snippet of Archive Articles

##DATA

- DATA - NYT API -Article
- DATE RANGE - 31st December 2016

- With the help of nltk.corpus and regular expression top 100 most frequent words have been found.
- The JSON files in Article_search folder is read one by one.
- Data is determined using regular expression.
- All the data are stored in a list 'Words'.
- The data is then transformed by removing stopwords and punctuations to have only words.
- The words are converted to lower case to avoid redundancy and determine each words counts.
- Tha word and its count is stored in a dictionary.
- The data in the dictionary is used to generate csv called 'Article.csv'.

##RESULT
##The most frequenctly used 100 words have been determined.
##In this case the word 'new' is the most frequent word.

## ANALYSIS 2 - Graph Generation of article counts and storing data in csv

##DATA

- DATA - NYT API -Archive
- DATE RANGE - October Month 2015

- In this analysis the data used is for the OCtober month of 2016.
- The date for each article in the each JSON file of Archive folder is considered.
- The publish date of the article is trimmed to get the day part of the date to generate graph for 
- every date of October to count the articles that were publihed
- The collected data is stored in a dictionary with count of article for a particular date.
- Using the data graph is generated with the help of matplotlib.pyplot.
- Also a csv Archive.csv is generated which contains news_desk,document_type,word_count,source & 
- pub_date information of each article

##RESULT
##WE know on which day of OCtober month the number of article published.

## ANALYSIS 3 - Traversing through nested Dictionaries and list and Storing data in CSV

##DATA

- DATA - NYT API -Books
- DATE RANGE - 2017

- The data from JSON files of Books folder is loaded and analyse one by one.
- By traversing throught the nested dictionary and lists useful information about each book published is retrived
- The data retrieved is stored in a Book.csv
