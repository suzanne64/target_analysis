# Target Analysis
Machine learning for underwater target detection

### Main issue
The results are not great, by that I mean 70% +/- 15%, roughly. The non-comforting thing, is that the stats are
so different (same everything) for different runs. And by a run, I mean training the model ten times and aggregating
to get a target prediction (like the Matlab code).  My thought is I might not be treating the
validation data properly, or maybe with so little data (99 for train/val, 84 for test), I shouldn't use
the validation idea. Simply train and test.  Which begs the question, how similar are train data and test
data?

### ideas explored
adjusting the model: more layers, dropout, BN:  some improvement
adjust the optimizer: adam                      some improvement
trimming acoustically into thirds: 
* all, All
* left third, A
* center third, B
* right third, C
* left and center thirds, AB
Also 'image' data. What is that exactly? , IMAGE

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

