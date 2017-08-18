my notes as I work through for Udacity's Robotics Nanodegree

## 1. Intro to the ND

Introduces the ND and requirements.

Robotics is growing tremondsouly, and many companies are building out their robotics departments. 

The Udacity ND is built with industry partners and very focused on making things happen with code - so more vocational rather than academic.


What is a Robot?

- a robot has 3 essentials: sensors, capibility to make a decision and ability to perform an action
- A machine which performs a task somewhat autonomously - either by itself like a drone flying by itself or with limited guidance like surgical robotics.
- is a google home a robot? since it takes in inputs, thinks and performs a task. 
- decision making is an essential part of what makes a robot a robot. doesn't need to be AI, just some sort of computational decision making

## Project: Search and Sample Return

Udacity has built a [simulator for this project](https://github.com/udacity/RoboND-Rover-Unity-Simulator). Simulators are a huge part of robotics development, two main ones:

- Unity offers photorealistic image quality, which is great for computer vision (and I imagine demos) and many teams are working to integrate it with ROS
- [Gazebo](http://gazebosim.org/) has a realistic physics engine and integrates well with ROS

Configure environment by following the [steps here](https://github.com/udacity/RoboND-Python-StarterKit/blob/master/doc/configure_via_anaconda.md)

In this project we:
- focus on the image data coming from a front facing camera on the rover
- [telemetery data](https://en.wikipedia.org/wiki/Telemetry): rover's position, throttle, brake, steering angle, speed, [roll, pitch, yaw](https://robotics.stackexchange.com/questions/1051/what-are-human-friendly-terms-for-mobile-robot-orientation-and-relative-directio) etc

Start the project by:

**Record simulator data** in training mode, where you control the rover and record the session as a series of image alongside a csv file which saves image name along with corresponding telemetery data.

**Read camera images** to make a map of the area. Since the drivable area is light and everything else is dark, the problem is simple: map the light/dark areas and assume light areas can be driven on.