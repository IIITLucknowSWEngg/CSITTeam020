# Test Documentation for OYO booking system

## Test Plan

### Introduction

The purpose of this test plan is to outline the testing approach, strategies, and activities for the OYO Booking System.

### Purpose

The purpose of testing is to ensure that the OYO Booking System meets the specified requirements, functions as intended,
and provides a satisfactory user experience.

### Scope

This test plan covers the functional and non-functional testing of the OYO Booking System, including its core features
and key system components.

### Test Items

The test items for the OYO Booking System include:

- User registration and login
- Hotel search and booking
- Payment processing
- Room availability and pricing
- Booking confirmation and cancellation
- User management and administration

### Features to be Tested

The following features of the OYO Booking System will be tested:
User registration and login, Hotel search and filtering, Room availability and pricing, Booking creation and management,
Payment processing, Booking confirmation and cancellation, User profile management, Administrative functions (hotel
management, reporting, etc.)

### Test Approach

The test approach for the OYO Booking System includes the following:
Conducting functional testing to verify that the system meets the specified requirements and functions correctly.
Performing usability testing to ensure the system is user-friendly and provides a seamless booking experience.
Conducting regression testing to verify that system updates or changes do not introduce new defects or impact existing
functionality.

### Responsibilities

The following roles and responsibilities are assigned for the testing process:

- Test Manager: Overall test planning and coordination
- Test Analyst: Test case design and execution
- Development Team: Assist in defect analysis and resolution
- Business Analyst: Provide requirements clarification and validation

### Test Strategy

The test strategy covers the functional and non-functional testing aspects of the OYO Booking System, including user
registration and login, hotel search and booking, payment processing, room availability and pricing, booking
confirmation and cancellation, user management, and administrative functions.

### Test Levels:

1. Component Testing: Individual components of the OYO Booking System will be tested in isolation to ensure their
   functionality and correctness.
2. Integration Testing: The integration between different components will be tested to verify the seamless interaction
   and data flow.
3. System Testing: The entire OYO Booking System will be tested as a whole to validate its end-to-end functionality,
   performance, and usability.

### Test Types:

1. Functional Testing: Verifying that the OYO Booking System meets the specified functional requirements and performs as
   expected.
2. Usability Testing: Evaluating the user interface, user experience, and ease of use of the booking system.
3. Performance Testing: Assessing the system's performance, responsiveness, and scalability under normal and peak loads.
4. Security Testing: Identifying and addressing potential security vulnerabilities, such as data breaches or
   unauthorized access.
5. Compatibility Testing: Ensuring that the OYO Booking System works correctly on different platforms, browsers, and
   devices.
6. Regression Testing: Repeating select tests to ensure that new changes or updates do not introduce new defects or
   impact existing functionality.
7. User Acceptance Testing (UAT): Conducting tests with real end-users to validate that the system meets their
   requirements and expectations.

### Test Techniques

1. Equivalence Partitioning: Grouping test inputs into classes and selecting representative test cases from each class.
2. Boundary Value Analysis: Testing input values at the boundaries of valid and invalid ranges.
3. Decision Table Testing: Using decision tables to capture combinations of inputs and corresponding actions or
   outcomes.
4. Error Guessing: Applying experience and intuition to identify potential defects or weak areas in the system.
5. Exploratory Testing: Concurrent test design, execution, and learning based on real-time exploration of the system.

### Entry and Exit Criteria

#### Entry Criteria

- Availability of the test environment with all necessary hardware, software, and data.
- Completion of unit testing and component testing.
- Test plan and test cases prepared and reviewed.
- Test data prepared and available.
- Test environment and test tools set up.

#### Exit Criteria:

- Successful completion of all planned test cases.
- Defects are resolved and retested.
- Test coverage objectives are achieved.
- Acceptance criteria defined for each test level are met.
- Test logs, test reports, and other required deliverables are generated.

### Suspension and Resumption Criteria

Testing may be suspended under certain circumstances, such as critical defects,
unavailability of resources, or changes in project priorities. It can be resumed once the issues are resolved,
resources become available, or the project priorities change.

### Test Schedule

The testing activities will be conducted according to the following schedule:

* Test Planning : May 25,2023 – June 1,2023
* Test Design and Preparation: June 2,2023 – June 5,2023
* Test Execution: June 5,2023 – June 9,2023
* Test Reporting and Closure: June 10,2023 – June 12,2023.

### Test Environment/ Ressources:

#### Hardware Requirements:

- Server: 8GB RAM, 2 CPU cores
- Client machines: Minimum 4GB RAM, 1 CPU core

#### Software requirements:

- Operating System: Windows/Linux
- Web Browsers: Chrome, Firefox, Safari
- Test Database: MySQL
- Test Server: Apache Tomcat
- Test Tools: Selenium, JUnit, Postman

### Test Data

- Sample asset data for testing
- User credentials for different access levels

### Personnel

Test Managers, Test Leads, Testers, Developers, Database

### Test Deliverables:

