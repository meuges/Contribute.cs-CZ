---
title: ms-date-too-late
description: Vysvětlení a řešení problému sestavení ms-date-too-late na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431477"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="e18c1-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="e18c1-103">ms-date-too-late</span></span>

<span data-ttu-id="e18c1-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="e18c1-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="e18c1-105">Upozornění</span><span class="sxs-lookup"><span data-stu-id="e18c1-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="e18c1-106">Atribut `ms.date` se používá k indikaci „aktuálnosti“ – to znamená, kdy byl článek naposledy zkontrolován z hlediska relevance, přesnosti, správných snímků obrazovek a funkčních odkazů.</span><span class="sxs-lookup"><span data-stu-id="e18c1-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="e18c1-107">Proto nemůže být v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="e18c1-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="e18c1-108">S pěti dny můžete počítat na dobu vydání – například když je obsah zmrazený kvůli kontrole kvality při přípravě na nějakou důležitou událost.</span><span class="sxs-lookup"><span data-stu-id="e18c1-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="e18c1-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="e18c1-109">Resolution</span></span>

<span data-ttu-id="e18c1-110">Zadejte `ms.date` ve formátu MM/DD/RRRR. Datum nesmí být od dnešního dne vzdálenější než pět dnů.</span><span class="sxs-lookup"><span data-stu-id="e18c1-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
