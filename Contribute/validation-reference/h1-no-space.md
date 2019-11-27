---
title: h1-no-space
description: Vysvětlení a řešení problému sestavení h1-no-space na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7058367a6edd7f663ea42a4fc2e9fafd9cbfb34f
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528961"
---
# <a name="h1-no-space"></a>h1-no-space

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
