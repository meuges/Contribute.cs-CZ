---
title: Odeslání žádosti o přijetí změn
description: Tento článek popisuje postup žádosti o přijetí změn a vysvětluje osvědčené postupy, které zajistí slučitelnost vašeho příspěvku.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290074"
---
# <a name="best-practices-for-pull-requests"></a>Osvědčené postupy u žádostí o přijetí změn

Když chcete publikovat změny obsahu, odešlete ze svého forku žádost o přijetí změn. Každá žádost o přijetí změn se musí před sloučením zkontrolovat.

## <a name="target-the-correct-branch"></a>Volba správné větve

Všechny změny je potřeba provést ve větvi `staging`. Změny by se nikdy neměly provádět ve větvi `live`. Změny provedené ve větvi `staging` se sloučí do větve `live`, takže všechny změny provedené ve větvi `live` se přepíšou.

Pokud odesíláte změnu v dokumentaci, která platí jenom pro nevydanou verzi PowerShellu, zkontrolujte, jestli má daná verze svou větev. Všechny změny, které se týkají určité budoucí verze, musí být určeny pro větev vydané verze. Větve vydaných verzí mají název v následujícím tvaru: `release-<version>`.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>Efektivnější fungování fronty žádostí o přijetí změn pro všechny

Ve frontě žádostí o přijetí změn fungují dvě základní skutečnosti:

- Kontrola žádostí o přijetí změn, které jsou menšího rozsahu a obsahují podobné změny, trvá kratší dobu.
- Naopak kontrola žádostí o přijetí změn, které jsou rozsáhlé nebo obsahují nesouvisející změny, trvá déle.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>Eliminace větví, které aktualizují velký počet souborů

Oddělte menší aktualizace stávajících článků od nových článků nebo výrazných přepracování. Na těchto změnách pracujte v samostatných pracovních větvích.

Hromadné změny se používají u žádostí o přijetí změn s velkým počtem změněných souborů. Omezte své žádosti o přijetí změn na nejvýše 50 změněných souborů. Rozsáhlé žádosti o přijetí změn se obtížně kontrolují a je u nich větší pravděpodobnost výskytu chyb.

### <a name="renaming-or-deleting-files"></a>Přejmenovávání nebo odstraňování souborů

Když přejmenováváte nebo odstraňujete soubory, snažte se nemíchat tyto změny s přidáváním nebo aktualizací obsahu.
Tyto změny zpracujte do samostatných žádostí o přijetí změn, které se sloučí až po žádostech o přijetí změn týkajících se souvisejících aktualizací. Například před odstraněním článku aktualizujte soubor přesměrování a ověřte, zda přesměrování funguje.

Musíte aktualizovat všechny soubory, které odkazují na přejmenovaný soubor. Patří k nim i všechny soubory s obsahem. Dále musíte do hlavního směrovacího souboru (`.openpublishing.redirection.json`), který je v kořenovém adresáři úložiště, přidat záznamy o přesměrování.

## <a name="docs-pr-validation-service"></a>Odkaz na službu ověřování žádostí o přijetí změn Docs

Služba ověřování žádostí o přijetí změn Docs je githubová aplikace, která spouští ověřovací pravidla u souborů v žádosti o přijetí změn.

Uvidíte následující chování:

1. Odešlete žádost o přijetí změn.
1. V komentáři GitHubu, který označuje stav vaší žádosti o přijetí změn, se zobrazí stav kontrol povolených u úložiště. Všimněte si, že v tomto příkladu jsou povolené dvě kontroly, Commit Validation a OpenPublishing.Build:

   ![Některé kontroly nebyly úspěšné.](media/powershell-pull-requests/validation-failed.png)

   Sestavení může projít, i když se ověření potvrzení nezdaří.

1. Další informace se zobrazí po kliknutí na **Details** (Podrobnosti).
1. Na stránce podrobností se zobrazí všechny neúspěšné validační kontroly, včetně informací o možném řešení problémů.
1. Pokud je ověření úspěšné, přidá se do žádosti o přijetí změn následující komentář:

   ![Ověření sestavení](media/powershell-pull-requests/build-validation.png)

Pokud jste externím přispěvatelem (nepatříte k Microsoftu), nemáte přístup k podrobným sestavám o sestavení ani k odkazům na verzi Preview.

### <a name="build-warnings"></a>Upozornění sestavení

Normálně byste měli opravit všechny chyby, upozornění a doporučení, které se týkají sestavení. Některá upozornění ale můžete ignorovat.

Následující upozornění můžete ignorovat:

- > Can't find service name for `<version>/<modulepath>/About/About.md` (Nelze najít název služby pro...)

- > Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`. (Metadata s následujícím názvem nebo názvy nejdou nastavit v nadpisech Yaml, nejdou nastavit jako metadata na úrovni souboru docfx.json, ani jako globální metadata v souboru docfx.json...) Tato upozornění generuje platforma Docs, takže se k hodnotám nastaveným na těchto třech místech nebude přihlížet. Pokud chcete upozornění vyřešit, odeberte je ze všech tří míst.
