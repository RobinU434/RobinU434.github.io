---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

PDF versions: [short CV]({{ base_path }}/files/cv/CV_Robin_Uhrich.pdf) · [long CV]({{ base_path }}/files/cv/CV_Robin_Uhrich_long.pdf)

<details open>
  <summary><strong>Short CV</strong></summary>
  <object data="{{ base_path }}/files/cv/CV_Robin_Uhrich.pdf" type="application/pdf" width="100%" height="800px">
    <p>Your browser cannot display the PDF inline. <a href="{{ base_path }}/files/cv/CV_Robin_Uhrich.pdf">Download the short CV</a>.</p>
  </object>
</details>

<details>
  <summary><strong>Long CV</strong></summary>
  <object data="{{ base_path }}/files/cv/CV_Robin_Uhrich_long.pdf" type="application/pdf" width="100%" height="800px">
    <p>Your browser cannot display the PDF inline. <a href="{{ base_path }}/files/cv/CV_Robin_Uhrich_long.pdf">Download the long CV</a>.</p>
  </object>
</details>

Education
======
* M.S. in Machine Learning, University of Tübingen, 2026 (expected)
* M.S. in Computer Science, Politecnico di Milano, 2025 (Erasmus Exchange, February 2025 - August 2025)
* B.S. in Computer Science, University of Freiburg, 2023 (October 2019 - September 2023)
* Aeronautics and Space Engineering, University of Stuttgart, 2019 (October 2018 - September 2019)

