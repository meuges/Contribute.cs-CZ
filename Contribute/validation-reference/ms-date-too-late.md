---
title: ms-date-too-late
description: Vysvětlení a řešení problému sestavení ms-date-too-late na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637384"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Upozornění

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

Atribut `ms.date` se používá k indikaci „aktuálnosti“ – to znamená, kdy byl článek naposledy zkontrolován z hlediska relevance, přesnosti, správných snímků obrazovek a funkčních odkazů. Proto nemůže být v budoucnosti. S pěti dny můžete počítat na dobu vydání – například když je obsah zmrazený kvůli kontrole kvality při přípravě na nějakou důležitou událost.

## <a name="resolution"></a>Řešení

Zadejte `ms.date` ve formátu MM/DD/RRRR. Datum nesmí být od dnešního dne vzdálenější než pět dnů.

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
