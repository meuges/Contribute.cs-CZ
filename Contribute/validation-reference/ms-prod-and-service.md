---
title: ms-prod-and-service
description: Vysvětlení a řešení problému sestavení ms-prod-and-service na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b685144e92485df2dddb9bdda09fea47d75f588f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987668"
---
# <a name="ms-prod-and-service"></a><span data-ttu-id="0e9c9-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="0e9c9-103">ms-prod-and-service</span></span>

<span data-ttu-id="0e9c9-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="0e9c9-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0e9c9-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="0e9c9-105">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="0e9c9-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="0e9c9-106">Resolution</span></span>

<span data-ttu-id="0e9c9-107">Vyžaduje se buď `ms.prod`, nebo `ms.service`, ale ne obojí: `ms.prod` se používá pro místní produkty, `ms.service` se používá pro cloudové služby.</span><span class="sxs-lookup"><span data-stu-id="0e9c9-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="0e9c9-108">Zjistěte, které z obou polí je pro váš článek to patřičné, ověřte správnost hodnoty a odeberte zbývající pole.</span><span class="sxs-lookup"><span data-stu-id="0e9c9-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="0e9c9-109">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0e9c9-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
