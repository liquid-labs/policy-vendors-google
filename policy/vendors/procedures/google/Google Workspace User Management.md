# Google Workspace User Management

## Purpose and scope

This document describes baseline procedures for managing Google Workspace user accounts for a small business. It is intended for staff responsible for operations, HR, security, legal, and IT administration.

These procedures cover creating Google Workspace users, transferring user data before account removal, and deleting Google Workspace users when the business no longer has a need to retain the account. They focus on business, security, legal, and continuity concerns; Google Admin Console screens may change, so administrators should also consult current Google Workspace help when carrying out the steps.

## Procedures

### Create a Google Workspace user

Requires <role>Google Workspace Administrator</role> or another role authorized to create users in the Google Admin Console.

Create a Google Workspace user account only after HR or the responsible manager has approved the person's start date, role, and access needs.

1. Confirm the staff member's legal or preferred display name, start date, reporting manager, job function, and company email address.
2. Confirm whether the user should be created in a specific organizational unit and whether the user requires a custom email alias.
3. Navigate to the [Google Admin Console]({{ .GOOGLE_ADMIN_CONSOLE_URL }}).
4. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd>.
5. Click <kbd><samp>Add new user</samp></kbd>.
6. Enter the user's first name, last name, primary email address, and any other required profile information.
7. Select the appropriate organizational unit when applicable.
8. Create the account using a temporary password or the Google-generated password option.
9. Require the user to change the password at first sign-in unless another approved identity provider handles password setup.
10. Click <kbd><samp>Add new user</samp></kbd> or <kbd><samp>Save</samp></kbd>.
11. Assign the user only the Google Workspace licenses, groups, aliases, and administrator roles approved for the user's job responsibilities.
12. Confirm that required security settings apply to the account, including two-step verification requirements where required by company policy.
13. Send onboarding instructions to the user through an approved channel. Do not send temporary credentials through an insecure or publicly visible channel.
14. Record the account creation, approvals, assigned groups, assigned licenses, and any temporary exceptions in the onboarding or access management record.

### Transfer Google Workspace user data

Requires <role>Google Workspace Administrator</role> or another role authorized to manage users and data in the Google Admin Console.

Transfer Google Workspace user data before deleting or suspending an account when the company must preserve work product, business records, or legally relevant information. Coordinate the transfer with HR, the user's manager, legal, and security as appropriate.

1. Confirm that the user's departure, role change, or access removal has been approved by HR or the responsible manager.
2. Determine whether a legal hold, investigation hold, retention requirement, or other preservation requirement applies before making changes to the account or its data.
3. Identify the manager, successor, shared mailbox, or other approved custodian who should receive the user's business data.
4. Suspend the account if immediate access removal is required and the account has not already been disabled through an approved offboarding procedure.
5. Navigate to the [Google Admin Console]({{ .GOOGLE_ADMIN_CONSOLE_URL }}).
6. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd> and select the user.
7. Review the user's aliases, groups, delegated access, recovery information, licenses, and administrator roles so access can be removed or reassigned deliberately.
8. Transfer or preserve email according to the company's retention requirements. Use Google Workspace tools such as Google Vault, data export, delegated mailbox access, or another approved migration process as appropriate for the account and license type.
9. Transfer Google Drive files owned by the user to the approved custodian or shared drive. Verify that critical folders, shared documents, and externally shared files remain accessible to the business after transfer.
10. Transfer ownership or administration of calendars, shared drives, groups, sites, forms, apps scripts, service accounts, and other Google Workspace resources where the user is the owner or a required administrator.
11. Remove or update forwarding rules, delegates, third-party app access, app passwords, OAuth grants, recovery email addresses, recovery phone numbers, and personal device access that are no longer appropriate.
12. Confirm that business-critical data is accessible to the approved custodian and that unnecessary access for the departing or former user has been removed.
13. Record the transfer date, receiving custodian, preserved data locations, unresolved issues, and approvals in the offboarding or access management record.

### Delete a Google Workspace user

Requires <role>Google Workspace Administrator</role> or another role authorized to delete users in the Google Admin Console.

Delete a Google Workspace user only when the company no longer needs the account, access has been removed, applicable retention requirements have been satisfied, and required data has been preserved or transferred. Before deleting a user, complete the [Transfer Google Workspace user data](#transfer-google-workspace-user-data) procedure.

1. Confirm that HR, the user's manager, legal, and security have approved deletion or that the documented retention period for the suspended account has ended.
2. Confirm that no legal hold, audit requirement, investigation, or contractual obligation requires the account or its data to remain active or suspended.
3. Complete and verify the [Transfer Google Workspace user data](#transfer-google-workspace-user-data) procedure.
4. Confirm that required email, Drive files, shared drives, calendars, groups, sites, and other Google Workspace resources have been transferred or preserved.
5. Confirm that the user no longer owns critical integrations, third-party apps, service accounts, automations, or administrator responsibilities.
6. Navigate to the [Google Admin Console]({{ .GOOGLE_ADMIN_CONSOLE_URL }}).
7. Navigate to <kbd><samp>Directory</samp> | <samp>Users</samp></kbd> and select the user to be deleted.
8. Open the user's account actions menu and choose <kbd><samp>Delete user</samp></kbd>.
9. Review Google's deletion prompts carefully. If Google offers options to transfer Drive files, Calendar events, or other data, select the approved custodian and transfer the data unless the data has already been transferred and verified.
10. Confirm the deletion only after verifying that the selected account is the correct user account.
11. Remove or update references to the deleted account in internal access records, distribution lists, contact lists, ownership records, and vendor administration notes.
12. Record the deletion date, approval, data transfer confirmation, and any remaining follow-up tasks in the offboarding or access management record.
