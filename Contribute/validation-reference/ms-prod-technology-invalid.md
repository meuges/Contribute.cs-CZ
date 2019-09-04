---
title: ms-prod-and-technology-invalid
description: Vysvětlení a řešení problému sestavení ms-prod-and-technology-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236329"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="67fec-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="67fec-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="67fec-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="67fec-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="67fec-105">K zadání místních produktů používejte `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="67fec-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="67fec-106">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="67fec-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="67fec-107">Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="67fec-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="67fec-108">Buď je neplatná hodnota `ms.prod`, nebo hodnota `ms.technology` netvoří platnou dvojici s `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="67fec-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="67fec-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="67fec-109">Resolution</span></span>

<span data-ttu-id="67fec-110">Ujistěte se, jestli je hodnota `ms.prod` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="67fec-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="67fec-111">Pak zvolte platnou hodnotu `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="67fec-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="67fec-112">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="67fec-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="67fec-113">Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="67fec-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
