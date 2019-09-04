---
title: deprecated-attribute
description: Vysvětlení a řešení problému sestavení deprecated-attribute na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236232"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="ce0cb-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="ce0cb-103">deprecated-attribute</span></span>

## <a name="warning"></a><span data-ttu-id="ce0cb-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="ce0cb-104">Warning</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="ce0cb-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="ce0cb-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="ce0cb-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="ce0cb-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="ce0cb-107">Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.</span><span class="sxs-lookup"><span data-stu-id="ce0cb-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce0cb-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="ce0cb-108">Resolution</span></span>

<span data-ttu-id="ce0cb-109">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="ce0cb-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="ce0cb-110">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="ce0cb-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="ce0cb-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="ce0cb-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
