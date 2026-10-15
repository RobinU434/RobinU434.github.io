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

I want to build learning systems that work the way scientists do: take the record of what a system has done, infer the structure that explains it, and decide which new experiment is worth running. Reinforcement learning is the most general framework I know for this, and probabilistic generative models are the tools I reach for. Most progress in offline RL still means staying close to the data, with behavior foundation models pretrained on reward-free experience and then mostly imitating it. I want to understand what structure these models learn, how to go beyond imitation with it, and how a little online experience can help them most. None of this is specific to robotics: most scientific data is offline too, and a neural circuit or a lab experiment is an environment that cannot be reset.

**Discovering structure in behavior foundation models.** Occupancy and forward-backward models learn a compact representation of everything a system can do. When does that representation recover real structure, such as skills, symmetries or controllable factors? How can we test it, and how can structural hypotheses be fed back in as inductive biases for more data-efficient learning?

**Going beyond imitation with uncertainty.** A generative occupancy model can evaluate policies that were never executed in the data, but it is confidently wrong far away from that data. Epistemic uncertainty should mark where this trust ends. One-step generators make the necessary ensembles or posterior samples cheap, and simulation-based inference provides much of the toolkit.

**Offline-to-online as experimental design.** When an agent may collect a little new experience, it should spend it where it best separates its hypotheses about the world, not where things are merely novel. This is the step from imitating data to acting like a scientist, and it is the same problem as choosing the next experiment in a lab.

My master's thesis, supervised by Marco Bagatella, Dr. Núria Armengol Urpí and Dr. Pavel Kolev, is a first step in this direction: a temporal-difference objective for drifting models, one-step generators of discounted state occupancies learned from reward-free data. Because the model is differentiable in a single step, policies can be extracted by backpropagating straight through it, without distilling an auxiliary critic.

## Publications

- **Occupancy Modeling via Drifting: One-Step Generation Enables Direct Policy Extraction**  
  **Robin Uhrich**, Marco Bagatella, Núria Armengol Urpí, Pavel Kolev, Georg Martius  
  *Preprint*, 2026. [arXiv:2610.19883](https://arxiv.org/abs/2610.19883)

## Research experience

**UNC Chapel Hill, group of Prof. Weitong Zhang** (Nov–Dec 2026, upcoming)  
Research stay on offline reinforcement learning with expressive probabilistic samplers.

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
