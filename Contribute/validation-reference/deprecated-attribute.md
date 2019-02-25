---
title: deprecated-attribute
description: Vysvětlení a řešení problému sestavení deprecated-attribute na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322672"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="bceb4-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="bceb4-103">deprecated-attribute</span></span>

<span data-ttu-id="bceb4-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="bceb4-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bceb4-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="bceb4-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="bceb4-106">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="bceb4-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="bceb4-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="bceb4-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="bceb4-108">Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.</span><span class="sxs-lookup"><span data-stu-id="bceb4-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="bceb4-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="bceb4-109">Resolution</span></span>

<span data-ttu-id="bceb4-110">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="bceb4-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="bceb4-111">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="bceb4-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="bceb4-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="bceb4-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
