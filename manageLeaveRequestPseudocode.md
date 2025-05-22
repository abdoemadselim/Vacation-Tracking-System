# Pseudocode for Vacation Tracking System

## Submit Request Function
```
function submitRequest:
    isValid = false;
    while !isValid:
        DISPLAY "Enter title: "
        DISPLAY "Enter description: "
        DISPLAY "Enter date range: "
        DISPLAY "Enter leave type: "
        READ title, description, dateRange, leaveType
        isValid, validationErrors = validateData(title, description, dateRange, leaveType)
        leaveRequest = {title, description, dateRange, leaveType}
        displayValidationErrors(validationErrors)
    createdLeaveRequest = createNewLeaveRequestInDatabase(leaveRequest)
    updateEmployeeLeaveBalance()
    addLeaveRequestToManager'sList(createdLeaveRequest)
    SendAnEmailNotificationToManager()
```

## Cancel Approved Request Function
```
function cancelApprovedRequest:
    fetchEmployee'sLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    cancelRequest(selected_request)
    updateEmployeeLeaveBalance()
    removeLeaveRequestFromManager'sList(selected_request)
    SendAnEmailNotificationToManager()
```

## Edit Request Function
```
function editRequest:
    fetchEmployee'sLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    displayEditableMode()
    isValid = false;  
    while !isValid:
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
    SendAnEmailNotificationToManager()
```

## Cancel Pending Request Function
```
function cancelPendingRequest:
    fetchEmployee'sLeaveRequests()
    FOR index = 1 TO leave_request_list.length
        DISPLAY leave_request_list[index].details
    END FOR
    SET selected_request = GET_CLICKED_ITEM(leave_request_list)
    cancelRequest(selected_request)
    updateEmployeeLeaveBalance()
    removeLeaveRequestFromManager'sList(leaveRequest)
    SendAnEmailNotificationToManager()
```