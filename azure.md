# Azure

These are the Azure guidelines for building a RSAF compliant app from 2019 onwards.

## Authentication

Most of our apps require some form of basic authentication. We are now using [Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis) to manage our users. This has many benefits: 

1. This allows us to enforce strict security rules around our authentication system (e.g 2 fa).
2. This allows us to have one user account to many apps with its own permissions.
3. This allows us to maintain user accounts easily and revoke access using one portal.

**DOs**

:heavy_check_mark: Do use [Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis) to authenticate users.

:heavy_check_mark: Do use [MSAL](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-overview) instead of [ADAL](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries). They have a whole suite of SDKs for easy integration.

:heavy_check_mark: Do ensure that your users have two-factor authentication enabled.

:heavy_check_mark: Do ensure that your app is configured to be single tenanted to Swift Office azure's tenantId.

:heavy_check_mark: Do use [AAD custom roles](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/roles-create-custom) to give permissions to certain users or features.

:heavy_check_mark: Do ensure that you are using the correct authentication flow (implicit/explicit) for your applications.

**Don'ts**

:heavy_multiplication_x: Do not roll out your own user authentication.

## APIs

Your api may require authentication or certain permissions to access. To authenticate a user to use your API, you will have to acquire a token for your API's scope and send the token along with the request. For more information, read this article on [How to protect your backend with AAD](https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-protect-backend-with-aad).
