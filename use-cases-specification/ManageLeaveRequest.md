# Use Case: Manage Leave Request

### Actor
| Actor     |
|-----------|
| Employee  |

### Goals
| Goals                                                                 |
|------------------------------------------------------------------------|
| - The employee wants to submit a new leave request.                    |

### Preconditions
| Preconditions                                                                 |
|--------------------------------------------------------------------------------|
| - The employee is authenticated and identified as an employee of the company. |

### Postconditions
| Postconditions                                                              |
|------------------------------------------------------------------------------|
| - A new leave request is created and saved                                  |
| - A notification is sent to the manager                                       |

### Main Flow
| Step | Description                                                                                                                                                   |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | The system uses the employee credentials to retrieve all the employee’s leave requests and display them.                                                     |
| 2    | The employee wants to create a new request. The employee selects a leave type, leave start date, and end date with a visual calendar.                        |
| 3    | The employee enters a short title and description so that a manager will have more information with which to approve the request.                            |
| 4    | The employee submits the request.                                                                                                                             |
| 5    | If the submitted information is incomplete or incorrect, relevant errors are shown.                                                                          |
| 6    | The employee has the opportunity to change the information or cancel the request.                                                                            |
| 7    | If passes validation, an email is sent to manager, and the employee is returned to the VTS home page. If the employee’s leave request requires manager approval, it's added to the manager's pending list  |
| 8    | The leave request is placed in a pending state.                                                                                                               |
| 9    | The manager responds to the e-mail by clicking on the link embedded in the e-mail or by explicitly visiting the VTS.                                         |
| 10   | The manager enters his / her own credentials to enter the system.                                                                                             |
| 11   | The system lists the manager’s own vacation time requests and a section listing pending requests by other employees.                                         |
| 12   | The manager selects each of them one at a time to approve or reject.                                                                                          |
| 13   | The system displays the details of the leave request, and prompts the manager to approve or reject the request. If rejected, an explanation is required.     |
| 14   | Once the manager submits the result, the leave request status changes from pending to approved or rejected.                                                   |
| 15   | An e-mail notification is sent to the employee who made the request. The manager’s screen returns to the VTS home page.                                      |

---

## Alternate Flow: Withdraw Pending Request

### Goals
| Goals                                      |
|-------------------------------------------|
| - The employee wants to withdraw a submitted pending request. |

### Preconditions
| Preconditions                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------|
| - The employee is authenticated and identified as an employee of the company.                                                |
| - The employee has already made a leave request, and has yet to be approved or rejected by an authorized manager.            |

### Postconditions
| Postconditions                                                                                      |
|------------------------------------------------------------------------------------------------------|
| - A submitted leave request that's in a pending state is withdrawn.                                   |
| - A notification is sent to the manager                                                               |
| - The leave request is removed from the manager's pending requests list                             |

### Flow
| Step | Description                                                                                                                    |
|------|--------------------------------------------------------------------------------------------------------------------------------|
| 1    | The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.                     |
| 2    | The employee selects a leave request that’s currently in pending state to cancel and clicks on cancel.                        |
| 3    | The leave request is removed from the manager’s pending requests.                                                              |
| 4    | An e-mail notification is sent to the manager.                                                                                 |

---

## Alternate Flow: Cancel Approved Request

### Goals
| Goals                                   |
|----------------------------------------|
| - The employee wants to cancel an approved request |

### Preconditions
| Preconditions                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------|
| - The employee is authenticated and identified as an employee of the company.                                        |
| - The employee has already made a leave request, and it has been approved by an authorized manager.                 |

### Postconditions
| Postconditions                                                                                  |
|--------------------------------------------------------------------------------------------------|
| - A submitted leave request that's already has been approved is cancelled.                      |
| - A notification is sent to the manager.                                                          |
| - The allowance time used to submit the leave request is returned back to the employee.         |

### Flow
| Step | Description                                                                                                                                              |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.                                               |
| 2    | The employee selects a leave request that’s currently in approved state and scheduled for the future to cancel and clicks on cancel.                    |
| 3    | The employee is prompted to enter an explanation and confirms the cancellation. If confirmed, the time allowance is returned back to the employee.      |
| 4    | An e-mail notification is sent to the manager, and the employee’s screen returns to the VTS home page.                                                  |

---

## Alternate Flow: Edit Pending Request

### Goals
| Goals                                                               |
|----------------------------------------------------------------------|
| - The employee wants to edit a submitted request that’s in pending state |

### Preconditions
| Preconditions                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------|
| - The employee is authenticated and identified as an employee of the company.                                                |
| - The employee has already made a leave request, and has yet to be approved or rejected by a manager.                        |

### Postconditions
| Postconditions                                                                                      |
|------------------------------------------------------------------------------------------------------|
| - A submitted leave request that's in pending state is updated.                                     |
| - A notification is sent to the manager.                                                              |

### Flow
| Step | Description                                                                                                                                         |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | The systems uses the employee credentials to retrieve all the employee’s leave requests and display them.                                          |
| 2    | The employee selects a leave request that’s currently in pending state and scheduled for the future and clicks on edit.                           |
| 3    | The system displays an editable view of the request. The employee is allowed to change the title, description, date range, or leave type.                       |
| 4    | The employee changes request information and submits the changes.                                                                                  |
| 5    | An e-mail notification is sent to the manager, and the employee’s screen returns to the VTS home page.                                             |
