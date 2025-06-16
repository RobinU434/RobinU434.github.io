---
title: "Robots in on Farm: My Journey at the Field Robot Event 2025"
date: 2025-06-12
permalink: /posts/2025/06/FRE
tags:
  - Field Robot Event
  - Robotics
  - Computer Vision
  - University Project
---
*April 2025 - June 2025*

---
The Field Robot Event is more than just a competition—it's a crucible where academic theory meets the reality of autonomous systems in the field. This year, our 9-member team from Politecnico di Milano took on the challenge of adapting, programming (and soon repairing) our agricultural robot to master four challenging tasks, competing against 14 other teams from across Europe.


## The Challenge

Under the guidance of supervisors Simone Mentasti, Mirko Usuelli, and Matteo Matteucci, we embarked on this project as part of our coursework. Most of the team did it within the envelope of the current robots course, while other did it as a dedicated semester project. The Field Robot Event, an annual academic competition organized by participating European universities, presented us with four mandatory tasks:

1. **Line navigation in a field** - Basic autonomous navigation following crop rows
2. **Line navigation + object detection** - Navigation with simultaneous object recognition
3. **Navigating around trees and mapping fruits** - Complex obstacle avoidance with fruit detection and mapping
4. **Navigating in a field of mushrooms** - Detecting and mapping UV-glowing mushrooms

My responsibility centered on the third task: building a vision and mapping pipeline capable of detecting and mapping five different fruit types (apples, bananas, grapes, lemons, and oranges) in 3D space.

## The Technical Deep Dive

### Vision System Architecture

The foundation of my approach was YOLO11 nano, which we fine-tuned for fruit detection. This required extensive data collection and labeling—a process that taught me the unglamorous but crucial reality of machine learning applications, in most cases only data help. We paired this with a ZED2i stereo camera, leveraging its depth capabilities to estimate 3D fruit positions.

The theoretical pipeline seemed straightforward:
1. Detect fruits in the camera frame using YOLO11 nano
2. Use depth information to calculate 3D positions in camera coordinates
3. Transform coordinates to global map frame using tf2 and SLAM
4. Map individual fruit instances for competition scoring and return a mapping csv file.

Reality, as usual, had other plans.

### Navigation Nightmares

Our initial plan involved integrating Nav2, ROS2's navigation stack, with SLAM for robust autonomous navigation. What seemed like a standard implementation quickly became a nightmare of compatibility issues. Implementing custom odometry, refactoring control systems, and ensuring everything played nicely with Nav2 proved more challenging than anticipated.

But Nav2 was not the only problem we faced with navigation in task three and four. Because our Lidars where mounted quit low and the competition field was a nice field of gras we picked up to much noise from the gras which rendered SLAM more or less useless. Our solution, one night before rebuilding the Lidar setup and the tf-transformations for navigation (sounds again straightforward, but the robotics engineers among those who read this will understand the struggles which could / and have caused this). Unfortunately this did not fix the problems we had with Nav2 so....
after another sleepless night debugging on the competition venue itself, we made the difficult decision to abandon Nav2 entirely. Instead, we implemented a simplified Model Predictive Control (MPC) approach: sample control parameters, simulate collision scenarios, and select the safest trajectory. It wasn't elegant, but it worked and got the robot moving—a recurring theme in this project.

While seeing the robot just moving randomly on the field and not crashing into obstacles I felt relieved we pulled off what seemed a couple of hours earlier impossible. It was not an effective policy of individually circling trees to get nice detections but rather bouncing from corner to corner, from tree to tree. At this point I have to thank my teammates Adriano and Lorenzo who improvised the moving nodes on the morning such that we could start right after lunch.

### The Tracking Dilemma

Task 3 required mapping individual fruit instances, not just detections. This meant we needed either tracking or clustering algorithms to maintain fruit identity across multiple observations.

I initially chose visual tracking, implementing algorithms like DeepSORT, ByteSORT, and StrongSORT. These tools work excellently in traditional scenarios where the camera is stationary and objects move. However, our scenario was inverted—the entire scene moved as our robot navigated, while fruits remained stationary. This fundamental difference broke the assumptions these algorithms were built on.

With just days before the competition, I pivoted to clustering approaches based on  global coordinates. Using Gaussian Mixture Models (GMM) and DBSCAN with hyperparameter optimization through random search to minimize Bayesian Information Criterion (BIC), we achieved acceptable fruit instance mapping. Not perfect, but functional—another lesson in pragmatic engineering. On the competition reality said 'Hi' again-this meant something in the pipeline broke again which resulted in collapsed 3D coordinates and not correct mapping. 

## Lessons from Outside Research

