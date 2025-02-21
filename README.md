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
#-	**Analysis:**
-	*Clarity:* The requirement is clear in its intent to separate questions from answers.
-	*Specificity:* It specifies that categorization is needed, but it could be more specific about how the categorization should be done (e.g., tags, folders).
-	*Achievability:* It is achievable with the right tools and methods.
# Client Questions for Requirement Gathering on Categorized Training Questions
(Goal: Understand how training questions should be structured and managed.)
1.	How do you currently categorize training questions?
2.	What specific categories do you use for training questions?
3.	Do you require the system to suggest categories automatically?
4.	Should developers be able to create custom categories?
5.	How do you expect the interface for managing categorized questions to look like?
6.	What is the expected response time for categorizing training data?
**2 need. Balanced Training Data :** Developers want to know that the training data they are using is “balanced” (does not contain biases) because this will give them better AI models.
#-	Analysis:
-	*Clarity: *The requirement is clear in its intent to have balanced, unbiased training data.
-	*Specificity:* It specifies the need for balanced data but could be more specific about how to measure and achieve balance.
-	*Achievability:* It is achievable with the right algorithms and methods for bias detection and correction.
# Client Questions for Requirement Gathering on Balanced Training Data
(Goal: Ensure training data is free from biases and properly structured.)
1.	How do you define "balanced" training data?
2.	What biases are you most concerned about in your training data?
3.	Should the system automatically flag biased data or provide reports for manual review?
4.	How frequently should bias detection be performed?
5.	Should developers be able to adjust bias parameters manually?
6.	How do you currently validate whether a dataset is balanced? Do you have specific benchmarks for bias detection accuracy?
# General Verification Questions for Client: 
(Goal: To generate appropriate system usage requirements)
1.	Do you have any examples or use cases that illustrate your needs?
2.	Do you have preference for who have access to edit training questions and categories?
3.	Should different roles (e.g., developer, admin, manager) have different access  permissions?
4.	Should the system log all actions related to data categorization and bias detection?
5.	What security measures are you currently using what should be implemented? (e.g., encryption, 2FA, role-based access)
6.	Should access logs be kept for compliance tracking?
7.	How will you measure the success of this project?
# Assumptions :
-	The client currently lacks an automated system for categorizing training questions.
-	Developers have different preferences for category customization, requiring manual and automated options.
-	Bias detection should be transparent and adjustable for developers.
-	The system will integrate with existing AI model training environments.
