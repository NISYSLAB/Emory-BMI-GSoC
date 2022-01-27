# Emory BMI Google Summer of Code (GSoC) 2022

We are currently actively working on the project ideas. Please make sure to come back to check the complete list of the project ideas next week.

<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Emory BMI is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from https://github.com/Emory-HITI, https://github.com/sharmalab, and https://github.com/NISYSLAB


Emory BMI has been a successful mentoring orgnaization for Google Summer of Code 2021, 2019, 2016, and all the previous years from 2012! We had 6 great contributors in 2021. We are excited and looking forward to working with another batch of contributors for GSoC 2022.




# Communicating with the mentors

We are using Slack as the primary medium of communication. Find and join the Emory BMI slack workspace using the link - http://bit.ly/emory-bmi.

Each idea on this page has at least one mentor assigned. Each project idea also has a relevant channel in the Slack workspace, listed below under each project idea. Make sure to join the rooms that are relevant for the projects that you are interested in. Specific discussions on each project idea happens in those channels.
 
# List of Ideas
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.


***

**[1] Adopt DHGWorkflow for Concore with a seamless integration**

**Mentors:** Mark Arnold (markgarnold -at- yahoo.com), Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu), and Babak Mahmoudi (b.mahmoudi at emory.edu).

**Overview:** Concore is a framework for closed-Loop peripheral neuromodulation control systems https://github.com/ControlCore-Project/concore. DHG Workflow is a browser-based directed hypergraph editor. Concore uses DHG Workflow as a front-end workflow editor. However, DHG Workflow is a stand-alone graph editor. A seamless integration with DHG Workflow with user-defined validation will make the concore framework more user-friendly.

**Current Status:** Concore scripts can run DHG Workflow to compose a concore workflow. However, many enhancements such as custom user-defined validations, composing workflows with awareness of existing concore programs, a seamless integration with concore are proposed.

**Required Skills:** Javascript, Python (recommended)

**Code Challenge:** 

**Source Code:** https://nisyslab.github.io/DHGWorkflow/

**Slack room:** gsoc-emory-bmi.slack.com concore

**Effort:** Full-time

***

**[2] Interactive Multidimensional Visualizations for Eaglescope**

**Mentors:**  Ryan Birmingham (rainventions -at- gmail.com) and Nan Li (nan.li -at- emory.edu)

**Overview:** EagleScope (also known as Datascope2) is a framework for exploratory analysis on high dimensional datasets, especially biomedical datasets. Currently Eaglescope uses templated visualizations. 

