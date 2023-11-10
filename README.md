# I310D-Data-Bias-Assignment
Assignment Submission


# **Data Bias Assignment: Testing Model Fairness for Hate Speech Tweets for two marginalized groups of American Society**

**Chinmayee Channuri**




# **Aim + Methodology:** 

In this study, I aimed to utilize the Perspective API and test it with regards to social media hate speech against two marginalized groups of society, Asian Americans and African Americans. Hence, my sensitive attributes were "Against Asian-Americans" and "Against African Americans". 

I collected a sample size of 50 tweets (comprising of tweets with hate speech for Asian Americans and African Americans), and marked them with binary identifiers, "Toxic" or "Non-Toxic" according to how I felt about them, or what my reaction was to them when I read them. These values became my expected values. 

Then, I utilized the Perspective API to run each tweet text through it to receive a predicted value for the toxicity of the tweet, which was a number in the range of 0-1. 

I loaded the CSV file with my data in it using Pandas into my Jupyter Notebook to analyze and apply the accuracy study to it. 

The main transformation I performed for my dataset was when I added a seperate column, "Predicted Label" into the data frame to deem a tweet as toxic or non-toxic based on the predicted values from Perspective API.

Then, I analysed the Model Fairness from the Predictive Equity standpoint to measure and observe the accuracy performance for each category, Toxic v. Non-Toxic, for each ethnicity group, Asian Americans and African Americans. 


# **Hypothesis:**

I hypothesize that there would be differences between the accuracies for the toxicity levels for hate speech against Asian Americans and African Americans to account for the dataset that Perspective API was potentially trained on. 



#**Analyzing the Accuracy of the Classifier:**

The overall accuracy of the model is moderatly high, at 66%. But, further analysis must be conducted to understand if the model is able to take into consideration the semantics, mood,message, and overall tone of the tweet rather than just taking the words used at face value and mapping them to being toxic or non-toxic.


# **Final Insights**

If we compare how close the accuracy values are for both Asians and African-Americans for the Toxic Comments category, we can see that they are roughly close. This means that if a comment is toxic, the model can predict it's toxic with a 61-63% acccuracy. 

But what is troubling here with the Perspective API usage is the difference in accuracies for the Non-Toxic catgeories for Asians and African-Americans. For African-Americans, the accuracy is at a steep 90%, but for Asians, it's only 53%. This difference indicates that the model is able to recognize toxicity for hate speech against African Americans over that against Asians. 


# **Detailed Evaluation for Asian American Group**
 
**To identify why there is a discrepancy just for the Non-Toxic comments for Asian Americans**

It was surprising to see 61.5% accuracy for the Toxic category for Asian Americans, since most if not all tweets in the dataset were offensive. But, the Perspective API model was not able to detect this due to any subtleties in language, or. Something that could've helped us to delve deeper into understanding the real reasons as to why the accuracies were lower is if the Perspective API model had algorthmic transparency. If us users were given access to the data that the API model was trained/tested on would give us more context.  


The accuracy for the Non-Toxic comments for Asians indicated to only be about 50% correct, because of how some tweeters decided to use swear words and profanity to express their frustration about the racist situation post COVID-19 outbreak in the US but they weren't trying to demonstrate any hate towards Asians. This shows that the Perspective API model is weak in understanding tone and mood of the semantics used in statements. In these tweets, they were using toxic vocabulary, like profane language, due to which the API automatically flagged them as "Toxic" but are really not and rather are showing support and defending the Asian American population on Twitter. 


# **Conclusion + Limitations + Scope for Further Research**

Based on our study conducted, the analysis we performed, and insights we drew from it, we can conclude that the scope for th ePerspective API being able to identify or demarcate differences in semantics, mood, message, and overall tone of the claim that is inputted is quite limited. This was shown by how the accuracy values were extremely different for the Non-Toxic category in specific for Asian Americans and African Americans. This bias in identifying toxicity for African Americans more than Asian Americans propels us to think about the potential limitations of the model. 

As identified above, the main limitation of the Perspective API model is that we don't have much context on the dataset it was trained on. There is not much Algorithmic Transparency here, as us users do not have access to the dataset that the model was trained on. This context would help us understand why there was a difference of 40% of accuracy between the Non-toxic accuracy for both marginalized groups. 

The scope for further research is large here, since this study uncovered great insights into racial differenciation between two different set of marginalized groups in social media. Apart from increasing the sample size, one of the opportunities that can be explored is considering other social media other than Twitter like Facebook, Instagram, and etc. Potentially, we can compare the results obtained for Tweets vs. Facebook posts and understand whether there are more factors affecting it. Another method to extend this research is considering the political side of it, since political arguments are very common in the disucssion of discrimination against marginalized groups in the US. These methods would both equally be interesting and intriguing to explore. 
