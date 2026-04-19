---
title: Erik Fredin
---
<h1 style="font-size: 2.6rem; margin-bottom: 0.2rem;font-family: 'Georgia', serif;">

  <a href="/" style="text-decoration: none; color: inherit;">
    Erik Fredin
  </a>

  <span style="font-size: 2.0rem; color: black; font-weight: normal; margin-left: 10px;">
    |
    <a href="./Resume.pdf" style="color: black">Resume</a> |
    <a href="./projects" style="color: black">Projects</a> |
    <a href="./publications" style="color: black">Publications</a>
  </span>

</h1>
# 🚀 Projects

### *Robot Pose Estimation in Medical (OCT) Images |  University of Toronto*
  
<!-- ![Project Screenshot](./assets/VoxelNeXtChanges.jpg)
*a) VoxelNeXt architecture from orignal paper, b) VoxelNeXt architecture for pose estimation in OCT images* \
🎥 Demo (GIF):  
![Demo GIF](assets/project1-demo.gif) -->

<!--📹 Video Demo:-->  
<video src="./assets/oct-video.mp4" controls width="600"></video>

<!--📝 Description:-->  
This is project was a collaboration between my lab and another lab at the University of Toronto. We estimate the 8 degree-of-freedom pose of a small surgical robot in medical (OCT) images. To achieve this, I reworked the architecture of a deep-learning model originally designed for detecting objects in LiDAR scans. The model leverages a keypoint detection approach to estimate the pose very accurately (5 degree joint angle error, 0.6 mm position error). We also used pose estimation to control the robot for performing a simple task, specifically picking up and dropping off a tube. Using pose estimation to do this task (closed loop) outperforms conventional control without pose estimation (open-loop). This work has been published in IEEE Robotics and Automation Letters. 


🔗 Links:
- 🌐 [Publication](https://ieeexplore.ieee.org/abstract/document/11297825)    
- 📜 [Paper PDF](https://microrobotics.mie.utoronto.ca/wp-content/uploads/2025/12/xSeed_RaL___Final_Submission.pdf)  
- 🖥️ [Project Website (incl. code)](https://medcvr.utm.utoronto.ca/ral2025-oct-pose.html)  

---

### *Computer Vision via Endoscopic Cameras | University of Toronto* 

<video src="./assets/0315.mp4" controls width="600"></video>

The aim of this project was to estimate the surgical robot's 3D pose in real time via a small monocular camera. The camera here simulates the use of an endoscope in a surgical settings. This project was split into two scenarios, specifically estimating the robot's 3D pose when 1) the camera is fixed relative to it, and 2) when the camera moves relative to the robot. 

Regarding scenario 1), I developed two methods to estimate the robot's joint angles: a deep-learning method and a particle-filter based method. For the deep-learning based method, I designed a DNN architecture that estimates the joint angles with a 4.4° error and 30 Hz speed. The particle filter was designed for the robot's unique magnetic actuation system, and outperformed the deep-learning method in a video sequence (see video above). These results were presented at the International Conference on Intelligent Robot's and Systems (IROS), 2024.

For scenario 2), I developed a automatic label extraction method via Segment Anything Model (SAM2) and optimization. This method automatically extracts 8 degree-of-freedom pose pseudo-labels given an image of the robot. I extracted data using this method, and trained a real-time pose estimation model using it. The resulting DNN estimated the pose with a position error of 2.8 mm, an orientation error of 4.8° and a joint angle error of 6.4°. This work has not yet been published, but will likely be published at a major robotics conference in the near future. 

🔗 Links:  
- 🌐 [Publication (first half of project)](https://ieeexplore.ieee.org/abstract/document/10802411)    


---
### *Pioneering a driverless racecar | Lund Formula Student*
<div style="display:flex; gap:20px;">
<div style="min-width:220px; max-width:220px;">
<video src="./assets/LFS-Driverless.mp4" controls width="100%"></video>
</div>

<div style="flex:1;">
Lund Formula Student (LFS) is a design team at Lund University, Sweden, designing and building a racecar in a year, and competing against other universities over the summer. In 2020-2021, I was part of the newly created driverless team, which pioneered the development of a self-driving racecar at Lund University. I was in charge of developing an emergency brake system (EBS). Since the EBS needed to brake the car in emergencies, it could not rely on any electric or combustion energy to actuate braking. Instead, I designed a system of pistons and actuators that used compressed air to acomplish emergency braking. This system was used in the video shown here to brake the car. I also helped to conceptualize the electronic components of the EBS, designed a speed controller for the car in ROS and designed other mechanical components. Due to complications with COVID-19, we could not compete with the driverless vehicle. But the video to the left provides a demonstration during a test drive. 

<br>

In 2018-2019, LFS worked on a combustion engine based racecar. Here, I was working on the mechanical design of the car's suspension system. During production, I was mainly responsible for making carbon-fiber components for the car's chassis. For this year, the team placed 2<sup>nd</sup> in the FS Netherlands competition and 8<sup>th</sup> in FS Germany.
</div>
</div>

### *Autonomous vehicle simulations | Volvo Cars, Sweden*
<video src="./assets/Esmini1.mp4" controls width="600"></video>

For my Master's Thesis, I developed algorithms in C++ to control simulated vehicles at Volvo Cars, Sweden. Volvo Cars had previously developed an open-source, light-weight traffic simulator called Esmini as a means to cheaply test autonomous driving and assisted driving software in simulation. My project involved developing a controller that decides when to change how other vehicles behave, switching from reacting relative to the autonomous car to acting independently. This allows simulated traffic scenarios to remains realistic. It does this by briefly predicting how the situation will unfold and switching from relative to independent control if the predictions are not matched by the scenario. The solution has been tested inside Esmini and produced reliable results across 5+ different scenarios. My code was added to the Esmini GitHub after the project was completed.  

🔗 Links:  
- 🌐 [Esmini GitHub](https://github.com/esmini/esmini)
- 📜 [Thesis](https://lup.lub.lu.se/student-papers/search/publication/9061680)    


