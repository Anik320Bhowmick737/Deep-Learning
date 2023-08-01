# CNN for Cats and Dogs Image Classification with Model Deployment
Cats and Dogs classifier using convolutional neural network is very well known and simple project to start working on Deep Learning projects. For the model training purpose I used **The Asirra data set**. This [dataset](https://www.kaggle.com/competitions/dogs-vs-cats/data) has 25000 dogs and cats. 
## Description of the Training
* Tensorflow was used for this purpose. The images are loaded in batches of size 200 with ImageDataGenerator. Images are augmented using shear, zoom ranges, horizontal flip etc.
* For the Transfer Learning purpose VGG16 network was used whose top fully connected layer was eliminated. Because original VGG16 was trained on ImageNet dataset which has 1000 labels but in our case we have only two output labels.
<div style="width:100%;text-align: center;"> <img align=middle src="https://www.dropbox.com/s/uvl6nb911qtcdnf/VGG-16.jpg?raw=1" alt="Heat beating" style="height:300px;margin-top:3rem;"> </div>

* I froze the layers from conv1-1 to conv4-1. So that the weights won't update during Training Process.
* I further added some fully connencted layers and dropouts for regularization. The final activation is Sigmoid. Stochastic Gradient Descent was used as optimizer.
* The Model gave 99.9% Training Accuracy and 98.8% Validation Accuracy.
* After the training the model was converted to tensorflowlite model and used for the app design.
## Android Studio Part
* Java was used for the backend part and xml for the frontend UI part. This App is designed to take only static images from the phone gallery. As I am quite new to Java and Android Studio I couldn't do much better in the front end. I focused more on the deployment of ML model part. Below are two pictures from my app.

<p float="left">
  <img src="https://www.dropbox.com/s/b79vityxzm4ern6/cat.jpg?raw=1" width="300" />
  <img src="https://www.dropbox.com/s/4hjp4c3e06x1kad/dog.jpg?raw=1" width="300" /> 
</p>

* To access the apk file and the tflite model click [here](https://drive.google.com/drive/folders/1JtA0dsqNHQAwbPBkFJXyRmIcBXo42rVM)


