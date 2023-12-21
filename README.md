# Emory BMI Google Summer of Code (GSoC) 2024


<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Department of Biomedical Informatics, Emory University (often stylized "Emory BMI" for GSoC communications) is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from the GitHub repositories of the research labs of Emory University School of Medicine: https://github.com/Emory-HITI, https://github.com/sharmalab, https://github.com/NISYSLAB, and https://github.com/controlcore-project/


Emory BMI has been a successful mentoring organization for Google Summer of Code 2012 - 2016, 2019, 2021, 2022, and 2023! In recent years, we had 6 accepted contributors in 2023, 8 in 2022, and 6 in 2021. We are excited and looking forward to working with another batch of contributors for the upcoming GSoC. Emory BMI takes pride in having past successes and GSoC contributors turn into long-term collaborators and mentors themselves. Emory BMI also encourages the contributors to collaborate further towards research outcomes, alongside their coding, as most of our GSoC projects include a fair amount of research.

**We have been using Slack as the primary medium of communication. Since Slack has limited the features of the Slack free version, we are slowly moving away from Slack and asking the contributors to communicate via the discussion forums of each project and this central repository instead. These discussion forums also give the contributors the potential to reach a larger audience through their public discussions, providing more transparency to our open source development discussions.**

Please refer to the [contributor guidelines](/CONTRIBUTOR-GUIDANCE.md) for more details on how to apply and a standard template for the application. The ideas list is given below.

Please go through this [introductory presentation on GSoC](https://pradeeban.github.io/projects/), especially if you are new to GSoC and need some pointers/help on getting started.

# List of Ideas
Discuss the project on the project's discussion forum (as listed below under each project idea), and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.

The ideas are marked easy, medium, and hard in difficulty level. They are also tagged 175 hours, 350 hours, or 350 hours / 175 hours. These three values represent medium-sized projects, large projects, and projects that have the flexibility to be adopted as medium-size projects or extended as large projects.


***

**[1] A Framework for Unsupervised Deep Clustering**

**Mentor:** Mahmoud Zeydabadinezhad (mzeydab -at- emory.edu) and Babak Mahmoudi (b.mahmoudi -at- emory.edu)

**Overview:** Clustering is a fundamental task in machine learning and data mining, with a wide range of applications such as image and speech recognition, anomaly detection, and natural language processing. Traditional clustering methods, such as k-means and hierarchical clustering, are based on shallow models and rely on hand-engineered features. In recent years, deep learning techniques have been applied to clustering, resulting in improved performance and the ability to automatically learn features from the data. However, existing methods are mostly supervised and require labeled data, which is not always available. Additionally, they are often not designed to handle low-resource scenarios.

The objective of this project is to develop an open-source framework that utilizes unsupervised deep learning techniques for data clustering. The framework should be capable of handling low-resource scenarios and be able to scale to large datasets.

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

**[2] Auto-detect coverage bounding boxes for brain MRI images**

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
