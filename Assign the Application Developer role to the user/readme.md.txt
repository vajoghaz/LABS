Assign the Application Developer role to the user

disable the Users can register applications option in Microsoft Entra

https://learn.microsoft.com/en-gb/entra/identity/role-based-access-control/permissions-reference

https://learn.microsoft.com/en-gb/training/modules/manage-application-access-microsoft-entra-id/

https://learn.microsoft.com/en-gb/entra/identity/role-based-access-control/delegate-app-roles

To restrict application registration and consent permissions to selected users, set 'Users can register applications' to 'No' and assign the Application Developer role to those users. This ensures that only selected users can register applications and consent to applications accessing company data. Assigning the Cloud Application Administrator role to all users grants excessive permissions, not meeting the goal. Disabling user consent for all applications contradicts the goal of allowing selected users to manage consents. Assigning the Application Developer role to selected users restricts permissions appropriately.
----------------------------------------------
Although the permission to manage App1:
Correct: Cloud Application Administrator – Since App1 is an app in Azure, this role provides administrative permissions to App1 and follows the principle of least privilege.

Incorrect: Application Administrator – This role provides administrative permissions to App1 but also provides additional permissions to the app proxy for on-premises applications.

Incorrect: Cloud App Security Administrator – This role is specific to the Microsoft Defender for Cloud Apps solution.

Incorrect: Application Developer – This role allows the user to create registrations but not manage applications.