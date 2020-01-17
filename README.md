# Colorectal cancer tumor cells identification
Recognition of different tissue types in histological images. In this problem of identification different tissues was accutually implemnted in machine learning 
k-nearest neighbour and was employed with SVM(Support Vector Machine) by Jakob Nikolas Kather, Cleo-Aron Weis, Francesco Bianconi, Susanne M. Melchers, Lothar R.Schad, Timo Gaiser, Alexander Marx & Frank Gerrit Zollner, in the year 2016 they publshed a paper in scientific reports can be accessed by [Clicking here](https://www.nature.com/articles/srep27988) 


Now In this git repository the same paper is implemented in deepLearning (Tensorflow) with transferLearn (MobileNet) 
## Dataset 

Data was collected from the same papeer they have kept the data to be avaiable freely and they have also mentioned that data can be used for community purposes and can be accessed by the [Clicking Here](https://zenodo.org/record/53735#collapseCitations) 

## Data Preparation 

Data separated manually into training and testing in 10 fold validation(i.e 90% of the coplete data is used for training and rest 10% is used for testing) while training the CNN(Convolutional Neural Network) 80% is used for training and 20% is used for validation.

## implemention 

using tensorflow hub mobileNet CNN is imported using following code line
```
URL ="https://tfhub.dev/google/imagenet/mobilenet_v1_075_192/quantops/feature_vector/3"
feature_extractor = hub.KerasLayer(URL,
                                   input_shape=(192,192,3))
```

for this feature extractor a dense keras layer was added with 8 neurons as there are 8 classes.

## Results 

While training itself validation accuracy was able to reach to 91.56% and the trained model when given with the new test data was able to classify the data with an accuracy of 91.26% which is way better than the base paer.