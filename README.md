# Emory BMI's Journey with Google Summer of Code (GSoC) 2025: Pioneering Open Source Biomedical Informatics


<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Welcome to the Department of Biomedical Informatics at Emory University, a beacon of innovation in open-source development for biomedical informatics research. Department of Biomedical Informatics, Emory University (often stylized "Emory BMI" for GSoC communications) is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open-source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from the GitHub repositories of the research labs of Emory University School of Medicine: https://github.com/NISYSLAB


**Celebrating a Decade of Impact:**
Since our initial steps in GSoC 2012 to the remarkable milestones of 2024, Emory BMI has continued to thrive, welcoming numerous contributors year after year. As we gear up for GSoC 2025, we're excited to mentor a new wave of innovators, guiding them from contributors to long-term collaborators. Emory BMI takes pride in having past successes and GSoC contributors turn into long-term collaborators and mentors themselves. Emory BMI also encourages the contributors to collaborate further towards research outcomes, alongside their coding, as most of our GSoC projects include a fair amount of research.

**Commitment to Diversity and Inclusion:**
At Emory BMI, we ardently believe in the power of diversity to drive innovation. We are dedicated to creating an inclusive environment that encourages participation from all backgrounds, especially aiming to empower women and minorities in science and technology. Your unique perspectives are invaluable to us, and we invite you to join our diverse community of thinkers and creators.


**We have been using Slack as the primary medium of communication. Since Slack has limited the features of the Slack free version, we are slowly moving away from Slack and asking the contributors to communicate via the discussion forums of each project and this central repository instead. These discussion forums also give the contributors the potential to reach a larger audience through their public discussions, providing more transparency to our open-source development discussions.**

Please refer to the [contributor guidelines](/CONTRIBUTOR-GUIDANCE.md) for more details on how to apply and a standard template for the application. The ideas list is given below.

# List of Ideas
Discuss the project on the project's discussion forum (as listed below under each project idea), and once you are ready to submit your application, use the template below. **You must submit your application directly using the GSoC Program Site.** If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.

The ideas are marked easy, medium, and hard in difficulty level. They are also tagged 90, 175, and 350 hours. These three values represent small-size, medium, and large projects.


***
# **[1] Title: Securing Linux Storage with ACLs: An Open-Source Web Management Interface for Enhanced Data Protection**

Mentor(s): Mahmoud Zeydabadinezhad, PhD (mzeydab -at- emory.edu); Robert Tweedy

## **Overview:**
While the traditional POSIX permissions used by nearly all common Linux filesystems allow for simple data permissions management based on group membership, this can become complicated to manage in a large research environment where a project's directory tree may not be efficiently structured to permit access via the simple group management achievable via POSIX permissions, especially when a research PI would like to grant different levels of access to a file to users who are otherwise in the same group. Linux ACLs, while a de-facto standard rather than a formally defined one like POSIX, can be used to resolve these types of situations but have a higher learning curve & far fewer management tools available for a large-scale storage system than tools managing POSIX permissions, relying mainly on the command line tools "setfacl" and "getfacl" to view any details. While there is a GUI tool known as "eiciel" that can adjust Linux ACLs, its audience & feature set is aimed towards an individual user on their personal machine & thus is not suitable for large-scale storage system management. This project aims to develop an application with a web-based GUI that can be deployed on a research network's storage system to provide PIs with a graphical overview of all their research data & allow management of the Linux ACLs to grant appropriate levels of access to the PI's research team members.

## **Current Status: New project**

