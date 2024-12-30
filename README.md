## High-level Task Planning via Large Language Models (LLMs)

This project makes use of the rich prior and common sense knowledge of LLMs to plan a sequence of actions to solve simple tasks. Then, this sequence of actions are executed by a robotic arm.

### Setup

A set of ArUco markers are used to represent objects. The mounted camera is calibrated to detect and estimate the poses of the markers.

### Demo

Prompt: "I am hungry. Can you give me something to eat?"

![eat gif](eat.gif "Demo")

Prompt: "Clean the table."

![trash gif](trash.gif "Demo")

Prompt: "I need something to cut this onion."

![knife gif](knife.gif "Demo")

### Future Work
* Remove ArUco markers and use other methods for object recognition (like YOLO) and pose estimation (pasive/active stereo, active depth sensor, deep learning).
* Play around with decision-making frameworks like MDPs and POMDPs along with LLMs
