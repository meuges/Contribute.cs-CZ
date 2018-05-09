---
title: Jak přispívat na docs.microsoft.com
description: Tento článek poskytuje přehled různých způsobů, jak se dá přispívat k obsahu na web docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a>Jak přispívat na docs.microsoft.com

Existuje několik způsobů, jak se zúčastnit vylepšování obsahu na [docs.microsoft.com](https://docs.microsoft.com):

- Pokud chcete doporučit nové články nebo vylepšit stávající články, můžete [vytvářet problémy](#create-issues) (nadnést problém).
- V online editoru GitHubu můžete dělat malé změny a články [rychle upravovat](#quick-edits).
- [Revizemi konceptů nových článků](#review-new-articles) zajistíte kvalitu a technickou přesnost.
- Pokud chcete sami podpořit rozšiřování obsahu, můžete k důležitým tématům [vytvářet nové články](#create-new-articles).
- [Aktualizací](#update-samples) a [vytvářením](#create-samples) ukázek můžete vylepšovat ukázky kódu, které posilují důležité koncepce.

V tomto článku se seznámíte s různými způsoby přispívání, poznáte, jak se tyto úkoly provádějí, a najdete odkazy na další informace o těchto úkolech.

Naše veřejná úložiště jsou hostovaná na [GitHubu](https://wwww.GitHub.com).  Pokud se chcete na našich úložištích dokumentace podílet, musíte si na GitHubu vytvořit účet.

K aktualizaci dokumentů budete také potřebovat textový editor. Doporučujeme editor [Visual Studio Code](https://www.visualstudio.com/code). Měli byste mít základní znalosti syntaxe jazyka [Markdown](https://daringfireball.net/projects/markdown/syntax).

Pokud chcete přidávat nebo upravovat ukázky, budete potřebovat vývojové prostředí. Pro počítače PC nebo Mac doporučujeme [Visual Studio](https://www.visualstudio.com), pro všechny platformy se hodí [Visual Studio Code](https://www.visualstudio.com/code).

## <a name="create-issues"></a>Vytváření problémů

Pokud v nějakém článku najdete opomenutí nebo nepřesnosti, můžete k tomuto článku vytvořit (nadnést) problém. Správné umístění najdete nejsnadněji tak, že v prohlížeči kliknete na tlačítko Upravit. Tak se dostanete ke zdroji článku ve správném veřejném úložišti GitHubu. Na panelu Adresa pak můžete zjistit adresu URL zdroje článku. Nový problém k článku vytvoříte kliknutím na tlačítko Vytvořit problém.

> [!NOTE]
> Pokud najdete problémy, které se dají opravit malými úpravami, například překlepy nebo gramatické chyby, můžete ušetřit čas sobě i nám tím, že pomocí prohlížeče [odešlete žádost o opravu](#quick-edits) zdroje.

Většina našich veřejných úložišť obsahuje šablony pro nové problémy, které vás povedou při poskytování informací potřebných k opravě problému.

Novými problémy můžete přispívat také v případech, kdy nemůžete najít potřebné informace. Postup je stejný: Vytvoříte nový problém v jednom z veřejných úložišť dokumentů a sdělíte nám, co hledáte, co jste chtěli udělat a proč vám nepomohly články, které jste našli.

## <a name="review-new-articles"></a>Revize nových článků

Pokud pracujete s novým softwarem (nejspíš ve verzi CTP nebo beta), může se stát, že v době, kdy se s touto technologií seznamujete, dokumentaci vytváříme. V našich veřejných úložištích tak můžete najít rozpracované dokumenty. Svými komentáři nám můžete pomoct dokumenty vylepšit, než je vydáme.

Nové články se revidují veřejně – použitím [pracovního postupu GitHubu](https://guides.github.com/introduction/flow/). Podívejte se na libovolné z našich úložišť dokumentů a zkontrolujte otevřené žádosti o přijetí změn. Komentáře a revize k otevřeným žádostem o přijetí změn vítáme. Pomůže nám to publikovat lepší obsah při prvním vydání, místo toho, abychom čekali na vaše názory až po zveřejnění.

Hledáme způsoby, jak vylepšit technickou přesnost, srozumitelnost popisů a mluvnickou správnost.

## <a name="quick-edits"></a>Rychlé úpravy

Rychlé úpravy představují způsob, jak dělat malé opravy pomocí editoru založeného na prohlížeči. Pokud najdete drobné pravopisné nebo gramatické chyby nebo chybné názvy rozhraní API, nemusíte vytvářet problém. Uděláte úpravy a odešlete žádost o přijetí změn.

V libovolném článku klikněte na tlačítko Upravit (obvykle je poblíž pravého horního rohu stránky), udělejte úpravy a klikněte v dolní části stránky na tlačítko Odeslat žádost o přijetí změn. My žádost o přijetí změn v rámci denní revize žádostí zkontrolujeme a začleníme.

## <a name="create-new-articles"></a>Vytváření nových článků

Pokud se vážně zabýváte některými tématy a chcete je vysvětlit ostatním, můžete vytvořit články a odeslat žádosti o přijetí změn.

Vytváření nových článků je časově náročné. Oceňujeme vaše úsilí a příspěvky. Chceme se tohoto procesu od začátku zúčastnit, abychom se ujistili, že dodržujete naše pokyny a styl. Doporučujeme tento postup:

1. [Vytvořte problém](#create-issues), který popisuje, co chybí a jak to chcete řešit.
1. Okomentujte problém – sdělte nám, jak byste na něm chtěli pracovat, a navrhněte osnovu a obsah článku.
1. Budeme reagovat svými návrhy. Ty můžou zahrnovat odkazy na související články, návrhy ukázek nebo způsob uspořádání článku.
1. Až osnovu odsouhlasíme, vytvořte fork úložiště a začněte pracovat.
1. V rané fázi procesu otevřete žádost o přijetí změn s označením „[Rozpracováno]“ na začátku názvu.
1. Jeden z klíčových přispěvatelů vám pošle svůj počáteční názor.
1. Pokračujte v psaní, a až budete připravení na další názory, @-mention osobu, která revidovala první koncept.
1. Až budete připravení na konečnou revizi, odstraňte z názvu „[Rozpracováno]“.
1. Reagujte na názory.
1. Klíčoví přispěvatelé vaši žádost o přijetí změn začlení.

Několik bodů tohoto seznamu stojí za to rozepsat podrobněji. Obecně platí, že v souladu s [pracovním postupem GitHubu](https://guides.github.com/introduction/flow/) revidujeme obsah co nejdříve. Tímto způsobem odsouhlasíme, kde bude článek zařazený v obsahu, co článek přinese čtenářům a na co se zaměří vytvořené ukázky. Můžeme vás tak včas korigovat, než vynaložíte spoustu času na psaní textu.

## <a name="update-samples"></a>Aktualizace ukázek

Některé ukázky můžou být původně napsané pro předchozí verze s použitím již nedoporučovaných postupů. Takové ukázky nám můžete pomoct aktualizovat. Nebo například můžete přijít na to, že jednoduchá změna názvu proměnné může zlepšit srozumitelnost výkladu.

Vzorové (ukázkové) kódy zobrazené v jednotlivých článcích jsou součástí programů, které sestavujeme a často testujeme v systému kontinuální integrace (CI).

Pokud chcete udělat malé aktualizace, najděte zdroj v příslušném úložišti, změňte kód v prohlížeči a odešlete žádost o přijetí změny. Náš systém CI změny sestaví, a až skončí, začlení žádost o přijetí změn.

Pokud chcete udělat rozsáhlejší změny, vytvořte fork úložiště a proveďte změny ve svém oblíbeném vývojovém prostředí. Nezapomeňte přidat nějaké testy, abyste zajistili, že vaše změny budou fungovat, jak mají. Odešlete žádost o přijetí změn a my ji zkontrolujeme.

Při všech změnách kódu dodržujte stávající zásady vzorového (ukázkového) kódu, který upravujete. Naše standardy kódování úložišť ukázek budou odrážet standardy odpovídajících produktových týmů. Řiďte se konkrétními pokyny pro každé úložiště.

> [!NOTE]
> Pracujeme na tom, abychom i my sami tyto pokyny dodržovali. Některé z ukázek jsou staršího data než naše aktuální standardy a zatím se neaktualizovaly. Pracujeme na tom, aby se u všech pracovních, testovaných ukázek zobrazoval jenom aktuální vzorový (ukázkový) kód.

## <a name="create-samples"></a>Vytváření ukázek

Také můžete vytvářet nové ukázky, které předvádějí koncepce nebo scénáře. Každá ukázka musí být doprovázená článkem, který vysvětluje klíčové informace z ukázky.

Pokud vaše nová ukázka doplňuje existující článek, přidejte do tohoto článku odkaz na ukázku. Pokud ne, spolupracujte s námi a [napište článek](#create-new-articles), který bude ukázku doprovázet.

Náš vzorový (ukázkový) kód v každém případě dodržuje zásady kódování používané odpovídajícími produktovými týmy. Jedinou výjimkou je to, že kvůli srozumitelnosti používáme spíše proměnné s explicitně určenými typy než implicitně typované proměnné (deklarované pomocí `var`), když jsou tyto deklarace obsažené v článku.

Postupujte podle postupu pro ukázky, který je nastíněný v dřívější části popisující [nové články](#create-new-articles), abychom mohli kód revidovat v rané fázi vývojového procesu.
