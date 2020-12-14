# Introduction

The environmental and social changes brought about by the Corona pandemic have precipitated a mindset shift towards the virtual methods of learning. As a result Virtual Labs has witnessed a significant increase in the expression of interests for the development of new experiments. In the light of this increased interest, it becomes pertinent to publish the process for building and contributing new experiments to the Virtual Labs ecosystem. This document serves as a guideline for creating a new experiment from conception to deployment.

##  Audience 
The target audience for this document is the development team at CPE, IIITH and all the lab authors and owners who want to develop Virtual experiments (lab) and/or make it available on the Virtual Labs e-learning platform.


## Experiment Lifecycle

Virtual Lab follows a well defined experiment development process. An experiment goes through the complete lifecycle from conceptualization to archival. The lifecycle of an experiment consists of the following events:
1. Expression of Interest & Proposal Submission
2. Proposal Review
3. Experiment Repositories Creation
4. Experiment Pedagogy Submission
5. Experiment Pedagogy Review
6. Experiment Storyboard Submission
7. Experiment Storyboard Review
8. Experiment Development
9. Experiment Review
10. Experiment Hosting Preparation
11. Lab/Experiment Hosting and Publishing
12. Lab/Experiment Evaluation and Analytics
13. Experiment Update/Upgrade
14. Experiment Archival

## 1. Expression of Interest & Proposal Submission 

