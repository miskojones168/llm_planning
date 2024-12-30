## High-level Task Planning via Large Language Models (LLMs)

This project makes use of the rich prior and common sense knowledge of LLMs to plan a sequence of actions to solve simple tasks. Then, this sequence of actions are executed by a robotic arm.

### Setup

A set of ArUco markers are used to represent objects. The mounted camera is calibrated to detect and estimate the poses of the markers.

### Methodology

Build a set of primitive skills/actions and let the LLM use those actions to control the arm.

Implemented actions so far,

* ```move_to```: Use a path planning or control algorithm to move the end-effector to a target location. In this project, Positional Based Visual Servoing (PBVS) is used.
* ```pick```: Command gripper to close.
* ```release```: Command gripper to open.
* ```return```: Move arm to predefined joint configuration. 

### Demo

Prompt: "I am hungry. Can you give me something to eat?"

![eat gif](eat.gif "Demo")

Prompt: "Clean the table."

![trash gif](trash.gif "Demo")

Prompt: "I need something to cut this onion."

![knife gif](knife.gif "Demo")

### Future Work
* Remove ArUco markers and use other methods for object recognition (like YOLO) and pose estimation (using pasive/active stereo, active depth sensor, deep learning for depth estimation).
* Play around with decision-making frameworks like MDPs and POMDPs along with LLMs.
