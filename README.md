# mood_classifier_nn
The mood classifier neural network uses th Keras and Tensorflow frameworks to evaluate performance of different deep learning architectures.

The data included 600 training and 160 validation/dev sets of 64 X 64 X 3 potraits labelled as 1, for happy, and 0 for sad.

These were then trained on various architectures and evaluated.

##Data set
This project comes with a h5 datasets of 600 training data and 160 test images of size 64 X 64 X 3.

## Model 1
Model 1 was a simple densely connected deep network with 3 layers. 128 nodes on the 2 intermediate layers and 1 node for the output layer. The intermediate nodes used the relu activation while the output used the sigmoid activation and the binary crossentropy loss to output the probability that a given input image is either sad or a happy face.

This model was trained for 30 epochs using the adam optimization algorithm and a batch size of 64. The result was evaluated to have a final of 97.5% accuracy on the training set and 94.7% accuracy on the validation set. Given that bayes error is close to 0% for this task, the model result shows there is still room for improvement.

## Model 2
Model 2 was a simple convNet consisting of a single convolution layer (with 32 7x7 filters, padding of 3--same convolution and a stride of 1), a single max pool layer and an output layer with one node, sigmoid activation, and binary crossentropy loss.

The model was also trained for a total of 30 epochs, batch size of 64 and with the adam optimization algorithm and relu activation. The results showed an improvement when compared with model 1 with a training accuracy of 99.17% and validation accuracy of 96.67%.
