---
layout: default
title: Andrew Wood
---

# Andrew Wood

Aspiring Robotics Software Engineer | FIRST Robotics Alum | CS Student

📄 [Download Resume](Andrew_Wood_Resume.pdf)  
🔗 [GitHub](https://github.com/Experance) | [LinkedIn](https://www.linkedin.com/in/andrew-wood-936564245)

---

## 🚀 Projects / Experience

### [FIRST Tech Challenge](https://github.com/KCheck25/FtcRobotController/tree/Power-Play-Klaws) -- 2022-2023 School year
- **Tech**: Java, OpenCV, Servos, Motors
- Programmed a robot to have both a tele-op and autonomous portion (for the FTC competition), with a focus on autonomous
- What was my focus: I programmed the robot to be able to autonomously score a pre-given cone on a pole, as well as then drive to a different place to collect another cone and score again. The autonomous allowed length was 30 seconds, and the goal was to score as many cones on poles as possible (with cones on higher poles earning more points). There is a video [here](https://www.youtube.com/watch?v=HsitvZ0JaDc) that describes the competition in detail.

![20345FTC_frontview](https://github.com/user-attachments/assets/95a30e40-ace1-4c74-911e-a149e1619c66)

#### Challenges
- This was my first time ever programming a robot, so there was quite a bit to learn, but I focused hard and learnt as fast as I could, with the support of multiple more experienced programmers.
- The biggest challenge I faced when programming this robot's autonomous was consistency. At the beginning, I had programmed all the distances manually -- measuring the accumulated encoder value for the motors while driving the robot and then programming the robot to move each motor to that distance with a P-controller for the autonomous portion. And this was true not only for driving, but also for our elevator system. But after the autonomous failed miserably in our first competition, I began to look for another way to improve the consistency, which could account for the constantly accumulating errors. After extensive research, I landed on OpenCV, a computer vision library. I communicated with engineers about this problem, and worked with them to mount a basic webcam, with which I could utilize to adjust the robot's position to the poles to score at and cones to grab. The final result can be seen in the video below.
- [See here](https://www.youtube.com/shorts/M_ZZlYpLnVc)

#### Achievements
- Qualified and competed in the Washington State competition!
- Below is an image of me, my twin, and our head engineer talking about the new code we are adding to our robot as we test it at the States competition. I'm the one holding the laptop.

![20345FTC_statespic](https://github.com/user-attachments/assets/76c81750-cdbb-40e3-a006-fbadf5cc3a72)

---

### [FIRST Robotics Challenge](https://github.com/FIRSTRoboticsTeam9450/Crescendo2024/tree/KrakenGeneratedSwerve) -- 2023-2024 School year
- **Tech**: Java, WPILib, Command Based Programming, Servos, Motors
- This was our high school Robotics Club's first time ever doing FRC, and of course, my first time as well. My brother and I spearheaded the effort by putting together (wiring both power and CAN message cables as well) and programming basic components -- literally just trying to get motors to run and such -- and learning as much as possible.
- As we gained experience, we began putting together more complex systems, and I did less wiring and more programming as more engineers in our club joined the effort. By the end of the school year, we had a swerve drive robot (8 motors for the drive chain, where 4 determine the direction of the wheels and another 4 rotate the wheels forward and backward) with an arm that could extend, which also had a wrist at the end that held an intake.

![FRC_robot_worlds_pic_with_ring](https://github.com/user-attachments/assets/089543ef-8e11-48b1-942f-7a2753c9fa49)

- What was my focus? My focus this time was on teleoperations. In the first half of the season, I primarily worked on the swerve drive -- first trying to write one from scratch, then implementing a library we found and debugging it as well as tuning PID constants. During the second half, I put some time into the arm, extension, wrist, and intake subsystems, and also rewrote most of our codebase right before our Worlds competition so that it would be better organized and it would be easier to debug once we were competing.
- I also worked on a project where I translated the machine binary language of sticky faults into actual English so that we could understand what sort of errors were getting thrown, so that we could better understand what was happening during matches. It was helpful in telling us when we had brownouts and why the robot sometimes did unexplainable things.
- I also put a lot of time into figuring out how to efficiently log robot motor data, which was of huge help in tuning PID constants, as well as other bug fixing. The logging that I set up became the main tool with which we would try to understand and debug issues with our robot. Below is an image of some of those logs (and also of the fact that programmers can make tables out of anything)

![FRC_logging_pic_specialtable](https://github.com/user-attachments/assets/c37c4421-4b7a-4feb-aff9-c2918ce59895)

- Other than the above, I tuned the PD controllers for the arm, extension, and wrist when necessary (along with other programmers)
- Our robotics club had a side project with a turret and shooter, which my brother and I handled. That also involved tuning a PD controller for the turret (my focus was on the turret). I wrote a custom ramp-up and ramp-down for the turret to help protect the motors (and gears, since they were 3D-printed). Our club had some fun with that afterwards: [See here](https://youtu.be/Gbj8j9VlADM). I also got the turret to be able to track an AprilTag (I'm the one holding the AprilTag in the video): [See here](https://youtube.com/shorts/ilFk3bICOwI). Later, I also made it so that it could be teleoperated controlled, and after the operator stopped touching the controls, the turret would go back to tracking an AprilTag.
  
#### Challenges
- There were a bajillion challenges throughout this robotics season, just from the fact that we started off by knowing absolutely nothing about how FRC was programmed, but I'll focus on two. The first was that though FRC and FTC both used Java (or at least we chose Java), we decided to use an entirely different programming system for FRC -- command-based, which was a far cry from the sequential-based programming in FTC. So when I first started with trying to get a motor to run, I had trouble even figuring out where to put the code to run the motor! With some mentorship from more experienced teams as well as in-depth research online, me and the rest of the programmers in our club were able to figure out how to properly organize our code, and get it to run more complicated actions and steps.
- I mentioned above that my focus was primarily on the swerve-drive for the first half of the season. Out of the many troubles I had in getting it working, the biggest by far was a drive issue that no re-tuning of PID constants ever helped -- we called it "the drive bug". Now, that may seem very broad of a phrase, but it was such a recurrent issue that everyone in our club knew about it. What would happen was that the controller joysticks for driving the robot would be at 0, or within the deadband that we programmed, and the robot would continue driving forward. Checking the motor power data showed that it was being supplied some voltage, despite our code specifically setting it to 0! And it would randomly occur, too, so it was quite challenging to pinpoint what the issue was. It ended up taking me 3 months to fix, and I had to jump on it every so often to try to solve it. At the time, we were using a swerve drive library that someone else had written, and I had gotten into contact with the creator of that library and tried to debug with him, and he also couldn't figure out the issue. Eventually, I found a problem in his library which happened to affect just us, and I wrote a custom fix, which completely got rid of the problem. 
- I have added here a video of our robot scoring and driving: [See here](https://youtu.be/pJ0YbytgoHA)

#### Achievements
- Qualified and competed in Worlds (international competition) for our rookie year!
- Here we have a world's recap video that our club's media team made: [See here](https://youtu.be/clTzfojAXtk)

---

## 🧠 Skills
- Languages: Python, Java
- Tools: OpenCV, Git, WPILib Tools
- Other: Electrical (Wiring, Sautering), PID-Controller, Command-based Programming

---

## 📬 Contact
Email: andrewrxzwood@gmail.com  
GitHub: [github.com/Experance](https://github.com/Experance)  
LinkedIn: [linkedin.com/in/andrew-wood-936564245](https://linkedin.com/in/andrew-wood-936564245)

---
