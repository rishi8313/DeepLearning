Will Starting with MLP/ANN
1) 2 layer perceptron to train a model to do logical operation.
2) using 
   - stochastic gradient descent optimization
   - binary_crossentropy loss function
   - uniform_initializer
   - linear activation function
   - accuracy as the metrics

Sometimes, the example given won't work, as the training data i.e. only 4 rows are available for training. Whereas in real dataset, you will get 1000's or may be millions of rows.

This starting exercise is only for making us, used to create a Sequential model using Keras.

### Explanation of ANN starts from here

Basically, Think of input as a combination of different features.

Below example is overly simplified.

For an Ex : If you are trying to predict that a person has a particular disease or not (say dengue)
      so the tests which are done to check whether a person is sufferring from dengue are the
      input features. The features in this case would be following
   - Whether the person has fever (binary feature) - value 0 or 1
   - Degree of fever (numerical feature)
  
   Note: There can be categorical features as well (Enums) like category of the age - child (0), adult(1) or senior citizen(2) 
            
   These features are represented as a matrix, hence we use capital x (X) for input features.
   y is the output.

                  x1(hasfever)  x2(fever in degree) y(dengue or not)
                      1             101               1
                      0             98                0

   so, for first entry in this dataset, x1 = 1 and x2 = 101
       for second entry it is , x1 = 0 and x2 = 9
                
Our task is to feed all these entries/rows to the neural network and make the network learn the value of y.

for this, weights are multiplied to each inputs, which is a matrix W.

Here, we have 1 output and 2 input, hence the weight matrix is of order 2(row) X 1(columns).

[w1

 w2]

our output is nothing but a y' (y-hat, y-dash, can be called differently) which is defined as follows

   y' = f(w1*x1 + w2*x2) for above example
   
  where f(z) is the activation function and z = w1*x1 + w2*x2 in this case.
  
  f(z) can be sigmoid, tanh, relu, linear and many others.
  
Details are given in the [Deep Learning Stanford] (http://ufldl.stanford.edu/tutorial/supervised/MultiLayerNeuralNetworks/)
  
Challenge - We will discuss why XOR function is not learnable using above perceptron.
