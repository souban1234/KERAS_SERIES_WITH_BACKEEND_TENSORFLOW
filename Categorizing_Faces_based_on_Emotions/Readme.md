# Categorizing_Faces_based_on_Emotions
Fer2013.csv (a file consisting of data sets about different facial expressions) contains two columns, "emotion" and "pixels". 
The "emotion" column contains a numeric code ranging from 0 to 6, each code representative of an emotion as mentioned above.
The "pixels" column, on the other hand, contains a string surrounded by quotes for each image. The data set consists of 28,709 examples.
This data set was prepared by Pierre-Luc Carrier and Aaron Courville, as part of an ongoing research project. 
They have graciously provided the workshop organizers with a preliminary version of their datasetNote:

Please use Google Colaboratory –a free service by Google for AI developers –to work on this project. 
Also, make sure to opt for GPUunder ‘Hardware accelerator’ while selecting Python 3 under ‘Runtime type.’<br><br>
Source: https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5dF <br>
or more detailed information on Colaboratory, follow the below link:<br><br>
https://colab.research.google.com/notebooks/intro.ipynb#Note: 

Install the latest version of TensorFlow 2.0 using the below command 
!pip install --upgrade tensorflow


# Step 1: Reshape and normalize the data:

# Method : Split pixels by space to get columns
		Reshape the input image as demonstrated belowo48,48,1
		Change the data type to float32

# Step 2: Normalize the inputs & use the Train-Test Splitmethod to make the split.

# Method :
		Normalize the data by dividing it with 255
		Split the data into training and testing (90,10). 
		90% of the data will be allotted to training and the rest 10% to testing


# Step3 : Define CNN Model based on the layers mentioned below:

# Method :
		Layer 1
				2 Conv2d with 64 filters of 5,5 filter
				BatchNormalization layer
				Max Pooling layer with 2,2
				Activation ReLU
		Layer 2
				2 Conv2d with 128 filters of 5,5 filter
				BatchNormalization layer
				Max Pooling layer with 2,2
				Activation ReLU
		Layer 3
				2 Conv2d with 256 filters of 3,3 filter
				BatchNormalization layer
				Max Pooling layer with 2,2
				Activation ReLU
		Layer 4•
				Flatten layer
				Dense Layer with 128 Neuron
				BatchNormalization
				Activation Relu
				Dropout 0.25
				Dense 7 neurons with Softmax
		Loss: Categorical cross-entropy
		Optimizer: Adam
		
# Step 4 : Fit CNN Model on the training data using the method mentioned below:
	
# Method :
			Epoch = 20
			Batch_size 64
			Lr = 1e-3
	
	
# Step 5 : Draw a confusion matrix for the trained model using the mentioned below method .
	
# Method :
			Use model.predict_classes
			Use np.argmax(y_test,axis=1)
