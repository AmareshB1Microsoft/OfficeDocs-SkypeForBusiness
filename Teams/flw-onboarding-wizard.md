---
title: Use the Frontline Worker onboarding wizard to get your frontline workforce up and running
author: lanachin
ms.author: v-lanachin
ms.reviewer: aaglick
manager: samanro
ms.topic: article
audience: admin
ms.service: msteams
search.appverid: MET150
description: Learn how to use the Frontline Worker onboarding wizard to quickly deploy an experience in Teams that's tailored to frontline workers and managers in your organization.
ms.localizationpriority: medium
ms.collection: 
  - M365-collaboration
  - Teams_ITAdmin_FLW
appliesto: 
  - Microsoft Teams
---

# Use the Frontline Worker onboarding wizard to get your frontline workforce up and running

> [!NOTE]
> Don't see this feature yet? It's currently being rolled out and might not be available in your organization yet. To stay on top of upcoming Teams features, check out the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=microsoft%2Cteams).

## Overview

The Frontline Worker onboarding wizard in the Microsoft 365 admin center simplifies onboarding frontline workers to your organization. The wizard lets you quickly deploy an experience in Microsoft Teams that's tailored to your frontline workforce. Using the wizard, you can easily kick off your pilot deployment of Teams for the frontline workers in your organization.

The wizard sets up a team for your frontline workers and assigns licenses and [policy packages](manage-policy-packages.md) to each team member. You can create your team from scratch or from a [team template](get-started-with-teams-templates-in-the-admin-console.md), and then you add users and assign roles. The role determines the policy package that the wizard assigns to each user.

Currently, the wizard supports adding 100 users each time you run it. We're working on increasing the number of users per run soon. Check back here for the latest updates.

The wizard is available to all organizations that have at least one Microsoft 365 F license. You can run the wizard as many times as you need to roll out Teams to your frontline workforce in different locations or sites across your organization.

> [!NOTE]
> This wizard lets you quickly onboard your frontline workers to Teams through the Microsoft 365 admin center. For more information about how deploy Teams to your frontline workers using scripts, see [How to provision Teams at scale for Frontline Workers](flw-scripted-deployment.md).

## Run the wizard

1. In the left navigation of the [Microsoft 365 admin center](https://admin.microsoft.com/), choose **Setup**. Go to the **Apps and email** section, and then under **Get your frontline workforce up and running**, select **View**. Here, you can learn more about the capabilities that Microsoft 365 for frontline workers offers.

    :::image type="content" source="media/flw-onboarding-wizard-get-started.png" alt-text="Screenshot of the details page for the Frontline Worker onboarding experience in the Microsoft 365 admin center":::

2. When you're ready, select **Get started** to run the wizard.

3. Enter a name for your team, add one or more team owners, and select a privacy setting. Then, choose whether to create your team from scratch or from a team template. Team templates come with predefined channels and tabs, which optimize the team for a particular business need or project.

    :::image type="content" source="media/flw-onboarding-wizard-set-up-team.png" alt-text="Screenshot of the Set up a team page of the wizard":::

4. Add users to the team. You can also add groups. If you add groups, keep in mind that licenses and policy packages are directly assigned to each user in the group, not the group itself.

    :::image type="content" source="media/flw-onboarding-wizard-add-users.png" alt-text="Screenshot of the Add users page of the wizard where you add users and groups to your team":::

5. Assign one of the following roles to each team member: Frontline Worker, Frontline Manager, None. 
  
    :::image type="content" source="media/flw-onboarding-wizard-assign-roles.png" alt-text="Screenshot of the Assign job roles page of the wizard where you assign roles, locations, and licenses to team members":::

    By assigning a Frontline Worker or Frontline Manager role, that user will receive a policy package. The policy package will create an experience in Teams that's tailored to their role. This experience includes pre-pinned apps and policies for healthy frontline worker and manager communication and collaboration.

    Next, select a location and assign a Microsoft 365 F license to each team member. If you don’t have enough licenses, you can select **Buy more licenses** to purchase more licenses.  

6. Choose who receives the status email after the wizard is completed. The email contains success and failure information about the actions performed by the wizard&mdash;creating the team, adding team members, and assigning a license and policy package to each team member. Use this information to troubleshoot any errors that may occur.

    :::image type="content" source="media/flw-onboarding-wizard-email-recipients.png" alt-text="Screenshot of the Add status email recipients page of the wizard":::

7. Review your selections, and then select **Confirm**.

    :::image type="content" source="media/flw-onboarding-wizard-review-team.png" alt-text="Screenshot of the Review team page of the wizard where you review your team settings":::

    The wizard creates your team and assigns licenses and policy packages to team members. This may take a few minutes to complete, after which the recipients you chose receive a status email.

8. You're on your way but you're not done yet! Next, check out the [What to do after running the wizard](#what-to-do-after-running-the-wizard) section of this article.

## What to do after running the wizard

After you run the wizard, it's important to:

- Let your frontline workers and managers know that they're assigned Teams licenses.
- If you're using shared devices, make sure Teams is installed on those devices. If your organization uses a "bring your own device" model, let your frontline workers and managers know that they have to download and install Teams to their devices.

When the frontline employee opens Teams for the first time, they'll receive a tailored first run experience, which includes chats and channels, calling, and task management all within Teams.

## Related articles

- [Manage policy packages in Teams](manage-policy-packages.md)
- [Use team templates in the Teams admin center](get-started-with-teams-templates-in-the-admin-console.md)