Up to this point in my career I focused on research projects, carefully designing software for usability, reproducibility and innovation. But after seeing this robotics project on the initial list (without knowing what it is going to be like) and the thought of what to do after my master degree I wanted to try something which is more related to engineering and maybe real-world project work. In the end I took a couple of key-lessons learned with me.

### Beyond the Comfort Zone

This project put me far outside my research comfort zone. Instead of careful experimentation and methodical development, we operated in permanent hackathon mode. The mantra became: "If it works, move on to the next problem." Perfectionism was a luxury we couldn't afford. Reflecting this made me realize that I should stick for the moment maybe closer to research and development and step away from engineering. Although I think engineering has some pleasing moments in it (especially when something works out). 

### Team Dynamics and Skill Gaps

Working with a team spanning vastly different skill levels and backgrounds proved both challenging and educational. Some members were beginners heavily reliant on AI assistants like ChatGPT, while others brought technical knowledge and genuine curiosity to learn. Bridging these gaps while maintaining project momentum required constant adaptation of communication and task delegation strategies. Additionally it became clear that clear communication, knowledge unification (instead of fragmentation) and a project lead with a clear plan in mind, leading skills and technical oversight of the project is crucial. Especially if you work with a newly put together team and on a thigh time-budget where you do not have time to get back on, not even off track.    

### The Robustness Reality Check

My biggest technical takeaway lessons is similar to previous projects: simplicity trumps sophistication in real-world applications. Complex solutions might perform better in controlled lab environments, but robustness is infinitely more valuable in the field. A simple system that works consistently (but not as good) beats an elegant one that fails under different conditions. This is definitely something I will lookout for in future projects and design methods more closely to the designated schedule (simple to complex approaches). 

During this project we where interacting with ROS2 almost all the time, therefore I'm thankful for the opportunity to to learn from experience working with a real robotic system. Topics like node design, node interactions, modular development in the context of ROS2 where tackled by tutorials and guides but as almost always developing your project raises questions which those tutorials cannot really answer but hands on experience can.

## The Competition Experience

Despite the stress, sleep deprivation, and occasional (more towards frequent ;P ) frustration, the competition itself was remarkable. Seeing teams from across Europe converge in Milan, each bringing unique solutions to the same fundamental challenges, like completely different robot design or approaches in Software, created an atmosphere of collaborative competition, where people also where helping out across their team border, that I found genuinely inspiring and motivating. 

As a recurrent theme in this Blog-post I can only repeat: there's something magical about watching machines act autonomously—robots navigating complex environments, making decisions, and accomplishing tasks without human intervention. These moments made all the debugging sessions and architectural rewrites worthwhile.

## Mixed Feelings and Future Reflections

I'm leaving this experience with decidedly mixed feelings about robotics as a field. On one hand, the fundamental fascination remains strong. The technical challenges are engaging, the community is welcoming and intellectually inspiring, and the potential applications are genuinely exciting.

On the other hand, I've gained a healthy appreciation for the frustrations inherent in robotics: hardware that breaks at inconvenient moments (or almost all the time), mysterious driver issues, embedded systems throwing unprecedented errors, and the general unpredictability of physical systems.

While reflecting this project I've also confirmed my preference for building persistent, well-architected software over hackathon-style rapid prototyping. While the latter has its place and can be exhilarating, my natural inclination leans toward creating robust, maintainable systems that outlast their initial use case.

## Conclusion

The Field Robot Event was simultaneously one of the most challenging and rewarding experiences of my academic career. It forced me to confront the gap between theoretical knowledge and practical implementation, taught me valuable lessons about team dynamics and project management under pressure, and provided invaluable insights into the realities of robotics development.

Would I do it again? Absolutely. Would I approach it differently? Definitely. But that's perhaps the most valuable lesson of all—every project, successful or not, teaches us something essential about both technology and ourselves.

For anyone considering similar competitions or robotics projects, my advice is simple: embrace the chaos, prioritize robustness over elegance, and remember that the most valuable learning often happens when things don't go according to plan.

*Special thanks to our supervisors Simone Mentasti, Mirko Usuelli, and professor Matteo Matteucci for their guidance, and to my teammates: Angela Remolina​, Alessio Spineto​, Erdal Yalçın​, Alisa Pesotskaia​, Luis Caballero​, Lorenzo Arcangeli​, Filippo Di Fiore​ (and Paolo Ginefra, who participated in the last years edition of FRE and helped out especially during difficult time) for making this challenging journey memorable despite the occasional 3 AM debugging session.*

![FRE-team](https://robinu434.github.io/files/blog-post-figures/2025-06-12-FRE-team.png "FRE 2025 team Politecnico di Milano")



----- 
I have  written this blog post jointly with Claude.ai.