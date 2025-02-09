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

![IMG_20250123_174120](https://github.com/user-attachments/assets/ea8b04f2-5634-4fe5-b6f7-b66792e204c4)
![IMG20250123174033](https://github.com/user-attachments/assets/ca86d555-1cab-47ac-8358-411717ad5108)
![IMG-20250123-WA0018](https://github.com/user-attachments/assets/dd00f017-d24d-4612-a6b4-8718b6f9b1a4)
![IMG_20250123_173844](https://github.com/user-attachments/assets/1a1b9861-b317-4654-ac53-6c6ec87f7612)
![IMG-20250123-WA0021](https://github.com/user-attachments/assets/903eed4f-5405-441f-be2c-1349c05c2886)

Jack in angry mode and in nervous mode: 

![IMG-20250123-WA0020](https://github.com/user-attachments/assets/4f998e54-dba7-48b0-8999-678c8fca358c)
![IMG_20250209_123139](https://github.com/user-attachments/assets/23b9b419-a5be-4b23-b941-72ae17aac9f9)

# Programming
For programming Jack the Gripper we used the Lego Spike App and its programming user interface. After opening the app you will see some tutorials and example projects. If you have not programmed before or are unfamiliar with the platform, the "First steps"-Tutorial might be of use to you.
To start a new project, click the button "new project". If you want to use an already existing project you can find it by clicking "my projects" in the menu on the left. You can choose between different programming languages: symbol bricks, text bricks, or python. For our project, we used the text bricks.

Follow the instructions to connect your laptop to the Hub. If you connect sensors to the Hub, you will also see their output on the top menu. On the left you can see a menu with different types of bricks with different functions. 

In the following, we will present our code (shown in its entirety here) for Jack and explain what it does.

![WhatsApp Image 2025-01-23 at 16 49 34](https://github.com/user-attachments/assets/f98240bf-8da2-45e0-9147-71ca9a26e278)

![Linie folgen](https://github.com/user-attachments/assets/354a179a-6f8a-4ddb-903d-ead9bbba13d7)

![Arme bewegen](https://github.com/user-attachments/assets/282ec485-11e9-4a2d-86a8-7a9271548141)

![Greifen](https://github.com/user-attachments/assets/0d5afa0e-edef-4e1e-8f35-036da081a42c)

![Ausweichen](https://github.com/user-attachments/assets/ba058e99-5d01-4a48-aaae-73b1859d872f)

![Main](https://github.com/user-attachments/assets/e330c550-6c75-4d12-ac75-186ea00fd65e)
dann Erklärung für die verschiedenen Blöcke mit jeweils bildern, welchen Block man gerade beschreibt -> siehe vergleich Spike Dog

# Lessons learned and future works
We learned a lot about working with the LEGO set and about how to put the parts together in a way that makes sense and works for the intended functions, like the gripping arms of Jack. 
We also learned how the sensors work and about their limitations. For example, the colour sensor only works in very close proximity to an object and only recognizes specific colours (only colours that are present in the LEGO set). Also, the line of colour/black that Jacks follows has to be quite thick, otherwise it only recognizes the white ground in the arena and cannot follow the line. Generally, working with the sensors was quite the trial-and-error, we had to find out what works and what does not. 
The same is also true for the programming. -> bisschen was man beim Programmieren beachten musste etc, was vlt erst schief gelaufen ist -> programmier teil zusammenfassen
