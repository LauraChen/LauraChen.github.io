---
layout: single
title:  "Web Scraping for the Greater Good"
date:   2018-01-28
categories: Projects
author_profile: true
---

One of the coolest parts of studying data science is applying it to real life questions. One thing I’ve thought about a lot through my experiences with Net Impact at NYU and during consulting projects at nonprofits is the concept of how to run charities efficiently. When I found out our second project was on web scraping and linear regressions, I decided to do an analysis of charities.   
  
![One of the best scences in the movie](https://media.giphy.com/media/I6rM4juHFpL3y/giphy.gif)

I pulled data from the Charity Navigator website and created a model to predict what percentage of a charity’s total expenses actually go towards charitable programs versus administrative and fundraising expenses.  I do recognize that this metric is not entirely fair. I would much prefer to measure the total benefit provided by a charity such as the number of adoptions facilitated or the number of vaccinations administered. Since it is only a percentage, it also does not take into account the total benefit of a charity. Nonetheless, this is the metric that was available and I think it serves the purpose for this analysis.  
  
The model is far from perfect, with an R-squared of .57, but it was interesting to see which factors mattered the most in my model. Unsurprisingly, I found that organizations that have transparent reporting policies and accept government grants tend to allocate more of their budget to programs. I saw a negative relationship between my dependent variable and fundraising expenses, which also makes a lot of sense. I also saw that charities that offer services for a paid fee spend less on their charitable programs. My hypothesis would be that these organizations are spending more on overhead expenses such as real estate and equipment.  
  
As I mentioned, the % of a charity's budget comprising of program expenses is just one metric but it is not totally giving the full picture. It would be great to have more data to incorporate into the model such as the size of the charity or whether it operates on a national or local level.
