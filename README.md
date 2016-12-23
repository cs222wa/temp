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
  - 3.1.4 - Security and Access Control Testing
  - 3.1.5 - Browser Testing
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
* Identify components of the application and web server to be tested
* List the recommended Requirements for Test
* Recommend and describe the testing strategies to be employed
* Identify the required resources and provide an estimate of the test efforts
* List the deliverable elements of the test project


## 1.2 - Background
The Product Owner (PO) wants to give out a simple-to-deploy web-server. PO wants to be able to deploy the java-server on several devices to attract a wider range of Stake-holders (SH). PO wants to use an open source abandonware software called “My web server”, and for Testers to evaluate if it fulfills the requirements stated in the Requirement document. 


## 1.3 - Scope
This document will be used by the Testers to plan and document the tests and test results. The document will then be reviewed and approved by the Product Owners.
The Testers have been given a timeline of 2 weeks to plan and conduct Installation, Functionality, Supportability and Security tests on the system, but due to external circumstances, this has now been limited to two days. All test will be conducted using Google Chrome (Version 55.0.2883.87 m) as default web browser if nothing else is stated in the Test Case. The tests will not include Reliability or Performance tests. Deadline is set to the 23’rd of December, when a test-strategy, test-plan, test-cases and test-report shall be submitted for review. 


## 1.4 - Glossary
* Testers - Responsible for the Testing of the application and web-server
* Product Owner - Responsible for reviewing the final test-report and documentation.
* Stake-holders - Users of the final product.
* Web-server - The Java based web server used to run the application
* Application - Product to be tested
* Administrator - Responsible for the server and basic server configurations

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

### 3.1.1 - Configuration Testing
### 3.1.1.1 - Configuration Testing - Port and Resource Container
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 1 | R3 | Test to configure software needed to run web-server | Correct version of JAVA and Eclipse have been installed | Tester enters socket port number and a correct shared resource container | Server should start and a note should be written in the access log |	


### 3.1.2 - Load Testing 
#### 3.1.2.1 - Load Testing - Server Access (localhost:1091)
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 1  | R3 | To test if the main page is loaded when web-server is accessed | Web-server is running | Tester enters the url to the server in the web browser | Index.html is shown |	


### 3.1.3 - User Interface Testing
#### 3.1.3.1 - User Interface Testing - Index.html
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if a page loads when accessing web server | Web-server is running | Tester enters the url to Index.html in the web browser | Index.html is shown |		

#### 3.1.3.2 - User Interface Testing - images/works.png
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if it’s possible to access a file on the web-server through the web browser | Web-server is running | Tester enters the url to images/work.png in the web browser | The chosen image is shown |	

#### 3.1.3.3 - User Interface Testing - images/works.png  (removed)
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R2, R3 | Test to see if removing a requested resource and trying to access it through the web browser results in a “resource can not be found” message | Web-server is running, resource “works.png” has been temporarily removed from resources folder | Tester enters the url to images/work.png in the web browser | System presents that the resource cannot be found - 404 Not Found |	


### 3.1.4 - Security and Access Control Testing
#### 3.1.4.1 - Security and Access Control Testing - /.../secret.html 
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3 - 2B | R2, R3 | Test to see if it’s possible to access a forbidden file through the web server | Web-server is running | Tester enters the url to /.../secret.html in the web browser |  System presents that the source is forbidden - 403 Forbidden |

#### 3.1.4.2 - Security and Access Control Testing - Shut down  server 
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 2 | R2 | Test to see if web-server is still accessible after having been shut down | Administrator has shut the server down | Tester enters the url to Index.html in the web browser |  System presents that the resource cannot be found - 404 Not Found, and a note should be written in the access log |	


### 3.1.5 - Browser Testing
#### 3.1.5.1 - Browser Testing - Chrome
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if the index page is loaded correctly when using a Google Chrome browser | Web-server is running | Tester enters the url to Index.html in the Google Chrome browser | Index.html is shown |			

#### 3.1.5.2 - Browser Testing - Mozilla
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if the index page is loaded correctly when using a Mozilla Firefox browser | Web-server is running | Tester enters the url to Index.html in the Mozilla Firefox  browser | Index.html is shown |		

