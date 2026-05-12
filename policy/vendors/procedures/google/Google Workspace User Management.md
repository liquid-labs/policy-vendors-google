# Google Workspace User Management

## Purpose and scope

This document describes baseline procedures for managing Google Workspace user accounts in a small business environment. It is intended for operations, IT, HR, and security staff who create accounts, transfer company data, and remove accounts when staff or contractors leave the organization.

These procedures focus on business controls and common administrative steps. They should be followed together with the organization's staff onboarding, role management, access review, records retention, legal hold, and termination procedures.

## Procedures

### Create a Google Workspace user

Create a Google Workspace user account only after the staff member or contractor has been approved through the applicable hiring, contracting, or onboarding process.

Before creating the account:

1. Confirm that HR or the engagement owner has approved the start date, legal name, work name if different, department, manager, role, and employment or contractor status.
2. Confirm the user's required Google Workspace license type and any additional product access.
3. Confirm the user's initial Google groups, shared drives, aliases, and privileged roles from the approved role or access request.
4. Confirm whether the account must be created in a specific organizational unit.
5. Confirm whether the account should be active immediately or held until the user's start date.

To create the account:

1. Sign in to the [Google Admin console]({{ .google.workspace.admin.console.url }}) with an administrator account authorized to manage users.
2. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
3. Select <kbd><samp>Add new user</samp></kbd>.
4. Enter the user's first name, last name, and primary email address using the organization's approved naming convention.
5. Assign the correct organizational unit and Google Workspace license.
6. Set an initial password using the Admin console generated password or another approved secure process.
7. Require the user to change the password at first sign-in when that option is available.
8. Save the account.
9. Add the user to the approved Google groups and shared drives.
10. Add email aliases only when they have been approved for business use.
11. Record the completed account creation in the onboarding ticket or access request.
12. Send first sign-in instructions through an approved channel. Do not send passwords in public chat, shared documents, or unencrypted email.

After creating the account:

1. Confirm that the user has multi-factor authentication enabled according to company policy.
2. Confirm that privileged roles, if any, are limited to the minimum required for the user's job duties.
3. Confirm that the manager or engagement owner has validated the user's access after onboarding.
4. Schedule any required access review if the user has administrative or sensitive access.

### Transfer Google Workspace user data

Transfer Google Workspace user data before deleting a user account whenever business records, customer data, legal records, project files, or operational continuity may be affected.

Do not transfer user data until all of the following are complete:

1. HR, Legal, or the engagement owner has confirmed that the user is leaving, changing roles, or otherwise no longer requires the account.
2. The user's manager or designated data owner has identified the destination account for transferred data.
3. The organization has checked whether the user or their data is subject to a legal hold, investigation hold, records retention requirement, or customer contractual obligation.
4. Any required offboarding or access revocation ticket has been opened.
5. Administrative access needed for the transfer has been approved.

Data transfer requirements:

1. Transfer ownership of business-critical Google Drive files and shared drive content where ownership or access would otherwise be lost.
2. Transfer primary Calendar data when calendar history or future meetings are needed for business continuity.
3. Transfer Looker Studio or other supported Google Workspace application data when applicable to the user's role.
4. Preserve email according to the organization's retention requirements. If mailbox contents are needed after account removal, export, delegate, migrate, retain with Vault, or otherwise preserve the data using an approved method before deleting the account.
5. Review aliases, groups, delegated mailboxes, and forwarding rules that may need to be reassigned.

To transfer supported data during account deletion:

1. Sign in to the [Google Admin console]({{ .google.workspace.admin.console.url }}) with an administrator account authorized to manage users.
2. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
3. Open the user account that is being removed.
4. Select the option to delete or remove the user.
5. When the Admin console offers data transfer options, select the supported data that must be transferred.
6. Enter the approved destination user account for transferred data.
7. Review the transfer selections before confirming deletion.
8. If the transfer fails, stop the deletion process, record the error in the offboarding ticket, and resolve the issue before trying again.
9. Record the transfer date, source account, destination account, data types transferred, and approving person in the offboarding ticket.

For transfers that cannot be completed during account deletion, use an approved Google Workspace migration, export, Vault, shared drive, or Data Transfer API process and document the result before account deletion.

### Delete a Google Workspace user

Delete a Google Workspace user only when account retention is no longer required and the business has completed required offboarding controls.

Before deleting the user:

1. Confirm that HR or the engagement owner has approved account removal.
2. Confirm that the account is not the only super admin account and is not needed for emergency access.
3. Confirm that the account is not subject to a legal hold or investigation hold. Do not delete accounts under hold.
4. Confirm that all required data has been transferred or preserved. See [Transfer Google Workspace user data](#transfer-google-workspace-user-data).
5. Confirm that required aliases, group memberships, shared drive access, delegated mailbox access, app-specific access, and admin roles have been reviewed.
6. Confirm that any active devices, sessions, app passwords, OAuth grants, and recovery options have been addressed according to offboarding procedures.
7. Confirm that the manager or data owner has approved the final deletion.

To delete the user:

1. Sign in to the [Google Admin console]({{ .google.workspace.admin.console.url }}) with an administrator account authorized to manage users.
2. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
3. Find the user account to be removed.
4. Open the user actions menu and select the delete or remove user option.
5. Complete any required [data transfer](#transfer-google-workspace-user-data) selections.
6. Review the deletion summary carefully, including data transfer destination, aliases, and warnings.
7. Confirm the deletion only after all warnings have been reviewed and accepted.
8. Record the deletion date, administrator, approvals, transfer destination, and any unresolved exceptions in the offboarding ticket.

After deleting the user:

1. Monitor for failed data transfers or alerts from the Admin console.
2. Remove or reassign remaining aliases, groups, shared resources, and third-party application accounts that depended on the deleted user.
3. Confirm with the user's manager or data owner that business-critical files, calendars, and communications are accessible.
4. Retain the offboarding ticket and deletion evidence according to records retention requirements.

## References

* [Google Workspace Admin Help: options for adding users](https://support.google.com/a/answer/179832)
* [Google Workspace Admin Help: delete or remove a user from your organization](https://support.google.com/a/answer/33314)
* [Google Workspace Admin SDK: manage user accounts](https://developers.google.com/workspace/admin/directory/v1/guides/manage-users)
* [Google Workspace Admin SDK: Data Transfer API overview](https://developers.google.com/workspace/admin/data-transfer)

## Version history

Date | Change description | Ticket | Ver. (git) | Author | Reviewed by
-----|--------------------|--------|------------|--------|-------------
2026-05-12 | Initial draft. | liquid-labs/policy-vendors-google#2 | | Stevennva28 |
