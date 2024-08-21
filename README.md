# World Cup Tweets Project

### Project Steps
1. Defining the project question
2. Collecting the data
3. Cleaning the data
4. Analyzing the data
5. Results and conclusions

### Defining the Project Question
The Men's World Cup in 2022 was one filled with team successes, failures, upsets, injuries, controversy, and at the very end one singular world champion. To be fair, each World Cup is filled with moments just like the one the most previous one, taking fans along for an emotional ride that is four years in the making. I wanted to explore the sentiment surrounding the World Cup, an event that stretches across international borders and captivates the world for a few months every time it rolls around. To investigate the big ideas and concepts surrounding the 2022 World Cup, I decided to get a dataset from Kaggle that contains tweets about the World Cup as well as a few other important variables such as date created, number of likes on the tweet, and the source of the tweet. Additionally, the dataset has categorized each tweet as having a "positive", "negative", or "neutral" sentiment. Due to this dataset already contained sentiments of the tweet, I will focus more on contextualizing important topics throughout the World Cup and tracking sentiment over time. This will be completed through cleaning data specific to twitter and visualization wordclouds to show bigrams that are of importance in the dataset. Then sentiment over time will be explored in the initial data analysis and LDA will be performed to show the topics that were most important in a sample of the dataset.

### Cleaning the Data
After loading the CSV file where the 2022 FIFA World Cup tweets are stored, I began cleaning the data. Due to the fact that the dataset was tweets scraped exactly as they were posted, there we many cleaning steps that had to be taken such removing references to pictures, memes, or other people's tweets that were being quoted. Typical steps when it comes to cleaning text data were taken, such as creating a corpus and turning the corpus into sentences which gave me the ability to extract individual tweets from the dataset. Next I tokenized the corpus and used some preprocessing steps available from the quanteda package. After getting a clear idea of exactly what needed to be removed to look at the "meat" of the tweet rather than the extra language, the hashtag used to scrape the tweets was removed along with all of the variations of that hashtag that were present in the tweets. Additionally, stop words were removed and anything that I could not gather meaning from in text format such as links to pictures, videos, and other tweets.

### Analyzing the data
After I had a cleaned dataset containing tweets without the superfluous language and links that were present, I moved on to contextualizing important topics that existed throughout the dataset. This entailed looking at the top 20 most frequent singular words, extracting collocations and analyzing the most compon words, and creating bigrams to represent important words combinations. After looking at generic bigrams, I decided to create custom bigrams based on the words "goal" and "team" as these are very signficant words in soccer and can illustrate important ideas related to them that are present in the tweets.

<center><img src="/TA_Wordcloud.png"/></center>

The next step in the analysis process was to track sentiment over the time span the dataset represented to find trends that may be present, such as when sentiment was positive versus negative and whether that could be related to events that were happening at that moment. The final step in my text analysis was implementing Latent Dirichlet Allocation (LDA) to identify hidden topics in the text data and their relationship with sentiment to explore whether certain topics tended to be classified as having a specific sentiment. Overall, the analysis enabled me to explore important topics relating to the World Cup on the first day of play and discover important events that happened as well how the public felt about ex[eriencing these moments live.

<center><img src="/TA_LDA.png"/></center>

### Results and conclusions
The main thing that I found interesting in the collocation analysis is that you can clearly relate the bigrams to events that were happening in the World Cup on the first day from which this data is collected. One collocation that stuck out to me in particular when running the analysis on all the tweets that distinguished it from the same analysis run on a sample is that the words "human rights" are shown here. Human rights were a massive topic of discussion when it came to the World Cup because of the country the tournament was hosted in. There were many human right violations on the part of Qatar in the building and creation of the infrastructure required to host the World Cup there as well as their historical violations of LGBTQ+ rights. It is cool to see that this conversation was an important one among twitter users talking about the World Cup even as it began.

From my exploratory data analysis, I was able to decipher a few clear trends as it relates to sentiment over time of the tweets. First off, when interaction on twitter with the World Cup was the highest, there is a larger neutral and negative sentiment compared to tweets with a positive sentiment. Additionally, tweets seem to occur more frequently at the top of the hour than the latter half of each hour. At this point is when the highest number of tweets with negative sentiment were sent out, possible representing sentiment surrounding the early goal that was overturned for Ecuador that have been shown to be a large topic of conversation in this dataset from the wordcloud visualizations



The LDA analysis that I completed shows a variety of information on the dataset. It shows the top terms depending on the beta values that covers a wide range of topics that made the first day of the World Cup particularly interesting. It also shows per-topic-per-word probabilities that highlight important terms such as "opening", "support", "luck" that show positive sentiment towards the teams kicking off the World Cup. It also shows which terms in documents are assigned to which topics and the top documents. All in all, without getting into extensive detail on what the output of the LDA analysis is, it shows that major topics in this dataset include tweets surrounding the opening of the World Cup, the teams playing in Group A, that streaming was a topic of discussion, and that many people were loving Enner Valencia's performance as well as his goal that got called back causing quite a stir.

This project was completed for the Text Analytics course in the MSBA program at the University of Utah. 
