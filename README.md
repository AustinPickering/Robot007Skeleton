# Introduction
This project is designed to give you experience with defining your own classes. Your task is to define a simple robot class so that others can use the methods of your class to create and operate the robot or retrieve information about it.

# Background
Tony has just invented a new kind of robot with a fantastic functionality -- teleportation! He calls his new robot "Robot 007". However, his new invention is not flawless since Robot 007 cannot reach the exact point expected. Instead, it may teleport to anywhere in a circle whose center is the intended destination with a radius of 5 feet. Of course, there are also some basic functionalities such as moving forward or backward and rotating left or right. You are required to finish a complete class for Robot 007 so that some user can create a Robot 007 with a name he or she defines and use methods of your class to operate the robot or check its status. 

# Polar Coordinate System
In mathematics, the polar coordinate system is a two-dimensional coordinate system in which each point on a plane is determined by an angle and a distance. As the coordinate system is two-dimensional, each point is determined by two polar coordinates: the radial coordinate and the angular coordinate. The radial coordinate (usually denoted as r) denotes the point's distance from a central point known as the pole. The angular coordinate (usually denoted by θ) denotes the positive or counterclockwise angle required to reach the point from the 0° ray or polar axis (which is equivalent to the positive x-axis in the Cartesian coordinate plane) (see Wikipedia for more information).

In this project, you are required to use the Cartesian coordinate system to represent the position of the robot. However, when moving your robot, what you know is the distance to move and the direction (angle in the polar coordinate system). So, you may want to convert a movement in the polar coordinate system to a movement in the Cartesian coordinate system. 

# Getting Started on the Project
1. Download the GitHub Repository as Zip file.
2. Unzip the file to the desired location.
3. Open the project in IntelliJ to start programming
   - If you are at the initial screen on IntelliJ, click **Open** in the top right corner and select the downloaded folder
   - If you have another project opened, click **File** -> **Open** in the top left corner and select the downloaded folder

# The Robot007 Class
This is the class you are expected to define, together with all its variables and methods. Here is a list of methods you should complete. Also, you are free to define any number of variables, which should all be private, and add any other methods, which may be either private or public. Remember there is no main method in the Robot007 class. 

## Creating method
<code>public Robot007( name : String, x : double, y : double, alpha : double )</code>
Create a new Robot 007 called name with the starting position (x, y) and the initial angle alpha (in the polar coordinate system) representing the robot's initial orientation. Note that this angle alpha is not necessarily the same as the angle formed by the location of the robot with the positive x-axis.

## Operating Methods:
<code>public void moveForward( dist : double )</code>

Move the robot forward (towards the robot's orientation) for dist feet.

<code>public void moveBackward( dist : double )</code>

Move the robot backward for dist feet.

<code>public void rotateLeft( angle : double )</code>

Turn the robot left for angle degrees (the angle increases). After turning, make sure your angle is no less than 0 and smaller than 360 (-1 is equivalent to 359, 100 is equivalent to 460, etc.). Try not to use if statements.

<code>public void rotateRight( angle : double )</code>

Turn the robot right for angle degrees (the angle decreases). After turning, make sure your angle is no less than 0 and smaller than 360.

<code>public void teleport(newx : double, newy : double)</code>

Teleport to (newx, newy). But the place actually reached may be something else (wisely use random numbers to locate a point inside the circle mentioned in the BACKGROUND section). Remember the orientation angle will not change after teleportation.

## Status-checking methods:
<code>public double getX()</code>

Get the x-coordinate of the robot's position.

<code>public double getY()</code>

Get the y-coordinate of the robot's position.

<code>public double getOrient()</code>

Get the orientation angle of the robot.

<code>public String getName()</code>

Get the name of the robot. 

# The RobotOperator class
This RobotOperator class is written for testing. You will be given a sample RobotOperater class. The result you should get after running RobotOperator.java except for the randomized position after teleportation. If there is a really small difference in the double values, for example, 0.9999999999 vs 1.0, do not worry about that. When your project is graded, there will be a totally different RobotOperator class. However, if you write your Robot007 class according to the specification, your result should be correct.
