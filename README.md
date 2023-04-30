Download Link: https://assignmentchef.com/product/solved-csce633-homework-3
<br>
<h1>Question 1: Activation Function in Neural Networks</h1>

Consider a two-layer fully-connected network with <em>D </em>input features, one hidden layer with <em>M </em>nodes, and one output layer. The activation function of each node is a sigmoid function of the form sigmoid(

<ul>

 <li>Provide a schematic representation of the network. Define the variables for the input, theoutput, and the weights.</li>

 <li>Express the output as a function of the input.</li>

 <li>Calculate the number of parameters that need to be inferred.</li>

 <li>Show that there exists an equivalent network with hidden unit activation functions givenby the hyperbolic tangent, which computes exactly the same function, where the hyperbolic tangent is given by</li>

</ul>

<em>Hint: </em>First find the relation between sigmoid(<em>α</em>) and tanh(<em>α</em>), then show that the parameters of the two networks differ by linear transformations.

<h1>Question 2: Image processing for human faces</h1>

In this problem, we will process face images coming from the Yale Face Dataset: http:

//vision.ucsd.edu/content/yale-face-database. This dataset contains images of the faces of 15 individuals. For each individual there are 11 images taken under a variety of conditions e.g., the person makes a happy expression, wears glasses etc.

1

<ul>

 <li>Download the dataset from the above URL. <em>Implement </em>Principal Component Analysis (PCA) on the input images. Assume that the input vector of PCA contains all rows of an image stacked one on top of the other. You can use available libraries that calculate eigenvalues and eigenvectors of a matrix. <em>Hint: </em>Don’t forget to normalize the data.</li>

 <li>Plot a curve displaying the first k eigenvalues <em>λ</em><sub>1</sub><em>,…,λ<sub>K</sub></em>, i.e. the energy of the first K principal components. How many components do we need to capture 50% of the energy?</li>

 <li>Plot the top 10 <em>eigenfaces</em>, i.e. the eigenvectors <strong>u<sub>k</sub></strong>, <em>k </em>= 1<em>,…,</em>10 obtained by PCA.</li>

 <li>Select a couple of images from the data. Use the first <em>k </em>eigenfaces as a basis to reconstruct the images. Visualize the reconstructed images using 1, 10, 20, 30, 40, 50 components. How many components do we need to achieve a visually good result?</li>

</ul>

<em>Hint: </em>Reconstruction of an input vector <strong>x </strong>based on the eigenvectors <strong>u<sub>1</sub></strong><em>,…,</em><strong>u<sub>K </sub></strong>is given by the following expression <strong>x</strong><strong>u<sub>k</sub></strong>, where <em>c<sub>k </sub></em>= <strong>u</strong><em><sup>T</sup></em><strong><sub>k</sub>x </strong>is the projection of the input image to the <em>k<sup>th </sup></em>eigenvector.

<ul>

 <li><em>Perform face recognition: </em>Split the input data into training and testing <em>making sure that every person is included in each set</em>. Use any of the classification methods that we have learnt so far to recognize a person’s identity. Use as input features the transformed feature space that resulted from PCA. Experiment with different number of PCA components through a 5-fold cross-validation. Report the recognition accuracy on the test set.</li>

 <li><strong>Bonus: </strong><em>Data augmentation: </em>Data augmentation is a way to increase the size of our dataset and reduce overfitting, especially when we use complicated models with many parameters to learn. Using any available toolbox or your own code, implement some of these techniques and augment the original Yale Face Dataset.</li>

</ul>

<em>Hint: </em>You can find more information in <em>hw3 DataAugmentationUsingDeepLearning.pdf </em>from <em>Homework 3 </em>folder on Piazza and in the following link: https://machinelearningmastery.com/image-augmentation-deep-learning-keras/

<ul>

 <li><strong>Bonus: </strong><em>Face recognition with CNNs: </em>Use CNNs to perform face recognition in the augmented Yale Face Dataset. Use the same split for the train and test set as in Question 2e. Experiment with different CNN parameters, e.g. filter size, stride size, activation function, dropout, pool size, etc.</li>

</ul>