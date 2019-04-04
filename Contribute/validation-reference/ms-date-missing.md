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
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Některé skupiny obsahu vyžadují atribut `ms.date`, který určuje „čerstvost“ článku, tzn. kdy byla naposledy zkontrolována jeho relevance, přesnost, správné snímky obrazovek a funkční odkazy. Není to totéž jako datum posledního *publikování* článku, které se na stránce objeví v případě, že `ms.date` není explicitně zadané.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je článek aktuální a obsah není narušený, a pak přidejte platné datum ve formátu MM/DD/RRRR:

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
