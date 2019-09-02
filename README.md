# Tensorflow.js-Image-Classification
Implementing a K-NN classifier using Tensorflow.js

NOTE: This is the result of following the Tensorflow tutorial available at 
https://www.tensorflow.org/js/tutorials/transfer/image_classification. I suggest you give it a go and experiment with Tensorflow.js yourself!

<h2>K-NN Classification</h2>

K-Nearest Neighbours is a classification method that uses similarity/dissimilarity metrics to classify new elements. Since it needs labeled samples to classify against, K-NN is a supervised learning method. When classifying a sample, the distance between that and the existing ones is calculated. The class our sample belongs to is that of the closest "training" sample. Additionally, we can order the distances to see how likely it is for our sample to belong to each of the classes (from most to least if the ordering is done in ascending distance).
