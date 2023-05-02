Download Link: https://assignmentchef.com/product/solved-cmsc421-project-3
<br>
What you’ll need to do

<ul>

 <li>Implement and train a basic neural network with backpropagation

  <ul>

   <li>We’ll give you part of the code, you need to fill in the details</li>

  </ul></li>

 <li>We’ll give you a ZIP archive containing two files:

  <ul>

   <li>py: the class and method outlines</li>

  </ul></li>

</ul>

○    studenttest.py: code to train and test your neural network

<ul>

 <li>py contains some, but not all, of the necessary methods

  <ul>

   <li>You’ll need to write the others yourself</li>

  </ul></li>

</ul>

activation(z):

<ul>

 <li>This is the activation function used in the feed-forward compution of the network.</li>

 <li>The included function is the sigmoid, but you can change this as you see fit.</li>

</ul>

Here is a graph showing visually how the sigmoid function works:

sigderiv(z):

This is the derivative of the sigmoid function

<ul>

 <li>You’ll need to use it to update the values when training your neural network</li>

 <li>If you use an activation function other than the sigmoid, then you’ll need to use a different derivative than the one returned by sigderiv</li>

</ul>

Class: neuralnetwork:

<strong>__init__(self, size, seed):</strong>

<ul>

 <li>This function will initialize the weights and biases for a neural network of the size specified by the ‘size’ parameter. ● The ‘size’ parameter is a list of the form

  <ul>

   <li>inputsize, hidden layer 1 size, … , hidden layer n size, output size]</li>

  </ul></li>

 <li>Example on next page</li>

</ul>

Example of __init__

Suppose size = [3, 4, 4, 1]

<ul>

 <li>then __init__ creates the network shown at right</li>

 <li>It initializes a variable weights = [ [v<sub>11 </sub>v<sub>12 </sub>v<sub>13</sub>]</li>

</ul>

[v21 v22 v23] [v31 v32 v33]

[v41 v42 v43] …]

<ul>

 <li>each v<em><sub>ij </sub></em>is the weight on the connection to unit <em>i </em>in the first hidden layer from unit <em>j </em>in the input layer</li>

</ul>




Methods/Classes provided in studNet.py (continued) forward(self, input):

Given a vector of input parameters of form:

[ [parameter 11, p12, …, p1n] [p21, p22, …, p2n] … ] This method will return a 3-tuple:

<ul>

 <li>the output value(s) of each example (the variable ‘a’ in the source code)</li>

</ul>

○    The values before activation was applied after the input was weighted (the variable ‘pre_activations’)

○   The values after activation for all layers (the variable ‘activations’)

<ul>

 <li>The reason it returns ‘pre_activations’ and ‘activations’ is because you’ll need them for updating the network</li>

</ul>

What you have to do:

<ul>

 <li>Implement a method called train(…)

  <ul>

   <li>test_train calls it to train the neural network on the data set</li>

  </ul></li>

</ul>

○   To do this training, you will need to perform back propagation and calculate deltas

<ul>

 <li>We’ve provided method headers for train(), backpropagate(), and calcDeltas()

  <ul>

   <li>If you want to use them, you’ll need to write the method bodies</li>

  </ul></li>

</ul>

○    But you don’t have to use them if you want to implement your network differently

<ul>

 <li>The only things that must stay the same for testing:

  <ul>

   <li>you <strong>MUST </strong>have the <strong>test_train </strong>method and <strong>predict </strong>as provided</li>

  </ul></li>

</ul>

○    test_train must return an instance of your neural network that can be used to call predict(a).<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/311.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2022/04/311.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>