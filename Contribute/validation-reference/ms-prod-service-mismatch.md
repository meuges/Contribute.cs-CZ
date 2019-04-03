---
title: ms-prod-service-mismatch
description: Vysvětlení a řešení problému sestavení ms-prod-service-mismatch na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636786"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="1a846-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="1a846-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="1a846-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="1a846-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="1a846-105">K zadání místních produktů používejte `ms.prod`, pro cloudové služby používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="1a846-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="1a846-106">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="1a846-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="1a846-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="1a846-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="1a846-108">Nemůžete použít `ms.prod` s `ms.subservice` ani `ms.service` s `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="1a846-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="1a846-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="1a846-109">Resolution</span></span>

<span data-ttu-id="1a846-110">Nejdříve ověřte, jestli jste pro váš článek vybrali správný nadřazený atribut (`ms.prod` nebo `ms.service`).</span><span class="sxs-lookup"><span data-stu-id="1a846-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="1a846-111">Pak přidejte patřičné podřízené pole s platnou spárovanou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="1a846-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="1a846-112">Odeberte všechna nadbytečná pole.</span><span class="sxs-lookup"><span data-stu-id="1a846-112">Remove any extra fields.</span></span>

<span data-ttu-id="1a846-113">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="1a846-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
