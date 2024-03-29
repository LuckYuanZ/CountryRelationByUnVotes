# CountryRelationByUnVotes

Project Theme:  

**Which two countries have the best relationship?** 

## (1) Data Collection, Clean-up & Analysis 

 - UN General Assembly votes of each country starting from 1940s. Data sourse:  
   -  https://dataverse.harvard.edu/dataset.xhtml?persistentId=hdl:1902.1/12379
   -  UNVotes-1.csv
   -  Codebook.docx
   -  Download date: 2023 June 10
   -  Change the csv file to UTF-8 encoding and named UNVotes-UTF-8.csv
 - COW country codes:
   -  https://correlatesofwar.org/cow-country-codes/
   -  COW-country-codes.csv
   -  Download date: 2023 June 10
   -  Read more at: https://rforpoliticalscience.com/2020/06/03/cow-codes/
 - Data cleaning code: [DataCleaning.ipynb](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/DataCleaning.ipynb)
 - Cleaned Data: UNVotes-Clean.csv (produced by above code)
 - Cleaned Data Description: [Codebook.md](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/Codebook.md)

## (2) Model Assumptions 

 - Each country’s vote at UN General Assembly represents the position of that country. 
 - Same votes on one issue represent alignment in positions, and opposite votes represent conflicting positions between countries. 
 - The relationship between a pair of countries can thus be proxied by the total number of agreeing votes minus the total number of disagreeing votes of the 2 countries. 
 - The project assumes that countries with better bilateral relationships are more likely to vote similarly on UN General Assembly, than countries with worse relationships. 

## (3) Model Development & Analysis 

check our code: [RelationshipScore.ipynb](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/RelationshipScore.ipynb)

and data: [score.zip](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/score.zip), [scoreSum.csv](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/scoreSum.csv)

 - Each time the UN General Assembly votes on an issue, each member should vote “yes” or “no”. Members can also vote “abstain” or be “absent”, etc. The adoption of the issue is then determined by whether “yes” outnumbers “no”. 
 - We form each UN member state into pairs, and the relationship of each country pair is measured by our “relationship score”. 
 - At time 0, each pair has a score of 0. Each time the UN General Assembly has an issue to vote on, the pair may have agreeing or disagreeing votes. 
 - If the pair has agreeing votes (yes – yes, no – no), the score +1. If the pair has disagreeing votes (yes – no), the score –1. If any one of the pair is “absent”, “abstain”, etc., the score does not change. 
 - As time goes on, the score should accumulate, and reflect the relationship of the country pair. We rank the accumulated score for every pair and the pair with highest score is then our 2 countries of best relationship. Also, the pair with lowest score is having the worst relationship. 
 - We would also be able to produce a [graph](https://github.com/LuckYuanZ/CountryRelationByUnVotes/blob/main/Visualization.ipynb) showing how the scores change across history. We can then label important historical events on the graph and analysis the impact of those events on relationships between countries. 

## (4) Results and Conclusions 

 - Recommendations and Policy Implications 
    - Which country pair has the best/worst relationship. 
    - How historical events affect the relationship between countries. 
 - Model limitations 
   - The voting data we use may not be a good enough proxy of country relationship. 
   - The “relationship score” we use may not be a perfect measure under this context. 
 - Further work 
   - Use distance measurement method, or cluster analysis, to analyze the segmentation of today’s world. 
   - Include more data, like Security Council vote, international trade, etc. 
