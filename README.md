*Heare is the explanation of the AI*

**Importing Libraries and Dataset:**

![carbon (2)](https://github.com/user-attachments/assets/b69e9f72-f4e7-44a0-a7f3-ff35a039b73a)

Here, the code imports the **Pandas** library to handle the dataset. The dataset is loaded from a CSV file named "cancer.csv" 

**Defining Features (x) and Target Variable (y):**

![carbon (1)](https://github.com/user-attachments/assets/b5c04f0d-b1c3-4bc2-877c-03b937df1a29)

The code separates the data into features x and the target variable y.

•x contains all columns except the "diagnosis(1=m, 0=b)" column, which indicates if the tumor is malignant (1) or benign (0). •y contains only the "diagnosis(1=m, 0=b)" column, which is the label the model will predict. 

**Splitting the Data into Training and Testing Sets:**

![carbon (3)](https://github.com/user-attachments/assets/548e5a4c-765d-44ac-8e79-5f2b39bfcaa5)

•• TXhetraidantaseand yt  is spltrainit wiinll to tbe usraiedning for tranainid testinng theg se modts el,usiwhilng ane x 80test/20and splyit.test are reserved for evaluation. 

**Building the Neural Network Model:**

![carbon (4)](https://github.com/user-attachments/assets/9678ee2e-c3b9-4125-8548-2c2ff474d05d)

•This section sets up a neural network using **TensorFlow's Keras** API.

•The model is **Sequential**, meaning layers are added one after the  

•Three **dense (fully connected)** layers are used: 

•The first layer has 256 neurons and takes the shape of x\_train as  input. 

•The second layer has 256 neurons. 

•The last layer has a single neuron with a **sigmoid activation**  function, providing output values between 0 and 1 (ideal for binary  classification).

![WhatsApp Image 2024-11-12 at 1 35 19 PM](https://github.com/user-attachments/assets/ff940575-d052-4722-903f-214ae89de7e0)


**Compiling the Model:** 

![carbon (5)](https://github.com/user-attachments/assets/81efddc3-35ce-46f0-bb6f-1ba2b5a46c08)

The model is compiled with:

- **Shivashish optimizer** (efficient for many neural networks).
- binary\_crossentropy** loss function (standard for binary classification).
- accuracy metric to monitor performance.

**Training the Model:**

![carbon (7)](https://github.com/user-attachments/assets/ed4ed1fe-b891-4df0-be1c-06918b53ab34)

The model is trained on the training data for **1000 epochs**. Each epoch represents a full pass over the training data.

**Evaluating the Model:**

![carbon (8)](https://github.com/user-attachments/assets/5f04280f-fabf-4710-93a4-84bb8534cb0a)

Finally, the model’s performance is evaluated using the test data (x\_test and y\_test), providing a measure of its accuracy on unseen data. 

**Visual Results:**

Training Loss and Accuracy Over Epochs: The loss curve steadily decreases, and the accuracy curve rises, showing the model’s learning progress over time.

![Screenshot 2024-11-12 140012](https://github.com/user-attachments/assets/9a97de8b-c14c-472c-8564-20c6c7d68e04)


Confusion Matrix: This matrix illustrates the model’s ability to distinguish between safe and dangerous tumors, which is crucial for medical decision-making.

![Screenshot 2024-11-12 140108](https://github.com/user-attachments/assets/76835236-9b36-41ca-a672-958dfb71eeb0)
