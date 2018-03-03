---
layout: single
title:  "Supervised Learning Models and Chocolate"
date:   2018-02-17
categories: Projects
author_profile: true
---
  
The most convenient part about building a supervised learning model for chocolate is that you can stress-eat in the name of "research". Jokes aside, I focused this project on classifying chocolate bars based on expert reviews from the Manhattan Chocolate Society. Whether you are trying to break into the chocolate industry, or you're just a connoisseur looking for the next delicious bar to eat, hopefully these findings will be of interest.  
  
The Manhattan Society of Chocolate maintains [a database](http://flavorsofcacao.com/chocolate_database.html) with information about more than 1,800 chocolate bars as of Feb 2018. My goal with this project was to determine the factors that would lead to a highly rated bar of chocolate. The official ratings provided in the database were from 1 to 5, but I grouped the data into Low, Medium, and High tiers to even out the classes.  
  
![choco-pie](\assets\choco-pie.jpg)
  
### Which factors mattered?
The most important predictor of high quality chocolate ended up being whether the bar was crafted from Criollo beans. Upon further research, I found that this bean is considered one of the most prized in the world for its rarity and flavor. Due to the rarity, I would also infer that chocolatiers who use this bean are probably more likely to meticulously craft their recipes to perfection. They are definitely not using this in your average Hershey's bar.  
  
I found it interesting that the location of the company processing the chocolate actually had a much bigger impact on the chocolate taste than the region where the beans were sourced. I created a D3 visualization to show a the average chocolate bar rating from different countries around the world. Darker colors represent a higher rating. I saw that Latin America and parts of southern Europe were producing many of the best bars in the world.    
  
![Map of Chocolate Production](\assets\map-of-chocolate.jpg)  
[Click for the full interactive version](https://bl.ocks.org/LauraChen/raw/e6cf35cd59ed0a756467d9d35a7f0682/)  
  
Why does location of production seem to matter more than bean origin? I interpret this two ways:  
1. Cocoa beans require very particular growing conditions. Thus, many different companies end up sourcing their beans from the same few locations. Within the sample, the vast majority of beans were sourced from Latin America and the Caribbean (about 70%). As a result, vastly different bars are showing up as from the same origin and the effect of bean origin is minimized. 
2. Local processing techniques, recipes, and culture/tastes can have a large impact on the final product.  
  
Between the two, I believe #1 is likely the more significant reason. I would love to see additional data to further investigate these ideas.  
  
### Technical Details  
The tiers of chocolate ratings were quite imbalanced at the start, so I had to upsample my training set to increase precision of the model.  I experimented with several models such as Logistic Regression, Naive Bayes, and Support Vector Classification, but my ultimate winner was the Random Forest model. As I further tuned the model, I prioritized precision over accuracy and recall because I'd rather let some highly rated chocolates slip through the cracks than accidentally predict that Low rated chocolates are High.  
  
In the end, my final model had about 48% precision and 41% recall for predicting High ratings for chocolates. While the performance was not the absolute best, I am fairly pleased with it considering how few features I was able to include.   
  
### Areas of further exploration  
I think there are a ton of factors that go into a chocolate bar's overall experience. It would be interesting to see more data on other qualities such as acidity, bitterness, texture, etc. I would like to see additional data on percentages of other ingredients such as sugar, vanilla, and emulsifiers. It would also be great to have details on processing techniques and agricultural techniques.   
  
The ability for a chocolate bar to receive a High rating from a panel of experts is one thing, but what about flavor ratings from real customers? It would be interesting to see how flavor preferences could be used to recommend chocolates that a specific type of person would enjoy. I think it would also be interesting to investigate sales numbers of different chocolate bars to see which ones are the most profitable.  
