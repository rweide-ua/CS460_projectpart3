# Homework 4 ROS2 Notes

## Miata Group for HW4 CS460
Anastasia Spencer, Lilly Eide, Jeongbin Son

### The Miata Algorithm

Our algorithm uses a rudimentary "wall-follow" algorithm.
At the start, the bot moves forward until it finds a wall. Once it finds a wall, it will turn until the right sensor readings from the LIDAR sensor no longer increases, meaning the bot is facing along the wall. Once this occurs, the bot is considered to be following the wall.
From here, the bot moves forward. If the distance from the wall becomes too small, the bot will turn away from the wall and continue moving forward.
If the distance from the wall becomes too big, it will turn back towards the wall to get closer and continue moving forward.

If the bot reads the same 10 values for the front and side values, it will consider itself to be stalled, and will try to get out of the stall.

Doing this wall follow creates snake like behavior allowing for the robot to scan all tags found on the following wall.
