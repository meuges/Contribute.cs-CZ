---
title: ms-prod-missing
description: Vysvětlení a řešení problému sestavení ms-prod-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636763"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="fb424-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="fb424-103">ms-prod-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="fb424-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="fb424-104">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="fb424-105">K zadání místních produktů používejte `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="fb424-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="fb424-106">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`, ale pokud zadáte `ms.technology`, musíte také zadat `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="fb424-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="fb424-107">Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="fb424-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="fb424-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="fb424-108">Resolution</span></span>

<span data-ttu-id="fb424-109">Ujistěte se, jestli je vámi zadaná hodnota `ms.technology` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="fb424-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="fb424-110">Potom přidejte příslušnou hodnotu `ms.prod`, která je platným nadřazeným objektem pro `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="fb424-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="fb424-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="fb424-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
