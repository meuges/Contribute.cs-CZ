---
title: Pracovní postup přispívání prostřednictvím GitHubu pro větší nebo dlouho probíhající změny
description: Tento článek popisuje, jak používat pracovní postup „větších“ přispěvatelů k přispívání do článků na webu docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: a43e9a8274c430b1eeed796fc74085c2248f1c14
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Pracovní postup přispívání prostřednictvím GitHubu pro větší nebo dlouho probíhající změny

> [!IMPORTANT]
> Všechna úložiště, která se publikují na docs.microsoft.com, přijala buď [pravidla chování pro Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/), nebo [pravidla chování pro .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Další informace najdete v [častých otázkách k pravidlům chování](https://opensource.microsoft.com/codeofconduct/faq/). Se svými dotazy nebo připomínkami se můžete také obrátit na [opencode@microsoft.com](mailto:opencode@microsoft.com) nebo [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Na menší opravy nebo vysvětlení k dokumentaci a ukázkám kódu ve veřejných úložištích se vztahují [podmínky použití pro docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Nové nebo výrazné změny vygenerují v žádosti o přijetí změn komentář, abyste odeslali online licenční smlouvu s přispěvatelem (CLA), pokud nejste zaměstnancem Microsoftu. Aby mohla být vaše žádost o přijetí změn sloučena, musíte online formulář vyplnit.

## <a name="overview"></a>Přehled

Tento pracovní postup je vhodný pro přispěvatele, kteří potřebují provést velkou změnu nebo budou častými přispěvateli do úložiště. Častí přispěvatelé obvykle mívají průběžné (dlouho probíhající) změny, které procházejí více cykly sestavení/ověření/přípravy nebo trvají více dní, než dojde k odsouhlasení a sloučení žádosti o přijetí změn.

Pro zaměstnance Microsoftu pracující na projektech, které využívají veřejná i soukromá úložiště, je také důležité, aby tyto typy příspěvků prováděli do soukromého úložiště. V soukromém úložišti jsou k dispozici integrované služby sestavení, ověření a přípravy OPS.

Mezi příklady těchto typů příspěvků patří:

[!INCLUDE[contribute-how-to-write-workflows-major-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Než začnete, seznamte se s některými termíny a výrazy pro Git/GitHub používanými v tomto pracovním postupu. Nemusíte jim hned rozumět. Stačí vědět, že se o nich budete dozvídat a můžete se k této sekci vrátit, když si budete chtít zjistit jejich definici.

| Název | Popis |
|-----------|-------------|
|fork|Označuje kopii hlavního úložiště GitHubu. V praxi je fork prostě další úložiště. Je ale speciální v tom smyslu, že GitHub udržuje jeho spojení zpět s hlavním/nadřazeným úložištěm. Někdy se používá jako sloveso, například "Je nutné nejprve rozvětvit úložiště."|
|remote (vzdálené)|Pojmenované spojení se vzdáleným úložištěm, například vzdálené úložiště „zdroj“ nebo „upstream“. Git je označuje za vzdálená, protože slouží k odkazování na úložiště hostovaná na jiném počítači. V tomto pracovním postupu je vzdálené úložiště vždy úložiště GitHubu.|
|origin (zdroj)|Název přidělený spojení mezi vaším místním úložištěm a úložištěm, ze kterého bylo naklonováno. V tomto pracovním postupu zdroj představuje spojení s vaším forkem. Někdy se používá jako označení pro samotné zdrojové úložiště, například „Nezapomeňte své změny odeslat do zdroje“.|
|upstream|Podobně jako vzdálené úložiště původ je i upstream pojmenovaným spojením s jiným úložištěm. V tomto pracovním postupu upstream představuje spojení mezi vaším místním úložištěm a hlavním úložištěm, z něhož byl vytvořen váš fork. Někdy se používá jako označení pro samotné úložiště upstream, například „Nezapomeňte své změny přijmout z upstreamu“.|

## <a name="workflow"></a>Pracovní postup

>[!IMPORTANT]
> Pokud jste to ještě neudělali, musíte provést kroky v sekci věnované [nastavení](get-started-setup-github.md). Ta vás provede nastavením účtu GitHub, instalací nástroje Git Bash a editoru Markdownu, vytvořením forku a zřízením místního úložiště. Pokud neznáte pojmy Gitu a GitHubu jako úložiště nebo větev, nejdřív si přečtěte [základy Gitu a GitHubu](git-github-fundamentals.md).

V tomto pracovním postupu se změny provádějí v opakujícím se cyklu. Z místního úložiště vašeho zařízení přecházejí zpět do vašeho forku GitHubu, do hlavního úložiště GitHubu a znovu zpátky do místního úložiště, když zakomponujete změny od ostatních přispěvatelů.

### <a name="use-github-flow"></a>Použití pracovního postupu GitHubu

Z článku o [základech Gitu a GitHubu](git-github-fundamentals.md#git) si možná vzpomínáte, že úložiště Gitu obsahuje hlavní („master“) větev a další větve s nedokončenou prací, které do hlavní větve nejsou integrované. Kdykoli zavádíte sadu logicky souvisejících změn, je osvědčeným postupem vytvořit *pracovní větev* ke správě změn v průběhu pracovního postupu. Takovou větev tady označujeme jako pracovní, protože jde o pracovní prostor k iteraci/vypilování změn, než je bude možné integrovat zpět do hlavní větve.

Izolování souvisejících změn v konkrétní větvi vám umožní tyto změny řídit a zavádět nezávisle a cílit je na konkrétní čas vydání v publikačním cyklu. V závislosti na typu práce můžete mít ve skutečnosti v úložišti několik pracovních větví. Není neobvyklé pracovat současně na více větvích, z nichž každá představuje jiný projekt.

>[!TIP]
>Provádět změny v hlavní větvi *není* dobrý postup. Představte si, že hlavní větev použijete k zavedení sady změn pro načasované vydání funkce. Změny dokončíte a čekáte na jejich vydání. Mezitím dostanete urgentní žádost o nějakou opravu, takže provedete změnu v souboru v hlavní větvi a pak změnu publikujete. V tomto příkladu neúmyslně publikujete opravu a *současně* i změny, se kterými jste čekali na vydání v konkrétní den.

Vytvořme tedy novou pracovní větev v místním úložišti k zachycení vašich navrhovaných změn. Každý klient Git je jiný, proto si prostudujte nápovědu ke klientovi, kterému dáváte přednost. Přehled tohoto procesu najdete v příručce GitHubu na webu s [pracovním postupem GitHubu](https://guides.github.com/introduction/flow/).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Další kroky
A to je vše! Přispěli jste k obsahu docs.microsoft.com.

- Pokud se chcete dozvědět víc o tématech jako Markdown a syntaxe rozšíření Markdownu a dalších tématech, pokračujte na sekci Základy psaní.
