---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987631"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="e3c62-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="e3c62-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="e3c62-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="e3c62-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="e3c62-105">Upozornění</span><span class="sxs-lookup"><span data-stu-id="e3c62-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="e3c62-106">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="e3c62-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="e3c62-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="e3c62-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="e3c62-108">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="e3c62-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="e3c62-109">Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="e3c62-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="e3c62-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="e3c62-110">Resolution</span></span>

<span data-ttu-id="e3c62-111">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="e3c62-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="e3c62-112">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="e3c62-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="e3c62-113">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="e3c62-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
