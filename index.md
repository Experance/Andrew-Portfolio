---
layout: default
title: Andrew Wood
---

# Andrew Wood

Aspiring Robotics Software Engineer | FIRST Robotics Alum | CS Student

📫 [Email me](andrewrxzwood@gmail.com)  
📄 [Download Resume](Andrew_Wood_Resume.pdf)  
🔗 [GitHub](https://github.com/Experance) | [LinkedIn](www.linkedin.com/in/andrew-wood-936564245)

---

## 🚀 Projects / Experience

### [FIRST Tech Challenge](https://github.com/KCheck25/FtcRobotController/tree/Power-Play-Klaws) -- 2022-2023 School year
- **Tech**: Java, OpenCV, Servos, Motors
- Programmed a robot to have both a tele-op and autonomous portion (for the FTC competition), with a focus on autonomous
- What did I do: I programmed the robot to be able to autonomously score a pre-given cone one a pole, as well as then drive to a different place to collect another cone and score again. The autonomous allowed length was 30 seconds, and the goal was to score as many cones on poles as possible (with cones on higher poles earning more points). There is a video [here](https://www.youtube.com/watch?v=HsitvZ0JaDc) that describes the competition in detail.
![20345FTC_frontview](https://github.com/user-attachments/assets/95a30e40-ace1-4c74-911e-a149e1619c66)

##### Challenges
- This was my first time ever programming a robot, so there was quite a bit to learn, but I focused hard and learnt as fast as I could, with the support of multiple more experienced programmers.
- The biggest challenge I faced when programming this robot's autonomous was consistency. At the beginning, I had programmed all the distances manually -- measuring the accumulated encoder value for the motors while driving the robot and then programming the robot to move each motor to that distance with a P-controller for the autonomous portion. And this was true not only for driving, but also for our elevator system. But after the autonomous failed miserably in our first competition, I began to look for another way to improve the consistency, which could account for the constantly accumulating errors. After extensive research, I landed on OpenCV, a computer vision library. I communicated with engineers about this problem, and worked with them to mount a basic webcam, with which I could utilize to adjust the robot's position to the poles to score at and cones to grab. The final result can be seen in the video below.
- [Demo Video](https://www.youtube.com/shorts/M_ZZlYpLnVc)

##### Achievements
- Qualified and competed in the Washington State competition!
- Below is an image of me, my twin, and our head engineer talking about the new code we are adding to our robot as we test it at the States competition.
![20345FTC_statespic](https://github.com/user-attachments/assets/76c81750-cdbb-40e3-a006-fbadf5cc3a72)

---

### [FIRST Robotics Challenge](https://github.com/yourusername/sorting-arm) -- 2023-2024 School year
- **Tech**: Python, OpenCV, Servo motors
- Designed a computer vision system to detect and sort colored objects using a robotic arm.
- [Demo Video](https://www.youtube.com/watch?v=demo-link)

---

## 🧠 Skills
- Languages: Python, Java
- Tools: OpenCV, Git

---

## 📬 Contact
Email: andrewrxzwood@gmail.com  
GitHub: [github.com/yourusername](https://github.com/Experance)  
LinkedIn: [linkedin.com/in/yourusername](https://linkedin.com/in/andrew-wood-936564245)

---

<footer>
<p>Last updated: {{ site.time | date: '%B %Y' }}</p>
</footer>
