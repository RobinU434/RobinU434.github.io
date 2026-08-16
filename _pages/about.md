---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a Machine Learning master's student at the University of Tübingen, writing my thesis in the Autonomous Learning Group of Prof. Georg Martius. Before Tübingen I studied computer science in Freiburg, and I spent the first half of 2025 on an Erasmus exchange at Politecnico di Milano.

Most of what I have worked on sits somewhere between reinforcement learning, probabilistic modelling, and robotics. I started on the applied side, classifying road damage from laser scans at Fraunhofer IPM, building a database for molecular cancer research at the University Clinic Freiburg, and moved toward reinforcement learning through my bachelor thesis on latent action spaces and a quadrupedal locomotion project applied to the Unitree A1. That mix has stuck: I like problems where a principled probabilistic idea stays in contact with the problem of decision making.

## Research interests

I am interested in generative modelling for sequential decision making, currently in two directions.

**Single-step samplers for action spaces.** Most policies still model actions as a diagonal Gaussian. I am looking at what changes when the action distribution comes from a more general single-step generative sampler instead (Drifting, Terminal-Velocity-Matching, ...), and what that buys an online RL algorithm.

**Meta-RL from offline data.** Given a fixed dataset and only little knowledge of the downstream task, how much can be learned in advance? Behavior foundation models are what interest me most here. What they actually internalise from offline data, how behavior ends up represented, and how far zero-shot RL can push that: extracting as much as possible from a dataset with respect to any task that might arrive later. Part of the appeal is practical, since probabilistic models that are cheap to sample from and differentiable end to end open up offline and model-based methods that would otherwise be out of reach.

My thesis sits between the two, on occupancy modelling and generative models for offline meta-RL, supervised by Marco Bagatella, Dr. Núria Armengol Urpí and Dr. Pavel Kolev.

## Research experience

**Autonomous Learning Group, University of Tübingen** (2025–2026)  
Finetuned Vision-Language-Action models for humanoid robots under Prof. Georg Martius and Prof. Wieland Brendel — collecting demonstration data and studying how action representations affect generalisation in behavior cloning.

**Politecnico di Milano, lab of Prof. Marcello Restelli** (2025)  
Reframed the Flatland3 rail environment around switches rather than trains, for asynchronous multi-agent RL on train scheduling.

**BG Clinic Tübingen** (2024–2025)  
Built a deep learning pipeline estimating hand kinematics from EMG signals, designed to be usable by researchers outside computer science.

**Fraunhofer Italia, Advanced Robotics** (2023)  
Vision-guided imitation learning for a modular robot manipulator, re-implementing task-parameterized Gaussian mixture models and handling multi-camera trajectory recording.

**Neurorobotics Group, University of Freiburg** (2022–2023)  
Bachelor thesis combining Soft Actor-Critic with variational autoencoders to expand action spaces, plus work on sim-to-real transfer for quadrupedal locomotion.

## Things I build

- [LazySlurm](https://github.com/RobinU434/LazySlurm) — a terminal UI for monitoring Slurm jobs, the way `htop` works for a machine. Live job overview, log inspection, GPU usage, and remote clusters over a single SSH connection. On PyPI as `lazyslurm-py`.
- [Tide](https://github.com/RobinU434/Tide) — a PyTorch data engine for sequential and time series datasets
- [SPARK](https://github.com/RobinU434/SPARK) — non-diagonal Gaussian policies for SAC, grown out of my bachelor thesis
- [CLIfy](https://github.com/RobinU434/PyArgWriter) and [Config2Class](https://github.com/RobinU434/Config2Class) — developer tooling for generating CLIs and typed configuration classes
- A hexapod robot I have been rebuilding since 2021, currently running ROS2 with custom proprioceptive sensing and stereo vision

## Toolbox

Python for most things (PyTorch and Lightning, Gymnasium, PettingZoo, Stable-Baselines3, NumPy, Pandas), C++ where it needs to be fast, ROS2 and Moveit for robots, Docker and SLURM for getting experiments to run somewhere other than my laptop.

## Teaching and service

- Organiser of the Machine Learning Reading Club at Politecnico di Milano, within Polimi Data Scientists (2025)
- Volunteer at the European Workshop on Reinforcement Learning (EWRL 18) in Tübingen (2025)
- Private statistics tutor (2025)

## Beyond research

Archery was my sport for years, seriously enough to take a bronze medal at the European Championships in 2018. I have since traded precision for endurance and put the competitive side into road cycling and running instead. Photography is the part I keep entirely uncompetitive.

The full record is on my [CV](/cv/), and I am happy to hear from anyone working on similar problems.
