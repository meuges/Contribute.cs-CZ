---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528868"
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
> Toto pravidlo se netýká zahrnutých souborů. Pokud se v zahrnutých souborech zobrazí výsledky představující nadpisy H1, budete pravděpodobně muset zahrnuté soubory přesunout do složky `includes`. Složka `includes` se může v cestě k souboru nacházet na libovolné úrovni. Sestavení na webu Docs na základě cesty rozpozná daný soubor jako zahrnutý soubor a ověření H1 se nebudou provádět.
>
> Běžnou příčinou chybějících nadpisů H1 v nadřazených souborech je chybné použití zahrnutých souborů: H1 je v zahrnutém souboru, ne v nadřazeném souboru. To není povoleno, protože použití nadpisu H1 v zahrnutém souboru znamená, že v nadřazených souborech budou duplicitní nadpisy H1 nebo bude zahrnutý soubor použitý jen jednou. Nadpisy H1 by měly být v rámci sady obsahu jedinečné a zahrnuté soubory by se měly používat jen ke sdílení obsahu mezi více soubory. Pokud se zobrazí výsledky `h1-missing`, protože se nadpis H1 nachází v zahrnutém souboru, dá se to vyřešit přesunutím nadpisu – a veškerého zahrnutého obsahu, pokud je zahrnutý soubor použitý jen jednou – do nadřazeného souboru. Další informace o zahrnutých souborech v dokumentaci najdete v interním článku Microsoftu o [zahrnování opakovaně použitelného obsahu do článků](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
