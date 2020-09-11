---
title: Pravidla způsobu vyjadřování v příspěvcích k dokumentaci rozhraní .NET
description: Naučte se pravidla způsobu vyjadřování prostřednictvím příkladů stylu v porovnání s příklady, které tato pravidla nedodržují.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 6f74eb9107612edfff76831fa4dea4f90e73d050
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559210"
---
# <a name="voice-and-tone-guidelines"></a>Pravidla způsobu vyjadřování

Vaše dokumenty čte celá řada lidí včetně IT specialistů a vývojářů kvůli tomu, aby se něco dozvěděli o rozhraní .NET a mohli ho používat při své práci. Vaším cílem je vytvořit skvělou dokumentaci, která čtenářům v pomůže v jejich snažení. Naše pravidla vám toho umožní dosáhnout. Tento průvodce správným stylem obsahuje následující doporučení:

## <a name="use-a-conversational-tone"></a>Používejte konverzační tón

Následující odstavec je napsaný v konverzačním stylu. Ten, který následuje, má akademičtější styl.

### <a name="appropriate-style"></a>Vhodný styl

Chceme, aby naše dokumentace měla konverzační tón. Při čtení jakéhokoli z našich výukových kurzů nebo výkladů byste měli mít pocit, že si povídáte s autorem. Znamená to, že byste měli používat neformální, konverzační a informativní styl. Čtenáři by měli mít pocit, jako kdyby poslouchali autora, který jim něco vysvětluje.

### <a name="inappropriate-style"></a>Nevhodný styl

Je možné pozorovat kontrast mezi konverzačním stylem a stylem, který lze nalézt u akademičtějšího zpracování odborných témat. Ačkoli jsou tyto materiály velmi užitečné, psali jejich autoři tyto články značně odlišným stylem, než má naše dokumentace. Při čtení akademického žurnálu si lze povšimnout velice odlišného tónu a zcela odlišného stylu vyjadřování. Lze to přirovnat ke čtení suchého referátu na velmi nezáživné téma.  

## <a name="write-in-second-person"></a>Vyjadřujte se ve druhé osobě

Následující odstavec je psaný v druhé osobě. Ten, který následuje, používá třetí osobu. Vyjadřujte se prosím ve druhé osobě.

### <a name="appropriate-style"></a>Vhodný styl

Články pište tak, jako byste mluvili přímo s čtenářem. Používejte často druhou osobu (jako v těchto dvou větách). To ale neznamená, že musíte pořád používat slovo „vy“. Obracejte se přímo na čtenáře. Pište věty rozkazovacím způsobem. Řekněte čtenáři, co chcete, aby se dozvěděl.

### <a name="inappropriate-style"></a>Nevhodný styl

Autor by se rovněž mohl rozhodnout používat třetí osobu. V takovém případě musí autor najít určité zájmeno nebo podstatné jméno, které použije, když se zmiňuje o čtenáři. Čtenář může často shledat, že styl vyjadřování ve třetí osobě není tak poutavý a čtivý.

## <a name="use-active-voice"></a>Používejte činný rod

Pište články v činném rodu. Činný rod znamená, že podmět věty je původcem děje (slovesa) této věty. To je rozdíl oproti trpnému rodu, kdy je věta sestavena způsobem, že je podmět cílem děje. Porovnejte tyto dva příklady:

>Kompilátor transformoval zdrojový kód do spustitelného souboru.

>Zdrojový kód byl kompilátorem transformován do zdrojového souboru.

První věta používá činný rod. Druhá věta byla napsána v trpném rodu. (Tyto dvě věty jsou dalším příkladem jednotlivých stylů.)

Doporučujeme používat činný rod, protože je čtivější. Čtení trpného rodu může být obtížnější.

## <a name="write-for-readers-who-may-have-a-limited-vocabulary"></a>Předpokládejte, že píšete pro čtenáře, kteří možná mají omezenou slovní zásobu

Svými články oslovujete mezinárodní publikum. Mnozí z vašich čtenářů nejsou rodilí mluvčí anglického jazyka a nemusí mít takovou slovní zásobu jako vy.

Pořád ale píšete pro odborníky z technického oboru. Můžete předpokládat, že vaši čtenáři umí programovat a mají specifickou slovní zásobu programovacích pojmů. Objektově orientované programování, třída a objekt, funkce a metoda jsou známé pojmy. Ne každý, kdo čte vaše články, ale musí mít formální vzdělání v informatice. Pokud použijete pojmy jako „idempotentní“, bude nejspíš potřeba je definovat, například:

> Metoda `Close()` je idempotentní, což znamená, že ji můžete volat několikrát a výsledek je stejný, jako kdybyste ji volali jednou.

## <a name="avoid-future-tense"></a>Vyhněte se budoucímu času

V některých neanglických jazycích není koncepce budoucího času stejná jako v angličtině. Používání budoucího času může znesnadnit pochopení vašich dokumentů. Při používání budoucího času navíc vyvstává otázka „kdy“. Když tedy řeknete „Znalost PowerShellu se vám bude hodit“, má čtenář samozřejmou otázku „Kdy se mi bude hodit?“ Místo toho jednoduše řekněte „Znalost PowerShellu se vám hodí“.

## <a name="what-is-it---so-what"></a>Co je to?

Kdykoli čtenáři představíte nový pojem, napřed ho definujte a teprve pak vysvětlete, proč je užitečný. Je důležité, aby čtenář věděl, co tento pojem znamená, než dokáže pochopit jeho výhody (nebo něco jiného).
