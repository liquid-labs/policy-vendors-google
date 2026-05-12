# Google Workspace User Management

## Purpose and scope

This document describes the standard procedures for managing Google Workspace user accounts for {{ .company.name }}. It is written for administrators and managers in small organizations (roughly <50 staff) and focuses on business and security outcomes (when/why to take actions), while linking to Google documentation for step-by-step console navigation.

This guidance applies to employee and contractor accounts in the Google Admin console ({{ .google.admin.console.url }}).

## Procedures

### Create a Google Workspace user

Use this procedure when onboarding a new staff member who needs access to Google Workspace services (Gmail, Drive, Calendar, Chat, etc.).

1. Confirm onboarding prerequisites:
   - The hire is approved and a start date is confirmed.
   - The staff member’s manager is identified.
   - Required access level is defined (groups, shared drives, admin roles, and any app access restrictions).
2. Create the user in the Google Admin console:
   - Navigate to Users → Add new user.
   - Use the standard naming convention and primary email address (for example: `first.last@{{ .company.domain }}`).
   - Generate a temporary password and require a password change at first sign-in.
3. Apply baseline access and controls:
   - Add the user to standard groups (for example: `all@{{ .company.domain }}`) and role-based groups as needed.
   - Assign shared drive membership (and roles) based on least privilege.
   - Enforce 2-step verification according to {{ .policy.security.standards.SECURITY_STANDARDS_URL }}.
4. Confirm recovery and support setup:
   - Ensure the user has appropriate recovery options set per policy (recovery email/phone if allowed).
   - Provide the user with support contact details (for example: `itsupport@{{ .company.domain }}`).
5. Record the change:
   - Update the staff onboarding tracker / ticketing system with the account email, groups granted, and the date/time of creation.

References (Google):
- Admin help: Add users (placeholder): {{ .google.admin.add_users.url }}

### Transfer Google Workspace user data

Use this procedure when a staff member is changing roles, leaving the organization, or when their manager needs continued access to business records. Transfer should be completed **before** deleting the user.

1. Confirm the transition requirements:
   - Identify the recipient account (typically the staff member’s manager or a role account like `team@{{ .company.domain }}`).
   - Decide which data needs to be retained (Drive, Calendar, Groups, shared drive access, key email threads).
2. Secure the account to prevent further changes during transfer:
   - Suspend the user account.
   - Revoke active sessions and application passwords (where applicable).
3. Transfer Drive and Calendar data using Admin tools:
   - Use the Admin console “Data transfer” tool (or equivalent) to transfer Drive ownership (My Drive files) and Calendar events to the recipient.
   - Validate that key folders/files now show the recipient as owner.
4. Handle shared drives:
   - Ensure the user’s shared drive memberships are removed or replaced appropriately.
   - Confirm the intended owners/managers retain access.
5. Preserve or provide access to Gmail:
   - Preferred: retain mail via a compliant archive method (for example Google Vault retention/export) per {{ .policy.security.standards.RECORDS_RETENTION_URL }}.
   - If operational access is needed, configure mailbox delegation or routing/forwarding according to policy and legal requirements.
6. Record the transfer:
   - Document what was transferred, to whom, and when (include links to tickets and any exports performed).

References (Google):
- Admin help: Transfer data between users (placeholder): {{ .google.admin.data_transfer.url }}
- Vault: retention and exports (placeholder): {{ .google.vault.retention.url }}

### Delete a Google Workspace user

Delete a user only when the account is no longer needed and data retention and transfer requirements have been met.

Before deleting, complete: [Transfer Google Workspace user data](#transfer-google-workspace-user-data).

1. Confirm deletion is appropriate:
   - Employment/contract termination is finalized and approved by HR/management.
   - Access is no longer required for ongoing work.
   - Legal/records retention requirements are satisfied (Vault retention or exports completed as required).
2. Perform pre-delete safeguards:
   - Ensure the account is suspended (if not already).
   - Confirm Drive/Calendar transfers are complete and validated.
   - Remove the user from groups and shared drives (or replace memberships with the successor).
3. Delete the user in the Admin console:
   - Navigate to Users → select the user → Delete user.
   - Follow prompts regarding data handling (ensure transfer/retention choices match the steps above).
4. Post-delete checks:
   - Verify the account no longer appears in active users.
   - Verify critical shared resources and ownerships are still accessible by the intended recipients.
5. Record the change:
   - Update the termination/offboarding ticket with deletion date/time and who approved the deletion.

References (Google):
- Admin help: Delete a user (placeholder): {{ .google.admin.delete_user.url }}

