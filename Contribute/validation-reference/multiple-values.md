---
title: multiple-values
description: Vysvětlení a řešení problému sestavení multiple-values na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899652"
---
# <a name="multiple-values"></a>multiple-values

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

Zadali jste více hodnot atributu, u kterého je povolena jen jedna hodnota.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Atributy, které nemůžou mít více hodnot, je potřeba zadávat ve formátu YML s jednou (tj. skalární) hodnotou.

## <a name="resolution"></a>Řešení

Tento návrh se vám zobrazí vždy, když pro atribut s jednou hodnotou použijete pole více hodnot, ať už toto pole obsahuje více hodnot, nebo jen jedinou.

U atributů s více hodnotami, jako je `ms.custom`, podporuje jazyk YML následující formáty polí:

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Tyto formáty nejsou platné pro atributy s jednou hodnotou, jako je `author`.

Pokud jste zadali více hodnot, zkontrolujte je a určete, která je správná. Odeberte ostatní hodnoty a správnou hodnotu zadejte bez závorek na stejný řádek jako atribut, takto:

```yml
---
author: meganbradley
---
```

Pokud jste použili pole s jednou hodnotou, změňte ho na skalární formát popsaný výše.

## <a name="attributes-in-scope"></a>Kterých atributů se to týká

Následující atributy musí mít jenom jednu hodnotu:

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
