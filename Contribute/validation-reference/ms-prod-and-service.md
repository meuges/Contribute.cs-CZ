---
title: ms-prod-and-service
description: Vysvětlení a řešení problému sestavení ms-prod-and-service na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236353"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="3880c-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="3880c-103">ms-prod-and-service</span></span>

## <a name="warning"></a><span data-ttu-id="3880c-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="3880c-104">Warning</span></span>
<span data-ttu-id="3880c-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span><span class="sxs-lookup"><span data-stu-id="3880c-105">https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`</span></span>

## <a name="resolution"></a><span data-ttu-id="3880c-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="3880c-106">Resolution</span></span>

<span data-ttu-id="3880c-107">Vyžaduje se buď `ms.prod`, nebo `ms.service`, ale ne obojí: `ms.prod` se používá pro místní produkty, `ms.service` se používá pro cloudové služby.</span><span class="sxs-lookup"><span data-stu-id="3880c-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="3880c-108">Zjistěte, které z obou polí je pro váš článek to patřičné, ověřte správnost hodnoty a odeberte zbývající pole.</span><span class="sxs-lookup"><span data-stu-id="3880c-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="3880c-109">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="3880c-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="3880c-110">Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="3880c-110">To request new values, follow [this process](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
