# Artifacts

#Table of Content
1. Introduction
  - 1.1 - Purpose
  - 1.2 - Background  
  - 1.3 - Scope
  - 1.4 - Glossary
  - 1.5 - References
  - 1.6 - Risk Analysis
2. Requirements for Test
3. Test Strategy
  - 3.1 -Testing types
   - 3.1.1 - Configuration Testing
   - 3.1.2 - Load Testing
   - 3.1.3 - User Interface Testing
   - 3.1.4 - Browser Testing
   - 3.1.5 - Security and Access Control Testing
  - 3.2 - Tools
4. Resources
  - 4.1 - Workers
  - 4.2 - System
5. Project Milestones
6. Deliverables
  - 6.1 - Test Model
  - 6.2 - Test Results
  - 6.3 - Test Evaluation Report


# 1- Introduction

## 1.1 - Purpose
This Test Plan document for “My web server” supports the following objectives:
* Identify existing project information and application components that should be tested
* List the recommended Requirements for Test
* Recommend and describe the testing strategies to be employed
* Identify the required resources and provide an estimate of the test efforts
* List the deliverable elements of the test project


## 1.2 - Background
The Product Owner (PO) wants to give out a simple-to-deploy web-server. PO wants to be able to deploy the java-server on several devices to attract a wider range of Stake-holders (SH). PO wants to use an open source abandonware software called “My web server”, and for Testers to evaluate if it fulfills the requirements stated in the Requirement document. 


## 1.3 - Scope
This document will be used by the Testers to plan and document the tests and test results. The document will then be reviewed and approved by the Product Owners.
The Testers will be conducting Installation, Functionality and Security tests within a timeline of 2 weeks. The tests will not include Reliability, Supportability or Performance tests. Deadline is set to the 23’rd of December, when a test-strategy, test-plan, test-cases and test-report shall be submitted for review. 


## 1.4 - Glossary
* Testers - Responsible for the Testing of the application and web-server
* Product Owner - Responsible for reviewing the final test-report and documentation.
* Stake-holders - Users of the final product.
* Web-server - The Java based web server used to run the application
* Application - Product to be tested

## 1.5 - References
[Requirement Document](https://docs.google.com/document/d/1fgQngHIZ4_aGIeB2S9YOBCghcBN9EEKBiaN-71MbGac/) - Use Cases and Requirements

## 1.6 - Risk Analysis
The risks involved are to great extent connected to the collected experience of the Testers. They have only used Windows as an operating system, have limited experience in coding with Java, and they have not worked using Eclipse IDE before. There is also a limited time frame to conduct the testing. 
Successful testing is dependant on having a reliable testing environment.
In order to limit these risks, the testing should be started early within the given time frame, in order to solve potential problems while using the IDE and coding language. The testing should be conducted within a stable environment.

# 2 - Requirements for Test
* Tester must have started the web-server.
* Tester must have access to a web browser.

# 3 - Test Strategy
Testers will write manual Test Cases based on the Use Cases provided in the external Requirements Document. They will then conduct the test according to the instructions specified in the Test Cases. Whether the test is successful or not will be determined by comparing expected results based on the scenarios of the Use Cases with actual results provided from the tests. 

## 3.1 -Testing types
Manual testing

### 3.1.1 -   Configuration Testing
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 1 | R3 | Test to configure software needed to run web-server | Correct version of JAVA and Eclipse have been installed | Tester enters socket port number and a correct shared resource container | Server should start |	











### 3.1.2 - Load Testing
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |	


### 3.1.3 - User Interface Testing
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |	


### 3.1.4 - Browser Testing
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |	

#### 3.1.4.1 - Chrome
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |	

#### 3.1.4.2 - Mozilla
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |

#### 3.1.4.3 - Microsoft Edge
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |

#### 3.1.4.4 - Opera
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |

### 3.1.5 - Security and Access Control Testing
Use Case Tested | Requirement Tested | Test Objective | Instructions | Expected Results | Actual Result |
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- | 
What is being tested | What requirement is tested | Why should we test | What tester does | What should happen | What happens |	



## 3.2 - Tools
* Eclipse IDE 
* JAVA-SE 1.7 (or newer)
* Microsoft 10, x64-bit
* Google Chrome (Version 55.0.2883.87 m)
* Mozilla Firefox (Version 50.1.0)
* Microsoft Edge (Version 38.14393.0.0)
* Opera (Version 42.0.2393.94)

# 4 - Resources
## 4.1 - Workers
Testers x 2
## 4.2 - System
* Java-SE 1.7 or more recent
* Eclipse IDE
* Web browser


# 5 - Project Milestones

Milestone Task | Time | Start | End |
----------------- | ------ | ----- | ----- |
Setup Testing Environment | 4h (x2?) | 9.00 | 12.20 |
Plan Tests | 4h (x2?) | 13.30 | 18.00 |
Design Tests | h | 19.30 | ----- |
Implements Tests | h | ----- | ----- |
Execute Tests | h | ----- | ----- |
Evaluate Tests | h | ----- | ----- |


# 6 - Deliverables
## 6.1 - Test Model
Define Test Cases & reference the Test Procedures, test scripts associated with test cases (???)



## 6.2 - Test Results

### 6.2.1 - Configuration Testing

Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
 3.1.1 - Configuration Testing | Date | Tester ID | Correct version of JAVA and Eclipse has been installed | Tester enters socket port number and a shared resource container | Server should start | Server didn’t start due to incorrect source code. | Alter source code.



## 6.3 - Test Evaluation Report
Final evaluation of test activities.

### 6.3.1 - Configuration Testing

Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.1 - Configuration Testing | When running the application in Windows 10, the configuration for the shared resource container is case sensitive.| Reflection |




