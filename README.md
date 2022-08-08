# Road-Lane-Image-Segmentation-
This project is a deep learning course project consisting of a set of python notebooks that take a video of a car driving down the road and output a video with the lane pixels highlighted in green.
The program uses a Convolutional Neural Network that was trained to segment the pixels of the car's lane from the other pixels. Each pixel in the input image is given a number between 0 and 1, where 0 means that the corresponding pixel is not in the car's lane and 1 means that it is.

for example if this were a frame input to the program:
![image](https://user-images.githubusercontent.com/40373518/183518858-5f298504-23c5-45bb-b028-168cfa6422a6.png)

its expected output should be like this:
![image](https://user-images.githubusercontent.com/40373518/183519000-362e6477-2a39-4a8e-a1ad-2b66c6c56e39.png)

This is achieved with 2 seperate notebooks:
1. Model_Training.ipynb
2. DLProject_videoGeneration.ipynb

#### 1. Model_Training.ipynb:
This is the notebook where the training dataset is retrieved, processed, and used to train our created CNN model. The architecture of the CNN model are also showcased in this notebook

#### 2. DLProject_videoGeneration.ipynb
This notebook loads the trained model so it can use it to predict which pixels are in the car's lane. Based on the model's predictions for each frame, we highlight the corresponding pixels in green and stitch all the frames together to generate the output video.