#### 3.1.5.3 - Browser Testing - Microsoft Edge
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if the index page is loaded correctly when using a Microsoft Edge browser | Web-server is running | Tester enters the url to Index.html in the Microsoft Edge browser | Index.html is shown |	

#### 3.1.5.4 - Browser Testing - Opera
Use Case Tested | Requirement Tested | Test Objective | Post Conditions | Input | Expected Results | 
------------ | ------------ | ------------ | ---------------- | ---------------- | ---------------- |
UC 3  | R3 | Test to see if the index page is loaded correctly when using an Opera browser | Web-server is running | Tester enters the url to Index.html in the Opera browser | Index.html is shown |


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
Setup Testing Environment | 4h (x2) | 2016-12-22 09.00 |  2016-12-22 12.20 |
Plan Tests | 4h (x2) |  2016-12-22 13.30 |  2016-12-22 18.00 |
Design Tests | 3,5h(x2) |  2016-12-22 19.30 |  2016-12-22 23.00 |
Implements Tests | 2(x2) |  2016-12-23 7.00 | 2016-12-23 9.00 |
Execute Tests | 3h(x2) | 2016-12-23 9.00 | 2016-12-23 12.00 |
Evaluate Tests | h | 2016-12-23 12.00 | 2016-12-23 16.00 |


# 6 - Deliverables

## 6.1 - Test Results
### 6.1.1 - Configuration Testing
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
 3.1.1.1 - Configuration Testing - Port and Resource Container
 | 2016-12-22| Tester 1, Tester 2 | Correct version of JAVA and Eclipse has been installed | Tester enters socket port number and a shared resource container | Server should start | Server didn’t start due to incorrect source code. | Alter source code.


### 6.1.2 - Load Testing
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.2.1 - Load Testing - Server Access (localhost:1091)
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running | Tester enters the url to the server in the web browser | Index.html is shown | Index.html is shown | None|

### 6.1.3 - User Interface Testing

#### 6.1.3.1 - User Interface Testing - Index.html
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.3.1 - User Interface Testing - Index.html)
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running |Tester enters the url to Index.html in the web browser | Index.html is shown | Index.html is shown | None|


#### 6.1.3.2 - User Interface Testing - images/works.png
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.3.2 - User Interface Testing - images/works.png
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running |Tester enters the url to images/work.png in the web browser | The chosen image is shown | The chosen image is shown | None|

#### 6.1.3.3 - User Interface Testing - images/works.png (removed)
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.3. 3 - User Interface Testing - images/works.png (removed)
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running, resource “works.png” has been temporarily removed from resources folder | Tester enters the url to images/work.png in the web browser | System presents that the resource cannot be found - 404 Not Found | System presents that the resource cannot be found - 404 Not Found | None|


### 6.1.4 - Security and Access Control Testing

#### 6.1.4.1 - Security and Access Control Testing - /.../secret.html 
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.4.1 - Security and Access Control Testing - /.../secret.html  | 2016-12-23| Tester 2 | Web-server is running | Tester enters the url to /.../secret.html in the web browser | System presents that the resource is forbidden  - Forbidden 403 | System presents that the resource is forbidden  - Forbidden 403 | None|

#### 6.1.4.2 - Security and Access Control Testing - Shut down server
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
 3.1.4.2 - Security and Access Control Testing - Shut down server   | 2016-12-23| Tester 1 | Web-server is running | Administrator has shut the server down|  System presents that the resource cannot be found - 404 Not Found, and a note should be written in the access log | System presents that the resource cannot be found - 404 Not Found, and a note should be written in the access log | None|

### 6.1.5 - Browser Testing

#### 6.1.5.1 - Browser Testing - Google Chrome
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.5.1 - Browser Testing - Chrome
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running | Tester enters the url to Index.html in the Google Chrome browser | Index.html is shown | Index.html is shown | None |


#### 6.1.5.2 - Browser Testing - Mozilla Firefox
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.5.2 - Browser Testing - Mozilla
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running | Tester enters the url to Index.html in the Mozilla Firefox browser | Index.html is shown | Index.html is shown | None |

