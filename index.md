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
<html><iframe width="560" height="315" src="https://www.youtube.com/embed/JOaKPQlaxiY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br><br><br></html>   

# Second Milestone
My second milestone was creating the audio spectrum on Processing, and sending the information to Arduino, which lights up the same information on the matrix. First, I decided to open the FFTSpectrum example code and understand how the audio spectrum works. I was able to then modify the code so that the program now takes the line in of my mic input instead of a sample sound file. Then, I made if statements to round the long numbers into integers ranging from 0-8, which was all concatenated to one string to send. On the arduino side, it takes the long string and takes the information and lights up the correct pixels. One challenge I had was that the pixel flickered every single time the code ran and also lighted up wrong pixels. To fix this problem, I used a special serial function called serial.parseInt which took only integers and ignored all letters and empty spaces. Also, running the matrix.show function outside of the for loop fixed the LED flickering glitch. Additionally, deciding how to convert between strings, character, and integer confused me a lot of at the end, I was able to understand how to efficiently store information as integers. All in all, I was able to finish the base project and successfully create a high performance LED audio monitor. The code segment below explains more in detail about this process. Circuit is the same. The video below shows a demonstration of the second milestone.

### Arduino Code:
![Arduino code 2](https://user-images.githubusercontent.com/69173660/123169572-51269800-d42e-11eb-9ac3-32822f0b4e66.png)

### Processing Code:
![Processing code 2](https://user-images.githubusercontent.com/69173660/123169601-5a176980-d42e-11eb-84d6-f41b3e0cdfed.png)

### Video:
<html><iframe width="560" height="315" src="https://www.youtube.com/embed/uLhRJsGWr3o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br><br><br></html>   

# Final Milestone
My final milestone was fixing all the bugs that were present and adding customization to my base project. I noticed later on that all of the matrix was not lighting up and showing up correctly. If you look closely to the milestone two video, the last few columns are not lighting up at all. To fix this problem, my instructor and I spent countless hours debugging and trying out a lot of different codes and fixes. What I figured out was that changing the serial communication bps changed the output, which made me wonder if changing the bps value can fix the bug. Sadly, it did not work. At the end, I was about to give up but luckly, I was able to fix the entire bug by changing one if statement into a while loop. 

Now that my base project is officially finished, I decided to start customizing my project. First, I decided to change the color of each row and create a rainbow depending on the height of each column. This customization was reletively easy by just creating three variable naming it rgb1, rgb2, and rgb3. Then, I just created a long if else statement that declared the correct rgb values depending on the row. Next customization I decided to create was taking the stereo mix input (computer line out) and displaying on matrix instead of the mics line in. I was able to easily create this modification by using sound lists and declaring a specific sound device whichw as the stereo mix.

The final customization I decided to create was using a 4x4 keypad to control various parameters of the matrix. I first downloaded the correct Keypad library and decided to experiment with example codes on the internet for reference. With a simple copy paste code, I was able to get the keypad to work no problem. Now it was sending the information from arduino to processing. One problem I thought I will encounter is that sending information to processing will be impossible while data is sent the other way simultaneously. Thankfully, this problem was not present. Also, another struggle creating my final customization was changing the keypad input (char) to the correct index of the audio device (int). With a few console logs and debugging, I was able to sucessfully map out the keypad so each button controls a unique part of the matrix. I have attached a picture of the final circuit, mapping of the keypad, and the final code pdf for arduino and processing.

### Final Circuit:
![circuit 2](https://user-images.githubusercontent.com/69173660/124025322-25169400-d9a5-11eb-9649-cb34095b18fb.png)

### Mapped Keypad
![Mapped keypad](https://user-images.githubusercontent.com/69173660/124028592-07e3c480-d9a9-11eb-99d9-9918e2fd6a4d.png)

### Final Arduino Code:
[Arduino Final Code.pdf](https://github.com/ryos17/RyotaSato_BSE_Portfolio/files/6743799/Arduino.Final.Code.pdf)

### Final Processing Code:
[Processing Final Code.pdf](https://github.com/ryos17/RyotaSato_BSE_Portfolio/files/6743806/Processing.Final.Code.pdf)

### Final Milestone Video:

# Conclusion
All in all, I learned a lot about engineering through working on this project. In the beginning, I had no idea about arduino, libraries, and the specific codes that are unqie to the program. At the end of the project, I can now fully understand the hardware and lines of code to create any project. Also, the project made me realize that I love working on fields which combine music and engineering. One overarching bug that is still present on this project is that if I switch between the audio inputs too much by using keypads, the program crashes. Even after hours of debugging and searching through the internet, I could not find any resolutions. In the future, I want to fix this bug and attempt to complete more difficult projects. 





