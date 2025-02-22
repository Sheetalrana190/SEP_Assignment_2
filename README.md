# Assignment 2: Requirements

### Student Information
**Name:** Sheetal Rana  
**Student ID:** 8994226  

---

## Purpose
The purpose of this assignment is to practice analyzing and documenting requirements, including functional, non-functional, and system-based requirements, and verifying them with the client. Then to analyze the current status and push the project forward.

To achieve this task my approach will be as follow from lecture slide 6: Week-4-Analysis
Systems analysis activities  
- Gather detailed information:  Interviews, questionnaires, documents, observation of business practices, vendor research,
comments, suggestions
- Define requirements : Model functional and non-functional requirements
- Develop user interface dialogs : Interaction flow between user and system
- Evaluate Requirements with Users: User involvement, feedback, adapt to changes

## 1.2 Given Scenario
We are working with an AI developer who uses web scraping to generate training data. The client has specific needs and challenges regarding categorizing training questions and ensuring balanced data. 
After few meetings with the client we have able narrowed down to following needs and challenges.
## 1.3 Client's Needs and Challenges
### Training Questions
Developers want to have categorized training questions that are separate from the answers because developers care about self-affirmation.
### Balanced Training Data
Developers want to know that the training data they are using is "balanced" (does not contain biases) because this will give them better AI models.

---
## Step 1. Analyze the Current Need of the client and gather detail Information 
First, we will take a closer look at the two main needs provided and analyze them using best practices. 

**1 need. Training Questions :** Developers want to have categorized training questions that are separate from the answers because developers care about self-affirmation.

#### Analysis:
-	*Clarity: * The requirement is clear in its intent to separate questions from answers.
-	*Specificity:* It specifies that categorization is needed, but it could be more specific about how the categorization should be done (e.g., tags, folders).
-	*Achievability:* It is achievable with the right tools and methods.
### Client Questions for Requirement Gathering on Categorized Training Questions
(Goal: Understand how training questions should be structured and managed.)
1.	How do you currently categorize training questions?
2.	What specific categories do you use for training questions?
3.	Do you require the system to suggest categories automatically?
4.	Should developers be able to create custom categories?
5.	How do you expect the interface for managing categorized questions to look like?
6.	What is the expected response time for categorizing training data?
**2 need. Balanced Training Data :** Developers want to know that the training data they are using is “balanced” (does not contain biases) because this will give them better AI models.

#### Analysis:
-	*Clarity: *The requirement is clear in its intent to have balanced, unbiased training data.
-	*Specificity:* It specifies the need for balanced data but could be more specific about how to measure and achieve balance.
-	*Achievability:* It is achievable with the right algorithms and methods for bias detection and correction.
### Client Questions for Requirement Gathering on Balanced Training Data
(Goal: Ensure training data is free from biases and properly structured.)
1.	How do you define "balanced" training data?
2.	What biases are you most concerned about in your training data?
3.	Should the system automatically flag biased data or provide reports for manual review?
4.	How frequently should bias detection be performed?
5.	Should developers be able to adjust bias parameters manually?
6.	How do you currently validate whether a dataset is balanced? Do you have specific benchmarks for bias detection accuracy?
### General Verification Questions for Client: 
(Goal: To generate appropriate system usage requirements)
1.	Do you have any examples or use cases that illustrate your needs?
2.	Do you have preference for who have access to edit training questions and categories?
3.	Should different roles (e.g., developer, admin, manager) have different access  permissions?
4.	Should the system log all actions related to data categorization and bias detection?
5.	What security measures are you currently using what should be implemented? (e.g., encryption, 2FA, role-based access)
6.	Should access logs be kept for compliance tracking?
7.	How will you measure the success of this project?
### Assumptions :
-	The client currently lacks an automated system for categorizing training questions.
-	Developers have different preferences for category customization, requiring manual and automated options.
-	Bias detection should be transparent and adjustable for developers.
-	The system will integrate with existing AI model training environments.

## Step 2: Define Requirements
The functional and non-functional were structured based on collected data from client and for verifiaction from client open for changes in it.

### 1. Training Questions:
#### Functional Requirements:
1.	The system shall separate questions from answers for self-affirmation training.
2.	The system shall allow developers to categorize training questions manually and automatically.
3.	The system shall enable users to filter, search, and manage categorized questions.
#### Non-Functional Requirements:
1.	The system shall process training data categorization within 5 seconds per request.
### 2. Balanced Training Data:
#### Functional Requirements:
1.	The system shall include a mechanism to detect and highlight biases in training data.
2.	The system shall generate reports on data balance and bias detection.
3.	Developers shall be able to adjust and fine-tune bias detection criteria.
#### Non-Functional Requirements:
1.	The bias detection mechanism shall flag issues with at least 90% accuracy.

## Step 3 : Define System Requirements:
Based on the functional and non-functional requirement above system requirements are drawn for developmet team
1.	Implement data base to store question and answer separately.
2.	Implement a classification algorithm to automatically tag training questions.
3.	Provide an interface for users to manage categorized training questions.
4.	Integrate bias detection algorithms for analyzing training data.
5.	Store training data in a secure, scalable database.
6.	Use a role-based access control system to manage permissions.
7.	Implement audit logging to track changes in training data.
8.	Integrate with existing AI model training workflows.


## Step 4. Develop user interface dialogs : Interaction flow between user and system
This how the system will look like for client 
-	Design an interface where answers are not visible by default and require user interaction to view.
-	Only authorized users (e.g., reviewers) can access answers.
-	Ensure the AI learns from questions without seeing answers initially, followed by a separate validation phase.
-	Provides a dashboard for managing training question categories and bias detection.
-	Uses machine learning models for bias detection and classification automation.
-	Stores training data securely with version control and audit tracking.
-	Integrates seamlessly with existing AI training pipelines using API endpoints.
-	Implements an intuitive UI/UX that requires minimal onboarding for developers.

