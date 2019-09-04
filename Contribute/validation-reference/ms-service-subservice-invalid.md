---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236529"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="fbb41-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="fbb41-103">ms-service-and-subservice-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="fbb41-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="fbb41-104">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="fbb41-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="fbb41-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="fbb41-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="fbb41-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="fbb41-107">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="fbb41-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="fbb41-108">Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="fbb41-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="fbb41-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="fbb41-109">Resolution</span></span>

<span data-ttu-id="fbb41-110">Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="fbb41-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="fbb41-111">Pak zvolte platnou hodnotu `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="fbb41-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="fbb41-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="fbb41-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="fbb41-113">Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="fbb41-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
