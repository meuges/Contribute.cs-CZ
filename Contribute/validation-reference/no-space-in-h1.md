---
title: no-space-in-h1
description: Vysvětlení a řešení problému sestavení no-space-in-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427314"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Upozornění

`A space is required after the hash (#) in H1.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu. Pokud za znakem hash není mezera, web Docs nerozpozná nadpis H1.

## <a name="resolution"></a>Řešení

Tuto chybu opravíte tak, že v nadpisu H1 za znak hash přidáte mezeru.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]