This project would involve creating or adapting interactive visualizations that would assist with cohort creation, manual dimensionality reduction, and dataset exploration. There could be several approaches the contributor could consider. For example, we could provide users the ability to declaratively specify what visualizations they’d want to see in Eaglescope using an existing tool such as [Vega](https://vega.github.io/). All of Eaglescope's visualizations are interactive, so the challenge would be to ensure that whichever visalizations chosen are smoothly integrated with interactivity.

Adding multidimensional interactive visualizations would allow users to explore the relationship between two or more variables, and to create cohorts based upon combinations of interest.

**Current Status:** Currently, EagleScope has interactive visualizations, but only of a single variable each, and has some multidimensional visualizations, but they are noninteractive.

**Required Skills:** Javascript, D3 (recommended)

**Code Challenge:** Either from scratch or an existing toolkit, make a simple univariate interactive visualization. Alternatively, a meaningful bug report or contribution to the Eaglescope Repository.

**Source Code:** https://github.com/sharmalab/Eaglescope 

**Slack room:** gsoc-emory-bmi.slack.com eaglescope

**Effort:** Full-time/Half-time

***

**[3] A Middleware framework to integrate the backend frameworks with frontend visualization frameworks**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Rishi Kamaleswaran (rkgsoc -at- gmail.com)

**Overview:** The proliferation of infrastructures for biomedical informatics machine learning applications, including backend frameworks and visualization frameworks have posed an interesting challenge of integration. While the backend applications stand alone, they often lack of a proper frontend to visualize the data from the backend. On the other hand, frontend interfaces can be utilized to view the images and models stored by these backend frameworks better. However, such a seamless integration does not exist, and integrations are often custom-built scripts. An extensible seamless middleware that consumes the APIs of the frontend and backend could avoid this repeated manual effort of custom configurations. The middleware could enable federation of data sources that are viewable through potential frontends.

**Present Status of the work:** Integration middleware such as Enterprise Service Bus (ESB) have been quite common in the enterprise. However, in biomedical informatics research, often such integration is segmented. With proliferating number of backend and frontend architectures such an extensible framework will be novel and unique.

**Expected results:** An integration middleware that facilitates the dynamic integration of frontend interfaces with the backends, such as servers and local file systems. Contributors can start with certain file types and frameworks. For example, DICOM images. Images retrieved to a server with Niffler could be configured to view through DICOM viewers such as the OHIF Viewer. The project is intentionally left broad for the contributors to select the best potential frameworks and applications.

We envision a visual analytic pipeline that connects with real-time data from a variety of sources, along with asynchronous data to display on a visual frontend.
The tool will both display information from real-time sources, and also integrate machine learning predictions, forecasts, among other derivations. 

**Required Skills:** APIs, Middleware, Selected language of choice.

**Slack room:** gsoc-emory-bmi.slack.com middleware

**Effort:** Full-time/Half-time

***


**[4] Creating shareable "albums" from Niffler data sets**

**Mentors:** Judy Gichoya (judywawira -at- emory.edu)

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Images can be retrieved from a PACS via Niffler in real-time (via Niffler meta-extraction module) or on-demand (via Niffler cold-extraction module). However, these downloaded data sets remain in the local environments such as a research server or a cluster where Niffler is run from. To use this data, researchers must identify certain subsets of data. This can be achieved by querying the retrieved data. For instance, Niffler stores the metadata of the data retrieved in real-time in a Mongo database. By querying the metadata, subsets of images can be identified. However, currently Niffler does not possess the ability to create such "albums" from a set of DICOM images retrieved by Niffler, and share with other users.

**Present Status of the work:** Currently, Niffler does not have the ability to select subsets of images or create albums. We are sharing images through other orthogonal approaches (via rclone, for example).

**Proposed Methodology:** There are several approaches to implement such albums feature. One approach is to using [Kheops](https://docs.kheops.online/) to provide an interface to create and view the albums. [MEDIator](https://github.com/sharmalab/MEDIator) can be extended and incorporated to Niffler to create subsets and share the images via a unique URL as well.

**Benefits:** The proposed feature will make the images retrieved by Niffler accessible by more researchers for their experiments, by replacing the current manual efforts of data sharing. Moreover, Kheops natively integrate with OHIF Viewer. As such, images retrived by Niffler can be viewed through OHIF Viewer, by creating albums with Kheops.

**Deliverables:** An approach to creating shareable datasets from the DICOM images retrieved by Niffler. It could be adopting existing frameworks such as MEDIator and Kheops and scripts and integration code with those frameworks or an entirely new module to Niffler for this feature. However, contributors are encouraged to use Kheops or alternatives, rather than reinventing the wheel (unless there is a convincing reason).
 
**Required Skills:** Python and Java.

**Code Challenge:** A demonstration of potential integration of Niffler with such existing frameworks. The proposed frameworks are samples only. The contributors may choose their own.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler

**Effort:** Half-time

***




**[5] Better representations of scanner utilization from DICOM metadata**

**Mentors:** Puneet Sharma (puneet.sharma -at- emory.edu), Nan Li (nan.li -at- emory.edu), and Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu)

**Overview:**  Niffler enables computing scanner utilization using real-time DICOM metadata extraction. Niffler acquires images from the PACS in real-time (meta-extraction) and on-demand (cold-extraction), then extracts DICOM metadata into a Mongo database or a CSV file, and performs computations on the metadata to compute utilization metrics for the scanners. We did the computations for the MR scanners, although it can be used for any modality. However, our computations were largely limited to the study level - how frequently a scanner idled between studies and how long it took for a scanner to perform a given study. Computing those metrics in a finger granularity, at the series level, is more challenging since the start time and end time of a series is harder to find with just public DICOM headers.

Furthermore, while we have a scanner utiliization computed in the backend, there is no integrated front-end to present the results elegantly. The created results are currently stored in CSV files and displayed through an Eaglescope (https://github.com/sharmalab/eaglescope) dashboard. The front-end can be improved with a better integration.

**Present Status of the work:** DICOM tags are used to compute scanner utilization (https://github.com/Emory-HITI/Niffler/tree/dev/modules/suvpar and https://github.com/Emory-HITI/Niffler/tree/dev/modules/app-layer) in a prototype. But using private tags, the computations can be made more accurate at series level - although they will be specific to the vendors.

Computing scanner utilization from the DICOM images currently go as either:
a) cold-extraction (retrieve images on-demand from the PACS to the research cluster) -> png-extraction (extract all the DICOM attributes from the images in a CSV file) -> suvpar (compute scanner utilization from the csv file and produce an output csv file, currently developed in python)
or
b) meta-extraction (retrieve images in real-time from scanners to the research cluster and store the metadata in a mongo database) -> app-layer (compute scanner utilization from the mongo database, and store in an output csv file, developed in java).

**Proposed Methodology:** Private tags, used in conjunction with the public tags. Currently, png-extraction module that extracts the DICOM metadata from the DICOM files do not consider private tags. That must be extended to support certain private tags. Approach (a) above is recommended as it does not require an existing PACS, rather just a set of DICOM images.

**Benefits:** Scanner utilization will be more accurate and can be visualized better.

**Deliverables:** A more complete scanner utilization (suvpar) module. If this is proposed as a full-time (large-size) project, a front-end should be developed as well, extending the existing Eaglescope-based dashboard.

**Required Skills:** Python or Java, Javascript (optionally, for front-end), and prior experience with DICOM would be a plus.

**Code Challenge:** A bug fix from Niffler can be a possible impact.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler

**Effort:** Full-time/Half-time

***



# Application Template

The contributors are encouraged to follow this template. However, they are not expected to strictly follow this template. They are rather advised to clearly include all the requested information in their application.

**1) Project Title:**

**2) Abstract / Project Summary**:

Summarize the project in your own words.

**3) Contributor Name:**

**4) Contributor Email and Slack username:**

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

This year, the full-time projects are expected a 35 hours a week contribution (large project) and half-time projects are expected a 18 hours a week contribution (medium size project). Please indicate your choice of the project length. All project ideas have an indication how we see a project to be (full-time, half-time, or a potential/flexibility to be either based on the contributor's proposal).

Please also indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. GSoC 2022 also allows flexibility of an additional two months - to complete the project at a later time frame (a shift of up to 2 additional months). Please indicate if you expect to do that as we can plan accordingly.

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).

