# Emory BMI Google Summer of Code (GSoC) 2023


<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Department of Biomedical Informatics, Emory University (often stylized "Emory BMI" for GSoC communications) is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from the GitHub repositories of the research labs of Emory University School of Medicine: https://github.com/Emory-HITI, https://github.com/sharmalab, https://github.com/NISYSLAB, and https://github.com/controlcore-project/


Emory BMI has been a successful mentoring orgnaization for Google Summer of Code 2012 - 2016, 2019, 2021, and 2022! In the recent years, we had 8 great contributors in 2022 and 6 in 2021. We are excited and looking forward to working with another batch of contributors for the upcoming GSoC. Emory BMI takes pride in having the past successes and GSoC contributors turning into long-term collaborators and mentors themselves.

**We have been using Slack as the primary medium of communication. Since Slack has limited the features of the Slack free versison, we are moving away from Slack and asking the contributors to communicate via the discussion forums of each project and this central repository instead.**

Please refer to the [contributor guidelines](/CONTRIBUTOR-GUIDANCE.md) for more details on how to apply and a standard template for the application. The ideas list is given below.

# List of Ideas
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.

The ideas are marked easy, medium, and hard in difficulty level. They are also tagged 175 hours, 350 hours, or 350 hours / 175 hours. These three values represent the medium-sized projects, large projects, and the projects that have the flexibility to be adopted as a medium-size project or extended as a large project.


***

**[1] An Integrated CONTROL-CORE experience.**

**Mentors:** Nan Li (nan.li -at- emory.edu), Mark Arnold (markgarnold -at- yahoo.com), and Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu)

