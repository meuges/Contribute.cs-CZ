---
title: h1-empty
description: Vysvětlení a řešení problému sestavení h1-empty na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427277"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Upozornění

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