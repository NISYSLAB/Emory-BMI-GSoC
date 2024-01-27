# Emory BMI Google Summer of Code (GSoC) 2024


<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Department of Biomedical Informatics, Emory University (often stylized "Emory BMI" for GSoC communications) is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open-source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from the GitHub repositories of the research labs of Emory University School of Medicine: https://github.com/NISYSLAB


Emory BMI has been a successful mentoring organization for Google Summer of Code 2012 - 2016, 2019, 2021, 2022, and 2023! In recent years, we had 6 accepted contributors in 2023, 8 in 2022, and 6 in 2021. We are excited and looking forward to working with another batch of contributors for the upcoming GSoC. Emory BMI takes pride in having past successes and GSoC contributors turn into long-term collaborators and mentors themselves. Emory BMI also encourages the contributors to collaborate further towards research outcomes, alongside their coding, as most of our GSoC projects include a fair amount of research.

**We have been using Slack as the primary medium of communication. Since Slack has limited the features of the Slack free version, we are slowly moving away from Slack and asking the contributors to communicate via the discussion forums of each project and this central repository instead. These discussion forums also give the contributors the potential to reach a larger audience through their public discussions, providing more transparency to our open-source development discussions.**

Please refer to the [contributor guidelines](/CONTRIBUTOR-GUIDANCE.md) for more details on how to apply and a standard template for the application. The ideas list is given below.

