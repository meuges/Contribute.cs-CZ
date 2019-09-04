---
title: ms-prod-missing
description: Vysvětlení a řešení problému sestavení ms-prod-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236302"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="23fb5-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="23fb5-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="23fb5-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="23fb5-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="23fb5-105">K zadání místních produktů používejte `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="23fb5-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="23fb5-106">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`, ale pokud zadáte `ms.technology`, musíte také zadat `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="23fb5-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="23fb5-107">Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="23fb5-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="23fb5-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="23fb5-108">Resolution</span></span>

<span data-ttu-id="23fb5-109">Ujistěte se, jestli je vámi zadaná hodnota `ms.technology` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="23fb5-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="23fb5-110">Potom přidejte příslušnou hodnotu `ms.prod`, která je platným nadřazeným objektem pro `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="23fb5-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="23fb5-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="23fb5-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="23fb5-112">Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="23fb5-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
