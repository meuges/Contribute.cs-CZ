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
# <a name="ms-date-missing"></a>ms-date-missing

## <a name="warning"></a>Upozornění

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
