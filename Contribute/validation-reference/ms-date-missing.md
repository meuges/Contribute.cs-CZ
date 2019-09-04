---
title: ms-date-missing
description: Vysvětlení a řešení problému sestavení ms-date-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb352552c133a77ec003bb54f3ab0f3bddfa1be6
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236228"
---
# <a name="ms-date-missing"></a><span data-ttu-id="055fe-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="055fe-103">ms-date-missing</span></span>

## <a name="warning"></a><span data-ttu-id="055fe-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="055fe-104">Warning</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="055fe-105">Některé skupiny obsahu vyžadují atribut `ms.date`, který určuje „čerstvost“ článku, tzn. kdy byla naposledy zkontrolována jeho relevance, přesnost, správné snímky obrazovek a funkční odkazy.</span><span class="sxs-lookup"><span data-stu-id="055fe-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="055fe-106">Není to totéž jako datum posledního *publikování* článku, které se na stránce objeví v případě, že `ms.date` není explicitně zadané.</span><span class="sxs-lookup"><span data-stu-id="055fe-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="055fe-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="055fe-107">Resolution</span></span>

<span data-ttu-id="055fe-108">Ujistěte se, jestli je článek aktuální a obsah není narušený, a pak přidejte platné datum ve formátu MM/DD/RRRR:</span><span class="sxs-lookup"><span data-stu-id="055fe-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
