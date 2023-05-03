I. Introduction



Disneyland parks are known worldwide as popular tourist destinations, attracting millions of visitors each year. Then, with such a large volume of visitors, there are differing opinions and sentiments towards the parks. In the following paper, we have done the evaluation of sentiment analysis about Disneyland parks. Sentiment analysis is a technique that involves analyzing text data to determine the sentiment expressed in the text. In the context of Disneyland parks, sentiment analysis involves analyzing the feedback provided by park-goers to determine the overall sentiment towards the park. This analysis can provide valuable insights into the strengths and weaknesses of the park, allowing for targeted improvements to be made. Additionally, sentiment analysis can be used to identify patterns in visitor feedback, such as popular attractions or common complaints.


The project’s overall objective with the sentiment analysis is to recognize keywords and sentiment in customers in order to answer the following questions:

● What can Disneyland focus on improving based on customer experience to increase brand engagement?

● How can Disneyland leverage the sentiment insights to develop more personalized experiences for its customers?

● What are the areas and reasons for customer dissatisfaction?



We will focus on this project on analyzing specifically the top three Disneyland parks in the world, Disneyland California, Paris, and Hong Kong. By using sentiment analysis, we can help Disney find areas that need improvement and identify reasons for customer dissatisfaction. Then, this information can be used to make the appropriate changes necessary to enhance visitor experience.

II. Dataset


Data was sourced from Kaggle, including 42,000 reviews of 3 Disneyland branches - Paris, California, and Hong Kong, posted by visitors on Trip Advisor. By comparing the ratings and conducting a sentiment analysis based on the reviews of customers, we could learn about the customer attitude to different Disneyland branches in general and provide suggestions to help improve customer satisfaction.

Review_ID. -  Unique id given to each review
Rating. -  Ranging from 1 (least satisfied) to 5 (most satisfied)
Year_Month -  When the reviewer visited the theme park
Reviewer_Location - Country or region of origin of the visitor
Review_Text -  Comments made by visitor
Branch -  Location of Disneyland Park

Data Cleaning & Processing


To begin with, we dropped all the rows that contained missing values and then identified the number of unique values in the Review_ID column. We found that the total number of unique Review IDs was 40,023, so in the following step we dropped duplicate values from the "Review ID" column, returning a clean dataset with distinct Review IDs.

Based on the rating scores, there were 21,908 individuals who gave a rating of 5, 10,086 individuals who gave a rating of 4, there were 4,782 individuals who gave a rating of 3, there were 1,929 individuals who gave a rating of 2, and there were 1,338 individuals who gave rating of 1.

Later on, we performed pre-processing on the content of the "Review_Text". We converted the content to lowercase, removed punctuation and numbers in texts, and then converted the reviews to tokens (i.e. broken into elements of a list). We then set stopwords to remove common words, which did not add any value to the analysis of the text, such as 'I' and 'you’. After that, we lemmatized the reviews and joined all the pre-processed review text to complete the processing of the "review" content.

 



            

          
