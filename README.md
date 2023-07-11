# Emory BMI Google Summer of Code (GSoC) 2024


<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Department of Biomedical Informatics, Emory University (often stylized "Emory BMI" for GSoC communications) is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from the GitHub repositories of the research labs of Emory University School of Medicine: https://github.com/Emory-HITI, https://github.com/sharmalab, https://github.com/NISYSLAB, and https://github.com/controlcore-project/


Emory BMI has been a successful mentoring orgnaization for Google Summer of Code 2012 - 2016, 2019, 2021, 2022, and 2023! In the recent years, we had 6 accepted contributors in 2023, 8 in 2022, and 6 in 2021. We are excited and looking forward to working with another batch of contributors for the upcoming GSoC. Emory BMI takes pride in having the past successes and GSoC contributors turning into long-term collaborators and mentors themselves. Emory BMI also encourages the contributors to collaborate further towards research outcomes, alongside their coding, as most of our GSoC projects include a fair amount of research.

**We have been using Slack as the primary medium of communication. Since Slack has limited the features of the Slack free versison, we are slowly moving away from Slack and asking the contributors to communicate via the discussion forums of each project and this central repository instead. These discussion forums also give the contributors the potential to reach a larger audience through their public discussions, therefore, providing more transparency to our open source development discussions.**

Please refer to the [contributor guidelines](/CONTRIBUTOR-GUIDANCE.md) for more details on how to apply and a standard template for the application. The ideas list is given below.

