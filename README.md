# lidar-project

This project is about a robot controlled by a Raspberry Pi hat has a lidar on it. 
It can move in various directions since it has mechanum wheels. t has 
software on the host machine that can control the robot, display the 
lidar readings visually, and calculate the robots position. The robot and the 
host machine communicate through a TCP socket.

I also recently added SLAM functionality to it, that can calculate the x and y 
coordinates of the robot and map its surroundings. However, the localization algorithm 
is currently imperfect and the mapping algorithm uses up so many resources that it 
maxes out on CPU and starts lagging behind the data the robot is sending. I'm exploring 
ideas to fix this issue.

Originally the robot used the Neato XV-11 lidar, but I switched to the RPLIDAR A1, 
because it has a much higher refresh rate. This greatly increased the effectiveness of 
the SLAM algorithm.

These are the two sub-repositories for this project:
- [Repository for the software on the host machine](https://github.com/gaborszita/lidar-project-vs)
- [Repository for the program on the robot](https://github.com/gaborszita/lidar-project-rpi)

You can check out the robot in one of its first stages [here](https://www.youtube.com/watch?v=bZktxaEqpzo).
