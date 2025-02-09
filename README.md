# Jack the Gripper

![WhatsApp Image 2025-01-23 at 17](https://github.com/user-attachments/assets/aeb9c37d-5446-4600-b461-a043e5375784)

# What it is
We built a small gripper robot, whose purpose is (as the name implies) gripping things and transporting them out of its path. The robots name is Jack the Gripper. Additionally Jack can follow a line based on its color sensor. The main function of Jack is following a line in an arena, and if he encounters/detects obstacles he grips them and he moves them out the way of the line, then returns to the line and starts following it again, until the next obstacle.

# Our idea and its developement
At the beginning we wanted to develop a gripping robot that can recognize different colored objects and sort them by color. This would work by bringing the different colored objects to platforms of the corresponding color (e.g. a red object will be transported to the red plattform/red area). However, we had to change this initial vision to accomodate the capacities of the color-sensor. This sensor only works at a very short distance, therefore making it impossible to identify the color of an object that is held in the gripping arms. Fastening the sensor onto the arms also was not possible, because that would make the arm too heavy and awkward to operate properly.
That is why we changed our idea. Now the color-sensor is used to identify a black line on white ground to follow. The gripping arms are now used to grip objects on the path and move them out of the way. Afterwards our robot returns to the line and follows it again.

The picture shows a first version of Jack.

![WhatsApp Image 2024-11-28 at 18 (1)](https://github.com/user-attachments/assets/7bc185c0-22d8-432e-80d4-8b426627de6d)


# Installation & Prerequisites
1. Get the [LEGO® Education SPIKE™ Prime-Set](https://education.lego.com/de-de/products/lego-education-spike-prime-set/45678/) to build your roboter.
2. Download the [LEGO® Education SPIKE™ App](https://education.lego.com/de-de/downloads/spike-app/software/) to your computer. Choose the right version for your operating system.

# Building Jack the Gripper
Our design for the gripping arms was inspired by [this website](https://www.robocamp.eu/en/blog/robot-spike-manipulator-lesson/), that showed a gripping robot. It fit our initial idea of the gripping function the best, and our gripping arms are build similary to the ones shown on the website, with minor changes. 
For the wheels and the driving function of the robot, we just tried different wheels from the LEGO set and how they fit with our design. The motors for the wheels, as well as the color and distance sensors, are located below the plattform on which the gripping arms are mounted. Below, you can see some pictures of the building process and the of us figuring out, where to best locate the sensors.

![WhatsApp Image 2024-11-14 at 18](https://github.com/user-attachments/assets/762f7a83-7465-48e8-8663-874baa7bd03b)
![WhatsApp Image 2025-01-23 at 16](https://github.com/user-attachments/assets/63eed561-5dd5-4441-bd12-fe26164e771c)

The most important parts from the Lego set that were used to build Jack are shown in this picture. Please note that the picture does not extensively show every piece and how many of them you have to use, but from the picure and the pictures of Jack you should be able to figure out what to use and how to connect the different pieces if you wanted to build Jack. Just add connecting pieces as needed. 

![WhatsApp Image 2025-01-23 at 17 (1)](https://github.com/user-attachments/assets/357b4dce-bfc2-4e10-8211-01148877d701)


Pictures of the final version of Jack from different perspectives are shown below. To make Jack look nicer, we added some decorative elements, like a big wheel at the rear of the robot, to hide some of its inner workings (like the motor for the gripping arms). We also added eyes that kind of look like the eyes of a crab, because of the similarity between the gripping arms of Jack and the claws of the crab. With the eyebrows, Jack can be made to look either angry or nervous. We also added some grey tubes for the cables of the motors/sensors to wrap around and stabilize. 

noch mehr Bilder aus mehreren Perspektiven von dem fertigen Roboter einfügen

![WhatsApp Image 2025-01-23 at 17 41 54(1)](https://github.com/user-attachments/assets/2c736761-079d-46a1-909c-ec5f6f0890f2)
![WhatsApp Image 2025-01-23 at 17 41 54(2)](https://github.com/user-attachments/assets/b906799b-a69c-41bd-b1fd-cd711eef71d8)
![WhatsApp Image 2025-01-23 at 17 (2)](https://github.com/user-attachments/assets/4cc1f7a8-bc80-4e15-a32e-669378ea5762)
![WhatsApp Image 2025-01-23 at 17 41 54(3)](https://github.com/user-attachments/assets/5614b3ac-ec0a-4e68-875f-ce29432bc264)
![WhatsApp Image 2025-01-23 at 17 30 50](https://github.com/user-attachments/assets/27b65096-fc3c-4c91-8a95-b6e8a31cb76e)


Jack in angry mode and in nervous mode: 

![WhatsApp Image 2025-01-23 at 17 29 51(2)](https://github.com/user-attachments/assets/f7c16577-385e-48a3-ab02-5c342522d9c7)
![WhatsApp Image 2025-01-23 at 17 29 51(3)](https://github.com/user-attachments/assets/bf91b179-2edd-4a60-ab2b-0a228aefd26c)


# Programming
For programming Jack the Gripper we used the Lego Spike App and its programming user interface. After opening the app you will see some tutorials and example projects. If you have not programmed before or are unfamiliar with the platform, the "First steps"-Tutorial might be of use to you.
To start a new project, click the button "new project". If you want to use an already existing project you can find it by clicking "my projects" in the menu on the left. You can choose between different programming languages: symbol bricks, text bricks, or python. For our project, we used the text bricks.

Follow the instructions to connect your laptop to the Hub. If you connect sensors to the Hub, you will also see their output on the top menu. On the left you can see a menu with different types of bricks with different functions. 

In the following, we will present our code (shown in its entirety here) for Jack and explain what it does.

![WhatsApp Image 2025-01-23 at 16 49 34](https://github.com/user-attachments/assets/f98240bf-8da2-45e0-9147-71ca9a26e278)

## Follow the Black Line

![Linie folgen](https://github.com/user-attachments/assets/354a179a-6f8a-4ddb-903d-ead9bbba13d7)

First, we wanted Jack to follow a black line. For better structure in our Code, we used the "Definiere" brick, which can be found by creating a new block under category "Eigene Blöcke". We labeled our new block "Linie folgen". Jack was equipped with a separate motor for each his left and right wheel. In order to follow the line, we used a color sensor. The power of the two motors are depending on the sensors' output. Therefore we defined new variables: "left_pwr" and "right_pwr" (left and right power), "des_pwr" (desired power), "gain" and "b/w". The last one was set to the color sensors output in case it is set exactly on the edge of black and white. Further information are provided in the "Main Block" section. These variables were used to calculate the left and right motor powers (orange bricks) depending on the sensors' input (blue brick within the calculation). As you can see, left and right motor power will be equally set to the value of the desired power variable in case that the color sensor is exactly on the black line. Otherwise the difference in powers will lead to a movement to the right or left side. The last brick in this block finally starts the movement with the calculated powers.

## Gripping an Object

![Greifen](https://github.com/user-attachments/assets/0d5afa0e-edef-4e1e-8f35-036da081a42c)

Here, we defined a new block that manages the process of gripping a detected object. Therefore, we used the first brick "stoppe andere Stapel" to stop any other processes like Jack moving along the black line. To create a smoother movement we also made Jack wait a second after stopping before he starts gripping the object. The Last brick here refers to another self-created block that defines the action of closing the arms. 

## Opening and Closing Arms

![Arme bewegen](https://github.com/user-attachments/assets/282ec485-11e9-4a2d-86a8-7a9271548141)

Opening and closing the gripping arms required a separate motor. The block "Arme schließen" consists of two bricks from the section "Motoren". In both bricks "E" was selected since the motor was attached to port "E" on the hub. The first brick sets the motor power to 7 % which can be changed according to own preferences. We chose 7 % in order to create a rather slow and careful motion. We found out that Jack's arms are closed when the value of the motor position is 180. The second brick therefore makes the motor move into this position by rotating counter-clockwise. 
The block "Arme öffnen" uses the sme to bricks with adapted values of the desired motor position and direction of rotation. 

## Setting the object down

![Ausweichen](https://github.com/user-attachments/assets/ba058e99-5d01-4a48-aaae-73b1859d872f)

Once Jack has gripped an object we wanted him to put it out of the way. We defined the "Ausweichen" action to enable Jack to drive away from the black line with the object, let it go and come back to the original position. The first three pink bricks make Jack turn right an drive five centimeters straight forward. Afterwards we used our self-created brick "Arme öffnen" for Jack to let go of the object. The following bricks are reversing the previous actions by moving backwards, closing the arms and turning left resulting in Jack being positioned back on the black line. All values used in this block can be adapted to own preferences. Make sure that the angels for the right and left turn as well as the distance for driving forwards and backwards are equal. Otherwise Jack will not return to the original position on the black line.

## Main Block

![Main](https://github.com/user-attachments/assets/e330c550-6c75-4d12-ac75-186ea00fd65e)

This block starts with the brick "Wenn Programm startet" since it is the main part of the program that is supposed to run as soon as Jack is activated. We first wanted to make sure that Jack drives around with his arms closed no matter in what position they were before. Since he should only start closing his arms if they are not already closed, we used a conditional brick here. Motor position values bigger than 180 come with opened arms so these were our condition for "Arme schließen".
For the beginning of the program we must define which motors are used for movement in order to be able to use bricks from the movement section. The motors for the wheels were in our case connected to ports "B" and "F" on the hub. You need to make sure to select the correct ports in the brick "weise Bewegungsmotoren Anschlüsse ... zu".
The following three orange bricks are used to set our previously mentioned variables to certain values. As always, these can be adapted regarding the following information: The desired power will affect the general pace of Jacks' movement. Gain will affect how much faster or slower than the general pace a wheel will move whenever Jack is not exactly on the edge of the black line. The value for black/white should be set to the value that the color sensor gives when placed on the edge of the line that has to be followed. Especially when using a different colored line this value might differ from 50. The last part of the main code consists of a never ending loop. By using this loop, Jack follows a line and puts objects away until the execution of the program is stopped. First, this loop contains another loop "wiederhole bis ...". By inserting the brick "Linie folgen" here, we made sure that the direction of movement is constantly adapted to the lines direction. The condition in this loop makes jack follow the line until the distance sensor (here port "C") returns a value smaller than 11 cm. Whenever this happens the next brick "halte an" will be executed. This causes Jack to stop with his arms right before the detected object (without touching it). After stopping, the bricks "Arme öffnen", "bewege dich 3 cm" and "Greifen" are used. Jack opens his arms and drives a little forward in order to grab the object. With the use of "Ausweichen" he puts the object aside as described previously and returns back to the line. Thanks to the outer loop, the actions following line until detecting an object, gripping the object and putting it aside will repeat themselves over and over. 

# Lessons learned and future works
We learned a lot about working with the LEGO set and about how to put the parts together in a way that makes sense and works for the intended functions, like the gripping arms of Jack. 
We also learned how the sensors work and about their limitations. For example, the colour sensor only works in very close proximity to an object and only recognizes specific colours (only colours that are present in the LEGO set). Also, the line of colour/black that Jacks follows has to be quite thick, otherwise it only recognizes the white ground in the arena and cannot follow the line. Generally, working with the sensors was quite the trial-and-error, we had to find out what works and what does not. 
The same is also true for the programming. For example, we used two nested if-conditions in the beginning which wouldn't work out. Since there was no mistake in the program to be found, we learned that this was maybe a little too hard to process for this development environment. We therefore tried to avoid nested code and instead used many separate blocks. To our surprise the nested loops in the main part of the code worked out perfectly fine. 
