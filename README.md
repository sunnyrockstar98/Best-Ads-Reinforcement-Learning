# Best-Ads-Reinforcement-Learning


This repo aims to use Upper Confidence Bound technique and Reinforcement Learning to find the best way of presenting SUV ads on a website.

The problem is that a car company is about to launch a brand new SUV in a month. To market it properly the Marketing and Publicty team came up with 10 different advertisments for the SUV....in different scenarios like near a bridge or forest or a stadium, etc.

Now online advertising these days can generate loads of revenue and the company's website has no idea which ad the customers would love the most or click the most.

So we got a sort of simulation dataset called "Ads_CTR_Optimisation.csv" which has 10 columns for 10 ads and around 10,000 rows where each row is a user who has just logged into the website. (I will explain in details later!!)

Each time the user logs into the website he/she is presented any 1 of the 10 ads. If the user clicks the ad it is considered as 1 else 0.

Now online websites generate money through this click through rate (CTR) of the ads. But customers hardly click on ads they don't like.
So if the car company could somehow find a method to presesnt ads in a manner (obviously random ads don't give a great reward) that would generate high reward for them it would be great!!

That method is Reinforcement Learning or Online Learning where the website learns from its mistakes or past actions.
The algorithm at play is the UCB (Upper Confdence Bound)
-----------------------------------------------------------------------------------------
Now coming back to the dataset "Ads_CTR_Optimisation.csv"...(it's a bit tricky).
Simplest way to explain is assume that this dataset is generated by GOD!!   :P

The row 1 for instance has 1s in columns 1 5 and 9:  interprets as  : the first user if is presented with ads 1 5 or 9 of the SUV he/she will end up clicking it.

Obviously this is something no one knows....(only GOD can tell wether this guy will click the ad or not)..
----------------------------------------------------------------------------------------------------------------
So the question is
In real life how do we generate this dataset (CTR optimisation)?

Ans:
In real life, your dataset would be streaming data (data that is integrated in real time). You can use Spark for streaming data. Each time a user connects to the web page, you get more data. 
I am just telling God Knows because only God Knows on which ad the user is going to click. And we can't know that because we can only show one ad to the user.
The tricky thing to understand is that we already have the data because it's a simulation.  

Simply this dataset is a sort of previous traffic log of the website helpful in training or preping the model 


Now I have put up two code files one to show the reward we get when we randomly give ads to the user at each round and other to show how UCB would give almost twice the reward!!


# Techniques to increses the reward even more would follow soon!!!
