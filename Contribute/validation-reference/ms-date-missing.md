---
title: ms-date-missing
description: Vysvětlení a řešení problému sestavení ms-date-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431454"
---
# <a name="ms-date-missing"></a><span data-ttu-id="30014-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="30014-103">ms-date-missing</span></span>

<span data-ttu-id="30014-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="30014-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="30014-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="30014-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="30014-106">Toto datum se používá k indikaci „aktuálnosti“ – to znamená, kdy byl článek naposledy zkontrolován z hlediska relevance, přesnosti, správných snímků obrazovek a funkčních odkazů.</span><span class="sxs-lookup"><span data-stu-id="30014-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="30014-107">Není to totéž jako datum posledního *publikování* článku, které se na stránce objeví v případě, že `ms.date` není explicitně zadané.</span><span class="sxs-lookup"><span data-stu-id="30014-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="30014-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="30014-108">Resolution</span></span>

<span data-ttu-id="30014-109">Ujistěte se, jestli je článek aktuální a obsah není narušený, a pak přidejte platné datum ve formátu MM/DD/RRRR:</span><span class="sxs-lookup"><span data-stu-id="30014-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
