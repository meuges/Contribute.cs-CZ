---
title: h1-empty
description: Vysvětlení a řešení problému sestavení h1-empty na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 691d72a3aee9204ba3fe55a398e954c7719f3680
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848549"
---
# <a name="h1-empty"></a>h1-empty

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`H1 is required. Add content to your top-level heading.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.

## <a name="resolution"></a>Řešení

Pro nápravu tohoto problému zajistěte, aby nadpis H1 obsahoval text, ne pouze znak hash.

Chybně:

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Správně:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]