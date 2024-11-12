*Heare is he implementation process of the AI*

**Importing Libraries and Dataset:** python

import pandas as pd

dataset = pd.read_csv('cancer.csv')

Here, the code imports the **Pandas** library to handle the dataset. The dataset is loaded from a CSV file named "cancer.csv" 

**Defining Features (x) and Target Variable (y):** python



The code separates the data into features x and the target variable y.

•x contains all columns except the "diagnosis(1=m, 0=b)" column, which indicates if the tumor is malignant (1) or benign (0). •y contains only the "diagnosis(1=m, 0=b)" column, which is the label the model will predict. 

**Splitting the Data into Training and Testing Sets:** python

![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.003.png)

•• TXhetraidantaseand yt  is spltrainit wiinll to tbe usraiedning for tranainid testinng theg se modts el,usiwhilng ane x 80test/20and splyit.test are reserved for evaluation. 

**Building the Neural Network Model:** python![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.004.png)![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.005.png)

•This section sets up a neural network using **TensorFlow's Keras** API.

•The model is **Sequential**, meaning layers are added one after the  ![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.006.jpeg)other. 

•Three **dense (fully connected)** layers are used: 

•The first layer has 256 neurons and takes the shape of x\_train as  input. 

•The second layer has 256 neurons. 

•The last layer has a single neuron with a **sigmoid activation**  function, providing output values between 0 and 1 (ideal for binary  classification).

**Compiling the Model:** python

![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.007.png)

The model is compiled with:

- **Shivashish optimizer** (efficient for many neural networks).
- binary\_crossentropy** loss function (standard for binary classification).
- accuracy metric to monitor performance.

**Training the Model:** python

![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.008.png)

The model is trained on the training data for **1000 epochs**. Each epoch represents a full pass over the training data.

**Evaluating the Model:** python

![](Aspose.Words.4fe01fe1-6d66-4183-ad5b-463b5c1a6ff8.009.png)

Finally, the model’s performance is evaluated using the test data (x\_test and y\_test), providing a measure of its accuracy on unseen data. 
