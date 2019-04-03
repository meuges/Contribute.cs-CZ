---
title: ms-service-missing
description: Vysvětlení a řešení problému sestavení ms-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636694"
---
# <a name="ms-service-missing"></a><span data-ttu-id="193f3-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="193f3-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="193f3-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="193f3-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="193f3-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="193f3-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="193f3-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`, ale pokud zadáte `ms.subservice`, musíte také zadat `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="193f3-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="193f3-107">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="193f3-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="193f3-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="193f3-108">Resolution</span></span>

<span data-ttu-id="193f3-109">Ujistěte se, jestli je vámi zadaná hodnota `ms.subservice` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="193f3-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="193f3-110">Potom přidejte příslušnou hodnotu `ms.service`, která je platným nadřazeným objektem pro `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="193f3-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="193f3-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="193f3-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
