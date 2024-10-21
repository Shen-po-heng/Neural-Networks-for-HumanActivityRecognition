# Neural Networks for recognition of human activities
This repository aims to investigate the application of Neural Networks (NNs) in the recognition of human activities, utilizing sensor data from smartphones.

## introduction
Human Activity Recognition (HAR) is a field gaining prominence due to its applications in areas such as healthcare, smart homes, and personal fitness. By utilizing data from built-in sensors such as accelerometers and gyroscopes, machine learning techniques can be applied to identify various human activities. This project focuses on leveraging Multilayer Perceptron (MLP), a type of Neural Network, to classify 12 daily human activities using sensor data collected from smartphones

## Human activity recognition
Human Activity Recognition involves classifying activities based on data from sensors embedded in devices like smartphones. Typically, this data is time-series, making preprocessing and feature extraction critical. Activities such as walking, sitting, standing, and transitioning between postures can be recognized by processing this sensor data through machine learning models. Traditional approaches required manual feature extraction, but Neural Networks, especially Deep Learning models, can now automatically learn and extract features, simplifying the process and improving accuracy.

## Neural Networks
Neural Networks, particularly Multilayer Perceptrons (MLPs), are well-suited for classification problems like HAR. An MLP consists of an input layer, hidden layers, and an output layer. The network learns by adjusting weights during training, using backpropagation. For HAR, MLPs can automatically recognize patterns in sensor data, such as accelerations and angular velocities, leading to efficient and accurate classification of activities. The performance of an MLP depends heavily on hyperparameters like the number of layers, neurons, and the learning rate.

## Data Explanation
The dataset used for this project is derived from the "[Smartphone-Based Recognition of Human Activities and Postural Transitions](https://archive.ics.uci.edu/dataset/341/smartphone+based+recognition+of+human+activities+and+postural+transitions)" data set from the UC Irvine Machine Learning Repository. It consists of data from 30 volunteers performing 12 distinct activities, including walking, standing, sitting, and various transitions. The sensors provide 3-axis accelerometer and gyroscope data, which is processed for use in the classifier. Preprocessing includes filtering, segmentation, and feature extraction, leading to a cleaner and more manageable dataset.

## Programs

### Data Process
The data processing pipeline includes:
- Preprocessing: The raw sensor data is cleaned and filtered to remove noise using a low-pass filter. Segmentation is done using a sliding window technique, which splits the time-series data into smaller segments. After segmentation, features such as mean, variance, and range are extracted.

- Feature Selection: After feature extraction, the ANOVA F-test is applied to select the most relevant features for classification, helping to reduce computational complexity and improve model accuracy.

### MLP Classifier
The MLP classifier consists of an input layer, two hidden layers with ReLU activation, and a softmax output layer for classification. Hyperparameters such as the number of neurons, learning rate, and dropout rate are fine-tuned to optimize performance. The classifier is trained using the Adam optimizer and evaluated based on accuracy, precision, recall, and F1 score. The data is split into training, validation, and test sets, and 10-fold cross-validation is used during training to ensure generalization.
