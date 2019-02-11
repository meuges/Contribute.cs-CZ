---
title: ms-component-deprecated
description: Vysvětlení a řešení problému sestavení ms-component-deprecated na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713147"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="2caff-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="2caff-103">ms-component-deprecated</span></span>

<span data-ttu-id="2caff-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="2caff-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2caff-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="2caff-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="2caff-106">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="2caff-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="2caff-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="2caff-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="2caff-108">Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.</span><span class="sxs-lookup"><span data-stu-id="2caff-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="2caff-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="2caff-109">Resolution</span></span>

<span data-ttu-id="2caff-110">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="2caff-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="2caff-111">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="2caff-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="2caff-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="2caff-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
