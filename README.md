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

## Step 5. Classified the major requirements and put them in user stories to take the project further.

### 1. Training Questions
### 1.1-Title: Viewing Training Questions Without Answers
As an AI developer, I want the system to present only training questions by default, so that I can conduct self-affirmation training without being influenced by answers.

###1.1.1- Default Question View
“As an AI developer, I want to view questions cards of the selected category, so that I can conduct self-affirmation training without being influenced by answers”
-	Goal : Implement search engine for questions to train on.
-	Expected outcomes: View questions card
### 1.1.2- Separate Data storage
“As a AI System Admin, I want separate storage for questions and answers, ensuring that answers are only fetched when necessary, so that I can maintain data security and self-affirmation training.”
-	Goal: Implement distinct database for questions and answers to enforce controlled data retrieval.
-	Expected Outcome: Questions can be accessed freely, while answers are protected and only fetched when authorized.
### 1.1.3- UI Design for Question & Answer Segregation
“As a AI develope, As reviewer, I want a two-step process where I first review questions separately and then validate AI responses against correct answers using a click of button, so that I can control when and how I access answers.”
- Goal: Implement a toggle button that allows users to reveal answers only when needed, ensuring valid user a focused and structured review process.
- Expected Outcome: Users can initially engage with questions without distractions and selectively reveal answers for validation, improving comprehension and evaluation efficiency.

### 1.2 - Categorizing Training Questions
"As a AI developer, I want to categorize training questions so that I can organize them into predefined or custom categories for better management."
### 1.2.1- Dropdown Menu:
"As a AI developer, I want to select from predefined categories when categorizing a training question, so I can quickly organize data."
- Goal: Provide a list of predefined categories for quick selection.
- Outcome: AI developers can easily choose the appropriate category for questions, speeding up the categorization process.
### 1.2.2- Text Field:
"As a AI developer, I want the option to type a custom category when it’s not available in the predefined list, so I can have full flexibility."
- Goal: Allow the addition of custom categories when predefined options are insufficient.
- Outcome: AI developers can create flexible categories without restrictions.
### 1.2.3-Save Button:
"As a AI developer, I want to save the category changes I made so that the new categorization is saved for later use."
- Goal: Provide a clear way to save categorization changes.
- Outcome: AI developers can save their changes successfully, ensuring consistency in data management.

### 1.3 - Customizing Categories
"As a AI developer, I want to create and modify categories, so that I can better structure and adapt the training questions as needed."
### 1.3.1-Add Category Button:
"As a AI developer, I want a button that opens a modal to create new categories, so I can easily add categories when needed."
- Goal: Provide an easy-to-use button to add new categories.
- Outcome: AI developers can quickly create new categories through a simple button click.
### 1.3.2-Modal for Category Creation:
"As a AI developer, I want a modal with a text input for naming the new category, so I can customize my categorization."
-	Goal: Design a user-friendly modal for category creation.
-	Outcome: AI developers can enter and save a custom category name effortlessly.
### 1.3.3-Edit/Delete Category Options:
"As a AI developer, I want to edit or delete categories directly from the interface, so I can manage categories flexibly."
-	Goal: Enable editing and deleting of categories from the UI.
-	Outcome: AI developers can modify categories at any time based on project requirements.

### 1.4 - Searching Categorized Questions
"As a AI developer, I want to search and filter training questions by category, so I can easily find the relevant questions without scrolling through all of them."
### 1.4.1-Search Bar:
"As a AI developer, I want to search training questions using keywords, so I can quickly find the right questions."
-	Goal: Allow searching of questions based on specific keywords.
-	Outcome: AI developers can find questions instantly by searching for keywords.
### 1.4.2-Filters:
"As a AI developer, I want to filter questions by category, date, or tags, so I can narrow down my search results."
-	Goal: Enable advanced filtering to refine search results.
-	Outcome: AI developers can filter questions by category, date, or other criteria for more relevant results.
### 1.4.3-Clear Filters Button:
"As a AI developer, I want an option to clear my filters, so I can reset my search and start fresh."
-	Goal: Provide a way to clear applied filters and start a new search.
-	Outcome: AI developers can easily reset their search parameters to begin a new search.

