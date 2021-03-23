# Emory BMI GSoC 2021

<img src="https://github.com/NISYSLAB/Emory-BMI-GSoC/blob/main/logo.jpg" width="150" height="150" align="left" /> Emory BMI is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with open-source licenses including BSD 3-Clause License and MIT license. Most of them can be accessed from https://github.com/Emory-HITI, https://github.com/sharmalab, and https://github.com/NISYSLAB


Emory BMI has been a successful mentoring orgnaization for [Google Summer of Code 2019](https://github.com/sharmalab/Emory-BMI-GSoC-2019) and before! We had 4 great students in 2019. We are excited and looking forward to working with another batch of students for GSoC 2021.




# Communicating with the mentors

We are using Slack as the primary medium of communication. Find and join the Emory BMI slack workspace using the link - http://bit.ly/emory-bmi.

Each idea on this page has at least one mentor assigned. Each project idea also has a relevant channel in the Slack workspace, listed below under each project idea. Make sure to join the rooms that are relevant for the projects that you are interested in. Specific discussions on each project idea happens in those channels.
 
# List of Ideas
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.



**[1] A test framework for Niffler DICOM frameworks for continuous integration and deployment**

**Mentors:** Ramon Correa (ramon -at- dbmi.emory.edu) and Hari Trivedi (hari.trivedi -at- emory.edu) 

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Niffler consists of multiple modules, for real-time extraction, on-demand retrieval, png extraction, and scanner utilization. In this project, we aim to develop a continuous integration test for Niffler, specifically for its on-demand retrieval (cold-extraction), real-time extraction (meta-extraction), png-extraction modules.

**Present Status of the work:** Currently, Niffler does not have posses checks to confirm commits do not break the functionality. As such, each major release requires a considerable manual testing before deploying on production. We test the modified modules for each release manually for failures before deploying a later version. We also test each modules locally before committing. However, especially for real-time and on-demand extraction such tests work only in the actual deployment environment. This has made updates more time consuming. Furthermore, currently, the code has little test coverage. As such, errors are harder to spot.

**Proposed Methodology:** Most modules of Niffler are developed in Python (cold-xtraction, meta-extraction, and png-extraction). The application layer (specifically, scanner utilization project) is developed in Java. A continuous integration framework should confirm that updates to Niffler do not break the features, slow down the extractions, or introduce new bugs. This can be a local execution as well as a GitHub integration, to handle the unit tests as well as integration tests.

**Benefits:** The proposed continuous integration tests for each update will reduce the manual effort in testing. We do not aim to remove the manual testing altogether. But we envision that such tests will significantly reduce the potential for bugs with each commits, and allowing us to deploy newer versions seamlessly.

**Deliverables:** The integration test framework for all the Niffler modules. For each commit made to the Niffler github repository, such tests should be triggered, and allowing merge into the main branch only when no failures are reported.
 
**Required Skills:** Python, Java (and the relevant framework of choice).

**Code Challenge:** A bug fix from the Niffler repository or a sample test for one of its modules.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler


***


**[2] TensorFlow-GUI: A Graphical User Interface for Tensorflow**

**Mentors:**  Monjoy Saha (monjoy.saha -at- emory.edu)

**Overview:** This project aims to develop a graphical user interface (GUI) for any deep learning model development and visualization of outcomes based on the existing TensorFlow functions. This interface will act just like a simulator similar to MATLAB. 
        
**Present Status of the work:** 
Preliminary work has been done on GUI development as part of the GSoC 2019.  Please see the GitHub link for details. There are very few organizations that are working on the development of almost similar kinds of tools. [Deep Cognition](https://deepcognition.ai/) is one of them. They charge for their services. 
        
**Proposed method:** 
Each operation, such as convolution, transpose convolution, pooling, and ReLu, will be as blocks. All the blocks should have drag-down properties. The parameters of each block will change as per the requirement. See previous code for details. 

**Benefits:** 
This GUI will be helpful for beginners and non-technical persons. 

**Deliverables:** 
The student will work on our existing GUI codes for future developments. Our goal is to develop a user-friendly software package. 

Data pipeline- The GUI should support images (.png, jpg, tiff), texts (.csv, .txt), and signals as input. 

Operations- The GUI should have all the essential operations, which are required for building a deep learning model. 

Training and testing - The GUI needs to be developed in such as way so that anyone can create a new model and tweak existing models. 

Results - The GUI should have a results visualization window.

Upload trained model---> feed an input image---> get the prediction results.

TensorBoard integration- TensorBoard is integrated into our existing GUI. You can add more features such as visualization of feature maps and statistical analysis to it.

Migration of existing GUI into a web-based GUI is also a good approach (optional). There have lots of directions to improve the existing package. New ideas are always welcome. 


**Required Skills:** Tensorflow, Python, Natsort, Pandas, NodeJS, Electron, Jquery, Jquery-ui-dist, Rimraf, Sweetalert

**Source Code:** https://github.com/sharmalab/tensorflow-gui

**Slack room:** gsoc-emory-bmi.slack.com gui-tf

***

**[3] Interactive Multidimensional Visualizations for Eaglescope**

**Mentors:**  Ryan Birmingham (rainventions -at- gmail.com) and Ramon Correa  (ramon -at- dbmi.emory.edu) 

**Overview:** EagleScope (also known as Datascope2) is a framework for exploratory analysis on high dimensional datasets, especially biomedical datasets. Currently Eaglescope uses templated visualizations. 

This project would involve creating or adapting interactive visualizations that would assist with cohort creation, manual dimensionality reduction, and dataset exploration. There could be several approaches the student could consider. For example, we could provide users the ability to declaratively specify what visualizations they’d want to see in Eaglescope using an existing tool such as [Vega](https://vega.github.io/). All of Eaglescope's visualizations are interactive, so the challenge would be to ensure that whichever visalizations chosen are smoothly integrated with interactivity.

Adding multidimensional interactive visualizations would allow users to explore the relationship between two or more variables, and to create cohorts based upon combinations of interest.

**Current Status:** Currently, EagleScope has interactive visualizations, but only of a single variable each, and has some multidimensional visualizations, but they are noninteractive.

**Required Skills:** Javascript, D3 (recommended)

**Code Challenge:** Either from scratch or an existing toolkit, make a simple univariate interactive visualization. Alternatively, a meaningful bug report or contribution to the Eaglescope Repository.

**Source Code:** https://github.com/sharmalab/Eaglescope 

**Slack room:** gsoc-emory-bmi.slack.com eaglescope

***




**[4] A frontend for LoopSim framework to model workflows with closed loops**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Babak Mahmoudi (b.mahmoudi -at- emory.edu)

**Overview:** LoopSim framework aims to facilitate workflows with loops, including simple and nested loops. Such workflows deviate from the standard workflows that consist of specific start and end services. As such, existing CWL and WDL workflow composers, including those with a compact front-end such as Rabix, cannot be used as such for loops. The current workflow frameworks limit their focus to supporting directed acyclic graphs (DAGs). Furthermore, workflow definitions can be made more efficient by representing them with more generic formats such as directed hypergraphs. A directed hypergraph supports workflows containing edges that connect multiple nodes. To support complex loops efficiently, we must expand our scope to include all the directed hypergraphs. Currently, LoopSim uses yEd GraphML editor as its front end. However, yEd is not open source and not ideal for customizing as our integrated front-end. As such, a custom front-end for LoopSim will be more advantageous.

**Present Status of the work:** Currently, LoopSim utilizes yEd to visualize its workflows. The workflows drawn using yEd are stored as GraphML files. The GraphML files are then parsed with LoopSim based on BeautifulSoup to represent them as hypergraphs in Python. The proposal is to custom-build a front-end framework to replace yEd. Students are encouraged to find open-source projects that can be extended and leveraged for the front-end.

**Proposed Methodology:** LoopSim is currently under active development. We aim to have the front-end that evolves with the framework. The students are encouraged to find open-source frameworks that support drag-and-drop of the components to create workflows with loops - as depicted in LoopSim with yEd as samples. 

**Benefits:** LoopSim currently uses yEd to design its directed hypergraphs. However, yEd is not open source. As such, adopting yEd for LoopSim poses a few challenges. First, we cannot adopt the front-end to customize based on LoopSim’s requirement. Second, as it is not open-source, a complete bundling of the framework is not possible. An open-source solution also removes the potential for vendor lockin, especially if yEd is discontinued in the future. Since LoopSim is also an on-going research project, the successful student also can contribute to the research as a co-author.

**Deliverables:** A minimal drag-and-drop front-end interface to compose workflows that can be represented by a diverse set of graphs, rather than being limited to DAGs. The minimal drag-and-drop front-end must be integrated into the existing graph parser to replace the current yEd-based graph composer. While several open-source frameworks such as Apache Airavata provide such a drag-and-drop interface, they do not offer the capability to compose workflows with loops with containerized microservices. As such, a front-end to LoopSim will make it towards a complete workflow framework. 

**Required Skills:** Python or the relevant frameworks/languages of choice.

**Source Code:** https://github.com/NISYSLAB/LoopSim

**Slack room:** gsoc-emory-bmi.slack.com loopsim



***

**[5] Enhancements to Bindaas Data Integration Middleware**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Tushar Aggarwal (tushar1997 -at- gmail.com)

**Overview:** Bindaas is a service-based data framework that offers unified access and RESTful APIs to various data sources, such as MySQL, PostgreSQL, Mongo, and Apache Drill. Additional data service providers can be implemented for various data sources and access mechanisms such as HTTP access. Bindaas is the backbone of several production systems such as the Cancer Imaging Archive (TCIA). Performance is an essential aspect of the Bindaas framework. Therefore, there have been several proposals for improving Bindaas’ performance. This project aims to improve the performance and usability of Bindaas by addressing some of those proposals. Students can choose a few from the below list of ideas or propose their own.

There have been several proposals to improve Bindaas’ usability. There are several tasks to follow up.

* More data source providers. Namely, we should extend Bindaas for cloud file systems and storages such as S3, by incorporating with the cloud CLIs.

* Currently Bindaas limits its API to REST. We also propose to have more interfaces to Bindaas such as GraphQL query language interfaces, in addition to its RESTful interfaces.

* Better serialization of Bindaas internal representation with Protobuf, Kryo, or other efficient serialization and deserialization approaches.

* SQLite-based audit logs have some performance and scalability limitation. The tight-coupling with SQLite should be removed, and replaced with a generic interface. Then, also implement persistence based on other data stores as alternatives. Consider Mongo and In-Memory Data Grids such as Infinispan and Hazelcast.

* Bindaas currently does not optimize its database queries. We should be able to reach better outputs than the database APIs themselves through query optimization.

**Expected results:** We are aiming for the Bindaas 4.5 release with a few of the enhancements and features in place.

**Code challenge:** The students are expected to configure Bindaas locally during the application period to understand the code base and to illustrate their capability in completing this task. If the student manages to resolve one of the issues listed in https://github.com/sharmalab/bindaas/issues, it will make them a strong candidate.
   
**Required Skills:** Java, Web Services, Apache Maven, OSGi, GraphQL, Cloud Computing

**Source Code:**  https://github.com/sharmalab/bindaas

**Slack room:** gsoc-emory-bmi.slack.com bindaas

***



**[6] An OpenSlide Reader for TensorFlow: Enabling Machine-Learning for Digital Pathology**

**Mentors:** Monjoy Saha (monjoy.saha -at- emory.edu) 

**Overview:** This project seeks to develop a custom TensorFlow reader for digital pathology whole slide images (WSIs). These images are massive, often 80K x 120K or larger, and are stored in proprietary formats that can be read by the OpenSlide Library but can not be directly read by Tensorflow. This project will develop a C reader based on OpenSlide to enable these images to be read efficiently within TensorFlow.

**Present Status of the work:** As per our knowledge, there is no such tool in the existing OpenSlide software for converting the images/datasets into the Tensorflow supported "TfRecord" file format (extension of files  .tfrecord). On the other hand, Tensorflow doesn't encourage the user to use some other file formats rather than TfRecords. TfRecords are the best way to handle a complex training dataset structure in a single record file. 

**Expected results:** A documented, tested implementation with build instructions for popular platforms.

**Required Skills:** C, software profiling, and optimization.

**Source Code:** New Project

**Community and Code License:** Apache License 2.0

**Slack room:** gsoc-emory-bmi.slack.com  openslider-tf


***

**[7] A Middleware framework to integrate the backend frameworks with frontend visualization frameworks**

**Mentors:** Monjoy Saha (monjoy.saha -at- emory.edu) and Rishi Kamaleswaran (rkgsoc -at- gmail.com)

**Overview:** The proliferation of infrastructures for biomedical informatics machine learning applications, including backend frameworks and visualization frameworks have posed an interesting challenge of integration. While the backend applications stand alone, they often lack of a proper frontend to visualize the data from the backend. On the other hand, frontend interfaces can be utilized to view the images and models stored by these backend frameworks better. However, such a seamless integration does not exist, and integrations are often custom-built scripts. An extensible seamless middleware that consumes the APIs of the frontend and backend could avoid this repeated manual effort of custom configurations. The middleware could enable federation of data sources that are viewable through potential frontends.

**Present Status of the work:** Integration middleware such as Enterprise Service Bus (ESB) have been quite common in the enterprise. However, in biomedical informatics research, often such integration is segmented. With proliferating number of backend and frontend architectures such an extensible framework will be novel and unique.

**Expected results:** An integration middleware that facilitates the dynamic integration of frontend interfaces with the backends, such as servers and local file systems. Students can start with certain file types and frameworks. For example, DICOM images. Images retrieved to a server with Niffler could be configured to view through DICOM viewers such as the OHIF Viewer. The project is intentionally left broad for the students to select the best potential frameworks and applications.

We envision a visual analytic pipeline that connects with real-time data from a variety of sources, along with asynchronous data to display on a visual frontend.
The tool will both display information from real-time sources, and also integrate machine learning predictions, forecasts, among other derivations. 

**Required Skills:** APIs, Middleware, Selected language of choice.

**Community and Code License:** Apache License 2.0

**Slack room:** gsoc-emory-bmi.slack.com middleware
***

**[8] CovCT: Development of an AI-based Android Application for distinguishing COVID-19 and Pneumonia using Computed Tomography Images**

**Mentors:** Monjoy Saha (monjoy.saha -at- emory.edu) 

**Overview:** Coronavirus disease 2019 (COVID-19) is a highly contagious respiratory disease caused by SARS-CoV-2. Uncounted people around the world got affected due to this virus. Various articles have reported that COVID-19 and Pneumonia cases have very few distinct features. We aim to develop an AI-based Android Application, which will distinguish COVID-19 and Pneumonia cases using computed tomography (CT) images.

**Present Status of the work:** A classification architecture using TensorFlow has been developed using Python. It works on Linux, Mac, and Windows systems.  

**Deliverables:** The student will work on the development of an AI-based android application. The students may explore the idea of federated learning techniques on Android phones. 

**Required Skills:** The student should have prior experience to develop an Android application and machine learning algorithms. The students have full freedom to choose any architecture/codes as per their comfort level. 

**Source Code:** https://github.com/monjoybme/CovCT

**Community and Code License:** Apache License 2.0

**Slack room:** gsoc-emory-bmi.slack.com covid19

***

**[9] Creating shareable "albums" from Niffler data sets**

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


**[10] A frontend for Niffler DICOM framework for machine learning pipelines and processing workflows**

**Mentors:** Pradeeban Kathiravelu (pradeeban.kathiravelu -at- emory.edu) and Imon Banerjee (imon.banerjee -at- emory.edu) 

**Overview:**  Niffler is a framework to retrieve DICOM images from PACS real-time as a DICOM stream as well as retrospectively. Niffler consists of multiple modules, for real-time extraction, on-demand retrieval, png extraction, and scanner utilization. However, Niffler is developed as a command-line based tool. In this project, we aim to develop a front-end for Niffler, specifically for its on-demand retrieval (cold-extraction), real-time extraction (meta-extraction), png-extraction modules.

**Present Status of the work:** Currently, Niffler does not have a front-end. The users are expected to log in to the server and run the Python scripts directly, after providing the configuration as json files. This limits the wide use of Niffler as a framework, as only those who have access to the server or VM instance can run their extractions or workflows on Niffler. A proper front-end can help with this shortcoming. However, security and access control measures must be taken as the framework will handle data with PHI.

**Proposed Methodology:** There are several approaches to implement a front-end to Niffler. The student must present their approach and defend it. Especially consider how the proposed approach will ensure only the authorized users can use Niffler. Currently, only those who can access the VM can access and use Niffler. When providing a front-end such access control must be implemented so that the front-end can be used in production.

**Benefits:** The proposed front-end will make Niffler accessible and usable by more users. We are now limited to running the Python code after configuring the json files. A front end can make it more user-friendly. Furthermore, this enables how the framework can be used beyond the organizational boundaries, with proper firewalls and security mechanisms in place.

**Deliverables:** A front-end environment for Niffler. This could be an integrated web application or a modular architecture. However, the existing stand-alone execution based on command-line should continue to run as now. Several aspects must be decided. For example, how the CSV files are passed for the on-demand extraction, and how the end-user will know the location of the files for the png-extraction. Students are encouraged to make relevant assumptions and state in their proposal.

Several factors such as how the CSV file to extract the images on-demand should be passed and how the outputs are shared with the users should be considered. Students are encouraged to use the existing standards, frameworks, and toolkits towards implementing the functionality, rather than developing everything from the scratch. For example, RESTful interfaces maybe developed to pass the data to and from the Niffler backend. 
 
**Required Skills:** Python (and the relevant framework of choice).

**Code Challenge:** A mock GUI to present a potential front-end to Niffler or a bug fix from the Niffler repository.

**Source Code:** https://github.com/Emory-HITI/Niffler/

**Slack room:** gsoc-emory-bmi.slack.com niffler


***

**[11] Graphical User Interface for OpenAI Gym**

**Mentors:** Parisa Sarikhani (psarikh -at- emory.edu) and Babak Mahmoudi (b.mahmoudi -at- emory.edu)

**Overview:** The goal of this project is to develop a graphical user interface (GUI) for simulating openai gym environments and RL algorithms. Openai gym is a toolkit that has a common interface for developing and comparing the performance of different RL algorithms. 

The goal is to develop a system-design platform that users can graphically select different gym environments and RL algorithms to train an agent. This development will result in a visual interface in forms of graphical block diagrams. These graphical block diagrams could represent the functions of the whole gym environment or the environment’s components, and the RL algorithms, which will be connected with links or wires in order tol define the execution flow of the system. The GUI will also enable visualizing some performance metrics, like the reward function during training and testing.

**Proposed Methodology:** This GUI will be inherited from the current structure of openai gym environment and RL algorithms that are compatible with openai gym, e.g. stable baseline, or spinning up. Each component will be converted into graphical block diagrams that users can select from to train a gym agent with their algorithm of choice.

**Benefits:** This technique will be helpful for the beginners who don't have sufficient programming knowledge, but are willing to test the functionalities of the RL algorithms in a similar setup to openai gym.

**Deliverables:** A minimal implementation of the user interface with minimal set of environments from openai gym and RL algorithms from stable baseline or spinning up libraries with the detailed documentation.

**Required Skills:** Python, PyQt5, and relevant frameworks of choice

**Source Code:** New Project

**Slack room:** gsoc-emory-bmi.slack.com openai

***


**[12] Reconstruct data visualized in a plot**

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

