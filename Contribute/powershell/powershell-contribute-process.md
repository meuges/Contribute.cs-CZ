---
title: Postup psaní příspěvků do úložišť dokumentace k PowerShellu
description: V tomto článku najdete stručný úvod k psaní příspěvků do úložišť dokumentace k PowerShellu. Dozvíte se, jaká se používají úložiště, jaký je postup při uspořádání obsahu a jaké zásady platí pro správu vzorového kódu a dalších prostředků.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290189"
---
# <a name="process-for-contributing-to-powershell-docs"></a>Postup psaní příspěvků do dokumentace k PowerShellu

Vážíme si příspěvků, kterými komunita přispívá do dokumentace. V následujícím seznamu najdete několik pravidel, která byste měli mít na paměti při psaní příspěvků do dokumentace k PowerShellu:

- **NEPŘEKVAPUJTE NÁS** rozsáhlými žádostmi o přijetí změn. Než budete něčemu věnovat hodně času, zadejte problém a zahajte diskusi, abychom se mohli předem dohodnout na postupu.
- **ŘIĎTE SE** těmito pokyny a také průvodci správným stylem psaní [kódu](powershell-style-code.md) a [referencí](powershell-style-reference.md).
- **POUŽÍVEJTE** jako výchozí bod své práce soubor se [šablonou](powershell-style-basic-markdown.md).
- **VYTVOŘTE** ve svém forku samostatnou větev dřív, než začnete pracovat na článcích.
- **DODRŽUJTE** [pracovní postup v toku GitHubu](../how-to-write-workflows-major.md).
- **BLOGUJTE A TWEETUJTE** (nebo jinak komunikujte) o svých příspěvcích co nejčastěji.

Dodržováním těchto pokynů usnadníte práci sobě i nám.

## <a name="make-a-contribution-to-powershell-docs"></a>Vytvoření příspěvku do dokumentace k PowerShellu

Můžete si vybrat některý ze stávajících [problémů](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose).
Problémy jsou uspořádané podle vašich zájmů a míry účasti do následujících kategorií:

