---
title: ms-prod-or-service-missing
description: Vysvětlení a řešení problému sestavení ms-prod-or-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987553"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="9bbf7-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="9bbf7-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="9bbf7-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="9bbf7-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9bbf7-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="9bbf7-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="9bbf7-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="9bbf7-106">Resolution</span></span>

<span data-ttu-id="9bbf7-107">Vyžaduje se buď `ms.prod`, nebo `ms.service`, ale ne obojí: `ms.prod` se používá pro místní produkty, `ms.service` se používá pro cloudové služby.</span><span class="sxs-lookup"><span data-stu-id="9bbf7-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="9bbf7-108">Zjistěte, které z obou polí je pro váš článek to patřičné, ověřte správnost hodnoty a odeberte zbývající pole.</span><span class="sxs-lookup"><span data-stu-id="9bbf7-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="9bbf7-109">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="9bbf7-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]