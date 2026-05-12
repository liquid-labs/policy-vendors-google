# Google Workspace User Management

## Purpose and scope

This document defines baseline procedures for creating, transferring, and
deleting Google Workspace user accounts in a small business environment. It is
written for <role>Operations Admin</role>, <role>HR Agent</role>, managers, and
other staff responsible for account lifecycle management.

The goal is to make Google Workspace account changes predictable, documented,
and secure. These procedures focus on business controls around approvals, access
scope, data preservation, retention, and evidence collection. Product-specific
screen names may change over time, so administrators should also refer to Google
Workspace Admin Help while performing the steps in the Admin console.

Use this procedure together with the organization's onboarding, role-change,
access-review, and offboarding procedures. Google Workspace changes should not
be treated as isolated technical actions; they affect identity, records,
customer data, shared drives, email, calendars, and third-party applications.

## Procedures

### Create a Google Workspace user

Requires <role>Operations Admin</role>.

Create a Google Workspace user only after the responsible manager or
<role>HR Agent</role> confirms that the person has been approved to join the
company, the expected start date is known, and the user's role and access needs
are documented in an onboarding ticket.

Before creating the account:

1. Confirm the user's legal name, preferred display name, primary email address,
   manager, department, role, start date, and employment or contractor status.
2. Confirm the account naming convention and whether any aliases are required.
3. Confirm the required organizational unit, Google Workspace license, groups,
   shared drives, delegated applications, and third-party application access.
4. Confirm whether the account should be active immediately or staged until the
   user's start date.
5. Confirm whether the user requires administrator privileges. Do not grant
   administrator roles unless a separate access request approves the role.

To create the account:

1. Navigate to the
   [Google Admin console]({{ .google.workspace.admin.console.url }}).
2. Open <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
3. Click <kbd><samp>Add new user</samp></kbd>.
4. Enter the user's name, primary email address, and required profile details.
5. Place the user in the correct organizational unit before saving the account.
6. Assign the required Google Workspace license.
7. Create a temporary password or allow Google Workspace to generate one.
8. Require the user to change the temporary password on first sign-in.
9. Save the account.
10. Add the user to approved company groups, role groups, and shared drives.
11. Add approved email aliases only when they are required for business use.
12. Apply role-specific security settings, including two-step verification
    requirements, context-aware access rules, and device management rules.
13. Send first sign-in instructions through the approved onboarding channel.
    Do not send passwords through unapproved personal email, public chat, shared
    documents, or text messages unless a documented exception is approved.
14. Update the onboarding ticket with the created email address, organizational
    unit, license, groups, aliases, privileged roles, and activation date.
15. Notify the responsible manager and <role>HR Agent</role> that the Google
    Workspace account is ready.

After creating the account:

1. Confirm that the user completes required two-step verification enrollment.
2. Confirm that the user's manager validates initial access after onboarding.
3. Schedule an access review when the user receives administrator or sensitive
   access.
4. Record any exceptions, delayed access, or temporary privileges in the
   onboarding ticket.

The user should receive the minimum access required for the starting role.
Additional access can be granted after the manager or system owner approves it.

### Transfer Google Workspace user data

Requires <role>Operations Admin</role>.

Transfer Google Workspace user data before deleting an account, when a staff
member changes roles, or when business records owned by one user need to be
preserved under another user. The transfer recipient should usually be the
user's manager, successor, department owner, or a dedicated archive account such
as `records@{{ .company.domain }}`.

Do not transfer or delete data until these checks are complete:

1. Confirm that the transfer is authorized by the responsible manager,
   <role>HR Agent</role>, legal contact, or other approved business owner.
2. Check whether the user is subject to a legal hold, investigation hold,
   customer obligation, regulatory requirement, or records retention rule.
3. Confirm the destination account for each data category that must be
   preserved.
4. Confirm whether mailbox contents must be retained, exported, delegated,
   migrated, or preserved through a separate retention workflow.
5. Confirm whether third-party applications, service accounts, OAuth grants,
   API credentials, or integrations depend on the user's account.

To transfer data:

1. Navigate to the
   [Google Admin console]({{ .google.workspace.admin.console.url }}).
2. Open <kbd><samp>Apps</samp> | <samp>Google Workspace</samp> |
   <samp>Drive and Docs</samp></kbd>.
3. Use the Drive transfer ownership tool to transfer the user's My Drive files
   and folders to the approved destination account.
