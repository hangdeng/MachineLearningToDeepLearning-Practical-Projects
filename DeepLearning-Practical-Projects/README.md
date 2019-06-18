## DL Practical Projects

The contents of the projects below were originally created by www.udacity.com - [Github](https://github.com/udacity/deep-learning-v2-pytorch).

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
  5. The Adam optimizer is used with `learnrate = 0.001`. `CrossEntropyLoss()` is used for criterion.
  6. Ran 40 epochs.
  
* Model from transfer learning:
  1. ResNet50 is selected for the dog breed classification project.
  2. The last layer (linear transformation layer) was modified for 133 classes output.
  3. Ran 20 epochs.
  
* Predict with the transferred ResNet50 model

Further reading: [tutorial on understanding convolution layers in CNNs](http://machinelearninguru.com/computer_vision/basics/convolution/convolution_layer.html)

------

#### Project III-3 [TV script generation](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/tree/master/DeepLearning-Practical-Projects/project-tv-script-generation):

Project brief summary:
* 1 - Preprocess text data; 2 - build LSTM model with embedding layer, etc.

* Model build with pytorch:
  1. Create dictionaries of vocabulary-to-integer and integer-to-vocabulary for the text data.
  2. Tokenize punctuation with `||||`. (e.g. period(.) to `||Period||`).
  3. Batch features and target with [TensorDataset class](https://pytorch.org/docs/stable/data.html) and [DataLoader class](https://pytorch.org/docs/stable/data.html)
  4. Build LSTM model: include embedding layer (`Embedding_dim = 300`), 2-layer LSTM (`dropout_prob = 0.5`), final fully-connected layer for output. hidden_state is initialized with zero weights.
  5. Hyperparameters tuning: `sequence_lengths = 10`, `batch_size = 128`, `num_epochs = 10`, `learning_rate = 0.001`, `hidden_dim = 256`, etc.
  6. Model with lowest training loss is saved among 10-epoch run.
  
* cuda runtime error (59) discussion: [c.20](https://github.com/pytorch/pytorch/issues/9585), [c.70](https://github.com/pytorch/pytorch/issues/6198), solution for the last few cells is to be posted.

#### Project III-4 [Faces generation](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/tree/master/DeepLearning-Practical-Projects/project-faces-generation)

------

#### Project III-5 [SageMaker deployment](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/tree/master/DeepLearning-Practical-Projects/project-sagemaker_deployment)

Project brief summary:
* The project uses Amazon Web Services (AWS)'s SageMaker instead of local Jupyter notebook to create deep learning neural nets model for predicting whether the movie reviews in an IMDB dataset are positive or negative.
* Project steps:
  1.
  2.

![deep learning certificate 1](https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/blob/master/DeepLearning-Practical-Projects/certificate%20DL%201.PNG)
<img src="https://github.com/hangdeng/MachineLearningToDeepLearning-Practical-Projects/blob/master/DeepLearning-Practical-Projects/certificate%20DL%201.PNG" width="500">
