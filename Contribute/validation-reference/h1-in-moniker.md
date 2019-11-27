---
title: h1-in-moniker
description: Vysvětlení a řešení problému sestavení h1-in-moniker na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528830"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

## <a name="warning"></a>Upozornění

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem. Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu. V každém souboru může být jenom jeden nadpis H1. V oddílech monikerů nejsou nadpisy H1 povolené, protože můžou snadno vést k duplicitám nebo chybějícím nadpisům H1 podle toho, jak je nakonfigurovaná správa verzí.

Tato zpráva se také může zobrazit, pokud oddíl monikeru obsahuje řádek stejných znaků, které tvoří dvojité podtržení. Příklad: `=======`. Jde o alternativní syntaxi jazyka Markdown pro nadpis H1. Často se s ní můžeme setkat u konfliktů při sloučení:

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Řešení

Tento problém opravíte tak, že nadpisy H1 odeberete ze všech oddílů a zajistíte, aby nadpis H1 na začátku článku odpovídal všem oddílům monikerů. Upozorňujeme, že přeskakování úrovní nadpisů (třeba H3 po H1) je zakázané.

Pokud nadpis H1 v oddílu monikeru znamená ve skutečnosti dvojité podtržení (`=======`), podle potřeby ho buď odeberte,nebo ho nahraďte nadpisem hashtag, například `##`. Pokud je dvojité podtržení součástí konfliktu při sloučení, nezapomeňte odebrat také počáteční a koncové značky konfliktu při sloučení a zastaralý text.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
