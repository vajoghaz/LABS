App Registration permissions

A permission allows the application to use a given API. A scope is used to request consent to run a given function on an API. An application ID URI does not handle permissions.

https://learn.microsoft.com/en-gb/entra/identity-platform/quickstart-configure-app-expose-web-apis

https://learn.microsoft.com/en-gb/entra/identity-platform/quickstart-configure-app-access-web-apis

https://learn.microsoft.com/en-gb/training/modules/manage-application-access-microsoft-entra-id/

Overview of permissions and consent in the Microsoft identity platform

Permission scope for an app reg
three OpenID Connect scopes

https://learn.microsoft.com/en-gb/entra/identity/enterprise-apps/user-admin-consent-overview

https://learn.microsoft.com/en-gb/entra/identity-platform/permissions-consent-overview#consent-types


Overview of permissions and consent in the Microsoft identity platform:

In a static user consent scenario, you must specify all required permissions in the app's configuration in the Azure portal. With incremental user consent and dynamic user consent, you can ask for a bare minimum set of permissions upfront and request more over time as the customer uses additional app features. Admin consent is required when your app needs access to certain high-privilege permissions, but it does not follow the principle of least privilege in this scenario.

Permission scope for an app reg
three OpenID Connect scopes
 - mail
 - offline_access
 - openID
The openID scope appears on the work account consent page as the Sign you in permission. The email scope gives the app access to a user's primary email address in the form of the email claim. The offline_access scope gives your app access to resources on behalf of a user for an extended time. On the consent page, this scope appears as the Maintain access to data you have given it access to permission.

A scope is used to request content to run a given function in an API. An application ID URI does not handle permissions, a permission is used to allow an application to access the scope created in another app, and a client application allows an application to use the API.