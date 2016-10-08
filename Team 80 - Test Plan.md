
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

Test case     | Purpose of the test case | Steps necessary to perform the test | Expected result | Actual Result | Pass/Fail
------------- | -------------------------- -----------------------------------   ----------------  -------------  ---------- 
Add item to a list  | To ensure the system functions as it should, allows the user to add items to list | When within a list's page, tester clicks on add item |New item is displayed on the list
Delete item from list  | To ensure the system functions as it should, allows the user to delete items from a list | From the list page, tester clicks on item, then clicks delete | The item should no longer appear on the list

Test case
Purpose of the test casem 
Steps necessary to perform the test
Expected result
Actual Result
Pass/Fail
Add item to a list
To ensure the system functions as it should, allows the user to add items to list
Tester clicks on add item
New item is displayed on the list


Delete item from list
To ensure the system functions as it should, allows the user to delete items from a list
Tester clicks on item, then clicks delete
The item should no longer appear on the list


Edit item quantity value
To ensure the system functions as it should, allows the user to edit an item's current quantity
Tester clicks on item's quantity
An editbox is loaded allowing the user to type a value. If the value is acceptable, item's quantity is changed to that just entered


Set item quantity value to zero
Ensures an item's quantity value is greater than zero
Tester clicks on item's quantity value, user types a zero in that editbox
The quantity value should be rejected and this message displayed “quantity should be greater than zero”. The previous quantity value should be maintained


Set item quantity value to less than zero
Ensures an item's quantity value is greater than zero
Tester clicks on item's quantity value, user types a negative value e.g. -1 in that editbox
The quantity value should be rejected and this message displayed “quantity should be greater than zero”. The previous quantity value should be maintained


Add item by name, existing name
Ensures a name match is tested when adding item to list by name
Tester clicks add item, types the item name, clicks search
A list of items with that name are returned alongside their type


Add item by name, non-existing name
Ensures a name match is tested when adding item to list by name
Tester clicks add item, types the item name, clicks search
The system displays a message “No matches were found. Please choose the item's type from the list below” and a list with existing item type is shown. Tester clicks on item type and the item is saved in the DB. A subsequent search by this name should return a match (see testcase 'Add item by name, existing name' above”


List saved immediately after modification, set item quantity
Ensures the system functions as it should, saves lists on modification
Tester clicks on an item's quantity on the list, tester enters a new value
If the value is less than or equal to zero, immediately a “unvalid quantity value” message is displayed. If the value is greater than zero, a flash message “item quantity updated” is shown and when tester exists this page back to the list, they see the new quantity value of that item


List saved immediately after modification, rename list
Ensures the system functions as it should, saves lists on modification
Tester clicks on a list's name, and types a new name
If the name value is empty, immediately a “unvalid name value” message is displayed. If the value is a valid name, a flash message “list name updated” is shown and when tester exists this page back to the main page and views all lists, they see the new name has updated.


Check off item
Ensures the system functions as it should, allows users to check items off a list
Tester clicks on item on the list, tester chooses the check-off option
A strike-through on the item is shown on the list.


Clear check-off, no  checked items
Ensures no changes are made when clear check-off is called in a list with no checked items
Tester clicks on clear checkoff on a list
The list stays the same, a message saying that there are no checked items is displayed


Clear check-off, one checked item
Ensures the strike through on an item is removed when clear check-off is called in a list where only 1 item is checked
Tester clicks on clear checkoff on a list
The strike-through on the item on the list is removed, a message indicating that the checked item has been cleared is displayed


Clear check-off, more than one checked item
Ensures the strike through on all items is removed when clear check-off is called in a list where more than 1 item is checked
Tester clicks on clear checkoff on a list
The strike-through on the items on the list are removed, a message indicating that the checked items have been cleared is displayed


Group items by type
Ensures the system functions as it should, enables user to group items by type
Tester clicks on 'group-by type' on the list
All items in the list as displayed in groups of their type


List existing lists
Ensures that the user can view all their lists in one place. Is a per-requisite for testcases such as “select list”
Tester, on the mainpage, clicks view, then chooses all lists
All existing lists are displayed


Create a list, provide a name as empty spaces
Ensures the system functions as it should, enables user to create a list only if the name provided is not empty spaces
Tester, on the mainpage, clicks new, then chooses list
The system prompts the tester to type the name of the new list and the tester types an empty space. The system should immediately display an 'invalid name' message telling the tester what values they can use in the list name. When tester goes on the mainpage, only the previously existing lists are displayed as their attempt to create a new one had failed.


Create a list, provide an existing name
Ensures the system functions as it should, enables user to create a list only if there is no existing list with such a name
Tester, on the mainpage, clicks new, then chooses list
The system prompts the tester to type the name of the new list and the tester types a name of an existing list.  The system should immediately display an 'invalid name' message telling the tester that the name they have chosen exists and they should choose a different one. When tester goes on the mainpage, only the previously existing lists are displayed as their attempt to create a new one had failed.


Create a list, provide a valid name (non-existing, non-empty)
Ensures the system functions as it should, enables user to create a list only if it has a valid name
Tester, on the mainpage, clicks new, then chooses list
The system prompts the tester to type the name of the new list and saves it. When tester goes on the mainpage, the newly created list is displayed


Rename list
Ensures the system functions as it should, enables the user to rename an existing list
Tester goes to the main page, clicks 'view' then chooses 'all lists', and on the displayed lists clicks on the desired list, on the name label
The system opens up an EditBox allowing the tester to type a new name value. If the name is valid (see testcases “Create a list, provide a name as empty spaces”, “Create a list, provide an existing name” and “Create a list, provide a valid name (non-existing, non-empty)” above), the list is renamed and new list name displayed on the mainpage → view→ all lists.


Select list
Ensures the system functions as it should, enables the user to select a list
Tester goes to the main page, clicks 'view', on the menu that appears they click 'all lists', and when the lists are shown, they click on a list to select it
The system should open the list showing items in it, it's properties and giving the user a chance to make edits such as editing item quantities or renaming the list


Delete list
Ensures the system functions as it should, enables the user to delete a list
Tester goes to the main page, clicks 'view', on the menu that appears they click 'all lists', and when the lists are shown, they click on a list to select it and on the operations menu, clicks 'delete'
The system provides a confirmation of deletion to the user e.g. “Do you want to delete this list? Yes, No”. If the tester chooses Yes, the list is deleted and is no longer available on the mainpage→view→all lists page.
If the user selects No, the operation is canceled and the list is shown on the mainpage→view→ all lists page









