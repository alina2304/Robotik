# Jack the Gripper

# What it is
We build a small gripper roboter, whose purpose is (as the name implies) gripping things and transporting them to different places. The robots name is Jack the Gripper. Additionally Jack can follow a line based on its color sensor. The main function of Jack is following a line in an arena, and if he encounters/detects obstacles he grips them and he moves them out the way of the line, then returns to the line and starts following it again, until the next obstacle.

# Our idea and its developement
At the beginning we wanted to develop a gripping robot that can recognize different colored objects and sort them by color. This would work by bringing the different colored objects to plattforms of the corresponding color (e.g. a red object will be transported to the red plattform/red area). However, we had to change this initial vision to accomodate the capacities of the color-sensor. This sensor only works at a very short distance, therefore making it impossible to identify the color of an object that is held in the gripping arms. Fastening the sensor onto the arms also was not possible, because that would make the arm to heavy and awkward.
That is why we changed our idea. Now the color-sensor is used to identify a black line on white ground to follow it. The gripping arms are used to grip objects on the path and take them out of the way. 

# Installation & Prerequisites
1. Get the LEGO® Education SPIKE™ Prime-Set to build your roboter.
2. Download the LEGO® Education SPIKE™ App to your computer. Choose the right version for your operating system.

# Building Jack the Gripper

# Programming

# Lessons learned and future works
We learned a lot about working with the LEGO set and about how to put the parts together in a way that makes sense and works for the intended functions, like the gripping arms of Jack. 
We also learned how the sensors work and about their limitations. For example, the colour sensor only works in very close proximity to an object and only recognizes specific colours (only colours that are present in the LEGO set). Also, the line of colour/black that Jacks follows has to be quite thick, otherwise it only recognizes the white ground in the arena and cannot follow the line. Generally, working with the sensors was quite trial-and-error, we had to find out what works and what does not. 