## **Expected Outcomes:**
A self-contained application (ie. the application should not require external APIs/javascript/etc. to be queried by the end-user's web browser at runtime & should have any relevant scripts packaged with it; the underlying back-end should only access local network resources & not need external Internet connectivity) that allows an end-user to view and manage the access permissions of a large research storage network at a fine-grained level via a web GUI. Both the back-end logic & front-end web interface are in scope of this project.
> - The application should support authentication via different modules, with a minimum of LDAP-based authentication.
> - The application should support deployment behind a reverse proxy running on Apache or Nginx
> - The application must be Linux distribution agnostic as much as possible, but at a minimum should support both running on both RedHat Enterprise Linux (or free derivatives like Rocky Linux) and Debian Linux (or other derivatives like Ubuntu Server) as a SystemD service.
> - The application must support running under a limited service account & not as the root user; if special permissions are required for the service account (ie. AmbientCapabilities defined in the SystemD service script) these should be stated in the application's documentation.
> - Documentation explaining a basic overview of application usage & installation steps for use by research network system administrators.
> - The code and documentation for the application will be made publicly available on a platform such as GitHub & licensed under an Open-Source license such as GPLv3.

## **Required Skills:**
Strong web application/frontend development skills using lightweight web frameworks (ie. this should *not* be a Java application that requires Tomcat/Glassfish/etc.).
Strong backend/logic development skills in any standard language commonly available by default on Linux systems (Python, C, C++, Rust, etc.)
A good understanding of POSIX and Linux ACL file permissions.
A security-focused mindset to ensure that the application's coded to only permit users to view/modify permissions on their own files & not those of others.
Familiarity with databases (PostgreSQL and/or MySQL) may be beneficial depending on the approach used to develop the application and track user permissions for the application itself.
Familiarity with standard web servers like Apache or Nginx, especially with the concept of reverse proxies.

## **Source Code: New Project**

## **Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

## **Effort: 350 Hours**

## **Difficulty Level: Hard**


***
# **[2] Title: Open-Source Framework for Advanced EEG Data Analysis Using Pre-trained Foundation Models**

Mentor(s): Mahmoud Zeydabadinezhad (mzeydab -at- emory.edu) and Babak Mahmoudi, PhD

## **Overview:** 
* A foundation model refers to a large-scale model that is pre-trained on extensive, often unlabeled data, capturing a broad understanding of that data. Recent studies have indicated that foundation models could potentially offer enhanced robustness and versatility in the analysis of complex patterns within Electroencephalography (EEG) data. This is particularly relevant in scenarios where EEG data for specific downstream tasks is limited in quantity. This project aims to create an open-source foundation model for EEG data analysis. It will involve developing algorithms for EEG signal processing, automatic feature extraction, and implementing deep learning-based algorithms for pre-training a foundation model on publicly available EEG datasets.
## **Current Status:** In Progress.

## **Expected Outcomes:** 
* Literature Review: Research and review existing open-source foundation models for medical data, specifically EEG data. Identify the current limitations and challenges in this field.
* A robust, open-source EEG foundation model.
* Documentation and examples demonstrating the model's usage.
* A report detailing the methodologies used and the performance of the model.
* The model weights and code will be made publicly available on a platform such as GitHub.

## **Required Skills:**
* Strong programming skills, preferably in Python.
* Experience with deep learning frameworks, preferably PyTorch.
* Knowledge of self-supervised learning and large language models
* Knowledge in signal processing, neuroscience, or related fields.

## **Source Code:**  In Progress

## **Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

## **Effort:** 350 Hours

## **Difficulty Level:** Hard
***

# **[3] Python Expansion of the Open Source Electrophysiological Toolbox**
Mentor(s): Reza Sameni, PhD

## **Overview:**
* Standardized, open-source codes are indispensable in advancing biomedical engineering and biomedical informatics. The Open-Source Electrophysiological Toolbox (OSET) [https://github.com/alphanumericslab/OSET] was conceived in 2006 with this perspective, aiming to offer researchers an open-source codebase for biomedical signal processing. The toolbox has incrementally evolved and expanded over the years. Many researchers have utilized this toolbox for their research. Notably, some modules of OSET have been translated to C/C++ and Python and integrated into medical devices and cloud-based automatic diagnostic systems for large data. It operates under a permissive open license, encouraging community-driven development.
The project aims to continue the Python expansion of OSET to convert it into a standard Python package, broadening access and maintaining consistency across platforms. The planned upgrades include comprehensive cross-language unit tests (between MATLAB and Python), documentation, example codes, installation, and maintenance mechanisms, with a modern software-engineered architecture and objective microbenchmarks. Through this expansion, we aim to extend OSET's benefits to a broader community of AI researchers, also contributing to the training of the next generation of biomedical engineers in the AI era.
OSET will be maintained under the 3-Clause BSD License, a permissive open-source license that allows the redistribution and use of software in any form with adequate disclaimer clauses, offering flexibility for both open-source and commercial use, while minimizing legal complexities.

## **Current Status:** Ongoing project.
## **Expected Outcomes:**
* A Python package for OSET, with standard unit tests, installation guidelines and documentation. The codebase should operate exactly identical to the current MATLAB implementation.
## **Key features:** 
* Open-source code development for biomedical engineering and biomedical informatics.
* Identical cross-language performance
* Standardized unit tests
## **Required Skills:**
* Proficiency in Python and MATLAB.
* A background in signal processing
* Experience in biomedical signal processing
  
## **Source Code:**  https://github.com/alphanumericslab/OSET
## **Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions
##**Effort:** 350 Hours
## **Difficulty Level:** Medium
***

# **[4] Health-AI Ethics Atlas**
Mentor(s): Selen Bozkurt, PhD

## **Overview:** 
* This project aims to develop an interactive global map that visualizes the application and development of ethical principles in medical AI across different countries. It will highlight the diversity in ethical standards, regulatory approaches, and implementation practices in healthcare AI worldwide.##
## **Key features:** 
* Interactive world map displaying medical AI ethics initiatives.
* Filters for different ethical principles and AI applications.
* Country-specific data on AI healthcare policies and ethics.
* Time-lapse feature to observe changes over time.
* Case studies and detailed reports linked to map locations.
* Dynamic interface allowing users to explore technological ethical dimensions.
## **Current Status: New project.**
## **Expected Outcomes:**
* A comprehensive resource for understanding global trends in medical AI ethics.
* Enhanced awareness of ethical diversity in medical AI applications.
* Tool for researchers and policymakers to identify global best practices and gaps.
## **Required Skills:**
* Proficiency in web development (e.g., HTML, CSS, JavaScript).
* Experience with data visualization tools and libraries (e.g., D3.js, Leaflet).
* Understanding of GIS and mapping software.
* Knowledge in data analysis and handling large datasets.
* Interest or background in AI ethics, particularly in healthcare.
## **Source Code: New Project.**
## **Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions
## **Effort: 350 Hours**
## **Difficulty Level: Medium**
***
***********