These following activities are included:
<br>: A comprehensive document that outlines the overall testing approach, strategies, scope, schedule,
resources, and responsibilities.<br>
**Test cases**:  Detailed test cases that cover various scenarios, inputs, and expected results for validating the
functionality of the OYO Booking System. These test cases should be well-documented, organized, and easily
understandable.<br>
**Test data**: Relevant and representative test data that includes both valid and invalid inputs to test different
system
functionalities, edge cases, and boundary conditions.<br>
**Test Scripts**: Automation scripts developed using testing frameworks or tools to automate the execution of repetitive
or regression test cases. These scripts help improve efficiency and reliability in testing.<br>
**Test logs**: Detailed records or logs capturing the execution of each test case, including information such as test
case ID, test steps, actual results, expected results, timestamps, and any encountered issues.<br>
**Incident reports**: Reports documenting any defects, issues, or incidents encountered during testing, including their
descriptions, steps to reproduce, severity, priority, status, and resolutions.<br>
**Test summary report**: A comprehensive report summarizing the overall testing activities, results, and observations.
It
includes a summary of test execution, coverage achieved, defects found, and recommendations for improvements .


### Test Execution:

- **Test Procedure**: Follow the defined steps to review test cases, set up the test environment, prepare test data,
  execute test cases, record results, report defects, retest resolved defects, and update test case status.
- **Test Environment Setup**: Prepare servers, install necessary software, configure the network, and deploy the
  application to create a suitable test environment.
- **Test Execution Schedule**: Divide test execution into phases, allocate time for each phase, determine the sequence
  of
  test case execution, and assign resources accordingly.
- **Test Execution Status Reporting**: Provide regular updates on test execution progress, report test case status,
  track
  and report defect status, and measure test coverage achieved.
- **Test Incident Management**: Log and track defects, prioritize them based on severity, collaborate with the
  development team to resolve defects, and retest and close resolved defects.
- **Test Completion Criteria**: Ensure all test cases are executed, defects are resolved and retested, desired test
  coverage is achieved, acceptance criteria are met, and generate comprehensive test logs and reports.

### Test Suspension and Resumption Criteria

#### Test Suspension Criteria:

- Critical defects impacting system functionality or stability.
- Environmental issues or unavailability of required resources.
- Blocking issues that prevent further progress in testing.
- Changes in project priorities or scope.

#### Test Resumption Criteria:

- Critical defects have been resolved and retested.
- Required resources and environment are available.
- Blocking issues have been addressed or circumvented.
- Project priorities and scope have been clarified.

### Test Risks and Contingencies

#### Test Risks:

* Data integrity issues: Risk of incorrect or incomplete data impacting the booking process.
* Integration challenges: Risk of difficulties in integrating the booking system with other systems or third-party
  APIs.
* Performance bottlenecks: Risk of system slowdown or unresponsiveness during peak usage.
* Security vulnerabilities: Risk of potential security breaches or unauthorized access to customer data.
* Compatibility issues: Risk of compatibility problems with different browsers, operating systems, or devices.

#### Contingencies:

* Data validation checks and regular backups to mitigate data integrity risks.
* Thorough integration testing and collaboration with relevant stakeholders to address integration challenges.
* Performance testing to identify and address performance bottlenecks before deployment.
* Implementation of robust security measures such as encryption, secure authentication, and regular security audits.
* Comprehensive compatibility testing across multiple platforms and devices to ensure seamless user experience.
  The above outlines some of the test risks and potential contingencies to mitigate those risks for the OYO Booking
  System. It is essential to assess and address specific risks based on the project's context and requirements.

### Approval

Approval for OYO Booking System involves obtaining approvals at various stages:

* Test Plan Approval: Get stakeholders' approval for the test plan document.
* Test Design Approval: Seek approval for the test design specification.
* Test Execution Approval: Obtain approval to proceed with test execution.
* Defect Resolution Approval: Get approval for resolving reported defects.
* Test Completion Approval: Present the test summary report for final approval.
* Deployment Approval: Seek approval for system deployment to the production environment.
* Maintenance Approval: Obtain approval for ongoing system maintenance. <br>
  The approval process ensures that the OYO Booking System meets quality standards and is ready for use.
  
### Test Design Specification

- **Test Objective**: Define the goal and purpose of the testing effort for the OYO Booking System.
- **Test Items**: Identify the components or modules of the OYO Booking System that will be tested.
- **Test Techniques**: Determine the methods and approaches to be used for testing, such as black-box testing, white-box
  testing, or a combination of techniques.
- **Test Coverage**: Define the scope and extent of testing to ensure comprehensive coverage of the system, including
  functional, non-functional, and integration aspects.
- **Test Environment Requirements**: Specify the hardware, software, and network configuration needed to set up the test
  environment.
- **Test Data Requirements**: Identify the type and source of test data required for executing the test cases
  effectively.
- **Test Cases**: Document the individual test cases, including inputs, expected results, and any preconditions or
  assumptions.
- **Test Procedure**: Define the steps and sequence to be followed for executing the test cases and recording test
  results.