- **Malé změny:** U malých změn si prohlédněte pokyny k úpravě GitHubu, které jsou na [domovské stránce](../index.md#quick-edits-to-existing-documents) příručky pro přispěvatele. Příklady malých změn:

  - Oprava překlepů a pravopisných chyb
  - Zlepšení gramatiky nebo formátování
  - Drobné technické nebo faktické úpravy

- **Údržba:** Tato kategorie obsahuje relativně jednoduché příspěvky, třeba opravu nefunkčních nebo nesprávných odkazů, přidání chybějících ukázek kódu nebo řešení menších problémů týkajících se obsahu. V některých případech se tyto problémy můžou týkat velkého počtu souborů. V takovém případě nám dejte předem vědět, na čem byste chtěli začít pracovat. Přidejte k problému komentář, ze kterého poznáme, že na něm pracujete.

- **Aktualizace obsahu:** Vzhledem k obrovskému rozsahu dokumentace se může snadno stát, že je obsah zastaralý a vyžaduje revizi. Navíc z různých důvodů může být obsah duplicitní nebo i triplicitní. Při aktualizaci obsahu je potřeba ověřit, jestli jsou jednotlivá témata aktuální, případně revidovat obsah funkční oblasti tak, aby se vyloučily duplicity. Je také potřeba zajistit, aby byl veškerý jedinečný obsah uchováván v menší sadě dokumentace.

- **Tvorba nového obsahu:** Pokud se zajímáte o tvorbu vlastních nových témat, najdete v těchto problémech seznam témat o kterých víme, že bychom je chtěli přidat do naší sady dokumentace. Přesto nám dejte předem vědět, než na tématu začnete pracovat. Pokud máte zájem o napsání tématu, které zde není, otevřete nový problém.

Jakmile jste vybrali úkol, na kterém chcete pracovat, postupujte podle [úvodních](../get-started-setup-github.md) pokynů, podle kterých si vytvoříte účet GitHub a nastavíte prostředí.

### <a name="making-large-changes"></a>Provádění velkých změn

**1. krok:** Pokud se zajímáte o psaní nového obsahu nebo o úplné přepracování stávajícího obsahu, otevřete problém a popište, co chcete dělat.

**2. krok:** Vytvořte kopii úložiště `MicrosoftDocs/PowerShell-Docs` a vytvořte pro své změny pracovní větev.

**3. krok:** V této nové větvi proveďte změny.

Pokud se jedná o nové téma, vyjděte ze šablony v [průvodci správným stylem](powershell-style-basic-markdown.md). Tento průvodce obsahuje pokyny pro psaní a vysvětluje metadata potřebná ke každému článku.

Přejděte do složky, která odpovídá místu v obsahu, které jste pro svůj článek vybrali v prvním kroku.
V této složce jsou soubory v jazyce Markdown všech článků v tomto oddílu. Pokud je to potřeba, vytvořte novou složku, do které umístíte soubory se svým obsahem. Hlavní článek v tomto oddílu se jmenuje *index.md*.
Pro obrázky a další statické prostředky vytvořte podsložku nazvanou **media** (pokud ještě neexistuje) a dejte ji do složky se svým článkem. Ve složce **media** vytvořte podsložku s názvem článku (kromě souboru indexu).

Dodržujte správnou syntaxi jazyka Markdown. Přečtěte si prosím podrobné pokyny a příklady, které najdete v [průvodci správným stylem](powershell-style-basic-markdown.md).

**Příklad struktury**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**4. krok:** Odešlete žádost o přijetí změn (PR) z pracovní do *přípravné* větve.

Žádost o přijetí změn by měla normálně řešit jenom jeden problém. Žádost o přijetí změn se může týkat změny jednoho nebo několika souborů. Pokud řešíte více oprav, které se týkají různých souborů, použijte raději samostatné žádosti o přijetí změn.

Pokud vaše žádost o přijetí změn řeší stávající problém, přidejte do zprávy o potvrzení nebo do žádosti o přijetí změn klíčové slovo `Fixes #Issue_Number`. Když ho přidáte, problém se po sloučení žádosti o přijetí změn automaticky uzavře. Další informace najdete v tématu o [zavírání problémů prostřednictvím zpráv o potvrzení](https://help.github.com/articles/closing-issues-via-commit-messages/).

Tým PowerShellu zkontroluje žádost o přijetí změn a bude vás případně informovat o dalších změnách potřebných ke schválení.

**5. krok:** Proveďte ve větvi potřebné aktualizace, které jste projednali s týmem.

Jakmile je žádost o přijetí změn schválená, sloučí správci vaši žádost do *přípravné* větve. Všechny potvrzené změny pravidelně sdílíme z *přípravné* do *živé* větve. Jakmile je příspěvek v živé větvi, můžete si ho prohlédnout na [webu s dokumentací k PowerShellu](https://docs.microsoft.com/PowerShell/). Příspěvky obvykle publikujeme v pracovním týdnu dvakrát nebo třikrát týdně.

## <a name="contributor-license-agreement"></a>Licenční smlouva s přispěvatelem

Před sloučením žádosti o přijetí změn musíte podepsat [licenční smlouvu s přispěvatelem (CLA)](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs). Jedná se o jednorázový požadavek při přispívání do naší dokumentace.

Smlouvu nemusíte podepisovat předem. Žádosti o přijetí změn můžete obvyklým způsobem klonovat, odeslat nebo můžete vytvořit fork.
Vytvořenou žádost o přijetí změn klasifikuje robot CLA. Pokud se jedná o malou změnu (třeba o opravu překlepu), bude žádost označena `cla-not-required`. V ostatních případech bude zařazena jako `cla-required`. Po podpisu smlouvy CLA budou všechny současné i budoucí žádosti o přijetí změn označeny `cla-signed`.
