# 8x32 LED High Performance Audio Monitor
An audio monitor is usually used in studios to express music in the form of audio. For example, the speakers you see in studios are called audio monitors. A lot of musicians utilize audio monitors to playback music and visualize sound. In this project, I attempted to create monitor where the audio spectrum is expressed visually through a 8x32 RGB LED Matrix.

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Ryota Sato | Adrian Wilcox High School | Audio/ Electrical/ Software Engineer | Incoming Junior

![32 x 16 led matrix](https://user-images.githubusercontent.com/69173660/123154752-23d0ee80-d41c-11eb-800e-6babe9db2edc.png)
  
# First Milestone
My first milestone is sending data from processing to arduino, and then lighting up the matrix depending on the data. First, I did not know anything about serial ports and sending data so I decided to look at one of the example code called SimpleWrite. In this code, a speicifc character was sent to the serial port whenever the mouse was hovering over a square. Then, arduino took in the letter sent into the serial port and lit up a LED. By looking at each line of code, I was able to fully understand how serial ports work and the specific libraries, functions, and setups required for the program to work. 

My other part of the milestone was lighting up the LED matrix. First thing I did to acheive this milestone was to download the library used for the LED matrix. Then, I looked at an example called matrixtest. In this example, the LED matrix displayed words and letters depending on the code. Through this code, I was able to understand how to setup a matrix, and functions which lights up speicifc pixels, screens, and colors. 

Finally, I was able to combine both examples and modify the code so that whenever the mouse is hovered over the square, the matrix turns red and if the mouse is off the square, the matrix turns green. Some important information to know is that 5V of power is not enough to light up the whole matrix board with brightness level 100. Also, everysingle time you want to show the matrix, you have to use a special function called matrix.show. Circuit, code, and video below explains other important bug fixes and a demonstration.
### Circuit:
![circuit](https://user-images.githubusercontent.com/69173660/123160342-e91e8480-d422-11eb-954e-6819badc5ad1.png)

### Arduino Code:
![Arduino Code 1](https://user-images.githubusercontent.com/69173660/123162043-fdfc1780-d424-11eb-945d-50c603534dfe.png)

### Processing Code:
![Processing code 1](https://user-images.githubusercontent.com/69173660/123162027-f8063680-d424-11eb-9997-96e63bac58df.png)

### Video:
<html><iframe width="560" height="315" src="https://www.youtube.com/embed/JOaKPQlaxiY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></html>   

# Second Milestone
My second milestone was creating the audio spectrum on Processing, and sending the information to Arduino, which lights up the same information on the matrix. First, I decided to open the FFTSpectrum example code and understand how the audio spectrum works. I was able to then modify the code so that the program now takes the line in of my mic input instead of a sample sound file. Then, I made if statements to round the long numbers into integers ranging from 0-8, which was all concatinated to one string to send. On the arduino side, it takes the long string and takes the information and lights up the correct pixels. One challenge I had was that the pixel flickered every single time the code ran and also lighted up wrong pixels. To fix this problem, I used a special serial function called serial.parseInt which took only integers and ignored all letters and empty spaces. Also, running the matrix.show function outside of the for loop fixed the LED flickering glitch. All in all, I was able to finish the base project and successfully create a high performance LED audio monitor. The code below and the video shows a demonstration of the second milestone.



