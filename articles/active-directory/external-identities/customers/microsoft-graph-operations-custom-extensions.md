---
title: Manage custom extension resources with Microsoft Graph
description: Learn how to manage custom extension resources in an Azure AD for customers tenant by calling the Microsoft Graph API and using an application identity to automate the process.
services: active-directory
author: garrodonnell
manager: celested
ms.author: godonnell
ms.service: active-directory
ms.workload: identity
ms.subservice: ciam
ms.topic: how-to
ms.date: 05/23/2023
ms.custom: developer

#Customer intent: As a dev, devops, I want to learn how to use the Microsoft Graph to manage custom extension operations in my Azure AD customer tenant.
---

# Manage Azure Active Directory (AD) for customers custom extension resources with Microsoft Graph

Using the Microsoft Graph API allows you to manage resources in your Azure AD for customers directory. The following Microsoft Graph API operations are supported for the management of resources related to custom extensions. Each link in the following sections targets the corresponding page within the Microsoft Graph API reference for that operation.

[!INCLUDE [preview-alert](../customers/includes/preview-alert/preview-alert-ciam.md)]

> [!NOTE]
> You can also programmatically create an Azure AD for customers directory itself, along with the corresponding Azure resource linked to an Azure subscription. This functionality isn't exposed through the Microsoft Graph API, but through the Azure REST API. For more information, see [Directory Tenants - Create Or Update](/rest/api/azurestack/directory-tenants/create-or-update).
## Custom authentication extensions (Preview)

Custom authentication extensions define interactions with external systems during a user authentication session. This is an abstract type that's inherited by the onTokenIssuanceStartCustomExtension derived type.

- [List custom authentication extensions](/graph/api/identitycontainer-list-customauthenticationextensions)
- [Create custom authentication extension](/graph/api/identitycontainer-post-customauthenticationextensions)
- [Get custom authentication extension](/graph/api/customauthenticationextension-get)
- [Update custom authentication extension](/graph/api/customauthenticationextension-update)
- [Delete custom authentication extension](/graph/api/customauthenticationextension-delete)

## How to programmatically manage Microsoft Graph

When you want to manage Microsoft Graph, you can either do it as the application using the application permissions, or you can use delegated permissions. For delegated permissions, either the user or an administrator consents to the permissions that the app requests. The app is delegated with the permission to act as a signed-in user when it makes calls to the target resource. Application permissions are used by apps that do not require a signed in user present and thus require application permissions. Because of this, only administrators can consent to application permissions.

> [!NOTE]
> Delegated permissions for users signing in through user flows or custom policies cannot be used against delegated permissions for Microsoft Graph API.
## Next steps

- To learn more about the Microsoft Graph API, see [Microsoft Graph overview](/graph/overview). 