---
title: ms-prod-and-technology-invalid
description: Vysvětlení a řešení problému sestavení ms-prod-and-technology-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713262"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="f3a4f-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="f3a4f-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="f3a4f-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="f3a4f-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="f3a4f-105">Upozornění</span><span class="sxs-lookup"><span data-stu-id="f3a4f-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="f3a4f-106">K zadání místních produktů používejte `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="f3a4f-107">Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="f3a4f-108">Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="f3a4f-109">Buď je neplatná hodnota `ms.prod`, nebo hodnota `ms.technology` netvoří platnou dvojici s `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="f3a4f-110">Řešení</span><span class="sxs-lookup"><span data-stu-id="f3a4f-110">Resolution</span></span>

<span data-ttu-id="f3a4f-111">Ujistěte se, jestli je hodnota `ms.prod` pro váš článek správná.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="f3a4f-112">Pak zvolte platnou hodnotu `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="f3a4f-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="f3a4f-113">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="f3a4f-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
