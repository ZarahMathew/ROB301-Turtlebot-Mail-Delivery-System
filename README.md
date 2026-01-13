# ROB301-Turtlebot-Mail-Delivery-System

The objective of this project is to design a control system by integrating PID line-based
following, dead-reckoning, and Bayesian localization techniques to simulate a robot mail
delivery system. Using ROS, the project designs and tests a Turtlebot to autonomously navigate
through a closed delivery loop and deliver mail to any office on the route. The map consists of
eleven office locations, each marked by one of the four possible colors (red, yellow, green, and
blue) with a numerical label from 2 through 12. It is connected through continuous white tape
that serves as a path for line following. The topological map is shown below:

<p align="center">
  <img alt="Profile Banner" 
       src="https://github.com/user-attachments/assets/a6df4158-2a40-4dd5-af0d-2584010d77c8" 
       width="300">
</p>
As multiple offices share the same colour, deterministic localization is not sufficient for
the robot to recognise its location; instead, it must build a belief distribution over possible
locations and refine this belief continuously using camera sensing. Thus, Bayesian localization is
central for this project. The Turtlebot must integrate accurate line following, color detection, and
state estimation to execute full proof-of-concept demonstration where the robot begins at an
arbitrary location and delivers mail to three randomly selected offices with limited intervention.
