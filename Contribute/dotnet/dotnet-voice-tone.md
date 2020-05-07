---
title: Pravidla způsobu vyjadřování v příspěvcích k dokumentaci rozhraní .NET
description: Naučte se pravidla způsobu vyjadřování prostřednictvím příkladů stylu v porovnání s příklady, které tato pravidla nedodržují.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 4108019ac50d703c6dd509eca7a6394cc1c9dc18
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "80625182"
---
# <a name="voice-and-tone-guidelines"></a>Pravidla způsobu vyjadřování

Vaše dokumenty čte celá řada lidí včetně IT specialistů a vývojářů kvůli tomu, aby se něco dozvěděli o rozhraní .NET a mohli ho používat při své práci. Vaším cílem je vytvořit skvělou dokumentaci, která čtenářům v pomůže v jejich snažení. Naše pravidla vám toho umožní dosáhnout. Tento průvodce správným stylem obsahuje následující doporučení:

Při jeho čtení uvidíte příklady jednotlivých doporučení. Při psaní tohoto průvodce jsme tato pravidla dodržovali a nabízíme příklady, které byste při psaní dokumentace k rozhraní .NET měli dodržovat. Součástí průvodce jsou také opačné ukázky, abyste viděli, jak článek vypadá, když tato pravidla nedodržíte.

## <a name="use-a-conversational-tone"></a>Používejte konverzační tón

### <a name="appropriate-style"></a>Vhodný styl

Chceme, aby naše dokumentace měla konverzační tón. Při čtení jakéhokoli z našich výukových kurzů nebo výkladů byste měli mít pocit, že si povídáte s autorem. Znamená to, že byste měli používat neformální, konverzační a informativní styl. Čtenáři by měli mít pocit, jako kdyby poslouchali autora, který jim něco vysvětluje.

### <a name="inappropriate-style"></a>Nevhodný styl

Je možné pozorovat kontrast mezi konverzačním stylem a stylem, který lze nalézt u akademičtějšího zpracování odborných témat. Ačkoli jsou tyto materiály velmi užitečné, psali jejich autoři tyto články značně odlišným stylem, než má naše dokumentace. Při čtení akademického žurnálu si lze povšimnout velice odlišného tónu a zcela odlišného stylu vyjadřování. Lze to přirovnat ke čtení suchého referátu na velmi nezáživné téma.  

První odstavec nahoře dodržuje naše doporučení ohledně konverzačního stylu. Druhý odstavec má akademičtější styl. Rozdílu si hned všimnete. 

## <a name="write-in-second-person"></a>Vyjadřujte se ve druhé osobě

### <a name="appropriate-style"></a>Vhodný styl

Články byste měli psát tak, jako byste mluvili přímo s čtenářem. Často byste měli používat druhou osobu (stejně jako já v těchto dvou větách). To ale neznamená, že musíte pořád používat slovo „vy“. Obracejte se přímo na čtenáře. Pište věty rozkazovacím způsobem. Řekněte čtenáři, co chcete, aby se dozvěděl.

### <a name="inappropriate-style"></a>Nevhodný styl

Autor by se rovněž mohl rozhodnout používat třetí osobu. V takovém případě musí autor najít určité zájmeno nebo podstatné jméno, které použije, když se zmiňuje o čtenáři. Čtenář může často shledat, že styl vyjadřování ve třetí osobě není tak poutavý a čtivý.

První odstavec se řídí naším doporučeným stylem. Ve druhém se používá třetí osoba. Vyjadřujte se prosím ve druhé osobě. Nejspíš zjistíte, že je to mnohem čtivější.

## <a name="use-active-voice"></a>Používejte činný rod

Pište články v činném rodu. Činný rod znamená, že podmět věty je původcem děje (slovesa) této věty. To je rozdíl oproti trpnému rodu, kdy je věta sestavena způsobem, že je podmět cílem děje. Porovnejte tyto dva příklady:

>Kompilátor transformoval zdrojový kód do spustitelného souboru.

>Zdrojový kód byl kompilátorem transformován do zdrojového souboru.

První věta používá činný rod. Druhá věta byla napsána v trpném rodu. (Tyto dvě věty jsou dalším příkladem jednotlivých stylů.)

Doporučujeme používat činný rod, protože je čtivější. Čtení trpného rodu může být obtížnější.

## <a name="target-a-fifth-grade-reading-level"></a>Zaměřte se na úroveň čtení páté třídy

Toto poslední pravidlo souvisí s tím, že rodným jazykem mnoha našich čtenářů není angličtina. Svými články oslovujete mezinárodní publikum. Mějte prosím na paměti, že toto publikum nemusí mít takovou slovní zásobu jako vy.

Pořád ale píšete pro odborníky z technického oboru. Můžete předpokládat, že vaši čtenáři umí programovat a mají specifickou slovní zásobu programovacích pojmů. Objektově orientované programování, třída a objekt, funkce a metoda jsou známé pojmy. Ne každý, kdo čte vaše články, ale musí mít formální vzdělání v informatice. Pojmy jako „idempotentní“ bude nejspíš potřeba definovat, pokud je použijete:

>Metoda `Close()` je idempotentní, což znamená, že ji můžete volat několikrát a výsledek je stejný, jako kdybyste ji volali jednou.

## <a name="avoid-future-tense"></a>Vyhněte se budoucímu času

V některých neanglických jazycích není koncepce budoucího času stejná jako v angličtině. Používání budoucího času může znesnadnit pochopení vašich dokumentů. Při používání budoucího času navíc vyvstává otázka „kdy“. Když tedy řeknete „Znalost PowerShellu se vám bude hodit“, má čtenář samozřejmou otázku „Kdy se mi bude hodit?“ Místo toho jednoduše řekněte „Znalost PowerShellu se vám hodí“.

## <a name="what-is-it---so-what"></a>Co je to?

Kdykoli čtenáři představíte nový pojem, napřed ho definujte a teprve pak vysvětlete, proč je užitečný. Je důležité, aby čtenář věděl, co tento pojem znamená, než dokáže pochopit jeho výhody (nebo něco jiného).
