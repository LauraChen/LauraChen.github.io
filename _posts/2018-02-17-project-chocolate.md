---
layout: single
title:  "Chocolate Flavor Rater"
date:   2018-02-17
categories: Projects
author_profile: true
---
  
They say you should find work you love. I love chocolate. I focused this project on classifying chocolate bars based on expert reviews from the Manhattan Chocolate Society. Whether you are trying to break into the chocolate industry, or you're just a connoisseur looking for the next delicious bar to eat, hopefully these findings will be of interest.  
  
The Manhattan Society of Chocolate maintains [a database](http://flavorsofcacao.com/chocolate_database.html) with information about more than 1,800 chocolate bars as of Feb 2018. My goal with this project was to determine the factors that would lead to a highly rated bar of chocolate. The official ratings provided in the database were from 1 to 5, but I binned the data into Low, Medium, and High tiers to even out the classes.  
  
### Which factors mattered?
The most important predictor of high quality chocolate ended up being whether the bar was crafted from Criollo beans. Upon further research, I found that this bean is considered one of the most prized in the world for it's rarity and fine flavor. Due to the rarity, I would also infer that chocolatiers who use this bean are probably more likely to meticulously craft their recipes to perfection. They are definitely not using this in your average Hershey's bar.  
I found it interesting that the location of the company processing the chocolate actually had a much bigger impact on the chocolate taste than the region where the beans were sourced. I interpret this to mean that local processing techniques and recipes can have a greater impact than the raw materials themselves, but would love to see further data on this.  
  
![Map of Chocolate Production](\assets\map-of-chocolate.jpg)
  
### Technical Details  
The tiers of chocolate ratings were quite imbalanced at the start, so I had to upsample my training set to increase precision of the model.  I experimented with several models such as Logistic Regression, Naive Bayes, and Support Vector Classification, but my ultimate winner was the Random Forest model. As I further tuned the model, I prioritized precision over accuracy and recall because I'd rather let some highly rated chocolates slip through the cracks than accidentally predict that Low rated chocolates are High.  
  
In the end, my final model had about 48% precision and 41% recall for predicting High ratings for chocolates. While the performance was not the absolute best, I am fairly pleased with it considering how limited the data available was.   
  
### Areas of further exploration  
I think there are a ton of factors that go into a chocolate bar's taste. I would like to see additional data on percentages of other ingredients such as sugar, vanilla, and emulsifiers. It would also be great to have details on processing techniques and agricultural techniques.   
  
The ability for a chocolate bar to receive a High rating from a panel of experts is one thing, but what about flavor ratings from real customers? It would be interesting to see how flavor preferences could be used to recommend chocolates that a specific type of person would enjoy. I think it would also be interesting to investigate sales numbers of different chocolate bars to see which ones are the most profitable.  
