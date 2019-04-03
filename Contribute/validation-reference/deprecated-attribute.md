---
title: deprecated-attribute
description: Vysvětlení a řešení problému sestavení deprecated-attribute na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636878"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="46b09-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="46b09-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="46b09-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="46b09-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="46b09-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="46b09-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="46b09-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="46b09-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="46b09-107">Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.</span><span class="sxs-lookup"><span data-stu-id="46b09-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="46b09-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="46b09-108">Resolution</span></span>

<span data-ttu-id="46b09-109">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="46b09-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="46b09-110">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="46b09-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="46b09-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="46b09-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
