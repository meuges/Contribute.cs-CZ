---
title: ms-date-missing
description: Vysvětlení a řešení problému sestavení ms-date-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637269"
---
# <a name="ms-date-missing"></a><span data-ttu-id="a2524-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="a2524-103">ms-date-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a2524-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="a2524-104">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="a2524-105">Některé skupiny obsahu vyžadují atribut `ms.date`, který určuje „čerstvost“ článku, tzn. kdy byla naposledy zkontrolována jeho relevance, přesnost, správné snímky obrazovek a funkční odkazy.</span><span class="sxs-lookup"><span data-stu-id="a2524-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a2524-106">Není to totéž jako datum posledního *publikování* článku, které se na stránce objeví v případě, že `ms.date` není explicitně zadané.</span><span class="sxs-lookup"><span data-stu-id="a2524-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2524-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="a2524-107">Resolution</span></span>

<span data-ttu-id="a2524-108">Ujistěte se, jestli je článek aktuální a obsah není narušený, a pak přidejte platné datum ve formátu MM/DD/RRRR:</span><span class="sxs-lookup"><span data-stu-id="a2524-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
