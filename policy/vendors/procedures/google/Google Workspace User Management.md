# Google Workspace User Management

## Purpose and scope

This procedure describes the baseline business process for creating, transferring, and deleting Google Workspace user accounts. It is intended for administrators who manage company Google Workspace access for staff, contractors, and service accounts.

Use these procedures together with the staff onboarding, role change, and termination processes. Google Workspace account changes should not be treated as a purely technical task. Before changing a user account, confirm that the business approval, role assignment, data ownership, security, and recordkeeping requirements for the staff action have been completed.

These procedures assume a small business environment with fewer than 50 employees. Organizations with regulatory, litigation hold, data residency, or formal eDiscovery obligations should add those controls before deleting accounts or transferring data.

## Procedures

### Create a Google Workspace user

Requires <role>Google Workspace Admin</role> or an administrator with user management privileges.

Create a Google Workspace user account when a person has been approved to join the organization, receive a company email address, or access Google Workspace resources. Do not create the account before the hiring or engagement approval is recorded.

1. Confirm the user's legal or preferred display name, company email address, department, manager, job role, start date, and employment or contractor type.
2. Confirm the approved Google Workspace groups, shared drives, and application access required for the role.
3. Navigate to the [Google Admin console]({{ .GOOGLE_ADMIN_CONSOLE_URL }}).
4. Open <kbd><samp>Directory</samp></kbd> | <kbd><samp>Users</samp></kbd>.
5. Select <kbd><samp>Add new user</samp></kbd>.
6. Enter the user's first name, last name, primary email address, organizational unit, and any required profile fields.
7. Create a temporary password or allow Google to generate one.
8. Require the user to change the temporary password at first sign-in.
9. If multi-factor authentication is required by company policy, confirm that the user enrolls before being granted production access.
10. Add the user to the approved Google Groups and shared drives for the role.
11. Record the account creation in the onboarding task, including the account email, organizational unit, groups assigned, and date created.
12. Send the initial sign-in instructions through the approved onboarding channel. Do not send passwords through public chat channels or shared documents.

The administrator should grant the minimum access required for the person's starting role. Additional access can be added after the manager or system owner approves it.

### Transfer Google Workspace user data

Requires <role>Google Workspace Admin</role> and coordination with the user's manager or the staff termination owner.

Transfer user data before deleting an account, before a long-term suspension, or when a user changes role and no longer owns certain work products. Data transfer protects business continuity and reduces the risk that files, email, calendars, or shared records become unavailable after the account is removed.

1. Confirm the business reason for the transfer, such as termination, role change, legal hold, manager request, or account consolidation.
2. Identify the receiving owner for each data category. The owner is usually the user's manager, the department head, or a role-specific service account.
3. Confirm whether the user's account is subject to a legal hold, investigation, audit, retention rule, or other preservation requirement. If so, pause the deletion process until the responsible officer approves the next step.
4. Review the user's Google Drive files, shared drives, Gmail, Calendar, Groups, and any other Google Workspace data used by the organization.
5. Transfer ownership of My Drive files to the approved receiving owner using the Google Admin console or Google Drive transfer tools.
6. Confirm that shared drive content is owned by the organization and that the user is removed from shared drive membership only after needed access has been reviewed.
7. If email history must be retained, use the approved mailbox retention, export, or delegation process before deletion.
8. Transfer or recreate calendar resources, recurring meetings, group ownership, and third-party app ownership where the user's account is the only owner or administrator.
9. Remove or rotate credentials, app passwords, OAuth grants, recovery contacts, and delegated mailbox access that should not survive the transfer.
10. Ask the receiving owner to confirm that critical files and records are accessible.
11. Record the transfer date, receiving owner, affected data categories, and any exceptions in the termination or role change task.

Do not delete the source account until the transfer is confirmed or an authorized exception is recorded.

### Delete a Google Workspace user

Requires <role>Google Workspace Admin</role> and approval from the staff termination owner or equivalent business owner.

Deleting a Google Workspace user removes the account and can make user data unavailable if the data has not already been transferred or preserved. Before deleting a user, complete [Transfer Google Workspace user data](#transfer-google-workspace-user-data).

Use deletion when the person no longer has an ongoing business relationship with the organization and account suspension, license removal, or archival is not sufficient. If there is uncertainty, suspend the account first and request approval before deletion.

1. Confirm that the termination, offboarding, or account removal task has been approved.
2. Confirm that [Transfer Google Workspace user data](#transfer-google-workspace-user-data) is complete or that an authorized exception is documented.
3. Confirm that legal hold, retention, investigation, and audit requirements have been checked.
4. Navigate to the [Google Admin console]({{ .GOOGLE_ADMIN_CONSOLE_URL }}).
5. Open <kbd><samp>Directory</samp></kbd> | <kbd><samp>Users</samp></kbd>.
6. Search for and select the user account.
7. Confirm that the selected user is the correct account. Check the primary email address, organizational unit, and manager if available.
8. If the account is still active, suspend it first when immediate access removal is required and deletion is not yet approved.
9. Select <kbd><samp>Delete user</samp></kbd> or the equivalent delete action in the user account menu.
10. When prompted, select the approved data transfer or data deletion choices. Do not skip data transfer unless the exception has already been approved.
11. Review the final confirmation screen and complete the deletion.
12. Confirm that the account no longer appears as active in the user list.
13. Remove the user from remaining groups, aliases, recovery workflows, third-party applications, password managers, and access control lists if those systems are not automatically updated.
14. Record the deletion date, administrator, approval reference, and data transfer confirmation in the staff termination or account removal task.

If an account was deleted by mistake, start the Google Workspace restore process immediately and notify the staff termination owner. Google account restoration is time-sensitive and may not recover every service or data type.

## References

* [Google Admin Help: Add an account for a new user](https://support.google.com/a/answer/33310)
* [Google Admin Help: Delete or remove a user from your organization](https://support.google.com/a/answer/33314)
* [Google Admin Help: Transfer Drive files to a new owner](https://support.google.com/a/answer/1247799)
* [Google Admin console]({{ .GOOGLE_ADMIN_CONSOLE_URL }})

## Version history

Date | Change description | Ticket | Ver. (git) | Author | Reviewed by
-----|--------------------|--------|------------|--------|-------------
2026-05-12 | Initial draft. | policy-vendors-google#2 | | | |
