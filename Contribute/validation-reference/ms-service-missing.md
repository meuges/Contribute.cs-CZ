---
title: ms-service-missing
description: Vysvětlení a řešení problému sestavení ms-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236497"
---
# <a name="ms-service-missing"></a><span data-ttu-id="3aa2e-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="3aa2e-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="3aa2e-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="3aa2e-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="3aa2e-105">K zadání cloudových služeb používejte `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="3aa2e-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="3aa2e-106">Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`, ale pokud zadáte `ms.subservice`, musíte také zadat `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="3aa2e-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="3aa2e-107">Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="3aa2e-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="3aa2e-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="3aa2e-108">Resolution</span></span>

<span data-ttu-id="3aa2e-109">Ujistěte se, jestli je vámi zadaná hodnota `ms.subservice` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="3aa2e-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="3aa2e-110">Potom přidejte příslušnou hodnotu `ms.service`, která je platným nadřazeným objektem pro `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="3aa2e-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="3aa2e-111">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="3aa2e-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="3aa2e-112">Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="3aa2e-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
