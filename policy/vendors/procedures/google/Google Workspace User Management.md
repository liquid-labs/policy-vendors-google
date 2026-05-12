# Google Workspace User Management

## Purpose and scope

This document describes the standard procedures for managing Google Workspace user
accounts in a small business environment. It is intended for <role>Operations
Admins</role>, <role>IT Admins</role>, and <role>Human Resources Agents</role>
who create, modify, transfer, suspend, and delete Google Workspace users.

These procedures focus on the business controls around user management: who may
request account changes, what must be checked before changes are made, and how
company data is protected before an account is removed. Product-specific screen
labels may change over time, so administrators should also refer to the current
[Google Admin Help]({{ .vendors.google.workspace.admin.help.url }}) when carrying
out the steps.

## Procedures

### Create a Google Workspace user

Requires <role>Operations Admin</role> or <role>IT Admin</role>.

1. Confirm that the account request is tied to an approved staff onboarding,
   contractor onboarding, or other authorized access request.
2. Confirm the user's legal name, preferred display name, job title, department,
   responsible manager, and expected start date with <role>Human Resources</role>
   or the responsible manager.
3. Confirm whether the user needs a mailbox, Google Drive access, Google Groups
   membership, shared drive access, or administrative privileges.
4. Navigate to the [Google Admin console]({{ .vendors.google.workspace.admin.console.url }}).
5. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
6. Click <kbd><samp>Add new user</samp></kbd>.
7. Enter the user's first name, last name, primary email address, and any
   available profile details needed by company policy.
8. Create the account with a temporary password.
9. Require the user to change the password at first sign-in whenever that option
   is available.
10. Add the user to the required Google Groups. At a minimum, this should include
    the groups required by the user's department, role, location, and employment
    status.
11. Grant access to shared drives or delegated mailboxes only when explicitly
    requested and approved.
12. If the user needs administrative access, assign the least-privileged admin
    role that supports the user's duties. Do not grant Super Admin unless the
    role has been approved by senior management.
13. Send sign-in instructions to the user through an approved onboarding channel.
    Do not send passwords in the same message as the account name when an
    alternate delivery method is available.
14. Update the onboarding record with the account creation date, primary email
    address, groups assigned, and the administrator who created the account.

### Transfer Google Workspace user data

Requires <role>Operations Admin</role> or <role>IT Admin</role>.

This procedure must be completed before deleting a Google Workspace user unless
<role>Human Resources</role> and the responsible manager confirm in writing that
the account contains no business records that need to be retained.

1. Confirm that the offboarding, role change, or data transfer request is
   authorized by <role>Human Resources</role>, Legal, or the responsible manager.
2. Identify the destination owner for the user's business data. This is usually
   the responsible manager, a department service account, or a replacement staff
   member.
3. Suspend the user account if access must be stopped immediately but data review
   is not complete.
4. Review the account for business data that must be retained, including Gmail,
   Google Drive files, shared drive content, Google Calendar events, Contacts,
   Apps Script projects, and any delegated mailboxes.
5. Transfer ownership of the user's My Drive files to the approved destination
   owner using the Google Admin console or the current Google-supported transfer
   workflow.
6. Confirm that files in shared drives remain available to the appropriate
   shared drive members. Shared drive files are owned by the organization rather
   than the individual user, but access and membership should still be reviewed.
7. Delegate or export mailbox data according to the staff termination,
   litigation hold, and records retention requirements that apply to the user.
8. Transfer or reassign recurring calendar events that are needed for ongoing
   business operations.
9. Remove or transfer ownership of any Google Groups, shared drives, forms,
   scripts, API credentials, or automation jobs owned by the user.
10. Record the transfer destination, completion date, and administrator who
    performed the transfer in the offboarding or access-change record.
11. Ask the responsible manager to confirm that the transferred data is
    accessible before the user account is deleted.

### Delete a Google Workspace user

Requires <role>Operations Admin</role> or <role>IT Admin</role>.

Deleting a user is irreversible for many practical business purposes and may
remove access to mail, files, and application data. Complete
[Transfer Google Workspace user data](#transfer-google-workspace-user-data)
before deleting the user.

1. Confirm that the user should be deleted rather than suspended, renamed, or
   retained for legal hold or records retention purposes.
2. Confirm that there is no active legal hold, audit request, security
   investigation, or unresolved data transfer requirement affecting the account.
3. Confirm that the user's business data has been transferred and that the
   destination owner has verified access.
4. Navigate to the [Google Admin console]({{ .vendors.google.workspace.admin.console.url }}).
5. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
6. Search for and select the user account.
7. Review the account details one final time to confirm the correct user is
   selected.
8. Choose the account deletion action.
9. When Google presents options to transfer data, verify that the destination
   owner matches the transfer record or complete any remaining transfer steps.
10. Confirm the deletion.
11. Remove the user from internal staff rosters, access trackers, password
    manager collections, device management records, and any vendor access lists
    that are maintained outside Google Workspace.
12. Record the deletion date, deletion reason, data transfer destination, and
    administrator who deleted the account in the offboarding record.

### Review Google Workspace user access

Requires <role>Operations Admin</role> or <role>IT Admin</role>.

1. Review active users at least quarterly.
2. Confirm that each active account maps to a current staff member, contractor,
   service account, or other approved business purpose.
3. Review suspended users and determine whether each account should remain
   suspended, be reactivated, or proceed through
   [Transfer Google Workspace user data](#transfer-google-workspace-user-data)
   and [Delete a Google Workspace user](#delete-a-google-workspace-user).
4. Review users with administrative privileges and confirm that each assignment
   remains necessary.
5. Review Google Groups used for access control and confirm group membership
   matches current job duties.
6. Document the review date, reviewer, exceptions, and follow-up actions.

## References

* [Google Admin Help: Add a new user]({{ .vendors.google.workspace.admin.help.add.user.url }})
* [Google Admin Help: Transfer important data before deleting a user]({{ .vendors.google.workspace.admin.help.transfer.user.data.url }})
* [Google Admin Help: Delete or remove a user from your organization]({{ .vendors.google.workspace.admin.help.delete.user.url }})
* [Staff Management Framework]({{ .staff.STAFF_MANAGEMENT_FRAMEWORK }})

## Version history

Date | Change description | Ticket | Ver. (git) | Author | Reviewed by
-----|--------------------|--------|------------|--------|-------------
2026-05-12 | Initial draft. | liquid-labs/policy-vendors-google#2 | | xiaopeng215-sys |
