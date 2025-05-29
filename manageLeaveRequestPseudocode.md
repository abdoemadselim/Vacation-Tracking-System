# Pseudocode for Vacation Tracking System

## Submit Request Function
```
function submitRequest:
    isValid = false;
    employeeLeaveBalance = fetchEmployeeLeaveBalanceFromHRSystem();
    WHILE !isValid OR employeeLeaveBalance < selectedBalance:
        DISPLAY "Enter title: "
        DISPLAY "Enter description: "
        DISPLAY "Enter date range: "
        DISPLAY "Enter leave type: "
        READ title, description, dateRange, leaveType
        isValid, validationErrors = validateData(title, description, dateRange, leaveType)
        leaveRequest = {title, description, dateRange, leaveType}
        displayValidationErrors(validationErrors)
    createdLeaveRequest = createNewLeaveRequestInDatabase(leaveRequest)
    IF needsManager'sApproval:
        addLeaveRequestToManager'sPendingList(createdLeaveRequest)
        @async
        SendAnEmailNotificationToManager()
    ELSE
        approveRequestAutomatically()
        updateEmployeeLeaveBalance()
```

## Edit Request Function
```
function editRequest:
    leave_request_list = fetchEmployee'sLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    displayEditableMode()
    isValid = false;  
    WHILE !isValid:
        DISPLAY "Enter title: "
        DISPLAY "Enter description: "
        DISPLAY "Enter date range: "
        DISPLAY "Enter leave type: "
        READ title, description, dateRange, leaveType
        isValid, validationErrors = validateData(title, description, dateRange, leaveType)
        leaveRequest = {title, description, dateRange, leaveType}
        displayValidationErrors(validationErrors)
    leaveRequest = updateLeaveRequestInDatabase(leaveRequest)
    updateEmployeeLeaveBalance()
    @async
    SendAnEmailNotificationToManager()
```

## Cancel Approved Request Function
```
function cancelApprovedRequest:
    leave_request_list = fetchEmployee'sLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    IF request in previous 5BD: 
        DISPLAY "Enter short explanation: "
        READ cancellation_explanation
    cancelRequest(selected_request, cancellation_explanation)
    updateEmployeeLeaveBalance()
    @async
    SendAnEmailNotificationToManager()
```

## Withdraw Pending Request Function
```
function withdrawPendingRequest:
    leave_request_list = fetchEmployee'sActiveLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    withdrawRequest(selected_request)
    removeLeaveRequestFromManager'sPendingList(leaveRequest)
    @async
    SendAnEmailNotificationToManager()
```