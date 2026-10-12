# Functional Scope

## In scope
1. **Service Catalog item:** A structured catalog item for network-related requests.
2. **Request types:** Initial choices may include network access, firewall change, and IP configuration.
3. **Request data capture:** Request type, access level, target device/system, business justification, priority, and any request-type-specific details.
4. **Validation:** Mandatory-field validation and conditional visibility of fields based on request type.
5. **Approval routing:** Route requests to the appropriate approver according to the agreed request and risk rules.
6. **Fulfillment task creation:** Create and assign work to the appropriate network fulfillment group after approval.
7. **Lifecycle tracking:** Use clear states such as New, Awaiting Approval, In Progress, and Completed; rejected requests must also be represented.
8. **Notifications:** Notify requesters and relevant approvers/fulfillers at key transitions.
9. **Auditability:** Retain approval decisions, timestamps, comments, and fulfillment work notes.
10. **Reporting:** Provide lists or dashboards for request status, pending approvals, task performance, and SLA compliance.

## Out of scope for the initial prototype
- Direct production firewall/router configuration.
- Unapproved changes to real network infrastructure.
- Integrations requiring credentials or licensed systems not available in the PDI.
- Production deployment without formal security and change approval.

## Proposed request fields
| Field | Purpose | Validation |
|---|---|---|
| Requester | Identify the employee | Required; default to logged-in user where possible |
| Request type | Select network service needed | Required |
| Access level | Specify requested access | Required where relevant |
| Target device/system | Identify the affected resource | Required |
| Business justification | Explain the business need | Required |
| Priority | Support triage | Required; controlled choices |
| Required date | Requested completion date | Optional or policy-driven |
| Status | Track lifecycle | Set and updated by workflow |
| Approval comments | Explain approval decision | Required on rejection; recommended on approval |
| Work notes | Record fulfillment activity | Used by fulfillers |

## Functional acceptance criteria
- Required fields prevent incomplete submission.
- Request type controls relevant fields.
- Submission creates a trackable request.
- Approval decisions update the lifecycle correctly.
- Only approved requests proceed to fulfillment, except explicitly defined exceptions.
- Notifications are triggered at configured lifecycle events.
- Reports accurately reflect request records and task states.