#### 6.1.5.3 - Browser Testing - Microsoft Edge
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.5.3 - Browser Testing - Microsoft Edge
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running | Tester enters the url to Index.html in the Microsoft Edge browser | Index.html is shown | Index.html is shown | None |


#### 6.1.5.4 - Browser Testing - Opera
Test Case | Date | Tester | Post Conditions | Input | Expected Results | Actual Result | Adjustment |
------------ | ---------------- | ---------------- |  ---------------- | ---------------- | ---------------- | ---------------- | ---------------- |
3.1.5.4 - Browser Testing - Opera
 | 2016-12-23| Tester 1, Tester 2 | Web-server is running | Tester enters the url to Index.html in the Opera browser | Index.html is shown | Index.html is shown | None |



## 6.2 - Test Evaluation Report

### 6.2.1 - Configuration Testing - Port and Resource Container
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.1.1 - Configuration Testing - Port and Resource Container | When running the application in Windows 10, the configuration for the shared resource container is case sensitive.| This may cause for unnecessary bugs and troubleshooting. Suggestion is to make the URL recognition of the Resource Container non case sensitive for future use. |


### 6.2.2 - Load Testing - Server Access (localhost:1091)
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.2.1 - Load Testing - Server Access (localhost:1091) | The main page is loaded directly when the web server is accessed. | This shows that the default main page setting for the web server works. |


### 6.2.3 - User Interface Testing - Index.html
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
3.1.3.1 - User Interface Testing - Index.html) | A page is loaded directly when the user enters the url to Index.html in the web browser. | This shows that the user is capable of navigating the web page. |


### 6.2.4 - User Interface Testing - images/works.png
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.3.2 - User Interface Testing - images/works.png | It is possible to access a file directly on the web server, when the tester enters the url to images/work.png in the web browser. | This shows that the user is able to access files on the web server. |

### 6.2.5 - User Interface Testing - images/works.png (removed)
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.3.3 - User Interface Testing - images/works.png (removed) | It is not possible to access a file directly through an old url in the web browser, once the file has been removed from the web server. | This shows that the security and privacy settings for the resource container works. |

### 6.2.6 - User Interface Testing - Security and Access Control Testing - /.../secret.html 
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
6.1.4.1 - Security and Access Control Testing - /.../secret.html 
 | It is not possible to access a file outside of the configured resource container |  This shows that the security and privacy settings for the resource container works. |

### 6.2.7 - User Interface Testing - Security and Access Control Testing - Shut down server
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
 3.1.4.2 - Security and Access Control Testing - Shut down server 
 | It is not possible to access the web-server after it’s been shut down. | This indicated that the web server and application does not leave a cache or cookies to display if the server is down. |

### 6.2.8 - Browser Testing - Google Chrome 
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
6.1.5.1 - Browser Testing - Google Chrome 
 | Web page works in Google Chrome | For the application to work in several web browsers, increases the range of potential Stake-holders that would be willing and capable to use the product. |

### 6.2.9 - Browser Testing -  Mozilla Firefox
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
6.1.5.2 - Browser Testing -  Mozilla Firefox 
 | Web page works in  Mozilla Firefox | For the application to work in several web browsers, increases the range of potential Stake-holders that would be willing and capable to use the product. |

### 6.2.10 - Browser Testing - Microsoft Edge
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
6.1.5.3 - Browser Testing - Microsoft Edge 
 | Web page works in Microsoft Edge | For the application to work in several web browsers, increases the range of potential Stake-holders that would be willing and capable to use the product. |

### 6.2.11 - Browser Testing - Opera
Test case | Evaluation | Reflection |
---------------- | ---------------- | ---------------- |
6.1.5.4 - Browser Testing - Opera
 | Web page works in Opera| For the application to work in several web browsers, increases the range of potential Stake-holders that would be willing and capable to use the product. |


##6.3 - Test Analyzation

More thorough testing could have been made if testing had begun earlier. As it was delayed, the Testers did not have enough time to implement Apache JMeter into the test suite, which limited the Test Types to Manual rather than Automated testing. This in turn meant that Performance and Reliability tests could not be made. 
Had the Testers been using JMeter to conduct a larger amount of tests, the results and evaluation of the Test Report would have been able to represent the finished product in a more correct way. 

