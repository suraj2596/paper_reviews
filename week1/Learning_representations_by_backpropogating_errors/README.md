# Review : Linear Representations by back-propagating errors
###### David E. Rumelhart, Geoffrey Hinton & Ronald J. Williams


## Abstract:
This paper mainly focuses on a new learning procedure called Back Propagation and the math required for the same. As a result of back propagating errors, the hidden layers learn the correlation among the previous layer outputs which is not possible if inputs were directly connected to the output.

## Architecture:
Proposed architecture for this neural network is a layered network, ie, extra layers between input and output layers called hidden layers. Hidden units are useful in capturing the patterns in the whole input sequence. This would not have been possible without introducing hidden layers.

Few rules have to be followed for connecting various units among various layers. Connections between units of same layer and between layers of higher and lower are not allowed. Few connections can be skipped. Inputs are given to input layer. These input units are connected  to various units in next layers.

Each connection has a value called weight which multiplies the output of previous unit before feeding it to a linear function and then to a limiting function. Initially, these weights are arbitrarily assigned and these weights are adjusted over time while training. 

Along with weights, there are ‘bias’ which is nothing but a threshold or a constant value present in all hidden layers. Usually its 1.

When inputs are fed to the network for the first time, it might give out something that is not even close to the desired output. To tune the output to our requirements, we have to change the weights. This is where backpropagation comes into the picture.

First we need a metric on how accurate or how near/far we are from desired output. This is called total error E which is sum of square of difference of actual and predicted outputs.

Using E, we adjust the weights by taking the gradient along that dimension. To get the gradient of final error wrt input, we take the computational graph and find gradients between all consequent blocks along the graph and multiply them. This is called chain rule.




## Capturing symmetry in input sequence:
In this paper, a 6-2-1 fully connected network with weights initialized randomly between 0.3 and -0.3 is considered. After training with an optimal setting, the weights get adjusted in such a way that the neural network outputs 1 if input is symmetric. 

This happens because the weights corresponding to one particular hidden node are mirrored/negated corresponding to another one. As a result, for a particular input, we get a zero output from hidden nodes(due to negative bias).

Also, the weights are in binary combination (1:2:4) so that only for a unique input ie symmetric  about the center, the output is one(due to positive bias).

## Determining relations among various inputs:
In this scenario, 2 similar trees are declared. Each node in the tree is a triplet ie, it consists of 2 persons and their relationship. A 5 layered neural network is used to predict the other person, given one person and the relationship.

## Application of Back Propagation on recurrent neural network:
A recurrent network can be dealt just like a layered network but it has to take care of 2 situations. 

First one is the outputs of nodes at each time step: they must be stored in order to apply during the backward pass. 

Second one is weights between different layers: as the same weights will be used, during the weight update stage, we take the average of gradient across all layers and use that value for finding the optimal value.

## Drawbacks of Back Propagation:
At time, we might end up in local minima. Also, this local minima and global minima won’t produce much of a difference most of the times. There is a rare case of bad performance due to local minima. And when this happens, increasing the connections will solve the problem. 
