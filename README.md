# Goals for 2025

## REPORT EVERYTHING

Log. Every. Thing. You. Do. Yes, even the slightest thing. This helps track changes, learn from others' mistakes, and is just good practice. 

## Implement NMPC

Didn't have time in 2024, better than the bodged together Stanley controller. Should also be able to avoid obstacles. 

## Implement car detection using computer vision. 

Supposed to get a Qualcomm RB5, probably won't, but we should still try and explore the vision option. Not my field of expertise, but the conditions are very optimal, so we'll maybe get something that works. 

## Optional: Double up on pies.

Two Raspberry Pis. One for the SLAM localization, another for the NMPC. More = better, right? Maybe dedicate one to only doing Vision stuff, if it's too heavy to run concurrently. To be tried out. 




# Autonomous RC Car Race 2025

![Us at ENS](ressources/pictures/ens_pic.jpeg)

## Project Overview
This is a project made by Sorbonne University students. The goal is to make autonomous RC cars that can drive around a track and avoid obstacles for the ENS organized CoVAPSy (*Course Voiture Autonome Paris Saclay*) race.

We entered two cars in the 2024 race, both using two different navigation heuristics. The hardware is pretty much identical between the two cars, but one of them uses a Dynamixel instead of a standard Servo for steering control. 

The project is divided into five main parts:
- **ROS packages for the first car (Reactive)** [course_2024_pkgs](https://github.com/SorbonneUniversityBolideContributors/course_2024_pkgs)
- **ROS packages for the second car (SLAM)** [course_2024_pkgs](https://github.com/SorbonneUniversityBolideContributors/course_2024_slam_pkgs)
- **Bolide scripts** [bolide_scripts](bolide_scripts/) contains scripts for specific implementations on the vehicle
- **ressources** [ressources](ressources/) contains some basic ressources for the project
- **Simulation** [SimuWebots](SimuWebots/) contains the simulation of the bolide in Webots
- **STM32 code** [CoVAPSy_STM32](CoVAPSy_STM32/) contains the code for the STM32 microcontroller that link the car sensors to the Raspberry Pi

![Bolide](ressources/pictures/cars.jpeg)
:-------------------------:|:-------------------------:

## ENS Race Overview
https://ajuton-ens.github.io/CourseVoituresAutonomesSaclay/

## Getting Started

Install ROS Noetic on your computer. Check the [ROS Noetic installation guide](http://wiki.ros.org/noetic/Installation/Ubuntu) for more information.

Check the [Robot_setup.md](ressources/Robot_setup.md) file to get started with the robot.

Bolide's IP when connected to the rooter (SSID=R15-AF66) at St-Cyr
- IP bolide2: 192.168.137.78
- IP bolide1: 192.168.137.165

Check the [ros_bashrc_lines.md](ressources/ros_bashrc_lines.md) file and copy ir to you're own `~/.bashrc`.
It'll save you a lot of trouble when connecting to the robots or interacting with the simulation or simply with ROS.
Make sure that there are no double declarations and that the ROS environement variables `ROS_NAMESPACE` and `ROS_MASTER_URI` are unset.

Then you are ready to clone the ROS packages and build them !

For further information about our ROS packages, check the [course_2024_pkgs](https://github.com/SorbonneUniversityBolideContributors/course_2024_pkgs) repository.
