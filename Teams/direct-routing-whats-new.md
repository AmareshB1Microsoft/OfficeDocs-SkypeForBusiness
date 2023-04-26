---
title: What's New Direct Routing
ms.reviewer: CarolynRowe
ms.date: 03/29/2022
author: wlibebe
ms.author: wlibebe
manager: serdars
ms.topic: article
audience: admin
ms.service: msteams
search.appverid: MET150
description: This article describes what's new in Direct Routing. Check back often for updates.
ms.localizationpriority: medium
appliesto: 
  - Microsoft Teams
ms.collection: 
  - M365-voice
  - Tier1
---

# What's new for Direct Routing

This article describes what's new in Direct Routing. Check back often for updates.

## New Direct Routing SIP endpoints 

Microsoft will introduce new signaling IPs to Teams Direct Routing SIP endpoints. To ensure this change doesn’t affect your service availability, make sure your Session Border Controller and Firewall are configured to use the recommended subnets 52.112.0.0/14 and 52.122.0.0/15 for classification and ACL rules. For more information, see [Microsoft 365, Office 365, and Office 365 GCC environments](direct-routing-plan.md#microsoft-365-office-365-and-office-365-gcc-environments).  

## Trunk demoting logic based on SIP Options

A new feature based on SIP Options is introduced for trunk health. When enabled in the gateway configuration (see Set-CsOnlinePSTNGateway cmdlet and SendSipOptions parameter), the routing logic for outbound calls demotes trunks that don't send SIP Options periodically (expected period is one SIP Option sent by the SBC per minute) to the Microsoft backend. These demoted trunks are put to the end of trunks list available for the outbound call and are tried last, which potentially decreases the call setup time.
Any trunk enabled for that feature that doesn't send at least one SIP Option within five minutes to any of the Microsoft regional (NOAM, EMEA, APAC, OCEA) SIP Proxies is considered demoted. If a trunk sends SIP Options to only a subset of Microsoft regional SIP Proxies, then these routes are tried first and the rest are demoted.
> [!NOTE] 
>
> Any SBC (configured under the customer or carrier tenant with **SendSipOptions** set to *true*) not sending SIP OPTIONS will be demoted. Customers who don't want that behavior should set **SendSipOptions** to *false* in their SBC configuration. The same applies to carrier trunks where the SBC configuration is either under the carrier or customer tenant. In these cases, when **SendSipOptions** is set to *true*, the SBC sends SIP OPTIONS.


## SIP support

On June 1, 2022, Microsoft will remove support for sip-all.pstnhub.microsoft.com and sip-all.pstnhub.gov.teams.microsoft.us FQDNs from Direct Routing configuration.

If no actions are taken before June 1, users won't be able to make or receive calls via Direct Routing.

To prevent service impact:

- Use the recommended subnets: (52.112.0.0/14 and 52.120.0.0/14) for any classification or ACL rules.
- Discontinue use of the sip-all FQDN when configuring Session Border Controls for  Direct Routing.

For more information, see [Plan Direct Routing](direct-routing-plan.md).
> [!NOTE]
> IP ranges presented in this document are specific to Direct Routing and may differ from the ones advised for Teams client.

## TLS certificates

Microsoft 365 is updating Teams and other services to use a different set of Root Certificate Authorities (CAs).

For more information and a full list of affected services, see [TLS certificate changes to Microsoft 365 services including Microsoft Teams](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/tls-certificate-changes-to-microsoft-365-services-including/ba-p/3249676).

## Certificate authorities

Beginning February 1, 2022, the Direct Routing SIP interface will only trust certificates signed by Certificate Authorities (CAs) that are part of the Microsoft Trusted Root Certificate Program. Take the following steps to avoid service impact:

- Ensure that your SBC certificate is signed by a CA that is part of the Microsoft Trusted Root Certificate Program.
- Verify that the Extended Key Usage (EKU) extension of your certificate includes "Server Authentication".

For more information about the Microsoft Trusted Root Certificate Program, see [Program Requirements - Microsoft Trusted Root Program](/security/trusted-root/program-requirements).

For a Trusted CA list, see [Microsoft Included CA Certificate List](https://ccadb-public.secure.force.com/microsoft/IncludedCACertificateReportForMSFT).

## Replace headers

Starting April 2022, Direct Routing will reject SIP requests that have Replaces headers defined. There are no changes to flows where Microsoft sends Replaces header to the Session Border Controller(SBC).

Check your SBC configurations and ensure sure that you aren't using Replaces headers in SIP requests.

## TLS1.0 and 1.1

To provide the best-in-class encryption to our customers, Microsoft plans to deprecate Transport Layer Security (TLS) versions 1.0 and 1.1. On April 3, 2022, Microsoft will force TLS1.2 usage for the Direct Routing SIP interface.

To avoid any service impact, ensure that your SBCs are configured to support TLS1.2 and can connect using one of the following cipher suites:

- TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 i.e. ECDHE-RSA-AES256-GCM-SHA384
- TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256 i.e. ECDHE-RSA-AES128-GCM-SHA256
- TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384 i.e. ECDHE-RSA-AES256-SHA384
- TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256 i.e. ECDHE-RSA-AES128-SHA256

## Related topics

- [Direct Routing - SIP protocol](direct-routing-protocols-sip.md)
