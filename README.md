## understanding neural networks:

* To understand neural networks, I got most of my knowledge from the book recommended in the task PDF, and these are the keypoints I learnet:

* based on what i learn in chapter 1, the expected accuracy should be over 96%

* The book mainly talks about 2 types of artificial neorns, Perceptrons and sigmoids, both of them output the result based on comparing inputs, weights and biases to a threshhold but there is one critical difference that makes sigmoids a much better choice

### perceptrons:

* The output is 0 if W.X + B <= 0, and 1 if W.X + b > 0

* where W is the wieght, X is the input, and B is the bias

* more weight means the input is more important

* bias makes the node biased towards a certain output (easier to reach an output)

* both weight and bias can be negative

#### main disadvantage:

if the neural network has multiple layers (input + hidden + output), then making small modifications to the weights and biases of some nodes can change the final output drastically from 0 to 1 or from 1 to 0

### sigmoid neurons:

* The output of a sigmoid neuron is binary like the output of a perceptron, it could be 1, 0 or anything in between based on the sigmoid/logistic function.

* at the end, we are going to deal with an output >= 0.5 as true and an output < 0.5 as false, so what is the difference? when there are multiple layers, each layer will get a more accurate input from the layer before it

## implementing the neural network

* in order to implement a nerual network, we need to find the appropriate values for the weights and biases, we can do so using a cost/objective function:

C(w,b) = 1/2n Σ||y(x) - a||^2

WHERE y(x) is the output we want to acheive and a is the actual output

* if the output we want is 5 then y(x) = (0,0,0,0,0,1,0,0,0,0)

* To find the minimum value for the cost/objective function, we need to apply a technique called the gradient descent
