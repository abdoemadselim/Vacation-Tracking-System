# Pseudocode for Vacation Tracking System

## Approve/Reject Request Function
```
function processRequest:
    pending_leave_request_list = fetchManager'sPendingList()
    FOR index = 1 TO pending_leave_request_list.length
        DISPLAY pending_leave_request_list[index].details
    END FOR
    SET approved_item = GET_APPROVED_ITEM(pending_leave_request_list)
    SET disapproved_item = GET_DISAPPROVED_ITEM(pending_leave_request_list)
    IF approved_item: 
        changeRequestStateToApproved()
        updateEmployeeLeaveBalance()
    ELSE IF disapproved_item: 
        DISPLAY "Enter rejection explanation: "
        READ rejection_explanation
        changeRequestStateToDisapproved()
    @async
    SendAnEmailNotificationToEmployee(rejection_explanation)
```
