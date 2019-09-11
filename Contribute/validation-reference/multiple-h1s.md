---
title: multiple-h1
description: Vysvětlení a řešení problému sestavení multiple-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848604"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu. V každém souboru může být jenom jeden nadpis H1.

## <a name="resolution"></a>Řešení

Pro nápravu tohoto problému změňte úroveň dalších nadpisů H1 na H2 (`##`) nebo reorganizujte soubor jiným způsobem. Upozorňujeme, že přeskakování úrovní nadpisů (například nadpis H1, za kterým následuje nadpis H3) není povoleno.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]