---
title: "Maze Bot"
image: "images/MazeBotThumbnail.jpg"   # you'll add this image soon
description: "Mechatronics class project to navigate through a maze without touching a wall"
draft: false
---

**What:** A robot goes through every section of a maze to learn the optimal path. Then, it returns back to the start, and completes the maze as fast as possible. The robot never touches a wall during any portion.
**Code:** C++ **Microcontroller:** Arduino Mega 2560
**How:** A lidar sensor (VL6180X) on the right side of the bot for precise wall distance detection. PID control used the lidar sensor to drive the bot straight. Two ultra sonic sensors, one on the front, and one on the left, detected if walls were present in those directions.
**Results:** Had the second fastest time out of 16 contestants.

---

Here's the robot learning the maze in real time:
<video controls autoplay muted playsinline loop width=100%>
  <source src="/videos/BotLearningSlowFixed4.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

Here's the robot learning the maze sped up:
<video controls autoplay muted playsinline loop width=100%>
  <source src="/videos/BotLearningFastFixed2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

Here's the traversing the maze after learning the optimal path:
<video controls autoplay muted playsinline loop width=100%>
  <source src="/videos/MazeRunningFixed.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