Please go through this [introductory presentation on GSoC](https://pradeeban.github.io/projects/), especially if you are new to GSoC and need some pointers/help on getting started.

# List of Ideas
Discuss the project on the project's discussion forum (as listed below under each project idea), and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.

The ideas are marked easy, medium, and hard in difficulty level. They are also tagged 175 hours, 350 hours, or 350 hours / 175 hours. These three values represent medium-sized projects, large projects, and projects that have the flexibility to be adopted as medium-size projects or extended as large projects.


***
**[1] Development of an Open-Source EEG Foundation Model**

**Mentor:** Mahmoud Zeydabadinezhad (mzeydab -at- emory.edu) and Babak Mahmoudi, PhD

**Overview:** A foundation model refers to a large-scale model that is pre-trained on extensive, often unlabeled data, capturing a broad understanding of that data. Recent studies have indicated that foundation models could potentially offer enhanced robustness and versatility in the analysis of complex patterns within Electroencephalography (EEG) data. This is particularly relevant in scenarios where EEG data for specific downstream tasks is limited in quantity. This project aims to create an open-source foundation model for EEG data analysis. It will involve developing algorithms for EEG signal processing, automatic feature extraction, and implementing deep learning-based algorithms for pre-training a foundation model on publicly available EEG datasets.



**Current Status:** New project.


**Expected Outcomes:** 
* Literature Review: Research and review existing open-source foundation models for medical data, specifically EEG data. Identify the current limitations and challenges in this field.
* A robust, open-source EEG foundation model.
* Documentation and examples demonstrating the model's usage.
* A report detailing the methodologies used and the performance of the model.
* The model weights and code will be made publicly available on a platform such as GitHub.

**Required Skills:**
* Strong programming skills, preferably in Python.
* Experience with deep learning frameworks, preferably PyTorch.
* Knowledge of self-supervised learning and large language models
* Knowledge in signal processing, neuroscience, or related fields.


**Source Code:**  New Project

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***
***
**[2] Python Expansion of the Open Source Electrophysiological Toolbox**

**Mentor:** Reza Sameni, PhD (rsameni -at- dbmi.emory.edu)

**Overview:** Standardized, open-source codes are indispensable in advancing biomedical engineering and biomedical informatics. The Open-Source Electrophysiological Toolbox (OSET) [https://github.com/alphanumericslab/OSET] was conceived in 2006 with this perspective, aiming to offer researchers an open-source codebase for biomedical signal processing. The toolbox has incrementally evolved and expanded over the years. Many researchers have utilized this toolbox for their research. Notably, some modules of OSET have been translated to C/C++ and Python and integrated into medical devices and cloud-based automatic diagnostic systems for large data. It operates under a permissive open license, encouraging community-driven development.
The project aims to continue the Python expansion of OSET to convert it into a standard Python package, broadening access and maintaining consistency across platforms. The planned upgrades include comprehensive cross-language unit tests (between MATLAB and Python), documentation, example codes, installation, and maintenance mechanisms, with a modern software-engineered architecture and objective microbenchmarks. Through this expansion, we aim to extend OSET's benefits to a broader community of AI researchers, also contributing to the training of the next generation of biomedical engineers in the AI era.
OSET will be maintained under the 3-Clause BSD License, a permissive open-source license that allows the redistribution and use of software in any form with adequate disclaimer clauses, offering flexibility for both open-source and commercial use, while minimizing legal complexities.


**Current Status:** Ongoing project.

**Expected Outcomes:**
* A Python package for OSET, with standard unit tests, installation guidelines and documentation. The codebase should operate exactly identical to the current MATLAB implementation.


**Key features:** 
* Open-source code development for biomedical engineering and biomedical informatics.
* Identical cross-language performance
* Standardized unit tests

**Required Skills:**
* Proficiency in Python and MATLAB.
* A background in signal processing
* Experience in biomedical signal processing


**Source Code:**  https://github.com/alphanumericslab/OSET

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***

**[3] A Framework for Unsupervised Deep Clustering**

**Mentor:** Mahmoud Zeydabadinezhad (mzeydab -at- emory.edu) and Babak Mahmoudi, PhD

**Overview:** Clustering is a fundamental task in machine learning and data mining, with a wide range of applications such as image and speech recognition, anomaly detection, and natural language processing. Traditional clustering methods, such as k-means and hierarchical clustering, are based on shallow models and rely on hand-engineered features. In recent years, deep learning techniques have been applied to clustering, resulting in improved performance and the ability to automatically learn features from the data. However, existing methods are mostly supervised and require labeled data, which is not always available. Additionally, they are often not designed to handle low-resource scenarios.

The objective of this project is to develop an open-source framework that utilizes unsupervised deep-learning techniques for data clustering. The framework should be capable of handling low-resource scenarios and be able to scale to large datasets.

**Current Status:** New project.

**Expected Outcomes:** The proposed framework will utilize unsupervised deep learning techniques for data clustering. Specifically, the framework will be based on autoencoder networks, which can be trained to learn a compact, low-dimensional data representation. The encoded data will then be used as input to a clustering algorithm. To handle low-resource scenarios, the framework will also incorporate techniques such as active learning and transfer learning. The framework will be implemented in an open-source programming language, such as Python, and will be made publicly available on a platform such as GitHub.

* Literature Review: Research and review existing unsupervised deep clustering methods for medical data, specifically EEG data. Identify the current limitations and challenges in this field.

* Data Preprocessing: Develop preprocessing techniques to prepare EEG data for unsupervised deep clustering. This includes filtering, denoising, and feature extraction.

* Clustering Framework: Design and develop an unsupervised deep clustering framework that can handle medical data, specifically EEG data. This framework should be able to extract meaningful patterns and insights from the data in an unsupervised manner.

* Evaluation: Evaluate the performance of the developed framework using a variety of metrics and benchmarks. Compare the results to existing unsupervised deep clustering methods for medical data. The framework will be evaluated on publicly available electroencephalography (EEG) data. The performance of the proposed framework will be evaluated using metrics such as normalized mutual information. The framework will also be compared to existing state-of-the-art methods for unsupervised deep clustering.

* Deployment: Create an open-source implementation of the developed framework and make it available for the community to use.

* Applications: Explore the potential applications of the developed framework on various medical data, specifically EEG data. This includes but is not limited to, epilepsy diagnosis, brain-computer interface, and sleep stage classification.

**Required Skills:** Python and deep learning

**Source Code:**  New Project

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***
**[4] A graphical user interface of Foundational Model Toolbox for Image Segmentation**
**Mentors:** Ozgur Kara and Babak Mahmoudi, PhD

**Overview**

* Foundational Model Concept: A foundational model represents a new paradigm in machine learning, characterized by its large-scale and versatile nature. These models are trained on extensive datasets that cover a broad spectrum of topics and data formats, making them robust and adaptable. The term "foundational" reflects their ability to serve as a base framework, adaptable for a myriad of applications across different domains. This adaptability is a key feature, that distinguishes foundational models from traditional models that are often designed for specific, singular tasks.
Graphical User Interface (GUI): The core objective of this project is to develop an open-source Graphical User Interface (GUI) that seamlessly integrates with existing foundational models, specifically tailored for image segmentation tasks. This GUI aims to democratize access to advanced machine learning techniques, enabling users with varying levels of expertise to leverage these powerful models for complex image analysis tasks.

**Key Features:**

* GUI:
Integration of Foundational Models: The GUI will be designed to incorporate several foundational models, providing users with a range of options to choose from based on their specific requirements.
Dataset Compatibility: It will support various datasets, including those commonly used in image segmentation tasks. The ability to handle different data formats and sizes is a crucial aspect of the GUI.
Scalability to MRI Datasets: A significant feature of this project is the GUI's capability to scale and perform efficiently with MRI datasets. This involves handling high-resolution images and complex data structures typical in medical imaging.
User-Centric Design: Emphasis will be placed on creating an intuitive and accessible interface. This involves clear navigation, real-time feedback mechanisms, and visualization tools that allow users to interact with the models and data effectively.
Extensibility and Customization: The GUI will be designed with extensibility in mind, allowing for the future incorporation of additional models, features, and dataset types. Customization options will enable users to tailor the tool to their specific needs.

* Literature Review:
Comprehensive analysis of existing foundational models suitable for image segmentation.
Well-Written Documentation
Detailed installation and setup guide for the GUI.
User manual explaining GUI features, tools, and navigation.
Examples and tutorials for common tasks like loading datasets, model training, and image segmentation.
Technical documentation for developers covering code structure, API usage, and extending the GUI functionality.
Open Source Codes and Demo
Regularly updated code repository on GitHub with source code, dependencies, and installation scripts.
Demo version of the GUI showcasing its key features and capabilities.

**Required Skills**:

* Core Technical Skills
Advanced Python Programming: Proficiency in Python, with a strong understanding of software development best practices, including version control (Git), debugging, and code organization.
Deep Learning Frameworks: Extensive experience with deep learning frameworks, preferably PyTorch.
Foundational Model Expertise
Self-Supervised Learning: Understanding of self-supervised learning principles and techniques, especially as they apply to large-scale foundational models.
Foundational Model Implementation: Experience in implementing, training, and fine-tuning foundational models, with an emphasis on adaptability to various tasks.

* Domain Knowledge
Image Segmentation Techniques: Proficiency in image segmentation techniques, including traditional methods and deep learning approaches.
Medical Image Processing: Familiarity with medical imaging datasets, particularly MRI, and understanding of unique challenges in medical image segmentation.
Signal Processing: Knowledge of signal processing, particularly as it relates to image data.

* Additional Skills
  
UI/UX Design: Skills in UI/UX design for developing an intuitive and user-friendly graphical interface.
Documentation and Communication: Excellent documentation skills for creating clear and comprehensive user manuals and technical guides. Effective communication skills for collaborating with team members and interacting with the open-source community.
Desirable Additional Qualifications
Contributions to Open Source: Previous contributions to open-source projects, especially in related domains, are highly desirable.
Research Experience: Experience in research, particularly in areas related to machine learning, image segmentation, or medical imaging.

**Source Code:** New Project

**Discussion Forum:** https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard

***
**[5] Auto-detect coverage bounding boxes for brain MRI images**

**Mentors:** Puneet Sharma (puneet.sharma -at- emory.edu) and Tony Pan (tony.pan -at- emory.edu)

**Overview:** In this project, we intend to assess whether or not a series of MR images encompass the anatomy of interest, specifically for brain regions. The contributor will develop a methodology to auto-detect and measure the extent of anatomical coverage on brain MR images and determine whether it complies with expected "bounding boxes" set forth by pre-defined protocol constraints.  For example, a protocol may require specific anatomical coverage (e.g., top of the head to ~C2/3 vertebral bodies, with left ear-to-right ear extent), which must be met by acquired MR image data. This module will be part of a larger pipeline to assess overall quality and compliance on MRI modalities.

**Current Status:** This is a new module to run on DICOM images, specifically brain MRI images in DICOM format. This module will execute on DICOM images acquired in real-time or on-demand from a [PACS](https://healthimaging.com/topics/health-it/enterprise-imaging/pacs). For testing purposes during the application period and early stages of development, brain MRI images obtained from public data sources such as [the Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/) can be used.

**Expected Outcomes:** We expect a versatile image processing methodology to autodetect coverage bounding boxes on brain MR images based on stated anatomic landmarks. The algorithm should output a binary compliance score based on comparing the expected "bounding box" and the actual MR image series. The algorithm will be trained on the brain (or other body parts) data and tested on more data of the same body parts for validation and accuracy.

**Required Skills:** Python. Prior experience with DICOM and basic human anatomy would be a plus.

**Code Challenge:** Experience working with machine learning libraries and similar problems is expected. Candidates are encouraged to include links/pointers to code samples or similar projects to highlight their experience in their proposal.

**Source Code:**  New Project

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***
