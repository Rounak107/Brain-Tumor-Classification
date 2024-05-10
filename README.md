# Brain-Tumor-Classification
This Project involves a comprehensive demonstration of Brain Tumor Classification  utilizing Python, TensorFlow and OpenCV. It introduces a web application designed for  categorizing images based on Yes and No images of a Brain Tumor. Various image  classification, emphasizing the user interface interactions for image uploading and  prediction.

This is an introduction on Brain Tumor image classification using deep learning where the 
Technologies used such as Python, TensorFlow, Keras, and OpenCV are highlighted asthe 
tools utilized in the classification process. A brief overview of the demonstration, 
emphasizing the use of a web app for the classification task.
The demo unfolds with the presentation of a web app designed for Brain Tumor 
classification using deep learning techniques. The process of uploading an image and 
classifying it as either having or not having a Brain Tumor is showcased. Multiple 
instances are demonstrated, illustrating user interaction with the app and the resulting 
classifications.
![Frontend](https://raw.githubusercontent.com/Rounak107/Brain-Tumor-Classification/main/images/image.png)

The Dataset contain with 3060 data and the input images are of size 64x64 pixels. These hyperparameters are crucial in training a deep learning model. The learning rate controls the step size during optimization, the batch size influences the number of samples used in each iteration and the quantity of epochs dictates the frequency with which the model traverses the complete training dataset.

In Training the data the model is compiled with binary cross-entropy loss and the Adam optimizer, then trained for 10 epochs on normalized training data with a batch size of 16. The dataset is split into training and testing sets, and the model achieves an accuracy of 90% with a validation accuracy of 97.5%. To handle categorical cross-entropy, the model architecture is updated, and the last layer's activation function is adjusted accordingly. Finally, the model is retrained with the updated configurations. Sequential model was employed for building the brain tumor detection model. The architecture includes Conv2D layers, MaxPooling2D layers, flatten layer, and Dense layers, forming a convolutional neural network (CNN). The model uses the sigmoid activation function in the output layer for binary classification (detecting brain tumors or not).

Then Flask web application integrates with the trained brain tumor classification model by:

Loading Model: Loading the pre-trained model within the Flask application.
Setting Up Route: Establishing a Flask route (e.g., /predict) to handle image classification. Handling Uploads: Allowing users to upload images through a form using Flask's request module.
Preprocessing Image: Preprocessing the uploaded image to align with the model's requirements.
Making Predictions: Using the loaded model to predict tumor presence in the preprocessed image.
Mapping Predictions: Mapping numerical predictions to meaningful class names (e.g., "Yes" or "No").
Returning Results: Displaying the classification results on the web app for user interaction.
