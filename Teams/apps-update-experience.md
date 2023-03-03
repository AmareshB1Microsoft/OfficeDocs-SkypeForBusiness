---
title: Apps update experience in Microsoft Teams
author: ashishguptaiitb
ms.author: guptaashish
manager: prkosh
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-apps
audience: Admin
ms.date: 03/03/2023
ms.collection: 
  - M365-collaboration
f1.keywords: 
  - NOCSH
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: In this article, learn how Microsoft apps, custom apps, and third-party apps in Microsoft Teams are updated and how admins facilitate it.
---

# Role of an admin in upgrading Teams apps

Teams admins can help their end-users get the latest version of the apps. To do so, they accomplish one or both of the following tasks:

* [Update Store apps](#store-app-updates) that are available in Teams store when a new version is provided by the app developer or vendor.
* [Update custom apps](#custom-app-updates) that are available only in your organization when your developer submits a new version.

## Store app updates

For users to install and use an app, they must give permissions to the app to access the required services and information. In most cases, when a new version of an installed app is available in the Teams store, the app is automatically updated for all users. However, a few specific changes in the new version of the app require a user permission again. This repeat user acceptance ensures awareness about the changes such as functionality or access to personal information.

If app developers make one or more the following changes to their apps, then the end-users must approve the update of app.

* Add a bot. Change the ID of the bot using the `botId` property.
* Change the `isNotificationOnly` property of an existing bot that may change the bot's notifications.
* Change `SupportsCalling`, `SupportsVideo`, and `SupportsFiles` properties of an existing bot to add capability to call, play video, and upload or download files.
* Add or remove permissions in authorization.
* Add or remove a messaging extension, add a group tab, add a connector, or add a channel.
* Change parameters in the [`webApplicationInfo`](/microsoftteams/platform/resources/schema/manifest-schema#webapplicationinfo) in the manifest file.

If an app's newer version doesn't require any new permissions and doesn't have changes in the above properties, then it updates to a new version automatically. When updating the app, users must update the app in each scope in which the app is added, for example, in personal, team, chats, and meeting scopes.

If an app's newer version requires new permissions, then the user is prompted to grant their consent for the permissions and update the app. The user can proceed if they have the permissions to update. Otherwise, Teams notifies the user to contact their IT admin.

It isn't possible for you to consent on behalf of your org for a new version of an app, if the new version requires more permissions. When an app updates, users must update the app on their own.

> [!NOTE]
> When any of the above mentioned changes are done in a newer version of an app, then you can't consent on behalf of the users. Each user must individually provide consent for one or more of the above mentioned permissions.

## Custom app updates

Custom apps that are created and deployed within your organization are available to the users on your tenant or organization. Teams admin updates a custom app to its new version when a new version is provided by their organization's developers. For more information, see [how admins manage custom apps](custom-app-overview.md).

For custom apps to update, after you upload the new version of the app to Teams, users must individually provide their consent if it is required.

## Related articles

* [Understand manifest schema for updates done in apps](/microsoftteams/platform/resources/schema/manifest-schema).
* [Know about custom app management](custom-app-overview.md).
