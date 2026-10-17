# Google Workspace — User Management Policy (draft)

> First-draft business policy for small teams (<50). Uses Liquid Labs style placeholders such as `{{ .company.domain }}`.

## 1. Purpose

This policy tells staff **when** and **how** to create, change, suspend, and delete Google Workspace users so access stays aligned with employment status and least privilege.

Refer to the [Employee Handbook]({{ .employee.handbook.url }}) for related HR procedures.

## 2. Roles

| Role | Responsibility |
| --- | --- |
| Requestor (manager / HR) | Requests joiners, movers, leavers with effective dates |
| Workspace Admin | Executes changes in Admin Console; keeps audit notes |
| Security / IT | Reviews privileged roles and shared-drive access quarterly |

Contact IT support at `itsupport@{{ .company.domain }}` for operational help.

## 3. Joiner (create user)

Create a user **only** after HR confirms start date and manager.

1. Create the account with company email on `{{ .company.domain }}`.
2. Place the user in the correct org unit / group for their role.
3. Apply baseline licenses required for the role (no unused paid seats).
4. Require 2-Step Verification on first login where enforced by company baseline.
5. Share the [Welcome / Access Checklist]({{ .workspace.onboarding.checklist.url }}) with the manager.

Do **not** create personal Gmail aliases as the primary corporate identity.

## 4. Mover (role or team change)

Within **1 business day** of a confirmed role change:

1. Update org unit / groups to match the new role.
2. Remove access that the old role required and the new role does not.
3. Review shared drives, Groups, and calendar resources owned by the user.
4. Record the change in the [Access Change Log]({{ .access.change.log.url }}).

## 5. Leaver (suspend then delete)

### 5.1 Same day as last working day (or earlier if instructed by HR)

1. **Suspend** the account (do not delete immediately) to stop sign-in while preserving data.
2. Sign the user out of all sessions; revoke app passwords / tokens where practical.
3. Transfer Drive ownership of business-critical folders to the manager or function mailbox.
4. Redirect mail as directed by HR/manager (delegation or routing) for `{{ .leaver.mail.retention.days }}` days.

### 5.2 After retention window

1. Export any legally required records per counsel/HR.
2. Delete the account only after the retention checklist is complete.
3. Confirm licenses are released.

{{ if .user.data.traced }}
* Ensure that the [User Data Tracking Log]({{ .user.data.tracking.log.url }}) is updated when user data location must be tracked.
{{ end }}

## 6. Privileged admins

- Super Admin seats are limited and named.
- Quarterly review of Admin roles by Security / IT.
- Emergency contact: {{ .ORG_EMERGENCY_DIRECTOR_NAME }}.

## 7. Acceptance (this draft)

- Covers create / change / suspend / delete with business timing (not only Google how-to links).
- Uses placeholders for company-specific values.
- Suitable as an outline for further iteration in this repository.
