# URC_Route_Planning

The Rover needs to be aware of the surroundings in order to compute the route planning, the input will be obtained from a camera, specifically an Intel® RealSense™ Depth Camera D435, this allows the Rover to obtain image and infrared data.The camera is going to be directly connected to the Jetson Tx1 and will be controlled using Robot Operating System (ROS). Inside the operating system nodes will be used to control the camera and send the data to be processed on a classification neural network which could change to a regression one in the future. The entire machine learning section will be developed with TensorFlow library, which will guarantee that the system is optimized and capable of detecting irregularities on the road, in order to generate the most optimal route. After having processed the terrain with the neural network, a route will be generated to get from point a to point b in real time, which will allow us to make changes to the route as necessary. The route planning will be generated with the A* search algorithm (A Star), which will use a cost dictionary for the allowed moves. The terrain classification generated by the neural network is expected to generate the most optimal routes that avoid the greatest number of obstacles and terrain irregularities at the lowest possible cost.

## Current State of Project

For this project height maps of Mars from the Lunar & Planetary Laboratory of the University of Arizona were used to develop a classification neural network. 

![Mars_surface](https://user-images.githubusercontent.com/78834111/155245858-4782dbee-2df1-4062-8d32-1477ddd8f804.png)

Route planning consisted of classifying the maps by navigable or non-navigable areas. 

![classified_mars_surface](https://user-images.githubusercontent.com/78834111/155245915-b1d09d6d-262d-4d31-bfbb-c3e13e8688ee.png)

From this, a search algorithm (A*) was used to generate routes from point A to point B with the lowest possible cost.

![route](https://user-images.githubusercontent.com/78834111/155245932-2a9a0fda-3e3c-4bfc-817c-f7fc07674d05.png)


