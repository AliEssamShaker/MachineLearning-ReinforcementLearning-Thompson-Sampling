# MachineLearning-ReinforcementLearning-Thompson-Sampling

Reinforcement learning :

Thompson sampling:-

We need to find the right balance between efficient exploration and exploitation. Unlike, the UCB algorithm, the Thompson Sampling algorithm is a probabilistic algorithm. The algorithm has those distributions which represents our perception of the world and where we think the actual expected return for each of those machines might lie. 

One of the advantages of Thomas sampling over UCB is that it can accommodate delayed feedback. 

I will be using the same dataset that I used for the UCB algorithm. The Thompson Sampling algorithm resulted in much better results (was able to determine the best advertising in the least amount of rounds possible) than the UCB algorithm.

Here is how the algorithm works:

-  At each round n, we consider two numbers for each ad i:
      - N1(n) :- the number of times the ad i got reward 1 up to round n, 
      - N0(n) :- the number of times the ad i got reward 0 up to round n.

-	For each ad i, we take a random draw from the distribution below:
 	0i(n) = B( N1(n)+1, N0(n)+1 )

-	We select the ad that has the highest 0i(n)
	