Publications
======
* Robin Uhrich, Marco Bagatella, Núria Armengol Urpí, Pavel Kolev, Georg Martius. **Occupancy Modeling via Drifting: One-Step Generation Enables Direct Policy Extraction.** Preprint, 2026. [arXiv:2610.19883](https://arxiv.org/abs/2610.19883)
 
Work Experience
======
* November 2026 - December 2026: Visiting Researcher (upcoming)
  * University of North Carolina at Chapel Hill
  * Host: Prof. Weitong Zhang
  * Research stay on offline reinforcement learning with expressive probabilistic samplers

* October 2025 - March 2026: Student Assistant
  * University of Tübingen, Autonomous Learning Group
  * Supervisor: Prof. Georg Martius, Jens Beißwenger, Anna Manasyan
  * Duties included: Working with humanoid robots, development of VLA (Vision-Language-Action) models applied to humanoid robotics

* August 2024 - February 2025: Student Assistant
  * BG Clinic - Tübingen, Hand, plastic, reconstructive and burn surgery
  * Supervisor: Dr. Cosima Prahm, Dr. Dominik Steiner, Daniel Höglinger
  * Duties included: Developing software interfaces, implementing deep learning pipeline for EMG to pose data, implementing convolutional, recurrent, and transformer architectures for time series data, making NinaPro dataset accessible through PyTorch

* July 2024 - February 2025: Freelancer
  * Volatilis, Ludwigsburg, Germany
  * Duties included: Implementing a browser-based simulation engine for risk modeling, business and operational development

* December 2023 - May 2024: Student Assistant
  * AI-Center Tübingen, Central Office
  * Duties included: Writing a wiki containing organizational aspects for international PhD students and post-doctoral researchers, performing and analyzing a department-wide survey on experiences of international researchers

* April 2023 - August 2023: Intern
  * Fraunhofer Italia, Advanced Robotics Group, Bolzano, Italy
  * Supervisor: Dr. Andrea Giusti, Dr. Marco Todescato
  * Duties included: Building vision-guided imitation learning pipeline for modular robot manipulator, implementation of computer vision pipeline for 3D hand trajectory tracking, object recognition and segmentation with multi-stereo camera feed, re-implementation of Task-Parameterized Gaussian Mixture Model for imitation learning, development of Modular-Robot optimization pipeline, web-based interface design for containerized pipeline setup
  * Technologies used: Python, NumPy, OpenCV, ROS2, C++, Moveit, Eigen

* July 2022 - April 2023: Student Assistant
  * Institute of Intelligent Machine-Brain Interfacing Technology (IMBIT), Neurorobotics Group, University of Freiburg
  * Supervisor: Prof. Joschka Boedecker, Jasper Hoffmann
  * Duties included: Maintenance and mechanical work for Unitree A1 robot, interface documentation for custom quadrupedal policy deployment, literature review in reinforcement learning and control theory

* June 2021 - March 2023: Student Assistant
  * Fraunhofer Institute for Physical Measurement Technology (IPM), Object and Shape Detection Department
  * Supervisor: Prof. Alexander Reiterer, Dr. Philipp von Olshausen, Dr. Annette Schmitt
  * Duties included: Development of multilabel image classification pipeline with convolutional neural networks, conducted hyperparameter optimization study on fine-tuning of CNNs, collection of 3D point cloud data of urban habitation

* March 2020 - May 2021: Student Assistant
  * University Clinic Freiburg im Breisgau, Institute of Medical Bioinformatics and System Biology (IBSM)
  * Supervisor: Prof. Melanie Börries, Dr. Patrick Metzger, Maria Hess
  * Duties included: Developing a database application for molecular cancer research, conducting technical feasibility study involving relational and non-relational databases, implementing web interface for SQL database with Flask and SQLAlchemy, making application feasible for server-deployment in containerized fashion

Project Work
======

## University Projects

* **Master Thesis** (since October 2025)
  * Lab of Prof. Georg Martius
  * Supervisors: Dr. Pavel Kolev, Núria Armengol Urpí, Marco Bagatella
  * Topics: occupancy modelling, generative models, offline meta-RL

* **Distributed RL on Optimal Transport** (April 2025 - October 2025)
  * Project at lab of Prof. Marcello Restelli, Politecnico di Milano
  * Supervisor: Dr. Marco Mussi
  * Redesign of rail environment from Flatland3 for multi-agent RL in asynchronous setting to solve train-scheduling problem
  * Switched perspective from train-focused to switch-focused
  * Tools: Python, Flatland3, Gymnasium, PettingZoo

* **Field Robot Event** (March 2025 - June 2025)
  * Multi-Disciplinary Project at Politecnico di Milano
  * Instructors: Prof. Matteo Matteucci, Dr. Simone Mentasti, Mirko Usuelli
  * Built and programmed robot for agricultural-robotics competition in team of nine
  * Third place at the Field Robot Event 2025 competition
  * Implementation of navigation, computer-vision and decision making algorithms
  * Conducted study on visual object tracking in moving stereo-camera setting with DeepSORT
  * Tools: Python, ROS2, PyTorch, Yolo

* **Multi-Agent RL in Laser Hockey** (December 2024 - February 2025)
  * Course Project on "Reinforcement Learning" taught by Prof. Georg Martius
  * Took part in an organized multi-agent RL competition in laser hockey
  * Extended SAC from Stable-Baselines3 with a custom replay buffer
  * Implemented and extended Deep Dyna-Q with entropy regularization
  * Contributed to development of the laser-hockey environment

* **Generalized Simulation Based Inference** (October 2024 - April 2025)
  * Practical Machine Learning, ML-Lab project
  * Supervisor: Prof. Jakob Macke, Julius Vetter
  * Extended sampling strategies in simulation-based inference with amortized cost estimation (paper by Dr. Richard Gao) with guided diffusion models
  * Re-implemented GBI-ACE for benchmarking on toy and real world datasets
  * Implementation using PyTorch framework

* **LR-Scheduler Analysis** (April 2024 - July 2024)
  * Seminar Project: "Deep Learning Research Kitchen"
  * Instructors: Prof. Philipp Hennig, Dr. Frank Schneider, Dr. Jonas Geiping, Dr. Antonio Orvieto
  * Conducted study of multiple learning rate schedulers and their hyperparameters affecting training of a Vision Transformer on CIFAR-10
  * Implemented pipeline using PyTorch-Lightning, TensorBoard, NumPy and Matplotlib

* **Precipitation Prediction Analysis** (December 2023 - February 2024)
  * Data Literacy Group Project by Prof. Philipp Hennig
  * Supervisor: Emilia Magnani
  * Data science project on climate data in group of four
  * Analyzed accuracy of precipitation forecast of German weather agency against real data for Baden-Württemberg

* **EASRL-LM-2D-IKB** (July 2023 - September 2023)
  * Bachelor Thesis at lab of Prof. Joschka Boedecker
  * Supervisor: Jasper Hoffmann
  * Topic: Expanding Action Space in Reinforcement Learning through Latent Models: A 2D Inverse Kinematics Benchmark
  * Merged Soft Actor-Critic with generative models such as pretrained Variational Autoencoder for noise augmentation and faster learning
  * Implementation of custom inverse kinematics environment with scalable action space

* **Learning Quadrupedal Locomotion From Scratch** (April 2022 - September 2022)
  * Bachelor research project with Felix Schulz at lab of Prof. Joschka Boedecker
  * Supervisor: Jasper Hoffmann
  * Implemented training pipeline for RL experiments around PPO concerned with perturbation and reward-shaping
  * Minimalist re-implementation of Vision-Guided Quadrupedal Locomotion
  * Used and extended existing physics-simulator based on PyBullet
  * Libraries: Stable-Baselines3, PyTorch, Gym, Weights & Biases, TensorBoard
  * Conducted study on closing sim-to-real gap on Unitree A1 robot

* **ALE Plots** (May 2022 - September 2022)
  * Seminar Project: "Fair and Interpretable Machine Learning"
  * Instructor: Dr. Janek Thomas
  * Re-implementation of Accumulated Local Effect plots
  * Implementation using Python with NumPy and Matplotlib

* **Humboldt Game** (October 2020 - April 2021)
  * Course project on "Practical Software Development"
  * Organizers: Prof. Andreas Podelski, Dr. Vincent Langenfeld
  * Supervisor: Antonia Hinkerohe
  * Designed, implemented and tested real-time multi-agent strategy game "Humboldt"
  * Collaborated in team of six using Git for version control
  * Programmed in C# using XNA-(monogame)-framework

## Private Projects

* **LazySlurm** (since November 2025)
  * Terminal user interface for monitoring Slurm HPC jobs, published on PyPI as `lazyslurm-py` under the MIT license
  * Live overview of running and past jobs, log inspection, resource and CPU/GPU usage, job cancellation, editing and resubmission, and partition load
  * Remote mode running over a single background SSH connection with one-time two-factor authentication
  * Built in Python with the Textual framework

* **Simplified RNNs Research Project** (since April 2025)
  * Based on GateL0rd paper by Dr. Christian Gumbsch
  * Simplifying architecture and conducting study on latent state similarities

* **SPARK Research Project** (April 2025 - November 2025)
  * Stochastic Policies Augmented for Robust Knowledge/Exploration
  * Built on idea of Bachelor's Thesis
  * Augmentation of stochastic policies for robust exploration and more expressive action distributions
  * Extension of SAC to leverage non-diagonal Gaussian distributions for action sampling
  * Benchmarking on 2D inverse kinematics environment using Stable-Baselines3

* **Tide - Torch Integrated Data Engine** (since February 2025)
  * Data toolkit for handling sequential data for single or multi-file datasets
  * Compatible with PyTorch dataset, data-loader integration, feature engineering, time-based splitting, filtering
  * Integration into publicly available time series data: EMG, climate, finance, robotics

* **Config2Class** (since October 2024)
  * Developed Python tool to automatically generate structured configuration classes from various file formats
  * Adds support for code completion in IDE
  * Integrates with Hydra and OmegaConf

* **PyArgWriter (CLIfy)** (since September 2023)
  * Developed Python tool to automatically create command-line interface for Python projects based on OOP paradigm
  * Implemented automatic code generation, code parsing tooling, tree-structured command generation, Hydra integration

* **Hexapod Robot** (since May 2021)
  * Building custom Hexapod robot using Freenove Big-Hexapod robot kit, Jetson Nano B01, stereo vision, custom stationary power supply
  * Implementing RViz2 and Gazebo simulation plugins, ROS2 architecture, low-level servo controller, high-level walking controller
  * Designing custom proprioceptive sensing for closed-loop controller design for cheap-PWM sensors
  * Conducted study on mobile neural-depth estimation for stereo-vision

## Student Assistant Research Projects

* **Human2Humanoid VLA Research Project** (October 2025 - March 2026)
  * Lab of Prof. Georg Martius and Prof. Wieland Brendel
  * Supervisors: Anna Manasyan, Jens Beißwenger
  * Finetuning Vision-Language-Action models applied to humanoid robotics
  * Collecting humanoid demonstration data
  * Conducting studies on action representations and generalization in behavior cloning
  * Topics: tele-operation, re-targeting, RL, action representation, human-to-robot generalization

* **Hand Kinematics Estimation from EMG Data** (August 2024 - February 2025)
  * BG-Clinic project
  * Supervisor: Daniel Höglinger at lab of Dr. Cosima Prahm
  * Designed deep learning pipeline for hand kinematics estimation based on EMG data
  * Designed the pipeline for use by researchers outside computer science
  * Involved redesign of dataset acquisition and processing, network architecture setup, augmentation handling
  * Pipeline based on PyTorch-Lightning
  * Datasets: NinaPro, SEED, emg2pose

* **PACT Deep Energy Retrofit** (August 2022 - March 2023)
  * Fraunhofer IPM project under Dr. Annette Schmitt
  * Collected 3D data for point cloud segmentation with laser scanners

* **Amphora Automated Pavement Operation** (September 2021 - November 2022)
  * Fraunhofer-IPM project under Prof. Alexander Reiterer with Dr. Annette Schmitt
  * Implemented multilabel image classification pipeline on laser scan data with CNNs (ResNet & VGG) and Vision Transformer
  * Conducted classification-oriented real-time study with hyperparameter optimization (Bayesian Optimization + Hyperband)
  * Implemented image processing pipeline: laser scanner → geojson

* **Molecular Tumor Board Research Database** (March 2020 - May 2021)
  * IBSM team project under Prof. Melanie Börries
  * Development of database application for molecular tumor research
  * Conducted study on database design choices between SQL, document-based and graph-based database systems
  * Knowledge acquisition from tissue collection to sequencing to annotation pipeline
  * Collecting wet-lab experience and testing UI-design choices with research staff

Awards
======
* **Field Robot Event** - 3rd place (August 2025)
* **System Design Project** - 3rd place (February 2020)

Extracurricular Activities
======

* **Private Statistics Tutor** (September 2025 - October 2025)
  * Tutoring undergraduate students in statistics

* **Organizational Staff - EWRL 18** (September 2025)
  * Volunteer at the 18th European Workshop on Reinforcement Learning in Tübingen
  * Assisting at registration, discussions, demonstrations

* **Organizer - Machine Learning Reading Club** (February 2025 - June 2025)
  * Organization of journal club for ML targeted at CS master students at Politecnico di Milano
  * Within association: "Polimi Data Scientists"
  * Tasks: selecting papers, organizing speakers, communicating to fellow students

Skills
======
* **Programming Languages:** Python, C, C++, C#
* **Python Libraries:**
  * Deep Learning: PyTorch, PyTorch Lightning
  * RL: Gymnasium, PettingZoo, Stable-Baselines3
  * Data Science: NumPy, Pandas, SciKit-Learn
* **Robotics:** ROS, ROS2, Moveit
* **Databases:** SQL, NoSQL Database Systems
* **Tools:** Git, SVN, Docker, SLURM
* **CAD:** Mechanical CAD (Autodesk Inventor)
* **Embedded Systems:** Arduino, ESP
* **Project Management:** SCRUM

Languages
======
* German (native)
* English (C1/C2)

Personal Interests
======
* Archery (bronze medal at European Championships 2018)
* Running (mid to long distance)
* Road cycling
* Photography