### 2. Balanced Training Data

### 2.1 - Detecting Bias in Data
"As a AI developer, I want the system to automatically detect bias in training data, so I can quickly identify areas of concern and improve fairness."
### 2.1.1-Bias Indicators:
"As a AI developer, I want to see visual indicators on biased data, so I can easily spot and address potential issues."
-	Goal: Clearly indicate biased entries with visual cues (e.g., red exclamation marks).
-	Outcome: AI developers can quickly identify flagged data entries for bias.
### 2.1.2-Bias Detection Dashboard:
"As a AI developer, I want to view a dashboard with an overview of detected biases, so I can monitor how much bias is present in my dataset."
-	Goal: Provide a central dashboard with bias statistics.
-	Outcome: AI developers can track bias trends and focus on the most problematic data areas.

### 2.2 - Adjusting Bias Detection Criteria
As a AI developer, I want to adjust bias detection settings, so I can fine-tune how biases are detected according to the specific needs of my model.
### 2.2.1-Bias Settings Panel:
"As a AI developer, I want a panel where I can adjust the sensitivity of bias detection, so I can customize the detection thresholds."
-	Goal: Provide a settings panel to modify bias detection behavior.
-	Outcome: AI developers can fine-tune bias detection parameters.
### 2.2.2-Sliders/Checkboxes:
"As a AI developer, I want to use sliders or checkboxes to easily adjust bias detection parameters, so I can have more control over how biases are flagged."
-	Goal: Enable intuitive control over bias detection settings.
-	Outcome: AI developers can adjust detection thresholds quickly and easily.

### 2.3 - Generating Bias Reports
"As a AI developer, I want to generate bias reports, so I can track improvements in data balance and fairness over time."
### 2.3.1-Generate Report Button:
"As a AI developer, I want a button to create a bias analysis report, so I can generate reports when I need them."
-	Goal: Add a button for generating bias reports on demand.
-	Outcome: AI developers can create reports whenever necessary.
### 2.3.2-Download/Export Option:
"As a AI developer, I want the option to download or export the report in formats like CSV or PDF, so I can share or analyze the results offline."
-	Goal: Allow export of bias reports in multiple formats.
-	Outcome: AI developers can download reports for offline analysis or sharing.
### 2.3.3-Show Report Summary:
"As a AI developer, I want to see a summary of the bias detection process in the report, so I can quickly understand the scope of detected biases."
-	Goal: Provide a clear summary of detected biases in the report.
-	Outcome: AI developers get a concise summary of the bias analysis.

### 3. AI Training Workflow: Two-Phase Training for Questions and Answers

### 3.1 - Training on Questions First
“As a AI AI developer, I want the AI model to be trained on questions separately first, so that it learns to classify and categorize them effectively before incorporating answers.”
-	Goal: Train the AI model initially on question patterns and categories.
-	Outcome: The model gains a strong understanding of question structures before considering answers.
### 3.2 - Validating Training with Answers
“As a machine learning engineer, I want to validate the AI model's learning by introducing answers in a second phase, so that it can refine predictions based on both questions and answers.”
-	Goal: Introduce answers only after initial question training to refine AI predictions.
-	Outcome: The AI can better map questions to correct answers, improving model accuracy.
### 4 - Secure Data Storage with Version Control and Audit Tracking
"As a AI developer, I want to store training data securely with version control and audit tracking, so I can ensure data integrity and traceability over time."
### 4.1- Version History Tab:
"As a AI developer, I want to view the version history of my training data, so I can track changes and revert if needed."
-	Goal: Provide version control for tracking changes over time.
-	Outcome: AI developers can access the full version history and manage data revisions.
### 4.2-Audit Log Access:
"As a AI developer, I want access to an audit log that records changes to the data and categories, so I can maintain full traceability of actions taken."
-	Goal: Enable auditing of all data modifications.
-	Outcome: AI developers have full visibility into changes and actions taken on the data.
