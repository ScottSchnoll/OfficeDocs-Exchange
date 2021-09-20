---
ms.localizationpriority: medium
description:  Office Config Service endpoint is not reachable
ms.topic: reference
author: joannehendrickson
ms.custom:
- ms-exch-setupreadiness-KB2999226NotInstalled
ms.author: jhendr
ms.reviewer: 
title: Office Config Service endpoint is not reachable
ms.collection: exchange-server
f1.keywords:
- CSH
audience: ITPro
ms.prod: exchange-server-it-pro
manager: serdars
---
#  Office Config Service endpoint is not reachable

::: moniker range="exchserver-2016"

Microsoft Exchange Server 2016 Setup displayed this warning because Setup failed to connect to the Office Config Service from the local computer. 

Exchange 2016 setup (for the September 2021 CU and later versions) installs the Exchange Emergency Mitigation (EM) service. The EM service checks for available mitigations every hour before downloading and applying them. 

::: moniker-end

::: moniker range="exchserver-2019"
Microsoft Exchange Server 2019 Setup displayed this warning because Setup failed to connect to the Office Config Service from the local computer. 

Exchange 2019 setup (for September 2021 CU and later versions) installs the Exchange Emergency Mitigation (EM) service. The EM service checks for available mitigations every hour before downloading and applying them. 

::: moniker-end

The functionality to check and download mitigations requires outbound connectivity to the Office Config Service. Without this connectivity, the EM service can’t function, which can pose a security risk. 

For the EM service to function correctly, admins need to enable connectivity to the following endpoint from the Exchange Server.


|Required|Address|Port|
|:-----|:-----|:-----|:-----|
|Yes|officeclient.microsoft.com/*|443|

**Having problems?** Ask for help in the Exchange forums. Visit the forums at: [Exchange Server](https://social.technet.microsoft.com/forums/office/home?category=exchangeserver)
