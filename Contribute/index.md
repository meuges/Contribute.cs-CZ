---
title: Průvodce pro přispěvatele na web Microsoft Docs – přehled
description: Tento průvodce popisuje, jak přispívat na web docs.microsoft.com, který obsahuje dokumentaci Microsoftu.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 04/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1cda40c890e5b30e6e1e10f3bcee0278f8004653
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Průvodce pro přispěvatele na web Microsoft Docs – přehled

Vítá vás Průvodce pro přispěvatele na webu [docs.microsoft.com](https://docs.microsoft.com) (Docs)!

Některé sady naší dokumentace jsou dostupné jako Open Source hostovaný na GitHubu. Tento model přijímá stále více týmů. Dokonce i sady dokumentů, které nejsou celé dostupné jako Open Source, mají veřejná úložiště, ve kterých můžete zadávat žádosti o přijetí změn. Komunikace mezi produktovými inženýry, týmy pro obsah a našimi zákazníky je tak jednodušší a efektivnější. Práce v otevřeném prostředí poskytuje několik výhod:

- Plánování úložišť Open Source se provádí otevřeně, což umožňuje získávat zpětnou vazbu o tom, které dokumenty jsou nejvíce žádané.
- Revize úložišť Open Source se provádějí otevřeně, takže je možné v naší nové verzi publikovat nejužitečnější obsah.
- Aktualizace úložišť Open Source se provádějí otevřeně, takže průběžné vylepšování obsahu je jednodušší.

Aby to bylo ještě jednodušší, uživatelské prostředí na webu [docs.microsoft.com](https://docs.microsoft.com) přímo integruje pracovní postupy [GitHubu](https://github.com). Můžete začít [úpravami dokumentu, který si prohlížíte](#quick-edits-to-existing-documents). Případně můžete pomoct s [revizemi nových témat](#review-open-prs) nebo s [vytvářením užitečných položek problémů](#create-quality-issues).

> [!IMPORTANT]
> Všechna úložiště, která se publikují na docs.microsoft.com, přijala [pravidla chování pro Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) nebo [pravidla chování pro .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Další informace najdete v [častých otázkách k pravidlům chování](https://opensource.microsoft.com/codeofconduct/faq/). Se svými dotazy nebo připomínkami se můžete také obrátit na [opencode@microsoft.com](mailto:opencode@microsoft.com) nebo [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Na menší opravy nebo vysvětlení k dokumentaci a ukázkám kódu ve veřejných úložištích se vztahují [podmínky použití pro docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Nové nebo výrazné změny vygenerují v žádosti o přijetí změn komentář, abyste odeslali online licenční smlouvu s přispěvatelem (CLA), pokud nejste zaměstnancem Microsoftu. Potřebujeme, abyste tento online formulář vyplnili. Teprve pak vaši žádost o přijetí změn můžeme revidovat a přijmout.

## <a name="quick-edits-to-existing-documents"></a>Rychlé úpravy existujících dokumentů

Rychlé úpravy zjednodušují proces oznamování a oprav drobných chyb a vynechávek v dokumentech. I přes veškeré úsilí můžou v našich publikovaných dokumentech zůstat drobné gramatické a pravopisné chyby. Je sice možné oznamovat tyto chyby tak, že vytvoříte položky problémů, když ale vytvoříte žádost o přijetí změn, bude oprava těchto chyb rychlejší a jednodušší. Téměř u každého článku se zobrazuje tlačítko pro úpravy, které je znázorněno na následujícím obrázku. Kliknutím na tlačítko **Edit** (Upravit) přejdete ke zdrojovému souboru na GitHubu.

![Umístění odkazu pro úpravy](./media/index/edit-article.png)

Pak klikněte na ikonu tužky, která je znázorněna na následujícím obrázku, abyste mohli článek upravit.

> [!NOTE]
> Pokud je ikona tužky šedá, je nutné, abyste se přihlásili ke svému účtu GitHub nebo abyste si vytvořili nový účet. Proveďte příslušné změny ve webovém editoru. Kliknutím na kartu **Preview changes** (Náhled změn) můžete zkontrolovat formátování jednotlivých změn.

![Umístění ikony tužky](./media/index/editicon.png)

Po provedení změn se posuňte do dolní části stránky. Zadejte název a popis pro vaši žádost o přijetí změn a klikněte na tlačítko **Propose file change** (Navrhnout změnu souboru), jak je znázorněno na následujícím obrázku:

![navržení změny](./media/index/submit-pull-request.png)

A to je vše! Členové týmu pro obsah provedou revizi a sloučení vaší žádosti o přijetí změn. Pokud jste provedli větší změny, je možné, že dostanete zpětnou vazbu vyžadující nějaké změny.

Uživatelské rozhraní GitHubu pro úpravy se přizpůsobuje podle oprávnění uživatele v daném úložišti. Předchozí obrázky jsou přesné pro přispěvatele, kteří nemají oprávnění k zápisu do cílového úložiště. GitHub automaticky vytvoří ve vašem účtu fork cílového úložiště. Pokud máte oprávnění k zápisu do cílového úložiště, GitHub vytvoří v cílovém úložišti novou větev. Název větve má formát **\<GitHubId\>-patch-n** a používá vaše ID pro GitHub a číselný identifikátor pro větev opravy.

Žádosti o přijetí změn používáme pro všechny změny, tedy i od přispěvatelů, kteří mají oprávnění k zápisu. U většiny úložišť je větev `master` chráněná, takže aktualizace je nutné odesílat jako žádosti o přijetí změn.

Prostředí pro úpravy v prohlížeči je nejvhodnější pro drobné nebo málo časté změny. Pokud provádíte velké příspěvky nebo používáte pokročilé funkce Git (třeba správu větví nebo pokročilé řešení konfliktů při sloučení), potřebujete [vytvořit fork úložiště a pracovat místně](how-to-write-workflows-major.md).

## <a name="review-open-prs"></a>Revize otevřených žádostí o přijetí změn

S novými tématy se můžete seznámit před jejich publikováním tak, že zkontrolujete aktuálně otevřené žádosti o přijetí změn. Revize se řídí procesem [toku GitHubu](https://guides.github.com/introduction/flow/). Ve veřejných úložištích můžete vidět navrhované aktualizace a nové články. Seznamte se s nimi a přidejte svoje komentáře. Podívejte se na libovolné z našich úložišť dokumentů a zkontrolujte otevřené žádosti o přijetí změn v oblastech, které vás zajímají. Zpětná vazba komunity na navrhované aktualizace pomáhá celé komunitě.

## <a name="create-quality-issues"></a>Vytváření užitečných položek problémů

Naše dokumenty jsou výsledkem nepřetržitě probíhající práce. Vhodně vytvořené položky problémů pomáhají zaměřit naše úsilí na to, co má pro komunitu nejvyšší prioritu. Čím více podrobností zadáte, tím je položka problému užitečnější. Sdělte nám, co jste hledali. Sdělte nám, jaké termíny jste při hledání použili. Pokud nemůžete zahájit práci, sdělte nám, jak se chcete s neznámou technologií začít seznamovat.

Položky problémů umožňují zahájit konverzaci o tom, co je potřeba udělat. Tým pro obsah bude na tyto položky problémů reagovat návrhy, co můžeme přidat, a požádá vás o váš názor. Až vytvoříme koncept, požádáme vás o [revizi dané žádosti o přijetí změn](#review-open-prs).

## <a name="get-more-involved"></a>Zapojte se více

Další témata vám pomáhají začít produktivně přispívat na web Microsoft Docs. Vysvětlují, jak používat úložiště GitHub, nástroje Markdown a rozšíření používaná na platformě Microsoft Docs.
