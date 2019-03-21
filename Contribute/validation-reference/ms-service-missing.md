---
title: ms-service-missing
description: Vysvětlení a řešení problému sestavení ms-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987714"
---
# <a name="ms-service-missing"></a><span data-ttu-id="5813f-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="5813f-103">ms-service-missing</span></span>

<span data-ttu-id="5813f-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="5813f-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5813f-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="5813f-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="5813f-106">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="5813f-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="5813f-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`, ale pokud zadáte `ms.subservice`, musíte také zadat `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="5813f-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="5813f-108">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="5813f-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="5813f-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="5813f-109">Resolution</span></span>

<span data-ttu-id="5813f-110">Ujistěte se, jestli je vámi zadaná hodnota `ms.subservice` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="5813f-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="5813f-111">Potom přidejte příslušnou hodnotu `ms.service`, která je platným nadřazeným objektem pro `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="5813f-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="5813f-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="5813f-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
