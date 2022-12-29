# **Zomato_Restaurant_Clustering_and_Sentiment_Analysis**
## Data Description:

Zomato is an Indian restaurant aggregator and food delivery start-up founded by Deepinder Goyal and Pankaj Chaddah in 2008. Zomato provides information, menus and user-reviews of restaurants, and also has food delivery options from partner restaurants in select cities.

India is quite famous for its diverse multi cuisine available in a large number of restaurants and hotel resorts, which is reminiscent of unity in diversity. Restaurant business in India is always evolving. More Indians are warming up to the idea of eating restaurant food whether by dining outside or getting food delivered. The growing number of restaurants in every state of India has been a motivation to inspect the data to get some insights, interesting facts and figures about the Indian food industry in each city. So, this project focuses on analysing the Zomato restaurant data for each city in India.

The Project focuses on Customers and Company, you have to analyze the sentiments of the reviews given by the customer in the data and made some useful conclusion in the form of Visualizations. Also, cluster the zomato restaurants into different segments. The data is vizualized as it becomes easy to analyse data at instant. The Analysis also solve some of the business cases that can directly help the customers finding the Best restaurant in their locality and for the company to grow up and work on the fields they are currently lagging in.

This could help in clustering the restaurants into segments. Also the data has valuable information around cuisine and costing which can be used in cost vs. benefit analysis.

Data could be used for sentiment analysis. Also the metadata of reviewers can be used for identifying the critics in the industry.

## Attribute Information:

### Zomato Restaurant names and Metadata:

* Name : Name of Restaurants

* Links : URL Links of Restaurants

* Cost : Per person estimated Cost of dining

* Collection : Tagging of Restaurants w.r.t. Zomato categories

* Cuisines : Cuisines served by Restaurants

* Timings : Restaurant Timings

### Zomato Restaurant reviews: 

* Restaurant : Name of the Restaurant

* Reviewer : Name of the Reviewer

* Review : Review Text

* Rating : Rating Provided by Reviewer

* MetaData : Reviewer Metadata - No. of Reviews and followers

* Time: Date and Time of Review

* Pictures : No. of pictures posted with review

## Business Problem Analysis:

The various regional and traditional foods that are indigenous to the Indian subcontinent make up Indian cuisine. You may discover something unique to adore in every state. Aside from the traditional foods of North and South India, many other civilizations have had a significant influence on and contributed to the development of culinary culture. It would be an understatement to say that Indians like eating. People in India like celebrating even the smallest milestones in their life with delicious food and a welcoming environment. Zomato is here to connect customers and restaurants. Zomato is an online directory of Indian restaurants that offers menus, user ratings, and the option of meal delivery. They essentially take orders on behalf of the restaurant and arrange for delivery of the meal to your door.

The problem statement here has two datasets for us to work on:
* Zomato Restaurant Names and Metadata
* Zomato Restaurant Reviews

Zomato must examine its datasets and make informed strategic decisions if it wants to ensure its success. In order to assist clients identify the finest restaurants in their city, according to their preferences, and to analyse the areas where they are falling short, the issue statement requests us to group the restaurants. This will aid Zomato in developing a strong consumer recommendation system. Use the restaurant prices and cuisines to do a cost-benefit analysis. It is crucial to do sentiment research to learn how customers truly feel about a certain restaurant in order to identify areas that require improvement. to locate the industry critics and, in particular, to work on their assessments in order to develop a reputation that is praiseworthy.

## Data Cleaning and Pre-Processing:

Due to the existence of undesirable data, such as duplicate values, null values, and outliers, the raw data received in the data collection may not be immediately accepted for analysis. Before moving on to further in-depth examination, we must deal with them first.

**Removing Duplicates:** There are roughly 105 entries in the "Zomato Restaurant names and Metadata" dataset that was given for this investigation. They are all original and have never been seen before. The "Zomato Restaurant Reviews" dataset, which is also offered, has 10,000 entries, all of which are distinct and have never been replicated. Before modeling, it is preferable to look for duplicate values.

**Handling null/missing values:** It is also conceivable that certain records in the supplied data set lack information for some or all of the characteristics; in this case, we must either delete such records or find alternatives to fill in the null values. More over half of the collections column entries in the "Zomato Restaurant names and metadata" dataset are null values. Therefore, we won't be using that column in our analysis. Additionally, a small number of columns in the "Zomato Restaurant Reviews" dataset have null values.

**Feature Handling:** In order to get the necessary information from the data, we can change some of the characteristics in accordance with our needs. As an illustration, we separated the "Time" column from the dataset of "Zomato Restaurant Reviews" to extract three additional new characteristics named the "year," "month," and "hour" columns. Furthermore, we divided the "MetaData" column into the "Reviews" and "Followers" columns.

## Text Preprocessing:

The most crucial phase of every machine learning model is data preprocessing. The performance of the model is significantly influenced by how effectively the raw data was cleaned and preprocessed. Similar to NLP, text processing comes first in this process.

● Lower Casing: Converting a word to lowercase (NLP -> nlp). Words like Book and book mean the same but when not converted to the lower case those two are represented as two different words in the vector space model (resulting in more dimensions).

● Tokenization: It is the process of tokenizing or splitting a string, text into a list of tokens. One can think of a token as parts like a word is a token in a sentence, and a sentence is a token in a paragraph.

● Punctuation Mark Removal: The punctuation removal process will help to treat each text equally. For example, the word data and data! are treated equally after the process of removal of punctuations.

● Stop Word Removal: The idea is simply removing the words that occur commonly across all the documents in the corpus. Typically, articles and pronouns are generally classified as stop words.

● Stemming: This is the process of reducing a word to its word stem that affixes to suffixes and prefixes.

● Lemmatization: This is the process of the grouping together of different forms of the same word and converting words into base or root form.