Experiments are developed in a group. The experiment developers create a collection of related experiments, which is called a lab. The experiment development process starts with an Expression of interest for the lab. To express the interest for developing a new lab, the developer fills the expression of interest form available [here](https://docs.google.com/forms/d/e/1FAIpQLSctFus-noUJL815JG1i7RhO_cWKiryfsQ2pOhz2xVBeG0GVTQ/viewform).  A completely filled lab proposal document also needs to be attached to the form. The [template](https://docs.google.com/document/d/1F1VEK0e3-rCRedkc3EkSzKxw-Mf-qoLgieyYPWhtqTo/edit?usp=sharing) of the Lab Proposal document, along with a [sample](https://docs.google.com/document/d/1F1VEK0e3-rCRedkc3EkSzKxw-Mf-qoLgieyYPWhtqTo/edit?usp=sharing) proposal, is available in the form. 

## 2. Proposal Review
On receipt of the Expression of Interest form, the Virtual Labs team reviews the proposal and either sends out an acceptance mail or suggests improvements to the proposal. 

## 3. Experiment Repositories Creation 

Once the proposal is accepted by the Virtual Labs team, the developer raises an [issue](https://github.com/virtual-labs/engineers-forum/issues/new?assignees=&labels=On-Boarding%2C+Phase-3&template=phase-iii-onboarding.md&title=Phase+III+Lab%2FExperiment%28s%29+OnBoarding+Request+for+%3Cfill+your+lab+name+here%3E) of type Phase III Experiment Repository Creation Request on engineers-forum repository under the  virtual-labs organization on Github. The developer attaches the pdf of the approved proposal to the request issue.

The Virtual Labs team creates a git repository for each experiment of the proposed lab. This repository is the single source of truth for the experiment. It contains all the resources and all communication related to the experiment.
The git repository created by the Virtual Labs team contains templates along with examples for all the documents to be submitted as part of the experiment development process.

The url of the experiment repository is shared with the developer by the Virtual Labs team on the Experiment Repository Creation Request issue.

### Experiment Repository Structure

The experiment repository created by the Virtual Labs team contains 3 default branches. Each branch serves a specific purpose and has certain conventions, which must be followed by the experiment developers. The developers are free to create any extra branches as they deem necessary. The 3 default branches in an experiment repository are:

1. **dev:** This is the branch where the experiment development process starts. The developers can either directly add code to the dev branch or can merge their custom or issue specific branches to the dev branch. This branch is also used for unit testing the experiment.
2. **testing:** Once the code passes unit testing in the dev branch, it is promoted to the testing branch by raising and approving a merge request from the dev branch to the testing branch. The code in the testing branch is used for the end-to-end testing of the code. Each experiment repository has a static site hosting url where the code in the testing branch is deployed. The deployment of the code is effected through an automated CI/CD pipeline provided in the experiment repository. Each merge to the testing branch automatically deploys the experiment to the testing url. The developer receives an email about the success/failure of the deployment on the email id associated with the github handle provided in the lab proposal.
3. **gh-pages:** This branch is automatically created when the automated CI/CD pipeline is triggered during the merge to testing branch. This branch should not be deleted. 
4. **main:** The branch named as main is the identifying branch of the experiment repository. The code and the documents in the main branch are the production artefacts. The only way code and documents can be added to the main branch is by merging the testing branch to it. It is mandatory that the code in the main branch is always in the deployable condition. All the reviews and hosting will be performed strictly on the documents and code present in the main branch.

The initial structure and hierarchy of each default branch of the experiment repository is shown below. Every directory has a README.md file, which details the purpose and organization of the directory. The developer adds the development artefacts into the repository while maintaining this structure:

<pre>
├── experiment
│   ├── images
│   │   └── README.md
│   ├── simulation
│   │   ├── css
│   │   │   ├── main.css
│   │   │   └── README.md
│   │   ├── images
│   │   │   └── README.md
│   │   ├── js
│   │   │   ├── main.js
│   │   │   └── README.md
│   │   └── index.html
│   ├── aim.md                                                                                                                                                     
│   ├── experiment-name.md
│   ├── posttest.js
│   ├── pretest.js
│   ├── procedure.md
│   ├── README.md
│   ├── references.md
│   └── theory.md
├── pedagogy
│   ├── images
│   │   └── README.md
│   └── README.md
├── storyboard
│   ├── flowchart
│   │   └── README.md
│   ├── mindmap
│   │   └── README.md
│   ├── storyboard
│   │   └── README.md
│   └── README.md
├── LICENSE
└── README.md
</pre>

## 4. Experiment Pedagogy Submission

After the creation of the experiment repositories, the experiment developer updates the README.md of the repository with details of the experiment, developing institute and development team. The experiment developer then fills the experiment pedagogy document by updating the experiment pedagogy [template](https://github.com/virtual-labs/ph3-exp-template/tree/main/pedagogy) in the experiment repository. The [template](https://github.com/virtual-labs/ph3-exp-template/tree/main/pedagogy) also contains links to [reference](https://github.com/virtual-labs/ph3-exp-dev-process/tree/main/pedagogy) and [sample](https://github.com/virtual-labs/ph3-exp-dev-process/tree/main/sample/pedagogy) documents. Following set of information needs to be provided in the pedagogy document:


1. Experiment Details </br>
  a. Experiment Name </br>
  b. Experiment Discipline</br>
  c. Lab Name
2. Focus Area
3. Learning Objective
4. Instruction Strategy
5. Assessment Methodology
6. Learning Interactions

Once the completed pedagogy document is merged to the main branch, the developer raises an [issue](https://github.com/virtual-labs/ph3-exp-template/issues/new?assignees=&labels=pedagogy&template=pedagogy-review-request.md&title=) of type Pedagogy Review Request on the experiment repository and fills up the link to the pedagogy document in the issue. 

## 5. Experiment Pedagogy Review

The Virtual Labs Reviewing Committee reviews the pedagogy document and, if needed, suggests certain alterations or requests extra information.
All communications regarding the suggestions, requests or clarifications are part of the raised issue in the form of comments.
Once the committee is satisfied with the proposal, they label the request issue as <b>Approved</b>.

## 6. Experiment Storyboard Submission
 
After the approval of the experiment pedagogy, the developer submits the experiment storyboard by updating the experiment storyboard [template](https://github.com/virtual-labs/ph3-exp-template/tree/main/storyboard) in the experiment repository. The [template](https://github.com/virtual-labs/ph3-exp-template/tree/main/storyboard) also contains links to [reference](https://github.com/virtual-labs/ph3-exp-dev-process/tree/main/storyboard) and [sample](https://github.com/virtual-labs/ph3-exp-dev-process/blob/main/sample/storyboard/README.md) documents. 
Following set of information needs to be provided in the storyboard:
1. Simulation Story
2. Simulation flowchart
3. Mindmap
4. Storyboard

Once the completed storyboard document is merged to the main branch, the developer [raises](https://github.com/virtual-labs/ph3-exp-template/issues/new?assignees=&labels=storyboarding&template=storyboarding-review-request.md&title=) an issue of type Storyboarding Review Request on the experiment repository and fills up the link to the storyboarding document in the issue. 

## 7. Experiment Storyboard Review

The Virtual Labs Reviewing Committee reviews the storyboard document and, if needed, suggests certain alterations or requests extra information. 
All communications regarding the suggestions, requests or clarifications are part of the raised issue in the form of comments.
Once the committee is satisfied with the storyboard, they label the request issue as <b>Approved</b>.
After the experiment storyboard is approved, the experiment development commences.

## 8. Experiment Development

The experiment developer starts experiment development. The developer needs to develop the experiment, test it locally, check the source code into the experiment repository and merge the source code to the main branch of the repository.
The experiment developer can either start the development on the dev branch or create a custom branch for development. During development, the developer unit tests the code. Once the code passes unit testing, the developer raises a merge request to merge the dev branch to the testing branch.
The experiment developer should not delete gh-pages branch. This is required for automatically deploying the experiment along with UI on GitHub pages for testing the complete experiment. They should also not delete .github directory and the LICENSE file in the any of the branches. 

Each merge to the testing branch automatically deploys the experiment to the testing url. A sample experiment code base can be found [here](https://github.com/virtual-labs/ph3-exp-dev-process/tree/main/sample/experiment) and the same experiment deployed on a testing url can be found [here](https://virtual-labs.github.io/ph3-exp-dev-process/). The developer receives an email about the success/failure of the deployment on the email id associated with the github handle provided in the lab proposal. The developer then starts testing the experiment end-to-end.
After the experiment passes the end-to-end testing, the experiment needs to be reviewed and approved. The developer raises an [issue](https://github.com/virtual-labs/ph3-exp-template/issues/new?assignees=&labels=request+for+review&template=experiment-review-request.md&title=) of type Experiment Review Request on the experiment repository and fills up the link to the testing url in the issue.

### Basic requirements for the Experiments

There are certain basic technical requirements that all experiments must follow in order to maintain consistency across the complete ecosystem. Primary of these requirements are:
1. All experiments must work on https
2. All experiments must follow responsive design principles
3. All experiments should be static, without any server side components (exceptions available on merits)
4. Average load size of all page on the experiment (including the loaded 3rd party libraries) should be below 5MB with no single page with load size of more than   10MB (exceptions available on merits)
5. The average load time for all pages on the experiment should be below 1.5 seconds with no single page with load time more than 3 seconds on a fast 3G  connection (exceptions available on merits)

## 9. Experiment Review

The Virtual Labs Reviewing Committee reviews the experiment for its adherence to the proposal and guidelines and, if needed, suggests certain alterations or requests extra information.
All communications regarding the suggestions, requests or clarifications are part of the raised issue in the form of comments.
Once the committee is satisfied with the proposal, they label the request issue  as <b>Approved</b>.

## 10. Experiment Hosting Preparation 

After the experiment is approved, the developer merges the testing branch to the main branch of the experiment repository. The developer also creates a tag on the main branch. This tag is used in the hosting request to uniquely identify the code to be hosted. Ater the code is merged to the main branch and the tag is created, the experiment is ready for public availability.

## 11. Lab/Experiment Hosting and Publishing

After the development and approval of all the experiments listed in the proposal, which constitute the lab, is completed and the developer is ready to publish the experiments to their target audience, they raise an [issue](https://github.com/virtual-labs/engineers-forum/issues/new?assignees=&labels=Phase-3&template=lab-experiment-s--hosting-request.md&title=Lab%2FExperiment+Hosting+Request+for++) of type Lab/Experiment Hosting Request on the Engineers’ Forum repository. A hosting request is in the form of a github issue containing the following information for each experiment in the lab :
1. Experiment Name
2. Experiment Repository URL
3. Tag to be hosted </br>
Along with the above details for each experiment, the issue should contain the following information and documents about the lab as a whole: </br>
4. Contact Person details
  a. Github handle of the developer 
5.Approved Proposal as an attachment

The Virtual Labs hosting team picks up the source code from the tag in the experiment repository and builds all experiments with the common Virtual Labs UI. The hosting team also builds the lab as a container for all the experiments. The hosting team, then deploys the lab and all experiments to the centrally managed cloud. Once the deployment process is complete, the experiments are ready to be used by the target audience. A detailed description of the hosting process can be found [here](https://github.com/virtual-labs/engineers-forum/blob/master/hosting-process.org).

## 12. Lab/Experiment Evaluation and Analytics

Virtual Labs collects basic analytics for all the experiments hosted on the central cloud. The most common parameters collected for analytics are:
1. Number of PageViews
2. Number of Users
3. Geographic location of users
4. Browsers used by the users to access the experiments
5. Device types used by the users to access the experiments

The experiment developer can access these parameters and can evaluate the performance of their experiments on the basis of their predefined performance criteria.

## 13. Experiment Update/Upgrade

The analysis of the evaluation data or bug reports filed by end users or other stakeholders may necessitate or suggest the experiment being updated or upgraded. In this way, the experiment developer stays involved with the experiment through its complete lifecycle.
Each time the experiment is updated, a new hosting request has to be raised in order to rehost the experiment. Each new hosting request must have a unique tag in order to uniquely identify the source code deployed for that hosting request.

## 14. Experiment Archival

The experiment lifecycle concludes in the archival of the experiment. The archival can be requested by the experiment developer or necessitated due to technological issues or other concerns.

## Best Practices

### Coding Standards 

The Virtual Labs recommends Google’s coding standard for Javascript. The standard can be accessed [here](https://google.github.io/styleguide/jsguide.html). In addition to this, a few things like colour/font theme to be kept in mind while developing the experiments  are shared [here](https://github.com/virtual-labs/ph3-exp-dev-process/blob/main/best-practices/README.md).

### Testing Guidelines

The Virtual Labs experiments are static sites. They do not have any server side components. This means that only the UI components need to be tested. The Virtual Labs framework creates a large part of the experiment UI, which the developer does not need to test. The developer is responsible for testing the simulation on both the functionality and UI aspects.
The Virtual Labs team strongly advises the developers to have automated testing set-up. The following framework can be used for writing unit test cases:
1. Jest (For functionality and as the test harness)
</br> For end-to-end testing one of the following frameworks can be used:
2. Cypress
3. Selenium

Apart from the functionality testing, the developer also has to ensure that the experiments meet the requirements like responsiveness, size and performance listed earlier. For testing the size and performance of the experiment, the Virtual Labs suggest the following tool: [Webpagetest](https://www.webpagetest.org/).

All of the above frameworks are just general recommendations. The developers are free to choose any framework based on their familiarity and fitness for the task.

### Security Guidelines 

The developer has to ensure that all the experiments work strictly on https. The Virtual Labs will not support any experiments over http going forward.

## Conclusion

The Virtual Labs Experiment Development Process defines in detail all the steps that an experiment developer needs to follow in order to make their experiments become part of the Virtual Labs e-learning platform.
