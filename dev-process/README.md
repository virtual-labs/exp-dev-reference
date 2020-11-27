# Introduction

The environmental and social changes brought about by the Corona pandemic have precipitated a mindset shift towards the virtual methods of learning. As a result Virtual Labs has witnessed a significant increase in the expression of interests for the development of new experiments. In the light of this increased interest, it becomes pertinent to publish the process for building and contributing new experiments to the Virtual Labs ecosystem. This document serves as a guideline for creating a new experiment from conception to deployment.

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

## Expression of Interest

Experiments are developed in a group. The experiment developers create a collection of related experiments, which is called a lab. The experiment development process starts with an Expression of interest for the lab. To express the interest for developing a new lab, the developer fills the expression of interest form available [here](https://docs.google.com/forms/d/e/1FAIpQLSctFus-noUJL815JG1i7RhO_cWKiryfsQ2pOhz2xVBeG0GVTQ/viewform).  A completely filled lab proposal document also needs to be attached to the form. The template of the Lab Proposal document, along with a sample proposal, is available in the form. On receipt of the Expression of Interest form, the Virtual Labs team reviews the proposal and either sends out an acceptance mail or suggests improvements to the proposal. 

## Experiment Repositories Creation 

Once the proposal is accepted by the Virtual Labs team, the developer raises an [issue](https://github.com/virtual-labs/engineers-forum/issues/new?assignees=&labels=Phase-3&template=phase-iii-experiment-repository-creation-request.md&title=) of type Phase III Experiment Repository Creation Request on engineers-forum repository under the  virtual-labs organization on Github. The developer attaches the pdf of the approved proposal to the request issue.

The Virtual Labs team creates a git repository for each experiment of the proposed lab. This repository is the single source of truth for the experiment. It contains all the resources and all communication related to the experiment.
The git repository created by the Virtual Labs team contains templates along with examples for all the documents to be submitted as part of the experiment development process.

The url of the experiment repository is shared with the developer by the Virtual Labs team on the Experiment Repository Creation Request issue.

## Experiment Repository Structure

The experiment repository created by the Virtual Labs team contains 3 default branches. Each branch serves a specific purpose and has certain conventions, which must be followed by the experiment developers. The developers are free to create any extra branches as they deem necessary. The 3 default branches in an experiment repository are:

1. Dev: This is the branch where the experiment development process starts. The developers can either directly add code to the dev branch or can merge their custom or issue specific branches to the dev branch. This branch is also used for unit testing the experiment.
2. Testing: Once the code passes unit testing in the dev branch, it is promoted to the testing branch by raising and approving a merge request from the dev branch to the testing branch. The code in the testing branch is used for the end-to-end testing of the code. Each experiment repository has a static site hosting url where the code in the testing branch is deployed. The deployment of the code is effected through an automated CI/CD pipeline provided in the experiment repository. Each merge to the testing branch automatically deploys the experiment to the testing url. The developer receives an email about the success/failure of the deployment on the email id associated with the github handle provided in the lab proposal.
3. Main: The branch named as main is the identifying branch of the experiment repository. The code and the documents in the main branch are the production artefacts. The only way code and documents can be added to the main branch is by merging the testing branch to it. It is mandatory that the code in the main branch is always in the deployable condition. All the reviews and hosting will be performed strictly on the documents and code present in the main branch.

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

## Experiment Pedagogy Submission

After the creation of the experiment repositories, the experiment developer updates the README.md of the repository with details of the experiment, developing institute and development team. The experiment developer then fills the experiment pedagogy document by updating the experiment pedagogy template in the experiment repository. The template also contains links to reference and sample documents. Following set of information needs to be provided in the pedagogy document:

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

## Experiment Pedagogy Review

The Virtual Labs Reviewing Committee reviews the pedagogy document and, if needed, suggests certain alterations or requests extra information.
All communications regarding the suggestions, requests or clarifications are part of the raised issue in the form of comments.
Once the committee is satisfied with the proposal, they label the request issue as <b>Approved</b>.

## Experiment Storyboard Submission

After the approval of the experiment pedagogy, the developer submits the experiment storyboard by updating the experiment storyboard template in the experiment repository. The template also contains links to reference and sample documents. 
Following set of information needs to be provided in the storyboard:
1. Simulation Story
2. Simulation flowchart
3. Mindmap
4. Storyboard

Once the completed storyboard document is merged to the main branch, the developer [raises](https://github.com/virtual-labs/ph3-exp-template/issues/new?assignees=&labels=storyboarding&template=storyboarding-review-request.md&title=) an issue of type Storyboarding Review Request on the experiment repository and fills up the link to the storyboarding document in the issue. 

## Experiment Storyboard Review

The Virtual Labs Reviewing Committee reviews the storyboard document and, if needed, suggests certain alterations or requests extra information. 
All communications regarding the suggestions, requests or clarifications are part of the raised issue in the form of comments.
Once the committee is satisfied with the storyboard, they label the request issue as <b>Approved</b>.
After the experiment storyboard is approved, the experiment development commences.
