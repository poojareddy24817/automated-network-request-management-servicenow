# Automated Network Request Management in ServiceNow

## Overview
This project demonstrates an end-to-end workflow for network-related service requests using ServiceNow: catalog submission, validation, approvals, fulfillment tasks, notifications, status tracking, and reporting.

## Objectives
- Reduce manual handling and incomplete submissions.
- Standardize approval and fulfillment workflows.
- Improve visibility into request status and SLA performance.
- Maintain traceable approval and work history.
- Provide reports for administrators and IT teams.

## Scope
The solution is planned for a ServiceNow Personal Developer Instance. Network changes will be represented by request and fulfillment records unless suitable, authorized infrastructure integrations are configured.

## Planned lifecycle
1. Requester submits a network request through the Service Catalog.
2. ServiceNow validates required data and creates a trackable request.
3. The request is routed for approval based on configured rules.
4. Approved requests generate fulfillment tasks for the network team.
5. The team updates work notes and completes the task.
6. Status notifications and reports support tracking and auditability.

## Documentation
- [Business Objectives](docs/business-objectives.md)
- [Functional Scope](docs/functional-scope.md)
- [Stakeholder Mapping](docs/stakeholder-mapping.md)
- [Execution Roadmap](docs/execution-roadmap.md)

## Status
Phase 1 — Requirement Analysis & Planning: documentation prepared; implementation and SkillWallet story completion should be confirmed as each deliverable is reviewed.
