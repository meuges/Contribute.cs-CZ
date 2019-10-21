---
title: multiple-h1
description: Vysvětlení a řešení problému sestavení multiple-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246274"
---
# <a name="multiple-h1"></a>multiple-h1

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu. V každém souboru může být jenom jeden nadpis H1.

Tato zpráva se také může zobrazit, pokud článek obsahuje řádek stejných znaků, které tvoří dvojité podtržení, například: `=======`. Jde o alternativní syntaxi jazyka Markdown pro nadpis H1. Často se s ní můžeme setkat u konfliktů při sloučení:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Řešení

Pro nápravu tohoto problému změňte úroveň dalších nadpisů H1 na H2 (`##`) nebo reorganizujte soubor jiným způsobem. Upozorňujeme, že přeskakování úrovní nadpisů (třeba H3 po H1) je zakázané.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

Pokud další nadpis H1 ve skutečnosti představuje dvojité podtržení (`=======`), podle potřeby ho buď odeberte, nebo ho nahraďte nadpisem hashtag, jako je například `##`. Pokud je dvojité podtržení součástí konfliktu při sloučení, nezapomeňte odebrat také počáteční a koncové značky konfliktu při sloučení a zastaralý text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
