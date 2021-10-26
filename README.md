# Target Analysis
Machine learning for underwater target detection

### Example Acoustic Image

<!--- https://user-images.githubusercontent.com/34384803/138285667-9e897f1b-b6b2-4dc7-a1d6-9a9a0d536ef8.png --->

![HowitzerReplicaR002_00001](https://user-images.githubusercontent.com/34384803/138285667-9e897f1b-b6b2-4dc7-a1d6-9a9a0d536ef8.png)

### Snipet of Code

The base model contains three layer bundles, I'll call them. They each consist of 
* 2D convolution
* batch normalization
* max pooling
* dropout

The model is compiled with an SGD (stochastic gradient descent) optimizer. A binary crossentropy loss function keeps track of the performnce. 

You can read through the code [here](https://gist.github.com/suzanne64/54f4741268a39b67932cb640ccd046cb)
