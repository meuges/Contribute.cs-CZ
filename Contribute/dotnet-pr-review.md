---
title: Proces kontroly žádosti o přijetí změn dokumentů .NET
description: Dokumenty .NET nemají povolené webhooky PR Merger. Tento článek popisuje proces kontroly žádosti o přijetí změn pro taková úložiště.
ms.date: 01/-4/2019
ms.openlocfilehash: d8f35e328beffcbd5bac9f0f7313d8127fbeffb0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713561"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>Proces kontroly žádosti o přijetí změn pro úložiště dokumentů .NET

Mnohá úložiště nemají povolené webhooky PR Merger, takže se automaticky slučují menší žádosti o přijetí změn. Tento článek popisuje proces kontroly žádosti o přijetí změn pro taková úložiště. Proces kontroly žádosti o přijetí změn byl navržen s těmito cíli:

1. Publikování vysoce kvalitního obsahu od našeho týmu, členů produktových týmů a členů komunity
1. Konzistentní poskytování včasné zpětné vazby s akcemi autorům
1. Usnadnění diskuze mezi autory a revidujícími

Procesy se neustále vyvíjejí, jak týmy přinášejí inovace a platforma se zdokonaluje.

## <a name="reviewers"></a>Revidující

Jeden ze členů týmu obsahu kontroluje každou žádost o přijetí změn. Členové týmu obsahu můžou požadovat přezkoumání od konkrétních členů produktového týmu, aby ověřili technickou přesnost. Tým obsahu používá funkci GitHubu Code Ownership (Vlastnictví kódu), která automaticky žádá o kontroly od členů týmu obsahu. Jako součást tohoto procesu může revidující označit jiné členy týmu, kteří mají zkontrolovat interní žádosti o přijetí změn. Členové týmu vidí požadované kontroly od členů týmu a členů komunity ve stejné frontě.

Členové komunity můžou také kontrolovat žádosti o přijetí změn a poskytovat zpětnou vazbu. Ovšem nejméně jeden člen základního týmu obsahu musí schválit každou žádost o přijetí změn před jejím sloučením.

## <a name="review-process"></a>Proces kontroly

Kontroly postupují podle jedné ze tří cest podle typu žádosti:

- **Malé žádosti o přijetí změn** – Malé žádosti o přijetí změn představují jednu opravu: překlepy, nefunkční odkazy, drobné změny kódu nebo podobné změny.
- **Větší příspěvky** – Větší příspěvky jsou významné úpravy existujícího článku, nové články nebo úpravy počtu článků.
- **Probíhající práce** – Autoři můžou požádat o průběžnou kontrolu otevřením žádosti o přijetí změn se značkou [WIP] v názvu. Značka WIP znamená Probíhající práce. 

Zpracování používané robotem pro licenční smlouvu s přispěvatelem (CLA) je dobré vodítko, jak rozlišovat malé a velké příspěvky. Žádosti o přijetí změn, které nevyžadují podepsání CLA, jsou pravděpodobně malé. Žádosti o přijetí změn, které vyžadují CLA, jsou pravděpodobně velké.

### <a name="small-prs"></a>Malé žádosti o přijetí změn

Ve změnách malých žádostí o přijetí změn se kontroluje přesnost, a to použitím sestavení na webu pro kontroly. Protože jsou malé, tyto žádosti o přijetí změn nespouštějí kontrolu celého článku. 

Revidující si můžou všimnout jiných malých změn, které by mohly zlepšit článek. Pokud jsou tyto změny také malé, navrhněte je jako komentáře ke kontrole. Pokud by navržené změny vyvolaly větší kontrolu, otevřete problém a věnujte se jim později. 

### <a name="larger-changes"></a>Větší změny

Větší žádosti o přijetí změn procházejí důkladnější kontrolou. Kontrolují se následující skutečnosti:

- Vzorový kód musí být součástí žádosti o přijetí změn, ve zdroji a jako soubor zip ke stažení.
- Vzorový kód se správně zkompiluje a spustí.
- Článek jasně čtenáři popisuje cíle a tyto cíle jsou splněny.
- Článek splňuje [stylistické a gramatické pokyny](dotnet-style-guide.md) a dodržuje naše [principy způsobu vyjadřování](dotnet-voice-tone.md).
- Všechny odkazy se správně překládají.

Členové týmu obsahu žádost o přijetí změn zkontrolují a odešlou ji s komentáři. Pokud se požadují jenom menší změny, členové týmu můžou žádost schválit se zpětnou vazbou. Autor pak může na zpětnou vazbu reagovat a žádost o přijetí změn sloučit. Většina kontrol bude vyžadovat změny a když se provedou, revidující udělá znovu kontrolu.

Pokud úpravy vyžadují technickou kontrolu, revidující z týmu obsahu požádá o kontrolu od příslušného člena produktového týmu.

### <a name="review-wip-pull-requests"></a>Kontrola žádostí o přijetí změn typu WIP

Noví autoři můžou chtít zpětnou vazbu v dřívějších fázích procesu. Můžou otevřít žádost o přijetí změn přidáním popisku [WIP] do názvu. V komentáři můžou požádat o ranou kontrolu.

Tyto rané kontroly nejsou tak důkladné jako úplná kontrola žádosti o přijetí změn. Tým obsahu přidá komentář, ale nebude žádost schvalovat ani žádat o změny pomocí funkce pro kontrolu z GitHubu. Tyto rané kontroly se zaměřují na strukturu článku: osnova, celkový obsah a ukázky. Nezahrnují důkladnou kontrolu gramatiky a správných odkazů.

## <a name="respond-to-reviews"></a>Reakce na kontroly

Autor aktualizuje žádost o přijetí změn a reaguje na komentáře, přičemž označí každý zpracovaný komentář reakcí +1, která znamená, že byl vyřešen. Pokud autor nesouhlasí s komentářem nebo komentář vyřeší jinak, přidá komentář s vysvětlením své změny.

Autor uvede původního revidujícího v komentáři, pokud chce požádat o novou kontrolu. 

## <a name="response-time-expectations"></a>Očekáváné reakční doby

Členové týmu obsahu obvykle zkontrolují nové žádosti o přijetí změn do dvou pracovních dnů. Pokud trvá kontrola déle, jeden z členů týmu přidá komentář, který žádost o přijetí změn potvrdí, a nastaví očekávanou dobu.

Poté, co byla kontrola odeslána, by se autoři měli snažit reagovat na komentáře do týdne nebo dříve. Dobrovolníci nemusí být schopni tuto lhůtu splnit z důvodu dalších závazků. V těchto případech se členové týmu zeptají, jestli autor z komunity aktualizuje žádost o přijetí změn. Pokud ne, aktualizuje ji člen týmu a sloučí ji za něj.
