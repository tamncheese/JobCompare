V2 - Updated the results and list of test cases
V3 - Updated for final results and list of test cases


# Test Plan

*This is the template for your test plan. The parts in italics are concise explanations of what should go in the corresponding sections and should not appear in the final document.*

**Author**: Team096

## 1 Testing Strategy

### 1.1 Overall strategy

*This section should provide details about your unit-, integration-, system-, and regression-testing strategies. In particular, it should discuss which activities you will perform as part of your testing process, and who will perform such activities.*

1. Unit Tests: Test the individual unit of code for correct functionality and proper error handling. Each developer will create unit tests alongside their application code. All unit tests will be run and are expected to pass with every commit. All unit tests must pass before merging any feature branch to the main branch.
2. Integration Tests: Test the interaction between different application units. These tests will be created by the developer during their code changes and pass before merging any feature branch into the main branch.
3. System Tests: Test the functionality of the system. These tests will be performed manually by the developer before deploying new versions of the application. The list of system tests will be laid out in Section 2: Test Cases.
4. Regression Tests: Manual regression testing will be performed. The developer is expected to add unit tests to cover their changes to the code base and help identify any regressions. In addition, the developer will test their code changes using the deployed application and user interface.

### 1.2 Test Selection

*Here you should discuss how you are going to select your test cases, that is, which black-box and/or white-box techniques you will use. If you plan to use different techniques at different testing levels (e.g., unit and system), you should clarify that.*

1. White-Box Testing will be used for the unit and integration tests. During this testing, we will know the components of the application and specifically test internal code that may not be exposed to the users of our application. (Example: Testing the job score calculation by verifying the actual score matches the expected score given some parameters)
2. Black-Box Testing will be used for the system tests. During this testing, we will examine the overall funcationality of the application from the user's perspective. For example, this could involve our developer manually using the application UI to perform overall application testing. (Example: Add and editing their current job)

### 1.3 Adequacy Criterion

*Define how you are going to assess the quality of your test cases. Typically, this involves some form of functional or structural coverage. If you plan to use different techniques at different testing levels (e.g., unit and system), you should clarify that.*

1. Unit Tests: We will aim for 80% coverage. Stretch goal will be 90%+ coverage.
2. Integration Tests: We will aim to cover all integrated componenets. 
3. System Tests: We will aim to test all potentials path through the application.

### 1.4 Bug Tracking

*Describe how bugs and enhancement requests will be tracked.*

1. For Bug Tracking, our team will be using Github issues. When an issue or enhancement is identified, a team member will open Github issues and provide all relevant information. 
2. Once the bug is resolved and merged to the main branch, the Github issue will be closed and marked as complete with notes.
3. In addition, specific unit and integration tests should be added to prevent this bug in the future.

### 1.5 Technology

*Describe any testing technology you intend to use or build (e.g., JUnit, Selenium).*

1. JUnit: For unit and integration tests
2. Selenium: Our team plans to execute manually with the stretch goal of using Selenium for integration testing if time permits.

## 2 Test Cases

*This section should be the core of this document. You should provide a table of test cases, one per row. For each test case, the table should provide its purpose, the steps necessary to perform the test, the expected result, the actual result (to be filled later), pass/fail information (to be filled later), and any additional information you think is relevant.*

| Purpose | Steps | Expected Result | Actual Result | Pass/Fail Information |
|---------|-------|-----------------|---------------|-----------------------|
| Unit: Validate getter and setter methods in Job class | Run the JUnit test suite | When a Job class attribute value is set, the getter should return that value | As expected | PASS |
| Unit: Validate all classes | Run the Junit Test suite | When ComparisonSettings class attribute value is set, the getter should return that value | As expected | PASS |
| Unit: Validate calculations (Adjusted Salary/Bonus, Job Score) | Run the Junit Test suite | Value calculated doing math by hand | As expected | PASS |
| System: Add current job | From the UI, navigate and add a job | Current job is saved, details are correct | Able to navigate to screen, add Job details, then save and see Job in Job list. | PASS |
| System: Add a job offer | From the UI, navigate and add a job offer | Job offer is saved, details are correct | Able to navigate to screen, add Job details, then save and see Job Offer in Job list. | PASS |
| System: Comparison Settings Defaults | From the UI, navigate to Settings Screen and check defaults | Defaults are already set when going to screen | All defaults are set to 5. | PASS |
| System: Job details validations | From the UI, navigate and try to enter invalid leave amount | Error is shown on screen | Leave outside 0-30 forces an error on the screen | PASS |
| System: Required field validations | From the UI, navigate and try to leave job fields blank | Error is shown on screen | Blank fields force an error to be shown | PASS |
| System: Edit Job Comparision Settings | From the UI, navigare and edit job comparison settings | Job comparison settings are changed | Natigated to screen and updated Settings | PASS |
| System: Compare two job offers | From the UI, navigate and compare two jobs offers. | Two job offers are shown in comparison screen with correct details | Navigated to screen, selected two jobs, and compared the details | PASS |
| System: Compare job offer with current job | From the UI, add a job offer and then compare with current job. | Job comparison screen is shown with the correct details about the entered job offer and current job | After adding job offer, I am able to compare that with my current job | PASS |
| System: Job offers are disabled if none are entered | From the UI, have no jobs offers and check if compare job offers is disabled | Compare job offers is disabled | After freshly starting the app, job offers should be disabled | On fresh startup, job offers are disabled |  
