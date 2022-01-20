# Emory BMI GSoC 2022

We are currently actively working on the project ideas. Please make sure to come back to check the complete list of the project ideas.

<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Emory BMI is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from https://github.com/Emory-HITI, https://github.com/sharmalab, and https://github.com/NISYSLAB


Emory BMI has been a successful mentoring orgnaization for [Google Summer of Code 2019](https://github.com/sharmalab/Emory-BMI-GSoC-2019) and before! We had 4 great students in 2019. We are excited and looking forward to working with another batch of students for GSoC 2021.




# Communicating with the mentors

We are using Slack as the primary medium of communication. Find and join the Emory BMI slack workspace using the link - http://bit.ly/emory-bmi.

Each idea on this page has at least one mentor assigned. Each project idea also has a relevant channel in the Slack workspace, listed below under each project idea. Make sure to join the rooms that are relevant for the projects that you are interested in. Specific discussions on each project idea happens in those channels.
 
# List of Ideas
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.



**[1] Interactive Multidimensional Visualizations for Eaglescope**

**Mentors:**  Ryan Birmingham (rainventions -at- gmail.com)

**Overview:** EagleScope (also known as Datascope2) is a framework for exploratory analysis on high dimensional datasets, especially biomedical datasets. Currently Eaglescope uses templated visualizations. 

This project would involve creating or adapting interactive visualizations that would assist with cohort creation, manual dimensionality reduction, and dataset exploration. There could be several approaches the student could consider. For example, we could provide users the ability to declaratively specify what visualizations they’d want to see in Eaglescope using an existing tool such as [Vega](https://vega.github.io/). All of Eaglescope's visualizations are interactive, so the challenge would be to ensure that whichever visalizations chosen are smoothly integrated with interactivity.

Adding multidimensional interactive visualizations would allow users to explore the relationship between two or more variables, and to create cohorts based upon combinations of interest.

**Current Status:** Currently, EagleScope has interactive visualizations, but only of a single variable each, and has some multidimensional visualizations, but they are noninteractive.

**Required Skills:** Javascript, D3 (recommended)

**Code Challenge:** Either from scratch or an existing toolkit, make a simple univariate interactive visualization. Alternatively, a meaningful bug report or contribution to the Eaglescope Repository.

**Source Code:** https://github.com/sharmalab/Eaglescope 

**Slack room:** gsoc-emory-bmi.slack.com eaglescope

***

**[2] A Middleware framework to integrate the backend frameworks with frontend visualization frameworks**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Rishi Kamaleswaran (rkgsoc -at- gmail.com)

**Overview:** The proliferation of infrastructures for biomedical informatics machine learning applications, including backend frameworks and visualization frameworks have posed an interesting challenge of integration. While the backend applications stand alone, they often lack of a proper frontend to visualize the data from the backend. On the other hand, frontend interfaces can be utilized to view the images and models stored by these backend frameworks better. However, such a seamless integration does not exist, and integrations are often custom-built scripts. An extensible seamless middleware that consumes the APIs of the frontend and backend could avoid this repeated manual effort of custom configurations. The middleware could enable federation of data sources that are viewable through potential frontends.

**Present Status of the work:** Integration middleware such as Enterprise Service Bus (ESB) have been quite common in the enterprise. However, in biomedical informatics research, often such integration is segmented. With proliferating number of backend and frontend architectures such an extensible framework will be novel and unique.

**Expected results:** An integration middleware that facilitates the dynamic integration of frontend interfaces with the backends, such as servers and local file systems. Students can start with certain file types and frameworks. For example, DICOM images. Images retrieved to a server with Niffler could be configured to view through DICOM viewers such as the OHIF Viewer. The project is intentionally left broad for the students to select the best potential frameworks and applications.

We envision a visual analytic pipeline that connects with real-time data from a variety of sources, along with asynchronous data to display on a visual frontend.
The tool will both display information from real-time sources, and also integrate machine learning predictions, forecasts, among other derivations. 

**Required Skills:** APIs, Middleware, Selected language of choice.

**Community and Code License:** Apache License 2.0

**Slack room:** gsoc-emory-bmi.slack.com middleware
***


**[3] Creating shareable "albums" from Niffler data sets**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Judy Gichoya (judywawira -at- emory.edu) 

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Images can be retrieved from a PACS via Niffler in real-time (via Niffler meta-extraction module) or on-demand (via Niffler cold-extraction module). However, these downloaded data sets remain in the local environments such as a research server or a cluster where Niffler is run from. To use this data, researchers must identify certain subsets of data. This can be achieved by querying the retrieved data. For instance, Niffler stores the metadata of the data retrieved in real-time in a Mongo database. By querying the metadata, subsets of images can be identified. However, currently Niffler does not possess the ability to create such "albums" from a set of DICOM images retrieved by Niffler, and share with other users.

**Present Status of the work:** Currently, Niffler does not have the ability to select subsets of images or create albums. We are sharing images through other orthogonal approaches (via rclone, for example).

**Proposed Methodology:** There are several approaches to implement such albums feature. One approach is to using [Kheops](https://docs.kheops.online/) to provide an interface to create and view the albums. [MEDIator](https://github.com/sharmalab/MEDIator) can be extended and incorporated to Niffler to create subsets and share the images via a unique URL as well.

**Benefits:** The proposed feature will make the images retrieved by Niffler accessible by more researchers for their experiments, by replacing the current manual efforts of data sharing. Moreover, Kheops natively integrate with OHIF Viewer. As such, images retrived by Niffler can be viewed through OHIF Viewer, by creating albums with Kheops.

**Deliverables:** An approach to creating shareable datasets from the DICOM images retrieved by Niffler. It could be adopting existing frameworks such as MEDIator and Kheops and scripts and integration code with those frameworks or an entirely new module to Niffler for this feature. However, students are encouraged to use Kheops or alternatives, rather than reinventing the wheel (unless there is a convincing reason).
 
**Required Skills:** Python and Java.

**Code Challenge:** A demonstration of potential integration of Niffler with such existing frameworks. The proposed frameworks are samples only. The students may choose their own.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler


***




**[4] Reconstruct data visualized in a plot**

**Mentors:** Matt Reyna (matthew.a.reyna -at- emory.edu)

**Overview:** 
There are a variety of software packages for visualizing data with plots, but recovering or reconstructing data that is visualized in a plot is a more difficult task — this is an example of an inverse problem. In some cases, the data shown in a plot may be unavailable, and recovering the data from the plot may be important for further analysis. There are existing tools for recovering data from general purpose plots (e.g., [WebPlotDigitizer](https://github.com/ankitrohatgi/WebPlotDigitizer) for an open-source package). This project proposes the creation of an open-source software package in Python or Julia for recovering data from plots that are common in clinical applications, helping clinicians and data scientists with their work. 

**Expected results:** A tool that recovers data from plots.

**Code Challenge:** Any similar work that demonstrates expertise in Python or Julia (the language that you choose to develop this project)

**Required Skills:** Python or Julia

**Source Code:** New project. 

**Slack room:** gsoc-emory-bmi.slack.com reconstruct-data

***



# Application Template

The students are encouraged to follow this template. However, they are not expected to strictly follow this template. They are rather advised to clearly include all the requested information in their application.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Student Name:**

**4) Student Email and Slack username:**

**5) Potential Mentor(s):**

**6) Personal Background (Brief CV)**

**7) Project Goals / Major Contributions**

(Enter as bullets)

..
     
..
     
..

**8) Project Schedule**

Break the timeline into periods of up to 7 days

**8.1) Community Bonding Period**

**8.2) Development Phase**

**8.3) Project Completion, testing, and documentation**

**9) Planned GSoC work hours**

This year, students are expected a 18 hours a week of contribution (as opposed to 2020 and previous editions which expected a full-time commitment of 35 hours). Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).

