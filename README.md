# Emory BMI GSoC 2021
Emory BMI GSoC 2021 Project Ideas 

<img src="https://pbs.twimg.com/profile_images/535105446957182978/4PApPZ-s_400x400.png" width="150" height="150" align="left" /> Emory BMI is committed to open source development of several biomedical informatics research projects. As a research organization, its source code lives across several open source project repositories, released with BSD 3-Clause License. Most of them can be accessed from https://github.com/Emory-HITI, https://github.com/sharmalab, and https://github.com/NISYSLAB


Emory BMI has been a successful mentoring orgnaization for [Google Summer of Code 2019](https://github.com/sharmalab/Emory-BMI-GSoC-2019)! We had 4 great students. We are excited and looking forward to working with another batch of students for GSoC 2021.




# Communicating with the mentors

We are using Slack as the primary medium of communication. Find and join the Emory BMI slack workspace using the link - http://bit.ly/emory-bmi.

Each idea on this page has at least one mentor assigned. Each project idea also has a relevant channel in the Slack workspace, listed below under each project idea. Make sure to join the rooms that are relevant for the projects that you are interested in. Specific discussions on each project idea happens in those channels.
 
# List of Ideas
Discuss the project on Slack, and once you are ready to submit your application, use the template below. You must submit your application directly using the GSoC Program Site. If you have a project idea that is relevant for Emory Biomedical Informatics, but is not listed here, feel free to consult the mentors to discuss your own idea. The ideas listed below can be open for interpretation. Feel free to discuss with the mentors for clarifications, questions, or alternative suggestions.


**[1] TensorFlow-GUI: A Graphical User Interface for Tensorflow**

**Mentors:**  Monjoy Saha (monjoy.saha -at- emory.edu)

**Overview:** This project aims to develop a graphical user interface (GUI) for any deep learning model development and visualization of outcomes based on the existing Tensorflow functions. This interface will act just like a simulator similar to MATLAB. This technique will be helpful for the beginners who don't have sufficient programming knowledge. Moreover, our proposed concept will help to maintain the quality of the work.
              
**Present Status of the work:** Preliminary work has been done and a TensorFlow-GUI has been implemented as part of GSoC 2019 project with Emory BMI organization. The GSoC 2020 student is expected to extend or utilize the work from the previous year.

There are very few organizations that are also working on the development of almost similar kind of tools. [Deep Cognition](https://deepcognition.ai/) is one of them. Though they have many limitations including the quality of the code/output and the number of users. This is not an open source software.
              
**Proposed Methodology:** We will use existing Tensorflow functions which will be converted into the blocks of layers (e.g., convolution, transpose convolution, pooling, ReLu, etc.). The parameters of each layer can be set as per the requirements of the model. Suppose in the case of convolution layer; the user can set the values of input, weight, bias, kernel dimensions, number of output channels, etc.
 
**Benefits:** The proposed GUI will be very much helpful for the beginners or who don't have sufficient knowledge of coding. This GUI will help in maintaining the quality of the work for Emory BMI researchers as well as the broader research community. The students also have the potential to submitting a pull request upstream to the Tensorflow community, if relevant.
 

**Deliverables:** 

It is expected that GSOC students will use our existing GUI code for further developments. In the last year, we have developed the main skeleton of the GUI, which can be used to create a simple CNN model using convolution, pooling, etc., operations.  

This year we are expecting something more. Hence, it is necessary to make our GUI more robust and user-friendly.  It will be a good idea if you can migrate our existing GUI into a web-based GUI. Rather than this, we feel there have lots of options to improve the existing GUI. The first part which you can look into is the input data pipeline part. We are mainly working on medical data. The data may be images (file format .svs/.dcm/.jpg/.tif/png, etc.), texts, or signals.  Hence, it is recommended to develop an input data pipeline that supports biomedical data. You can follow the flow diagram below to improve this section. 

Locate the path of datasets--> Extract the patches of required sizes ---> convert the patches into TensorFlow supported  (like tfrecords/h5/bin, etc.) single/multiple file formats for easy and fast processing of data-->feed into the model.  

In the second part, it is necessary to include all the TensorFlow operations/Ops in the node editor section to make this GUI perfect. You must have to confirm that all the Ops are working correctly. 

In the third part, you need to improve the code editor part.  Whenever you select an operation from the drag-down menu, automatically corresponding code will be generated in this section. So, when you work on the node editor part, you must have to look into the code editor part as well.

In the fourth part, you have to create a separate window where we can use already trained models for further analysis. This section will be primarily used for the interpretability purpose.  Suppose you have a trained model. Follow the flow diagram below. 

Upload trained model---> feed an input image---> get the prediction results.

The fifth part is the Tensorboard integration part. Tensorboard is already integrated into our existing GUI. In our future development, it is required to implement the visualization of feature maps and more statistical analysis options. 


**Required Skills:** Tensorflow, Python, Natsort, Pandas, NodeJS, Electron, Jquery, Jquery-ui-dist, Rimraf, Sweetalert

**Source Code:** https://github.com/sharmalab/tensorflow-gui

**Slack room:** gsoc-emory-bmi.slack.com gui-tf

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

Break the timeline into periods of 3 – 4 days

**8.1) Community Bonding Period**

**8.2) Development Phase**

**8.3) Project Completion, testing, and documentation**

**9) Planned GSoC work hours**

GSoC is expected to be a full time job, with 35 hours or more a week of contribution. Please indicate the work hours (including the timezone), that you hope to work on your project. 

**10) Planned absence/vacation days and other commitments during the GSoC period (including the community bonding period)**

Please indicate if you have any lectures/classes, examinations, or other personal commitments. 

**11) Skill Set**

Your relevant skill set to complete this project. Include pointers to bug fixes, demos, and previous work.

Also include pointers to the completed Code Challenge (if applicable).

