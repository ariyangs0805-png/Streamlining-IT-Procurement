# Phase 3: Project Design Phase

**Team ID:** SWTID-2026-4746  
**Project Title:** Streamlining IT Procurement: Automating Standard Laptop Orders with Flow Designer  
**Phase:** Phase 3 - Project Design Phase  
**Team Members:** Syed Mahmoodh J S (Team Leader & GitHub Repository Owner), Shaheen A, Mohammed Arshad M, Shenil X, Jenish R

## Workflow Architecture
1. **Initiation:** The end-user navigates to the Service Catalog and selects the "Standard Laptop" item.
2. **Submission:** The user fills out the required variables and submits the request, generating a Request (REQ) and Requested Item (RITM) record.
3. **Trigger:** ServiceNow Flow Designer listens for the Service Catalog trigger tied to the specific Standard Laptop item.
4. **Approval Logic:** The flow requests authorization from the designated approver.
5. **Execution:** Upon approval, the Flow Logic executes a "Create Catalog Task" action.
6. **Fulfillment:** A Catalog Task (SCTASK) is automatically generated with the short description "Laptop need to Configured" and routed directly to the "Hardware" assignment group.

## System Flowchart

```mermaid
graph TD
    A[End-User: Selects 'Standard Laptop' in Service Catalog] --> B[Submission: Generates REQ and RITM]
    B --> C[Flow Designer Triggered]
    C --> D[Approval Logic: Manager Authorization]
    D -->|Approved| E[Action: Create Catalog Task]
    E --> F[Fulfillment: SCTASK routed to Hardware Group]
