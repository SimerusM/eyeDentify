![Logo Screen](https://github.com/asyf16/eyeDentify/assets/144833617/93f2774c-cb8f-460a-b17f-5b9b4132dfc6)

# 🧠 Our inspiration
A world without facial recognition is a world full of strangers... EyeDentify was created to improve everyday experiences for those who cannot identify faces, turning all those distant strangers into loved ones.

# 🤔 What does it do? 
Eyedentify is a wearable headset powered by Raspberry Pi integrated with a camera and LCD screen that allows users to navigate the world with real-time facial recognition and labeling. This sleek device captures faces in real life and cross-references them with a database of images uploaded to our website.

# ⁉️ How does it work?
First, users can create an account on our website built with React. They can then upload photos of their friends and label them with names and notes. These photos are then stored in an AWS database, where they can then be retrieved for analysis. Upon logging into our Raspberry Pi EyeDentify system, our program will download the user's data based on their login credentials stored in a MongoDB database. Next, when the user wears the device, the Pi opens the camera using the OpenCV library. It finds the coordinates of the face in front of the screen and utilizes the pre-existing encoded data to recognize and label whoever appears. It displays a bounding box over the person’s face as well as their name and pre-entered notes.

# Features of our product
We also calculated an accuracy meter for each face detected and did not label faces that were below 90% accurate. 

# Challenges we faced
One challenge that we ran into was that the video stream can be slow if multiple faces are detected. 

![Running Facial Recognition every other frame](https://github.com/asyf16/eyeDentify/assets/144833617/a95b22f9-c61f-4b66-8a34-8daec0fc9fca)

To alleviate this, we decided to only run the facial detection on every other frame and to scale down the frames before running the detection, then scaling it up again. 

![Scaling Down Images](https://github.com/asyf16/eyeDentify/assets/144833617/84edd6a2-2e82-4e18-9ed5-07f6377c8bbb)

Furthermore, the camera we used was very sensitive and had trouble connecting to the Raspberry Pi. During our tests, we had to ensure that the camera was securely connected to both the Pi and the headset. 

# Video Demo
https://youtu.be/KergMVdy5mk 

