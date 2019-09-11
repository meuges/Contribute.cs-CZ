---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848473"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

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