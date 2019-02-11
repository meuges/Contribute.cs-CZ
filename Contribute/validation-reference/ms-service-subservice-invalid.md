---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713124"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="e1a29-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="e1a29-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="e1a29-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="e1a29-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="e1a29-105">Upozornění</span><span class="sxs-lookup"><span data-stu-id="e1a29-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="e1a29-106">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="e1a29-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="e1a29-107">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="e1a29-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="e1a29-108">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="e1a29-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="e1a29-109">Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="e1a29-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="e1a29-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="e1a29-110">Resolution</span></span>

<span data-ttu-id="e1a29-111">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="e1a29-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="e1a29-112">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="e1a29-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="e1a29-113">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="e1a29-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
