# KERAS_SERIES_WITH_BACKEND_TENSORFLOW
TEXT GENERATION USING RNN


# Use the data from Lord of Rings file and create a generation of new text based on the LOR method.The objective is to predict the next 100 words of the given sentence from the training data set.Datacan be obtained fromthe following link:
https://raw.githubusercontent.com/wess/iotr/master/lotr.txt

# Note : Please use Google Colaboratory–a free service by Google for AI developers –to work on this project. Also, make sure to opt for GPUunder ‘Hardware accelerator’ while selecting Python 3 under ‘Runtime type.’

#Source : https://medium.com/deep-learning-turkey/google-colab-free-gpu-tutorial-e113627b9f5d


Problem 1: Use the bi-directional  LSTM  model  to  learn  the  pattern  of  LOTR  dataand  run  it  for  100 epochs initially. 

![image](https://user-images.githubusercontent.com/61096571/184577288-30592f08-c296-4131-933a-24e1f0fff867.png)


#Problem 2: Use  the  same bi-directional  LSTM model  used  in the previous  steps  and  train  it  further  on  100 epochs, for it can learn more patterns.
Check for its accuracy by plotting the accuracy graph over the epochs.

![image](https://user-images.githubusercontent.com/61096571/184577615-5c406c71-e347-4391-a837-2b41c73aa44c.png)


![image](https://user-images.githubusercontent.com/61096571/184576973-520a651f-db90-468c-8b33-09d1376e9e25.png)

Note: After training the model, write a function to generate text using the patterns learned.
