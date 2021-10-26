# Target Analysis
Machine learning for underwater target detection

### Example Acoustic Image

<!--- https://user-images.githubusercontent.com/34384803/138285667-9e897f1b-b6b2-4dc7-a1d6-9a9a0d536ef8.png --->

![HowitzerReplicaR002_00001](https://user-images.githubusercontent.com/34384803/138285667-9e897f1b-b6b2-4dc7-a1d6-9a9a0d536ef8.png)

### Architecture of Base Model

The base model contains three layer, bundles, I'll call them. Each bundle consists of 
* 2D convolution
* batch normalization
* max pooling
* dropout
all with a relu activation function. The last layer of the base model is a fully connected layer 
with a softmax activation function resulting in probablities. A correct prediction has a probability
greater than 70%.

The model is compiled with an SGD (stochastic gradient descent) optimizer. A binary crossentropy loss 
function keeps track of model performance. 

### Snipet of Code

You can read through the code [here](https://gist.github.com/suzanne64/54f4741268a39b67932cb640ccd046cb)