4. Review shared drives where the user is a manager or content manager and
   assign a replacement manager before removing the user.
5. Review Google Groups owned or managed by the user and assign a replacement
   owner or manager.
6. Review Calendar resources and recurring meetings owned by the user. Transfer
   ownership, cancel obsolete events, or ask the manager to recreate
   business-critical events as appropriate.
7. Preserve Gmail data through an approved delegation, export, migration,
   retention, or archive process. Do not share or reuse the user's password.
8. Review aliases, forwarding rules, delegated mailbox access, recovery
   addresses, and app passwords.
9. Review OAuth app access and third-party integrations associated with the
   user. Transfer business-owned integrations to an approved owner or revoke
   access.
10. Record the transfer destination, transfer date, systems reviewed, approval
    source, and any known exclusions in the offboarding or access-change ticket.
11. Ask the responsible manager or data owner to confirm that critical files,
    calendars, and business records are accessible from the destination account.

Do not delete the source user until the required transfer and manager
confirmation are complete. If Google Workspace reports that a transfer failed,
stop the deletion process, record the error, and resolve the failure before
continuing.

### Delete a Google Workspace user

Requires <role>Operations Admin</role>.

Delete a Google Workspace user only after the account is no longer needed,
offboarding is approved, and required data preservation is complete. If there is
any uncertainty about retention, legal hold, payroll, customer records, active
business work, or account restoration, suspend the account instead of deleting
it.

Before deleting the user:

1. Confirm that HR, the responsible manager, and any required legal or
   compliance contact have approved deletion.
2. Confirm that the user no longer requires access to company systems.
3. Confirm that the account is not the only owner, super administrator, or
   billing contact for critical Google Groups, shared drives, calendars,
   third-party applications, domain settings, or emergency workflows.
4. Complete [Transfer Google Workspace user data](#transfer-google-workspace-user-data)
   before deleting the account.
5. Confirm that the manager or data owner has approved the final transfer
   result.
6. Reset active sessions, revoke app passwords, revoke OAuth tokens, remove
   registered devices, and address recovery options according to the offboarding
   procedure.

To delete the user:

1. Navigate to the
   [Google Admin console]({{ .google.workspace.admin.console.url }}).
2. Open <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
3. Search for and select the user account.
4. Review the account details one final time to confirm that the correct user
   is selected.
5. Select <kbd><samp>Delete user</samp></kbd>.
6. Follow the Admin console prompts to transfer, preserve, or remove data.
7. Confirm deletion only after all required data transfer and retention prompts
   are satisfied.
8. Record the deletion date, administrator, approval reference, data transfer
   destination, and manager confirmation in the offboarding ticket.

After deleting the user:

1. Confirm that the account no longer appears as active in the user list.
2. Monitor for failed data transfer messages or Admin console alerts.
3. Remove or reassign any remaining aliases, group ownership, shared resource
   ownership, vendor records, emergency contact lists, and third-party
   application records that are not automatically updated by Google Workspace.
4. Confirm with the manager or data owner that business-critical files,
   calendars, and communications are accessible.
5. Retain the offboarding ticket and deletion evidence according to the
   organization's records retention requirements.

If the user may need to be restored, document the reason and retention deadline
before deletion. Google Workspace deletion and restore behavior can depend on
account state, licensing, and timing, so administrators should not rely on
restore as the primary preservation method.

## References

* [Google Workspace Admin Help: Add an account for a new user](https://support.google.com/a/answer/33310)
* [Google Workspace Admin Help: Options for adding users](https://support.google.com/a/answer/179832)
* [Google Workspace Admin Help: Transfer Drive files to a new owner as an admin](https://support.google.com/a/answer/1247799)
* [Google Workspace Admin Help: Delete or remove a user from your organization](https://support.google.com/a/answer/33314)
* [Google Workspace Admin SDK: Manage user accounts](https://developers.google.com/workspace/admin/directory/v1/guides/manage-users)
* [Google Workspace Admin SDK: Data Transfer API overview](https://developers.google.com/workspace/admin/data-transfer)
* [General User Management]({{ .policy.staff.procedures.GENERAL_USER_MANAGEMENT }})

## Version history

Date | Change description | Ticket | Ver. (git) | Author | Reviewed by
-----|--------------------|--------|------------|--------|------------
2026-05-12 | Initial draft. | #2 | | Taher Dhanerawala | TBD
