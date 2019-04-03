---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637292"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="b4812-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="b4812-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b4812-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="b4812-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="b4812-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="b4812-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="b4812-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b4812-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="b4812-107">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="b4812-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="b4812-108">Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="b4812-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4812-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="b4812-109">Resolution</span></span>

<span data-ttu-id="b4812-110">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="b4812-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="b4812-111">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="b4812-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="b4812-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="b4812-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
