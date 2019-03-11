---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459112"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Upozornění

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.

## <a name="resolution"></a>Řešení

Pro nápravu tohoto problému přidejte do souboru nadpis H1 jako první obsah za blokem metadat YML:

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Toto pravidlo se netýká zahrnutých souborů. Pokud se upozornění H1 zobrazí u zahrnutých souborů, budete pravděpodobně muset zahrnuté soubory přesunout do složky `includes`. Složka `includes` se může v cestě k souboru nacházet na libovolné úrovni. Sestavení na webu Docs na základě cesty rozpozná daný soubor jako zahrnutý soubor a ověření H1 se nebudou provádět.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]