### Bug Report: Data Validation Failure During Account Merger Process

#### Description
An HTTP 400 validation exception occurs when trying to unify/merge duplicate customer profiles into a single primary account. Although the user interface permits selecting the conflicting records, triggering the final consolidation sequence causes the server layer to block the transaction due to an unhandled backend validation constraint.

#### Environment
* **Platform:** Enterprise Customer Relationship Management (CRM) System
* **Context:** Customer Profile Module -> Record Deduplication / Merge Workspace

#### Error Message
```text
400 A validation error occurred.[SYSTEM_VALIDATION_ERROR_ID]
```

#### Steps to Reproduce
1. Navigate to the Account Deduplication interface.
2. Search for and select two duplicate customer accounts intended for consolidation.
3. Review the selected records and proceed with the merge action.
4. Observe the operation fail with an instantaneous server validation error box.

#### Expected Behavior
The system should correctly combine the two customer accounts into a single record, applying standard rules to resolve any conflicting data and preserving the full customer history under one account.

#### Actual Behavior
The backend rejection parameters trip an HTTP 400 fault. The merger process is completely aborted, and both customer files remain separate and un-unified in the system database.