Please go through this [introductory presentation on GSoC](https://pradeeban.github.io/projects/), especially if you are new to GSoC and would need some pointers/help on getting started.

# List of Ideas
Discuss the project on the project's discussion forum (as listed below under each project idea), and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.

The ideas are marked easy, medium, and hard in difficulty level. They are also tagged 175 hours, 350 hours, or 350 hours / 175 hours. These three values represent the medium-sized projects, large projects, and the projects that have the flexibility to be adopted as a medium-size project or extended as a large project.


***


**[1] Making ZeroMQ a first-class feature of concore.**

**Mentors:** Mark Arnold (markgarnold -at- yahoo.com)

**Overview:** [concore](https://github.com/ControlCore-Project/concore) is a lightweight framework for closed-loop peripheral neuromodulation control systems. concore consists of its own file-sharing based _concore_ protocol to communicate between the programs in a study. We have introduced an [osparc-control](https://pypi.org/project/osparc-control/0.0.2/) based communication as an alternative to this default file-sharing based concore protocol. 

[osparc-control](https://github.com/ITISFoundation/osparc-control) is an extension of [ZeroMQ](https://zeromq.org/). osparc-control based implementation replaces the file-sharing mechanism restricted to one local machine with message queues that can be transmitted between locally networked machine. This osparc-control based communication should be promoted as a first-class approach to implement the edges of concore.

![The study with 0MQ](figures/0mq.png)
**Current Status:** Currently, a [simple osparc-control based implementation](https://github.com/ControlCore-Project/concore/tree/main/0mq) exists in concore. However, these ZeroMQ edges are not visible in concore editor, the browser-based visual editor for concore. Consequently, studies with ZeroMQ edges are represented as forests instead of directed hypergraphs, due to the "invisible" ZeroMQ edges. This also means, to run a concore study with ZeroMQ-based edges, we have to run each hypergraph in the forest separately.

**Expected Outcomes:** We need to promote a unified experience in concore, whether the edges are actually implemented via the default file-sharing approach, or through this experimental osparc-control/ZeroMQ message-based approach. To illustrate the ZeroMQ-based edges, the contributor can choose to introduce a new assumption that all the ZeroMQ-edges must start with "0" in their labels. Usually, we label the edges with alphabetical characters. Therefore, this is a safe assumption. Once such a graph with ZeroMQ-edges is made (a single directed hypergraph, rather than a forest with disjoint two or more directed hypergraphs), we should be able to seamlessly build and run the study regardless of the underlying communication mechanism. Thus, we aim to demonstrate the possibility of a seamless local vs. distributed execution in a cluster through ZeroMQ.

**Required Skills:** Python

**Code Challenge:** Prior experience in Python must be demonstrated. Prior experience with message-oriented middleware frameworks such as ZeroMQ can be a plus, although not mandatory.

**Source Code:**  https://github.com/ControlCore-Project/concore

**Discussion Forum**: https://github.com/ControlCore-Project/concore/discussions

**Effort:** 350 Hours

**Difficulty Level:** Medium

***

**[2] A Reference Implementation for concore Library in Java or Julia.**

**Mentors:** Mark Arnold (markgarnold -at- yahoo.com), Gautam Kumar (gautam.kumar -at- sjsu.edu)

**Overview:** [concore](https://github.com/ControlCore-Project/concore) is a lightweight framework for closed-Loop peripheral neuromodulation control systems. Currently, it supports implementations of programs in Python, C++, Matlab, Octave, and Verilog. In this project, the contributor will develop a reference implementation of the concore library in Java or Julia.

**Current Status:** We developed the concore library initially in Python, and then implemented support for other languages. The contributor will work towards a reference implementation in Java or Julia in this project. The successful completion of this project will expand the user base of concore to include Java/Julia developers.

**Expected Outcomes:** A complete reference implementation of the concore Library in Java or Julia.

**Required Skills:** i) Java or Julia and ii) Python

**Code Challenge:** Demonstration of previous expertise in Java/Julia and Python can be beneficial.
 
**Source Code:**  https://github.com/ControlCore-Project/concore

**Discussion Forum**: https://github.com/ControlCore-Project/concore/discussions

**Effort:** 175 Hours

**Difficulty Level:** Medium

***


**[3] A Framework for Unsupervised Deep Clustering**

**Mentor:** Mahmoud Zeydabadinezhad (mzeydab -at- emory.edu) and Babak Mahmoudi (b.mahmoudi -at- emory.edu)

**Overview:** Clustering is a fundamental task in machine learning and data mining, with a wide range of applications such as image and speech recognition, anomaly detection, and natural language processing. Traditional clustering methods, such as k-means and hierarchical clustering, are based on shallow models and rely on hand-engineered features. In recent years, deep learning techniques have been applied to clustering, resulting in improved performance and the ability to automatically learn features from the data. However, existing methods are mostly supervised and require labeled data, which is not always available. Additionally, they are often not designed to handle low-resource scenarios.

The objective of this project is to develop an open-source framework that utilizes unsupervised deep learning techniques for data clustering. The framework should be capable of handling low-resource scenarios and be able to scale to large datasets.

**Current Status:** New project.

**Expected Outcomes:** The proposed framework will utilize unsupervised deep learning techniques for data clustering. Specifically, the framework will be based on autoencoder networks, which can be trained to learn a compact, low-dimensional representation of the data. The encoded data will then be used as input to a clustering algorithm. To handle low-resource scenarios, the framework will also incorporate techniques such as active learning and transfer learning. The framework will be implemented in an open-source programming language, such as Python, and will be made publicly available on a platform such as GitHub.

* Literature Review: Research and review existing unsupervised deep clustering methods for medical data, specifically EEG data. Identify the current limitations and challenges in this field.

* Data Preprocessing: Develop preprocessing techniques to prepare EEG data for unsupervised deep clustering. This includes filtering, denoising, and feature extraction.

* Clustering Framework: Design and develop an unsupervised deep clustering framework that can handle medical data, specifically EEG data. This framework should be able to extract meaningful patterns and insights from the data in an unsupervised manner.

* Evaluation: Evaluate the performance of the developed framework using a variety of metrics and benchmarks. Compare the results to existing unsupervised deep clustering methods for medical data. The framework will be evaluated on a publicly available electroencephalograpghy (EEG) data. The performance of the proposed framework will be evaluated using metrics such as normalized mutual information. The framework will also be compared to existing state-of-the-art methods for unsupervised deep clustering.

* Deployment: Create an open-source implementation of the developed framework and make it available for the community to use.

* Applications: Explore the potential applications of the developed framework on various medical data, specifically EEG data. This includes, but is not limited to, epilepsy diagnosis, brain-computer interface and sleep stage classification.

**Required Skills:** Python and deep learning

**Source Code:**  New Project

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***

**[4] Auto-detect coverage bounding boxes for brain MRI images**

**Mentors:** Puneet Sharma (puneet.sharma -at- emory.edu) and Tony Pan (tony.pan -at- emory.edu)

**Overview:** In this project, we intend to assess whether or not a series of MR images encompass the anatomy of interest, specifically for brain regions. The contributor will develop a methodology to auto-detect and measure the extent of anatomical coverage on brain MR images, and determine whether it is compliant with expected "bounding boxes" set forth by pre-defined protocol constraints.  For example, a protocol may require specific anatomical coverage (e.g. top of the head to ~C2/3 vertebral bodies, with left ear-to-right ear extent), which must be met by acquired MR image data . This module will be part of a larger pipeline to assess overall quality and compliance on MRI modalities.

**Current Status:** This is a new module to run on DICOM images, specifically brain MRI images in DICOM format. This module will execute on DICOM images acquired in real-time or on-demand by Niffler. For testing purposes during the application period and early stages of development, brain MRI images obtained from public data sources such as [the Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/) can be used.

**Expected Outcomes:** We expect a versatile image processing methodology to autodetect coverage bounding boxes on brain MR images based on stated anatomic landmarks. The algorithm should output a binary compliance score based on the comparison between the expected "bounding box" and the actual MR image series. The algorithm will be trained on the brain (or other body parts) data and tested on more data of the same body parts for validation for accuracy.

**Required Skills:** Python. Prior experience with DICOM, along with basic human anatomy, would be a plus.

**Code Challenge:** Experience working with machine learning libraries and similar problems is expected. Candidates are encouraged to include links/pointers to code samples or similar projects to highlight their experience in their proposal.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Discussion Forum**: https://github.com/Emory-HITI/Niffler/discussions

**Effort:** 350 Hours

**Difficulty Level:** Hard


***
