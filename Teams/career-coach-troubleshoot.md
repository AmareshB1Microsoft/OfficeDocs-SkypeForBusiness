---
title: Troubleshoot Career Coach for Microsoft Teams
author: DaniEASmith
ms.author: danismith
ms.reviewer: norahak
ms.date: 06/06/2023
manager: serdars
ms.topic: article
audience: admin
ms.service: msteams
search.appverid: MET150
description: Learn how to troubleshoot common issues in Career Coach for Microsoft Teams.
ms.localizationpriority: medium
ms.collection: 
  - M365-collaboration
  - m365initiative-edu
  - tier2
appliesto: 
  - Microsoft Teams
---

# Troubleshoot Career Coach for Microsoft Teams

> [!NOTE]
> As of March 2023, customers are no longer able to purchase Career Coach. By June of 2023, Microsoft will stop all support of Career Coach. For more information and to learn how to export your Career Coach data, see [Career Coach Deprecation FAQs](https://download.microsoft.com/download/2/2/1/22167304-368d-417f-8c5b-8eb3129c5e4f/CareerCoachDeprecationFAQ.pdf).
>
> To remove the Career Coach app from your users' Teams clients, follow these instructions.
>
> 1. Sign into the [Teams admin center](https://go.microsoft.com/fwlink/p/?linkid=2066851).
> 2. Expand **Teams apps** in the left-side menu.
> 3. Select **Setup policies** in the menu.
> 4. Select **Global (Org-wide default)** from the policy group list.
> 5. Under **Installed apps**, find **Career Coach**, and select the checkmark next to the app name.
> 6. In the actions utility bar, select **X Remove**.
> 7. Under **Pinned apps**, find **Career Coach**, and select the checkmark next to the app name.
> 8. In the actions utility bar, select **X Remove**.
>
> The Career Coach app is now uninstalled and unpinned from your users' Teams clients.

This article is for education IT admins who need to troubleshoot Career Coach for Microsoft Teams.

Below are the common issues and resolution steps IT admins may take with Career Coach.

## Missing required configuration data

If you see "Career Coach is currently being set up for you to use soon" in the Career Coach experience, **all required configuration data hasn't been added**.

Your institution must have the [LinkedIn connection](career-coach-set-up-steps.md#linkedin-connection-required) fully configured.

Reference the [Career Coach configuration status](career-coach-set-up-steps.md#configuration-status) to see which settings need to be completed.

## Incorrect formatting of Course catalog or Fields of study data

CSVs for course catalog and field of study have required formats and a maximum size of 18 MB.

Reference the Career Coach [course catalog document schema](career-coach-set-up-steps.md#course-catalog-document-format-and-schema) and Career Coach [fields of study document schema](career-coach-set-up-steps.md#fields-of-study-document-format-and-schema) to ensure proper configuration.

Also, a course catalog file shouldn't have more than 15,000 rows to ensure successful processing.

## Missing fields in Career Coach settings pages

Career Coach settings pages have required fields. If necessary fields aren't completed, the page won't submit.

You may not see a warning message, and the page won't submit.

The submission is successful when you see a green banner at the top of the page.

## Setup policy changes aren't complete

If Career Coach isn't showing in Microsoft Teams for users, then the setup policy changes may not have taken effect yet. Career Coach won't be installed and pinned for users in Microsoft Teams until the setup policy changes take effect. Policy changes can take a few hours to take effect.

However, Career Coach can be installed directly from the Microsoft Teams app store.

- If users are unable to find Career Coach in the Microsoft Teams app store, review your app permission policies, and ensure that Career Coach isn't a blocked app.
- Career Coach is a Microsoft app, and it's a best practice to allow Microsoft apps by permission policies. Learn more about [configuring permission policies](teams-app-permission-policies.md).

## Career Coach initialization isn't complete

You may encounter the following error: “We can't retrieve the app's settings. Try again. If you continue to have problems, contact Microsoft customer support.”

Check the **Service Provisioning status** on the [Career Coach settings page](career-coach-set-up-steps.md#career-coach-settings-status).

If your tenant is still being initialized, wait 15 minutes and try again. Open a support ticket if you still receive the error.