**Overview:** [concore](https://github.com/ControlCore-Project/concore) is a lightweight framework for closed-Loop peripheral neuromodulation control systems. [concore-editor](https://github.com/ControlCore-Project/concore-editor) is a React-based front-end environment for concore. concore-editor is a fork of [DHGWorkflow](https://github.com/NISYSLAB/DHGWorkflow). DHWorkflow was developed as a visual directed hypergraph editor for workflows with loops in GSoC 2021. A GSoC 2022 project forked this repository to adapt it as a front-end for concore. concore has a server back-end developed with Python Flask, which should be invoked by concore-editor as the front-end, using an approach such as the one in [#59](https://github.com/ControlCore-Project/concore-editor/issues/59) as the first step.

concore and concore-editor are part of the CONTROL-CORE project.  This project should not be limited to [#59](https://github.com/ControlCore-Project/concore-editor/issues/59). Rather this project should provide a unified experience for control systems developers with the CONTROL-CORE project.

This GSoC aims to bring a unified experience for CONTROL-CORE users, accessing the environment through concore-editor, to create and run the studies visually.

**Current Status:** Although we currently have the concore-editor implementation which aims to be the front-end for concore, it has not been integrated with concore. Currently, the "Save" button allows saving a currently opened concore study back to its original location in the local filesystem where concore resides, when we use Chrome or Edge as the browser.

Currently, there is an option "Server" that introduces several buttons (Build, Debug, Run, Clear, Stop, and Destroy). But these buttons don't do anything when clicked.

**Expected Outcomes:**  We propose a similar integration (to that of the "Save" button in concore-editor) for all the concore methods (such as Build, Debug, Run, Clear, Stop, and Destroy). That will eliminate the need to use the commandline to invoke these methods, thus providing a browser-based integrated experience through concore-editor.

A complete integrated front-end for concore, with a seamless user experience through the visual concore-editor.


**Required Skills:** Javascript (including React) and Python. This is a front-end development project, and the contributors are expected to demonstrate their previous experience and potential to implement a front-end system with Javascript frameworks such as React.

**Code Challenge:** Pull requests to fix concore-editor bug reports are encouraged. Demonstration of local installation of concore editor through screenshots in the proposal is expected.
 
**Source Code:**  https://github.com/ControlCore-Project/concore-editor and https://github.com/ControlCore-Project/concore

**Discussion Forum**: https://github.com/ControlCore-Project/concore-editor/discussions

**Effort:** 350 Hours

**Difficulty Level:** Medium

***


**[2] Java Reference Implementation for concore Library.**

**Mentors:** Mark Arnold (markgarnold -at- yahoo.com), Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu), and Babak Mahmoudi (b.mahmoudi -at- bmi.emory.edu)

**Overview:** [concore](https://github.com/ControlCore-Project/concore) is a lightweight framework for closed-Loop peripheral neuromodulation control systems. Currently, it supports implementations of programs in Python, C++, Matlab, Octave, and Verilog. In this project, the contributor will develop a reference implementation of the concore library.

**Current Status:** We developed the concore library initially in Python, and then implemented support for other languages. The contributor will work towards a reference implementation in Java in this project. The successful completion of this project will expand the user base of concore to include Java developers.

**Expected Outcomes:** A complete reference implementation of the concore Library in Java.

**Required Skills:** Java and Python

**Code Challenge:** Demonstration of previous expertise in Java and Python can be beneficial.
 
**Source Code:**  https://github.com/ControlCore-Project/concore

**Discussion Forum**: https://github.com/ControlCore-Project/concore/discussions

**Effort:** 175 Hours

**Difficulty Level:** Medium

***

**[3] Develop a drag-and-drop frontend for WDL and CWL workflows**

**Mentors:** Babak Mahmoudi (b.mahmoudi -at- emory.edu), Özgür Kara (ozgurrkara99 -at- gmail.com), and Annie Gu (ping.gu -at- emory.edu)

**Overview:** Standard workflow languages such as Common Workflow Language (CWL) and Workflow Description Language (WDL) are traditionally written by hand and executed by workflow frameworks such as Cromwell and Toil. Drag-and-drop front-end frameworks exist, but are also limited limited by their usability across platforms. A seamless front-end to support workflow development can help the open source community tremendously. CWL and WDL limit their focus to workflows that can be represented by a directed acyclic graph (DAG). So, while a drag-and-drop interface may allow more diverse graph types such as directed graphs, when converting, the DAG format must be verified. 

**Current Status:** Our previous GSoC project DHGWorkflow enabled us to visually create Directed Hypergraphs (DHGs) and export them as GraphML files through its browser-based lightweight environment. This project could use a similar approach to generate WDL and CWL files from a browser-based application. Forking and adopting DHGWorkflow is an option. There are also stand-alone CWL and WDL drag-and-drop projects such as Rabix that can be adopted for this project. 

**Expected Outcomes:** APIs (such as RESTful interfaces) should be provided to internally pass the workflow definitions to the backend, to avoid having a backend application having to read and parse the workflow files (WDL and CWL) again, rather than having them directly use the workflow definitions by the other programs.

**Required Skills:** Languages of choice for front-end and the APIs.

**Code Challenge:** A demo to highlight the potential of developing this task, such as a prototype or a mock up.
 
**Source Code:**  New Project

**Discussion Forum**: https://github.com/NISYSLAB/Emory-BMI-GSoC/discussions

**Effort:** 350 Hours

**Difficulty Level:** Medium

***


**[4] Creating shareable "albums" from Niffler data sets**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu), Judy Gichoya (judywawira -at- emory.edu) and Ananth Reddy (ananth.reddy -at- emory.edu)

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Images can be retrieved from a PACS via Niffler in real-time (via Niffler meta-extraction module) or on-demand (via Niffler cold-extraction module). However, these downloaded data sets remain in the local environments such as a research server or a cluster where Niffler is run from. To use this data, researchers must identify certain subsets of data. This can be achieved by querying the retrieved data. For instance, Niffler stores the metadata of the data retrieved in real-time in a Mongo database. By querying the metadata, subsets of images can be identified. However, currently Niffler does not possess the ability to create such "albums" from a set of DICOM images retrieved by Niffler, and share with other users.

**Current Status:** Currently, Niffler does not have the ability to select subsets of images or create albums. We are sharing images through other orthogonal approaches (via rclone, for example).

**Expected Outcomes:** There are several approaches to implement such albums feature. One approach is to using [Kheops](https://docs.kheops.online/) to provide an interface to create and view the albums. [MEDIator](https://github.com/sharmalab/MEDIator) can be extended and incorporated to Niffler to create subsets and share the images via a unique URL as well.

The proposed feature will make the images retrieved by Niffler accessible by more researchers for their experiments, by replacing the current manual efforts of data sharing. Moreover, Kheops natively integrate with OHIF Viewer. As such, images retrived by Niffler can be viewed through OHIF Viewer, by creating albums with Kheops.

An approach to creating shareable datasets from the DICOM images retrieved by Niffler. It could be adopting existing frameworks such as MEDIator and Kheops and scripts and integration code with those frameworks or an entirely new module to Niffler for this feature. However, contributors are encouraged to use Kheops or alternatives, rather than reinventing the wheel (unless there is a convincing reason).
 
**Required Skills:** Python and Java.

**Code Challenge:** A demonstration of potential integration of Niffler with such existing frameworks. The proposed frameworks are samples only. The contributors may choose their own.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Discussion Forum**: https://github.com/Emory-HITI/Niffler/discussions

**Effort:** 175 Hours

**Difficulty Level:** Easy

***

