# Recurrent Neural Network
Recurrent neural networks (RNNs) are deep learning models, typically used to solve problems with sequential input data such as time series. A recurrent neural network, by contrast, retains a memory of what it has processed in its recent previous steps (we’ll come back to the “recent” qualifier in a minute). It makes recurrent connections by going through temporal feedback loops: the output of a preceding step is used as an input for the current process step. Unlike amnesiac FFNNs, this memory enables RNNs to process sequences of inputs without loosing track. The loops make it a recurrent network.

The hidden layers are located between the input and the output layer. In an RNN, they not only produce an output, but they also feed it back (“backpropagate” it) as an input for training the hidden layer on the next observation. They carry out the training by adjusting the synapse weights throughout the neural network. The network recalibrates the weights for both the current and the previous inputs, multiplies the vector of input values with the vector of new weights (thus raising or lowering their importance with respect to the training goal of lowering the prediction error), and passes the vector of results on as an input to the next layer. By adapting the weights, the hidden layer incrementally derives a kind of function which transforms the input values to output values that approximate the actual observations in the training dataset. But the function that maps the inputs to the outputs is not expressed as a closed-form equation — it remains hidden. If the RNN deals with time series, each period will be represented by a node, holding the period’s observational value.

![[rnn.png]]

---
Topics :: [[Neural Networks]] [[Machine Learning]]
Reference ::
Type :: #atom
Creator :: Michael 
TAF :: 
Discussion ::
Dis_Topic :: 
Resolved ::
Date :: 2022-07-15 16:40
