---
layout: single
title:  "The Truth About Secrets"
date:   2018-03-01
categories: Projects
author_profile: true
---
  
## Uncovering hidden themes in anonymous social media through Natural Language Processing 
  
> Nothing makes us so lonely as our secrets. – Paul Tournier  
  
Secrets can take so many forms: from lighthearted to intense, regrettable to silly, and everything in between. You can learn a lot about people from the things they hide from themselves and from others. By definition, you rarely get to peek behind the curtain, but people become surprisingly honest and vulnerable when you give them the benefit of anonymity. [Whisper](whisper.sh) is an anonymous social media platform for sharing secrets where I collected the data for my analysis.  
  
![Data about secrets](/assets/whisper-data.jpg)
  
You can see what people tend to talk about from a high level in this word cloud, but let’s dig a little deeper.  
  
# Sentiment Analysis
I used Vader sentiment Analysis to get the sentiment scores for all secrets in my dataset. A higher score means the message is generally more positive, while a lower score means it is more negative.   
  
 I was surprised to find that the secrets were generally fairly balanced, with most falling on the neutral or slightly negative side. The image below shows the exact breakdown of the scores as well as some examples of messages within those groups.   
  
![Compound sentiment score](/assets/whisper-sentiment.jpg)
  
 
  
# Topic Modeling
I extracted topics from the data using Non-negative Matrix Factorization (NMF). I summarized the top 10 topics as follows:  
1. Parents/family
2. Sex
3. Jobs/Money
4. Exes
5. Hatred
6. Marriage
7. Kids
8. Pregnancy
9. High School/College
10. Dating
  

I used the highest NMF coefficient for each secret to classify it into a topic. The illustration below shows the distribution of topics across my whole dataset.  
  
![Distribution of Topics](/assets/secret-topic-dist-all.png)  
  
Interestingly, I found a very different distribution of topics among positive and negative secrets from my sentiment analysis.  
  
![Distribution of Topics by Sentiment](/assets/secret-topic-dist.png)  
  
Many secrets had extremely low NMF coefficients (less than .00001). I experimented with my topics, expanding them beyond interpretability, and played with clustering models such as DBSCAN and K-means. I couldn’t seem to get any meaningful results for those noisy points. As I investigated them, I found that there were simply a lot of secrets along the lines of this: “It feels like a sin to wash bacon grease off a pan”. Totally random thoughts that anyone would have difficulty categorizing.  
  
# Web App Mockup  
There are a lot of potential practical applications for sharing your secrets. There is some comfort in knowing that you’re not alone. I made a simple mockup of a site where users can type their secret and the model will pull up the most similar secrets by cosine similarity.  
  
![shared secrets app](/assets/shared-secrets-app.png)  
  
# Conclusion  
There is a lot to learn from secrets. I would like to continue to explore them from additional angles. Some other ideas I have include building a supervised learning model to classify the higher themes of secrets (such as insecurities or regrets). I would also like to study secrets of people from other countries to understand how taboos may vary by cultures. Finally, I think it would be fascinating to compare my findings from Whisper to a public social media site such as Instagram or Facebook. When you look at a word like “pregnancy”, for example, you’ll see that it carries a lot of baggage on an anonymous site like Whisper. However, it is a topic that many people discuss positively, or even boastfully, on Facebook.  