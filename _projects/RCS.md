---
title: "Autonomous Rubik’s Cube Solver"
collection: projects
type: "Project"
permalink: /projects/RCS
venue: "SSNCE"
date: 2019-10-15
location: "Chennai, India"
--- 

## Introduction

The project is a Rubik’s Cube solver bot whose primary objective is to solve the Rubik’s Cube in the least number of moves. Stepper motors are used to control the rotation of 
grippers which rotate the faces of the cube during the cube solving process. The Bot utilizes an Arduino UNO microcontroller to control and coordinate the rotation of the 
stepper motors.

**Code for the project is found [here](https://github.com/marjerie/Rubiks-Solver).**

## Mechanical Assembly

The frame of the Bot was fabricated using aluminium as it is a lightweight material and so it makes the structure portable. 
The four grippers, used to rotate the faces of the cube, are manipulated using four NEMA 17 stepper motors which are mounted on a platform. 
These platforms are placed on aluminium rails and are connected to two NEMA 23 stepper motors which aid in its back and forth movement. 
A NEMA 23 stepper motor, which is positioned below the rails, helps with the motion of two NEMA 17 stepper motors. 
The grippers were made using acrylic sheets and are attached to the shaft of the corresponding stepper motors.

<p align="center">
  <img src="https://marjerie.github.io/files/RBS_ma.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

## Working

The current state of the Rubik’s Cube ie. the information of the colours on the faces of the unsolved cube are inputted to the computer. 
The code used for colour recognition is given [here](https://github.com/marjerie/Rubiks-colourrecognition).
Kociemba’s Algorithm is applied to the input on python and the optimum solution to solve the cube is computed and it is outputted in the form of a string data type. 
The output string is in the form of the "Singmaster notation", which was developed by David Singmaster. 
The letters L, R, F, B, U, and D indicate a clockwise quarter-turn of the left, right, front, back, up, and down face respectively. 
Half turns are indicated by appending a 2. A counterclockwise quarter turn is indicated by appending a prime symbol ( ′ ). 

<p align="center">
  <img src="https://marjerie.github.io/files/RCS_ka.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>

The [program](https://github.com/marjerie/Rubiks-Solver) in the Arduino UNO reads the output string and sends control signals to the stepper motor drivers. The control signals are sent sequentially 
to a particular motor driver which rotates the specific stepper motor which in turn rotates the face of the cube. The control signals are consecutively sent 
to the motor drivers with a small time delay to ensure proper rotation of faces of the cube. After all the rotation moves are performed on the cube by the grippers, 
the Rubik’s cube is completely solved.

<p align="center">
  <img src="https://marjerie.github.io/files/RBS.jpg?raw=true" alt="Photo" style="width: 450px;"/> 
</p>
