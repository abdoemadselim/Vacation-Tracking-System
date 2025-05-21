# Use Case: Manage Leave Request

## 1. Use Case Name: Manage Leave Request

## 3. Actor: Employee

## 4. Goals
- The employee wants to submit a new leave request.

## 5. Preconditions
- The employee is authenticated and identified as an employee of the company.

## 6. Postconditions
- A new leave request is created and saved
- Notification is sent to the manager

## 7. Main flow
1. The employee begins by entering his / her own credentials to log into the system.
2. The system uses the employee credentials to retrieve all the employee’s leave requests and display them.
3. The employee wants to create a new request. The employee selects a leave type, leave start date, and end date with a visual calender. The employee enters a short title and description so that a manager will have more information with which to approve the request.
4. The employee submits the request.
5. If the submitted information is incomplete or incorrect, relevant errors are shown.
6. The employee has the opportunity to change the information or cancel the request.
7. If passes validation, the employee is returned to the VTS home page, if the employee’s leave request requires manager approval, an e-mail is sent to the manager authorized to approve the employee’s request.
8. The leave request is placed in a pending state.
9. The manager responds to the e-mail by clicking on the link embedded in the e-mail or by explicitly visiting the VTS.
10. The manager enters his / her own credentials to enter the system.
11. The system lists the manager’s own vacation time requests, and also a section listing pending requests by other employees. The manager selects each of them one at a time to approve or reject.
12. The system displays the details of the leave request, and prompts the manager to approve or reject the request. If the request is rejected, the manager is prompted to enter an explanation. Once the manager submits the result, the leave request status changes from pending to approved or rejected.
13. An e-mail notification is sent to the employee who made the request. The manager’s screen returns to the VTS home page.

## 8. Alternate Flow: Cancel Pending Request

## 9. Goals
- The employee wants to cancel a submitted request.

## 10. Preconditions
- The employee is authenticated and identified as an employee of the company.
- The employee has already made a leave request, and has yet to be approved or rejected by an authorized manager.

## 11. Postconditions
- A submitted leave request that's in pending state is cancelled.
- Notification is sent to the manager
- The leave request is removed from the manager's pending requests list

## 12. Flow
1. The employee begins by entering his / her own credentials to log into the system.
2. The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.
3. The employee selects a leave request that’s currently in pending state to cancel and clicks on cancel. The leave request is removed from the manager’s pending requests.
4. An e-mail notification is sent to the manager.

## 13. Alternate Flow: Cancel Approved Request

## 14. Goals
- The employee wants to cancel an approved request

## 15. Preconditions
- The employee is authenticated and identified as an employee of the company.
- The employee has already made a leave request, and it has been approved by an authorized manager.

## 16. Postconditions
- A submitted leave request that's already has been approved is cancelled.
- Notification is sent to the manager.
- The allowance time used to submit the leave request is returned back to the employee.

## 17. Flow
1. The employee begins by entering his / her own credentials retrieve to log into the system.
2. The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.
3. The employee selects a leave request that’s currently in approved state and scheduled for some time in the future to cancel and clicks on cancel. The employee is prompted to enter an explanation and confirms the cancellation. If employee confirms the cancellation, the time allowance is returned back to the employee.
4. An e-mail notification is sent to the manager, and the employees screen returns to the VTS home page.

## 18. Alternate Flow: Edit Pending Request

## 19. Goals
- The employee wants to edit a submitted request that’s currently in pending state

## 20. Preconditions
1. The employee is authenticated and identified as an employee of the company.
2. The employee has already made a leave request, and has yet to be approved or rejected by a manager.

## 21. Postconditions
- A submitted leave request that's in pending state is updated.
- Notification is sent to the manager.
  
## 22. Flow
1. The employee begins by entering his / her own credentials to log into the system.
2. The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.
3. The employee selects a leave request that’s currently in pending state and scheduled for some time in the future and clicks on edit. The system displays an editable view of the request. The employee is allowed to change the title, date range, or leave type.
4. The employee changes request information and submits the changes.
5. An e-mail notification is sent to the manager, and the employees screen returns to the VTS home page.