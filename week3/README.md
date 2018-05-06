# Review :  Learning to predict by them methods of temporal difference

This paper introduces a new way of training which claims to be better than conventional supervised learning. Better in perfomances and also when there isn't previously recorded data as its prediction of final outcome is nased on the predictions that lead
--We feel that's not the case everytime.

In real life scenarios, the outcome of any process can be predicted from the events leading to it with a little previous data. Though an instance of the events is used to predict, it might not be correct everytime.
This was shown in the game-playing example.

This method exploits the temporal strucure of a sequential data. As it uses previously predicted value to predict the next value, this is one drawback of this method, ie, what if it predicted wrong the first time? The error would propogate and ultimately lead to wrong overall presiction.

Now this learning is used when a similar situation occurs. Keeping in mind of this experience, the algorithm does the predictions again.

Though the small chance of going wrong is present, it is faster than its fellow counter-parts. Since it uses the previously learnt experience, it doesn't have to learn from scratch.

--Rather than waiting till the actual data is obtained and then calculatin the loss function, this process compares the 2 most recent predictions

Once the prediction is done, during the learning process, weight cnagges are done similar to supervised learning.

Later, a family of TD procedures are introduced. Here, a parameter λ is used to generalize the learning procedures. This parameter is used to make more weight changes to more recent ones. That is because the immediate  previous ones are the ones which has more impact on the dinal prediction. λ gives us a control on how recent ones shoud have the weight changes.

Also, various λ values were used to choose the best learning rate. The usual supervised-learning seems to be the worst of all.

The perfomance of the algorithm was increasing as λ was reduced below 1. But λ=0 represents error is propogating only to the previous node.
Though this can be used in a loop to propogate the learning back, we lose the advantage of faster computation.

TD(0) seems to be faster while data is presented repeatedly. Though this process doesn't give perfect or universal results, it is better tha supervised learning. Usually, if data is repeatedly presented, it would overfit and could not be generalized.

An absorbing markov model is used to model the sequential data. probabilities of various states is taken based on maximum likelihood from previous experiences.

For TD methods to work, the sequential data is a must. This kind of learning is highly suitable for real time scenarios. Infact, this is how our brain works in recognizinf objects. We dont try to identify an object from scratch everytime. Instead we start with an object of similar characteristics and then we work our way on. 
