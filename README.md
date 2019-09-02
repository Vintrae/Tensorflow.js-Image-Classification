# Tensorflow.js-Image-Classification
Implementing a K-NN classifier using Tensorflow.js

NOTE: This is the result of following the Tensorflow tutorial available at 
https://www.tensorflow.org/js/tutorials/transfer/image_classification. I suggest you give it a go and experiment with Tensorflow.js yourself!

<h2>K-NN Classification</h2>

K-Nearest Neighbours is a classification method that uses similarity/dissimilarity metrics to classify new elements. Since it needs labeled samples to classify against, K-NN is a supervised learning method. When classifying a sample, the distance between that and the existing ones is calculated. The class our sample belongs to is that of the closest "training" sample. Additionally, we can order the distances to see how likely it is for our sample to belong to each of the classes (from most to least if the ordering is done in ascending distance).

|  We start with an empty model   |  We then add some **training samples** with their labels   |
| --- | --- |
| ![Empty graph](/../readmeimages/images/empty_graph.png?raw=true) | ![Graph with training samples](/../readmeimages/images/sample_points.png?raw_true) |

| Once trained, we can add our **testing sample** | The nearest training sample determines the class of ours! |
| --- | --- |
| ![Graph with training samples and a testing one](/../readmeimages/images/test_sample.png?raw=true) | ![Graph with test sample classified](/../readmeimages/images/test_sample_classified.png?raw=true) |

Here we can see that despite not having the prettiest of faces, this sample model classified me as belonging to the "Human" class based on previous samples. In the real world we would optimally want more samples than this, but it does provide a good example.

<h2>Tensorflow.js</h2>

Tensorflow.js is a Javascript implementation of the popular Tensorflow library used for many Machine Learning applications. It enables us to use off-the-shelf JavaScript models or convert Python TensorFlow models. Moreover, we can retrain models for our data, which is what I have done in this project. In my case I took the MobileNet K-NN classification model and adapted it to be able to distinguish between 4 facial expressions: 
* Happy
* Sad
* Angry
* Serious
By using a webcam, one can add samples to the model, which will predict in real time the label of the frame captured by the camera.
