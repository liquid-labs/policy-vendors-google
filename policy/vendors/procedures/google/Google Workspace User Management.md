# Google Workspace User Management

## Purpose and scope

These procedures define how to create, transfer, suspend, and delete Google
Workspace user accounts for a small business. They are intended for routine
HR-driven onboarding and offboarding, and for exceptional changes requested by
security, legal, or management.

## Procedures

### Create a Google Workspace user

Required role: Google Workspace administrator.

This procedure creates a company Google Workspace account after HR or management
has approved a new staff member, contractor, or service user.

1. Confirm the request has an approved start date, legal name, primary email
   address, job title, manager, and employment or contract type.
2. Confirm the account is for a real business need. Do not create shared human
   accounts when an individual named account or Google group will meet the need.
3. Open the Google Admin console and go to Directory, then Users.
4. Select Add new user.
5. Enter the user's legal first and last name.
6. Enter the approved primary email address. Use the company's standard email
   naming convention unless management approves an exception.
7. Assign the user to the correct organizational unit.
8. If Google Workspace license assignment is not automatic for that
   organizational unit, assign the least-privileged license that supports the
   user's role.
9. Add the user to approved Google groups only after the manager or system owner
   confirms the access is required.
10. Set a temporary password or use Google's generated password option.
11. Require the user to change the password at first sign-in.
12. Confirm two-step verification enrollment is required before or during the
    user's first sign-in, according to company security policy.
13. Send the sign-in instructions through an approved onboarding channel. Do not
    send passwords through public chat, personal email, or other unapproved
    channels.
14. Record the account creation in the onboarding ticket or HR checklist,
    including the groups and licenses assigned.
15. Review the account within one business day after the user's start date to
    confirm the account is active and no unapproved groups were assigned.

### Transfer Google Workspace user data

Required role: Google Workspace administrator with authority to transfer Drive,
Gmail, and related Workspace data.

This procedure preserves company information before an account is deleted or
when a user changes roles. Complete it during staff termination, long leave,
role transfer, or any other event where company data must remain available.

1. Confirm the transfer request is approved by HR, legal, management, or the
   affected business owner.
2. Identify the source user account and the destination owner. The destination
   should normally be the user's manager, replacement, or a controlled archive
   account.
3. Suspend the source account first if the user should no longer access company
   systems.
4. In Google Admin console, review the source user's groups, delegated access,
   shared drives, aliases, and recovery settings.
5. Transfer ownership of relevant Drive files to the approved destination owner.
   Do not transfer personal or non-business content unless legal or management
   has approved it.
6. For shared drives, confirm business-critical files remain in the shared drive
   and that at least two current staff members have manager access.
7. If Gmail data must be retained, use the approved Google Workspace migration,
   export, or retention process. Coordinate with legal before deleting or
   modifying mail that may be subject to a hold.
8. Reassign or remove group ownership, calendar ownership, delegated mailbox
   access, and application-specific ownership tied to the source account.
9. Update any system, vendor, or HR record that lists the source user as an
   owner, approver, billing contact, or emergency contact.
10. Document what was transferred, the destination owner, any retained data, and
    any items that could not be transferred.
11. Ask the destination owner to confirm access to the transferred information.
12. Keep the source account suspended until the transfer has been verified and
    all retention or legal requirements have been satisfied.

### Delete a Google Workspace user

Required role: Google Workspace administrator.

Deleting an account is permanent and may remove access to company data. Use this
procedure only after offboarding, transfer, and retention requirements are
complete.

1. Confirm HR, legal, management, or the business owner has approved account
   deletion.
2. Confirm the user no longer needs access and that the account has been
   suspended during the required waiting period.
3. Before deleting a user, complete and verify the
   [transfer Google Workspace user data](#transfer-google-workspace-user-data)
   procedure.
4. Confirm any legal holds, retention rules, export requirements, or customer
   commitments have been satisfied.
5. Confirm the account is not the sole owner of a group, shared drive, calendar,
   domain property, vendor integration, or billing relationship.
6. Confirm aliases, routing rules, delegated access, app passwords, recovery
   methods, and multi-factor devices have been removed or reassigned.
7. In Google Admin console, go to Directory, then Users.
8. Select the suspended user account.
9. Select Delete user and follow the Google Admin console prompts.
10. When prompted, transfer or confirm deletion of remaining services according
    to the approved offboarding record.
11. Record the deletion date, approver, transfer destination, and any exceptions
    in the offboarding ticket or HR checklist.
12. Notify the manager, HR, and any affected system owner that deletion is
    complete.

If any approval, transfer, or retention question is unresolved, stop the deletion
and keep the account suspended until the issue is resolved.

## Version history

Date       | Change description | Ticket | Ver. (git) | Author | Reviewed by
---------- | ------------------ | ------ | ---------- | ------ | -----------
2026-05-13 | Initial draft.     | #2     | TBD        | TBD    | TBD
