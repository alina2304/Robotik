# Jack the Gripper

# What it is
We build a small gripper robot, whose purpose is (as the name implies) gripping things and transporting them to different places. The robots name is Jack the Gripper. Additionally Jack can follow a line based on its color sensor. The main function of Jack is following a line in an arena, and if he encounters/detects obstacles he grips them and he moves them out the way of the line, then returns to the line and starts following it again, until the next obstacle.

# Our idea and its developement
At the beginning we wanted to develop a gripping robot that can recognize different colored objects and sort them by color. This would work by bringing the different colored objects to plattforms of the corresponding color (e.g. a red object will be transported to the red plattform/red area). However, we had to change this initial vision to accomodate the capacities of the color-sensor. This sensor only works at a very short distance, therefore making it impossible to identify the color of an object that is held in the gripping arms. Fastening the sensor onto the arms also was not possible, because that would make the arm to heavy and awkward.
That is why we changed our idea. Now the color-sensor is used to identify a black line on white ground to follow it. The gripping arms are now used to grip objects on the path and take them out of the way. Afterwards our robot returns to the line and follows it again.

# Installation & Prerequisites
1. Get the [LEGO® Education SPIKE™ Prime-Set](https://education.lego.com/de-de/products/lego-education-spike-prime-set/45678/) to build your roboter.
2. Download the [LEGO® Education SPIKE™ App](https://education.lego.com/de-de/downloads/spike-app/software/) to your computer. Choose the right version for your operating system.

# Building Jack the Gripper
Our design for the gripping arms was inspired by [this website](https://www.robocamp.eu/en/blog/robot-spike-manipulator-lesson/), that showed a gripping robot. It fit our initial idea of the gripping function the best, and our gripping arms are build similary to the ones shown on the website, with minor changes. 
For the wheels and the driving function of the robot, we just tried different wheels from the LEGO set and how to build them onto the robot. The motors for the wheels, as well as the color and distance sensors, are located below the plattform on which the gripping arms are mounted. 
To make Jack look nicer, we added some decorative elements, like a big wheel at the rear of the robot, to hide some of its inner workings (like the motor for the gripping arms). We also added eyes that kind of look like the eyes of a crab, because of the similarity between the gripping arms of Jack and the claws of the crab. With the eyebrows, Jack can be made to look either angry or nervous. We also added some grey tubes for the cables of the motors/sensors to wrap around and stabilize. 

![WhatsApp Image 2024-11-14 at 18](https://github.com/user-attachments/assets/762f7a83-7465-48e8-8663-874baa7bd03b)



# Programming

# Lessons learned and future works
We learned a lot about working with the LEGO set and about how to put the parts together in a way that makes sense and works for the intended functions, like the gripping arms of Jack. 
We also learned how the sensors work and about their limitations. For example, the colour sensor only works in very close proximity to an object and only recognizes specific colours (only colours that are present in the LEGO set). Also, the line of colour/black that Jacks follows has to be quite thick, otherwise it only recognizes the white ground in the arena and cannot follow the line. Generally, working with the sensors was quite the trial-and-error, we had to find out what works and what does not. 
