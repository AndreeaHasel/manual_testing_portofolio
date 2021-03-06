<h>Final project for ITF Manual Testing Course</h>


The scope of the final project for ITF Manual Testing Course is to use all gained knowledge throught the course and apply them in practice, using a live application.

Application under test: https://opensource-demo.orangehrmlive.com/

API Documentation: https://orangehrm.github.io/orangehrm-api-doc/

The final project will be split into 2 sections: Testing section and SQL section.

Tools used: JIRA, Zephyr Squad, Postman, MySQL Workbench.

<h1>Functional specifications</h1>

The below Story was created in JIRA and describes the functional specifications of the Dependants module, for which the final project is performed upon.

![image](https://user-images.githubusercontent.com/105125357/172057936-8e09df9e-56f0-467b-a8a9-f5c347e4d698.png)

<h1>1 Testing section</h1>

<h2>1.1 Test Planning</h2>

The Test Plan is designed to describe all details of testing for the Dependants module from the OrangeHRM application.

The plan identifies the items to be tested, the features to be tested, the types of testing to be performed, the personnel responsible for testing, the resources and schedule required to complete testing, and the risks associated with the plan

<h3>1.1.1 Roles assigned to the project and persons allocated</h3>

<ul>
<li>Project manager - Andrei Popescu</li><br>
<li>Product owner - Madalina Ionescu</li><br>
<li>Software developer - Gabriela Tomescu</li><br>
<li>QA Engineer - Iulia Albu</li><br>
</ul>


<h3>1.1.2 Entry criteria defined</h3>
<ul>
<li>functional specifications are defined</li><br>
<li>roles needed for the project are allocated</li><br>
<li>initial project risks were detected and mitigated</li><br>
</ul>
<h3>1.1.3 Exit criteria defined</h3>
<ul>
	<li>number of unresolved bugs is insignificant or they have low priority</li><br>
<li>all tests have been executed</li><br>
<li>all resolved bugs have been re-tested and approved by the QA team</li><br>
<li>deadline was reached</li><br>
<li>no detected major risk remained un-mitigated</li><br>
<li>exploratory regression testing must be performed on the PIM module, which includes the Add employee section</li><br>
</ul>	
<h3>1.1.4 Test scope</h3>
<b>Tests in scope:</b> All the feature of Add employee module which were defined in software requirement specs need to be tested: functional testing, GUI testing and API testing<br>
<b>Tests not in scope:</b> performance testing, integrations of the dependents module with other modules, compatibility testing with multiple browsers
<h3>1.1.5 Risks detected</h3>
<b>Project risks:</b> lack of experience of the QA team, short deadline of Zephyr Squad trial, unavailability of test environment<br>
<b>Product risks:</b> validation constraints on the fields might be too restrictive to the end-user
<h3>1.1.6 Evaluating entry criteria</h3>
The entry criterias defined in the Test Planning phase have been achieved and the test process can continue.

<h2>1.2 Test Monitoring and Control</h2>
Various periodic reports were generated to reflect the current status of the testing process, in case of major problems control measures could be taken. The following status report was generated after 40% of the test cases were executed, on 1st of April 2022:

<h2>1.3 Test Analysis</h2>
The testing process will be executed based on the above requirements for the Dependents module. The following test conditions were found:
<ul>
	<li>checking that if the mandatory fields are not completed, the employee cannot be added</li><br>
	<li>check that the API GET request for the get employees request is working</li><br>
	<li>checking that the employee cannot be added if the picture doesn't respect the required dimension and format</li><br>
	<li>check that the form can be submitted when we fill in all the mandatory information</li><br>
<li>checking that admin can save the employee when the uploaded picture respects the upload criteria</li><br>
	<li>check that the employee can be added when the password respects the criteria</li><br>
<li>check that the employee cannot be added if the password doesn't respect the security criteria</li><br>
	</ul>
	
<h2>1.4 Test Design</h2>
Functional test cases were created in Zephyr Squad. Based on the analysis of the specifications, the test design techniques used for generating test cases are boundary value analysis, equivalence partitioning and use case testing.
The test cases with steps can be viewed here: Add employee_test_cases.pdf

For the Add employee API, the following checklist was generated: API_test_checklist.csv

1.5 Test Implementation
The following elements are needed to be ready before the test execution phase begins:

Testing environment is up and running: https://opensource-demo.orangehrmlive.com/
Access to the testing environment is given: Username : Admin | Password : admin123
Cycle summary was created
Test cases were added to the cycle summary
Postman collection with the dependents API methods was created
Authorization token was created for accessing the API
1.6 Test Execution
Test cases are executed on the created test Cycle summary: Dependents_cycle_summary_execution.pdf
Bugs have been created based on the failed tests. The complete bug reports can be found here: Dependents_created_bugs.pdf
Date format is not dd/mm/yyyy
Future "Date of Birth" can be selected from calendar
Only 50 characters are allowed for "Please Specify" field
Only 50 characters are allowed for "Name" field
Relationship "parent" is missing
API tests are executed based on the checklist. The collection used can be found here: JSON file with the collection of requests created for the Dependents API
Full regression testing is needed after the bugs are fixed
1.7 Test Completion
As the Exit criteria were met and satisfied as mentioned in the appropriate section, this feature is suggested to ???Go Live??? by the Testing team
The traceability matrix was generated and can be found here: Traceability_matrix.csv
Test execution chart was generated, the final report shows that a number 5 tests have failed of a total of 23
A number of 23 test cases were planned for execution and all of them were executed
A number of 5 total bugs were found, from which the priority is: 1 is high, 4 are medium and 1 is low

<h1>2 SQL section</h1>
Created a database named 'orangehrm' and a table named 'dependents' with all the columns needed to save data per specifications. Performed different queries inside the sql file: dependents.sql
