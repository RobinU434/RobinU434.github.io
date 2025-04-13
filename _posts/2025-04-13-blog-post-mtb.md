---
title: 'Developing a Database Application for Molecular Cancer Research'
date: 2025-04-13
permalink: /posts/2025/04/mtb/
tags:
  - project work
  - clinical research
  - database system
---
        
*March 2020 - May 2021*

During my time as a student assistant at the Institute of Medical Bioinformatics and System Biology (IBSM) at the University Clinic Freiburg, I had the opportunity to work on a project with real-world impact in the field of cancer research. Our team was tasked with developing a comprehensive database solution for the Molecular Tumor Board, which would store and organize crucial data for personalized cancer treatments.

## The Challenge

Cancer treatment is increasingly becoming personalized based on the molecular characteristics of each patient's tumor. Molecular Tumor Boards bring together research from medicine, datascience, biology and also sometimes physics to discuss complex cases and determine the best treatment approaches based on genetic and other molecular data.

Our challenge was to create a database system that could:

- Store complex molecular and clinical data
- Enable efficient querying across multiple parameters for each patient
- Maintain strict medical data privacy standards
- Provide an intuitive interface for medical professionals

## From MongoDB to SQL: A Development Journey

Our initial approach was to build the system using MongoDB, a NoSQL database that offers flexibility for handling diverse and complex data structures similar to the document structure you find in medical reports. We spent several months developing a prototype with this technology, but as the project evolved, we encountered some limitations:

1. The need for complex relational queries became increasingly apparent.
2. Data consistency requirements were more stringent than initially expected.
3. The data was also able to be captured in a rigid structure by making some cutoff to flexibility.
4. The team had more expertise in SQL-based systems.

After careful consideration and evaluation, we made the strategic decision to pivot to a SQL-based approach using MariaDB. This decision wasn't taken lightly, as it meant rebuilding significant portions of our work. However, it proved to be the right choice for the project's long-term success.

## Building the Web Interface

With the database foundation solidified, we took off for developing a web interface that would make the system accessible to the medical team. We chose Flask as our web framework, paired with SQLAlchemy as an ORM (Object-Relational Mapping) layer, as Django seemed a bit to much of an overkill at this time.

The interface development focused on:

- Creating intuitive forms for data entry.
- Designing comprehensive but understandable API interfaces to create automatic reports as convenient as possible.
- Enabling efficient search and filtering capabilities.
- Writing tested software to pinpoint errors in future modifications as best as possible.
- Easy rollback capabilities to remove patients data at their will to be conform with data-privacy regulations.
- Inherit portability with Docker container orchestration.
- Deployment of state of the art security frameworks for API user management.

## Impact and Outcomes

By the end of my involvement with the project, we had successfully:

- Deployed a functional database system which was able to manage complex.
- Established protocols for data backup and security.
- Ready to deploy database and REST-API for research purposes.
- Built a system architecture that could scale with growing data needs.

## Wet-Lab Stay

As a very nice add-on professor Börries granted me a 6 weeks to the groups wet labs to see the pipeline of data I was handling in the database from the very beginning. Meaning I was able to see steps from collecting of tissue samples from the clinic, preparing them and sending them to the DKFZ. For me this was very important to understand some (off course not everything ;)) of the biology behind and what are the core characteristics of the data to take care of.

## Reflections

This was my first big programming project and I absolutely loved it. It taught me valuable lessons about database design decisions and the importance of understanding user requirements thoroughly before committing to a technical approach. The transition from MongoDB to SQL highlighted how different database paradigms serve different needs, and how choosing the right tool for the specific context is crucial. The experience of building both NoSQL and SQL implementations of the same system gave me a much deeper understanding of database technologies than any classroom exercise could have provided. Technical perspectives aside it also thought me how valuable and effective a well working team actually is, as I enjoyed my time working and talking with the lab.
The database we built was build as an academic research project if handling highly individual molecular data was even feasible but by the end it has the potential to be a tool that could help physicians make better treatment decisions for cancer patients.

By the end of the project I left the project and sadly also the group because I have seen how much potential data-driven application and methods actually have and wanted to learn more about them on a more theoretical level. Still at I fell in love with the interaction of computer-science and medicine / biology. Especially the wet-lab stay was an extremely nice and eye-opening experience which I would do again any time. the

---

I have written this blog post jointly with Claude.ai and in the retrospective as I setup my webpage in mid-early 2025.
