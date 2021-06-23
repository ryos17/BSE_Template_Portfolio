# 8x32 LED High Performance Audio Monitor
An audio monitor is usually used in studios to express music in the form of audio. For example, the speakers you see in studios are called audio monitors. A lot of musicians utilize audio monitors to playback music and visualize sound. In this project, I attempted to create monitor where the audio spectrum is expressed visually through a 8x32 RGB LED Matrix.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Ryota Sato | Adrian Wilcox High School | Audio/ Electrical/ Software Engineer | Incoming Junior

![32 x 16 led matrix](https://user-images.githubusercontent.com/69173660/123154752-23d0ee80-d41c-11eb-800e-6babe9db2edc.png)
  
# First Milestone
My first milestone is sending data from processing to arduino, and then lighting up the matrix depending on the data. First, I did not know anything about serial ports and sending data so I decided to look at one of the example code called SimpleWrite. In this code, a speicifc character was sent to the serial port whenever the mouse was hovering over a square. Then, arduino took in the letter sent into the serial port and lit up a LED. By looking at each line of code, I was able to fully understand how serial ports work and the specific libraries, functions, and setups required for the program to work. 

My other part of the milestone was lighting up the LED matrix. First thing I did to acheive this milestone was to download the library used for the LED matrix. Then, I looked at an example called matrixtest. In this example, the LED matrix displayed words and letters depending on the code. Through this code, I was able to understand how to setup a matrix, and functions which lights up speicifc pixels, screens, and colors. 

Finally, I was able to combine both examples and modify the code so that whenever the mouse is hovered over the square, the matrix turns red and if the mouse is off the square, the matrix turns green. The video below explains important bug fixes and a demonstration of this code. 

<html><iframe width="560" height="315" src="https://www.youtube.com/embed/JOaKPQlaxiY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></html>

# Final Milestone
My final milestone is the increased reliability and accuracy of my robot. I ameliorated the sagging and fixed the reliability of the finger. As discussed in my second milestone, the arm sags because of weight. I put in a block of wood at the base to hold up the upper arm; this has reverberating positive effects throughout the arm. I also realized that the forearm was getting disconnected from the elbow servo’s horn because of the weight stress on the joint. Now, I make sure to constantly tighten the screws at that joint. 

[![Final Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1612573869/video_to_markdown/images/youtube--F7M7imOVGug-c05b58ac6eb4c4700831b2b3070cd403.jpg )](https://www.youtube.com/watch?v=F7M7imOVGug&feature=emb_logo "Final Milestone"){:target="_blank" rel="noopener"}

# Second Milestone
My final milestone is the increased reliability and accuracy of my robot. I ameliorated the sagging and fixed the reliability of the finger. As discussed in my second milestone, the arm sags because of weight. I put in a block of wood at the base to hold up the upper arm; this has reverberating positive effects throughout the arm. I also realized that the forearm was getting disconnected from the elbow servo’s horn because of the weight stress on the joint. Now, I make sure to constantly tighten the screws at that joint.

[![Third Milestone](https://res.cloudinary.com/marcomontalbano/image/upload/v1612574014/video_to_markdown/images/youtube--y3VAmNlER5Y-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=y3VAmNlER5Y&feature=emb_logo "Second Milestone"){:target="_blank" rel="noopener"}
