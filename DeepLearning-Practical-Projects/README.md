## DL Practical Projects

The contents of the projects below were originally created by www.udacity.com - [Github](https://github.com/udacity).

------

#### Project III-1 [Bike sharing prediction with simple neural nets](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/blob/master/DeepLearning-Practical-Projects/Project-Bike_sharing/Predicting_bike_sharing_data.ipynb):

Datasets: included in the folder.

Project brief summary:
* Data processing: train, validation, and test data splitting, change to dummy variables, scale variables
* Neural networks: The neural networks in this project have three layers: input layer, hidden layer (`hidden_nodes = 14`) and output layer. It uses forward pass and backpropogation to model and update weights for finding the best model.
* Model performance: model predictability is tested with test data.

------

#### Project III-2 [Dog breed classification with Convolutional Neural Nets](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/tree/master/DeepLearning-Practical-Projects/project-dog-classification):

Datasets: Due to the data size limit, the dog dataset can be downloaded from [dog_data](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). The dataset shall be saved as `folder_path\dogImages`. The human dataset can be downloaded from [human_data](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip). The unzipped folder shall be saved as `folder_path\lfw`.

Project brief summary:
* 1 - Test human images with OpenCV human face detector (`cv2.CascadeClassifier`); 2- Test dog images with pre-trained CNN models (e.g. vgg16, ResNet50). (`tqdm` library is used to visualize progress bar during code running)

* Model from Scratch:
 1. The CNN model architecture from scratch include 5 convolutional layers which increase the depth 3 -> 16 -> 32 -> 64 -> 128 -> 256.
 2. `MaxPool2d(2,2)` is applied between every convolutional layer.
 3. relu activation function is applied after every pooling layer.
 4. 2 linear transformation layers are added to transfer output of convolutional layers to 500, and then -> 133 classes of dog breeds.
------

