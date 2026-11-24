Hello!

Here, I am going to just go over the basic outline
of the Neural Network's structure.


Our thing will start with a Neuron

A Neuron's instance variables includes:
* Weight Array, where the index of the weight matches
the index of the connecting Neuron
* Bias value, 0 if the input layer
* Z value, or pre-activated neuron value(weighted sum + bias)
* A value, or post-activated neuron value(weighted sum + bias)
* Layer, a 0 indexed int denoting which layer the Neuron is in
the value 0 indicates the Input layer, while the value n - 1
indicates output layer
* Index, a 0 index int denoting its spot in the vector of
neurons

Inside a Neuron class, the weight array is stored
as a Weight object. 

The Weight's instance variables are:
* Start Index: a 0 indexed int that stores the index of the starting Neuron
in its respective row Vector.
* End Index: a 0 indexed int that stores the index of the ending Neuron in
 its respective row Vector.
* Weight: a weighted multiplier that the activation of the starting Neuron
is multiplied by.

The Weight class MIGHT use the object Vector
I am debating if I actually need this(this would apply
to the weight array in Neuron too)

if a Vector class is made, its features would include:

* Instance Variables:
  * list of Object T that the vector contains
* Methods:
  * A get function
  * A set function

Overall, the Vector class would only exist to create a nicer
API usage. It could also be used in Matrix Multiplication.

Now, we are done with Neurons! The next step in the 
hierarchy is a Layer

A Layer's instance variables includes:
* Neuron Vector/Array of all of the Neurons in a particular
Layer
* Layer index, this is what gets passed to the Neuron's layer
index