### Test Case Specification:

- **Test Case Identifier**: A unique code assigned to each test case, such as TC001, TC002, etc., for easy
  identification
  and referencing.
- **Test Case Description**: A brief description of the purpose and objective of the test case, such as "Verify user
  registration functionality" or "Validate booking confirmation process."
- **Test Procedure**: Step-by-step instructions on how to execute the test case, including any preconditions or setup
  requirements specific to OYO Booking System. For example, "1. Launch the OYO Booking System application. 2. Navigate
  to the registration page. 3. Enter valid user details. 4. Submit the registration form."
- **Test Inputs**: Specific inputs or data values required to execute the test case. This could include things like
  valid
  or invalid user information, booking details, or system configurations.
  Expected Results: The anticipated outcomes or behaviors that should occur when the test case is executed
  successfully. For instance, "User registration is successful, and a confirmation message is displayed" or "Booking is
  confirmed, and a confirmation email is sent to the user."
- **Test Execution Status**: Indicates the current status of the test case, such as "Not Executed," "Passed," "Failed,"
  or "Blocked," based on the actual execution and observed results.
- **Test Priority**: Priority assigned to the test case to indicate its importance or urgency relative to other test
  cases.
  It helps in prioritizing testing efforts. For example, High, Medium, or Low priority.
- **Test Environment Requirements**: Hardware, software, and network configurations specific to the OYO Booking System
  necessary to execute the test case successfully. This could include details about the required operating system,
  browser versions, or test data.
- **Test Dependencies**: Any specific conditions or prerequisites that need to be satisfied before executing the test
  case.
  This could include the availability of test data, successful completion of a previous test case, or specific system
  configurations. <br>
  Ensuring consistency and facilitating efficient testing for the OYO Booking System.

### Test Procedure Specification

- **Test Procedure Identifier**: A unique identifier or code assigned to each test procedure, such as TP001, TP002,
  etc., for
  easy identification and referencing.
- **Test Procedure Description**: A brief description of the purpose and objective of the test procedure, such as "
  Verify the
  login functionality" or "Test the search and filtering functionality for hotel listings."
- **Test Steps**: Detailed step-by-step instructions outlining the actions to be performed to execute the test
  procedure. Each
  step should be clear, concise, and specific to OYO Booking System. For example,
    1. Launch the OYO Booking System application.
    2. Navigate to the login page.
    3. Enter valid credentials.
    4. Click on the 'Login' button."

- **Test Inputs**: Specific inputs or data values required during the execution of the test procedure. This could
  include
  login credentials, search criteria, or specific user interactions.
- **Expected Results**: The anticipated outcomes or behaviors that should occur when the test procedure is executed
  successfully. This could include successful login, display of search results, or appropriate error messages.
- **Test Execution Status**: Indicates the current status of the test procedure, such as "Not Executed," "Passed," "
  Failed,"
  or "Blocked," based on the actual execution and observed results.
- **Test Environment Requirements**: Hardware, software, and network configurations specific to OYO Booking System
  necessary
  to execute the test procedure successfully. This could include details about the required operating system, browser
  versions, or specific test data.
- **Test Dependencies**: Any specific conditions or prerequisites that need to be satisfied before executing the test
  procedure. This could include the availability of test data, successful completion of a previous test procedure, or
  specific system configurations.

### Test Incident Report:

- **Incident Identifier**: Unique code assigned to each incident for identification.
- **Incident Description**: Brief description of the encountered issue or problem.
- **Test Case Identifier**: Identifier of the test case associated with the incident.
- **Test Procedure Identifier**: Identifier of the test procedure during which the incident occurred.
- **Incident Severity**: Level of impact or seriousness of the incident.
- **Incident Priorit**y: Priority assigned to the incident based on its urgency or importance.
- **Incident Status**: Current status of the incident (Open, In Progress, Closed, etc.).
- **Incident Resolution**: Details of the resolution or solution applied to address the incident.
- **Incident Closure Date**: Date when the incident was officially closed or resolved.

### Test Summary Report

- **Introduction**: Provides an overview of the test summary report for the OYO Booking System.
- **Test Execution Summary**: Summarizes the overall test execution progress, including the number of test cases
  executed,
  passed, failed, and blocked. It gives a high-level view of the testing outcomes.
- **Test Coverage Summary**: Provides a summary of the test coverage achieved during testing, highlighting the areas or
  functionalities that were tested and any gaps in coverage. It assesses the thoroughness of the testing.
- **Defect Summary**: Summarizes the defects or issues discovered during testing, including the total number of defects,
  their severity levels, and their current status. It highlights the quality and stability of the OYO Booking System.
- **Conclusion**: Offers an overall assessment of the testing phase for the OYO Booking System, summarizing the key
  findings, challenges, and achievements. It gives an evaluation of the system's readiness for deployment.
- **Recommendations**: Provides suggestions and recommendations for improving the OYO Booking System based on the
  testing
  experience. It may include recommendations for enhancing test coverage, addressing critical defects, or optimizing
  testing processes.
  