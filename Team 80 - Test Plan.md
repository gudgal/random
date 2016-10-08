
**Author**: \<Purity Mugambi or team 80\>

## 1 Testing Strategy

### 1.1 Overall strategy

We plan to conduct unit tests (for the different modules in the system), integration tests (to evaluate how well the modules have been integrated), system tests and regression tests. In system tests, we will conduct both functional and non-functional test. Examples of planned tests in these categories include:

1. Unit tests:
We will test the add, delete, rename functions applied to a list
2. Integration tests:
We will test how well item and list modules integrate. Further, we will test the backend and frontend integrations especially in cases where the backend may expose APIs for use by the frontend.
3. System tests:
	1. functional tests
	We will test that all the requirements described by Brad and Janet are achieved in the system.
	2. non-functional tests:
	We will test load balancing, response times (especially from the DB and backend calls).
4. Regression tests:
This is planned to be agile. As the modules are built, unit tests will be conducted, and when integrated integration tests will be conducted. Thus when new integrations happen, regression tests will be run too to ensure previously working components have not been ruined by newly added parts.

We plan to run the tests continually, each time growing the system until the full functionality is achieved. The unit tests will be conducted by members in the team that did not write the module in test – i.e each person will write their module but someone else will test it. The integration tests will be conducted in smaller bits so that people whose modules are getting integrated are not involved in testing. We are working to finalize on the roles of the team in all levels of testing.

### 1.2 Test Selection
We plan to conduct black box testing and white box testing. In black box testing, we will use the category-partition method because it is easy to understand and implement and also, it aligns well with the problem. In white box testing we will use Modified Condition/Decision Coverage (MC/DC). It allows us to test combination of conditions which seem most important in this assignment for instance, we want to checkoff and not delete an item, clear all checked-off items at one go. This means that the user can play around a lot and it is important that an action does not undo the previous one.

### 1.3 Adequacy Criterion
We will write test specifications for the functions in the system. We will write test specifications for every functional requirement in the system. For instance, we will put constraints on the input values to evaluate if the system responds as expected base don these constraints.

### 1.4 Bug Tracking

We plan to maintain a log of bugs and actions against them. A GIST structure in Github could be used for this. Bugs are reported and the status updated whenever one acts on them.

### 1.5 Technology
We plan to use Junit. The NestedRunner in Junit will provide for integration testing.


## 2 Test Cases

| Test case             | Purpose of the test case                                                                 | Steps necessary to perform the test                               | Expected result                              | Actual Result | Pass/Fail |
|-----------------------|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------|---------------|-----------|
| Add item to a list    | To ensure the system functions as it should, allows the user to add items to list        | While on a list's page, tester clicks on add item                 | New item is displayed on the list            |               |           |
| Delete item from list | To ensure the system functions as it should, allows the user to delete items from a list | While on a list's page, tester clicks on item, then clicks delete | The item should no longer appear on the list |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
|                       |                                                                                          |                                                                   |                                              |               |           |
