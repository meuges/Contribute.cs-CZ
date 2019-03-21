---
title: ms-prod-missing
description: Vysvětlení a řešení problému sestavení ms-prod-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987691"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="6a8ec-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="6a8ec-103">ms-prod-missing</span></span>

<span data-ttu-id="6a8ec-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="6a8ec-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6a8ec-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="6a8ec-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="6a8ec-106">K zadání místních produktů používejte `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="6a8ec-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="6a8ec-107">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`, ale pokud zadáte `ms.technology`, musíte také zadat `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="6a8ec-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="6a8ec-108">Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="6a8ec-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="6a8ec-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="6a8ec-109">Resolution</span></span>

<span data-ttu-id="6a8ec-110">Ujistěte se, jestli je vámi zadaná hodnota `ms.technology` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="6a8ec-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="6a8ec-111">Potom přidejte příslušnou hodnotu `ms.prod`, která je platným nadřazeným objektem pro `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="6a8ec-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="6a8ec-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="6a8ec-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
