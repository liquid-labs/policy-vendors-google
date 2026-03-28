# Google Workspace User Management

## Purpose and scope

This document establishes procedures for managing Google Workspace user accounts within the organization. It covers the complete lifecycle of a user account from creation through data transfer upon departure, ensuring business continuity, data security, and compliance with company data handling policies.

This procedure applies to all employees and contractors who require Google Workspace access. It is intended for Operations Admins responsible for account provisioning and IT staff responsible offboarding.

User management procedures ensure that:
- New users have appropriate access to perform their job functions
- Departing users' data is properly transferred to designated successors
- User accounts are removed in a timely manner to prevent unauthorized access
- Company data in Google Workspace is preserved and not lost during personnel transitions

## Procedures

### Create a Google Workspace user

A new Google Workspace account must be created for each employee before their start date to ensure they can access necessary tools on day one.

Prerequisites: You must have Organization Admin privileges in Google Workspace Admin console.

1. Navigate to the <kbd><samp>Google Admin Console</samp></kbd> at `admin.google.com`.
2. Go to <kbd><samp>Directory</samp></kbd> | <kbd><samp>Users</samp></kbd>.
3. Click <kbd><samp>Add New User</samp></kbd>.
4. Enter the user's first name, last name, and primary email address in the format `{{ .first.name }}@{{ .company.domain }}`.
5. Set the user's organizational unit from the dropdown.
6. Assign appropriate roles based on their job function (see Roles Management for role definitions).
7. Click <kbd><samp>Add User</samp></kbd> to create the account.
8. The temporary password will be displayed — provide this to the user via a secure channel and require password change on first login.

Note: For contractors or temporary staff, set the account to expire on the expected contract end date using <kbd><samp>Security</samp></kbd> | <kbd><samp>Set custom account status</samp></kbd>.

### Transfer Google Workspace user data

When an employee departs or changes roles, their Google Workspace data must be transferred to a designated successor or archived before account deletion. This ensures continuity of business operations and compliance with data retention requirements.

Before initiating transfer, obtain written approval from HR confirming the departure date and designated data recipient.

1. Navigate to <kbd><samp>Google Admin Console</samp></kbd> | <kbd><samp>Users</samp></kbd>.
2. Select the departing user's account.
3. Click <kbd><samp>User information</samp></kbd> | <kbd><samp>Change data ownership</samp></kbd>.
4. For Google Drive files:
   - Select all folders or specific folders to transfer.
   - Enter the successor's email address.
   - Choose whether to transfer ownership or grant edit access.
   - Click <kbd><samp>Transfer</samp></kbd>.
5. For Gmail messages: Use <kbd><samp>Set up email delegation</samp></kbd> if the successor needs to access historical emails, or configure an automated vacation responder directing senders to the successor.
6. For Google Calendar: Transfer ownership of shared calendars to the successor or a departmental calendar.
7. Document the transfer in the IT asset management system, noting the transfer date, data types transferred, and recipient.
8. If the account will be deleted (see Delete a Google Workspace user), export any remaining data not covered by Drive transfer using <kbd><samp>Download data</samp></kbd> before proceeding.

Caution: Transfer ownership does not automatically transfer Drive files in shared drives (formerly Team Drives). These must be transferred separately through the Shared Drives management console.

### Delete a Google Workspace user

Account deletion should only occur after all data transfer procedures have been completed and verified. Deletion is permanent and irreversible.

Prerequisites: All user data must be transferred or exported prior to deletion. Failure to do so will result in permanent data loss.

1. Confirm with HR that the offboarding process is complete and all required data transfers have been verified.
2. Navigate to <kbd><samp>Google Admin Console</samp></kbd> | <kbd><samp>Directory</samp></kbd> | <kbd><samp>Users</samp></kbd>.
3. Search for and select the user account to delete.
4. Click <kbd><samp>More options</samp></kbd> | <kbd><samp>Delete user</samp></kbd>.
5. Review the warning dialog which lists data that will be permanently deleted.
6. If all required data has been transferred, click <kbd><samp>Delete</samp></samp></kbd> to confirm.
7. Verify the deletion by searching for the user's email — the account should no longer appear in the directory.
8. Update the IT asset management system to reflect the account deletion date and the reason for removal.

Warning: Deleted user data cannot be recovered through Google Workspace admin tools. Ensure all Drive content, emails, and calendar events have been transferred to the designated successor or exported to long-term storage before proceeding.

## Version history

Date | Change description | Ticket | Ver. (git) | Author | Reviewed by
-----|--------------------|--------|------------|--------|-------------
2026-03-28 | Initial draft covering user creation, data transfer, and deletion procedures. | | | | |
