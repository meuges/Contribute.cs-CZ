---
title: Průvodce pro přispěvatele na web Microsoft Docs – přehled
description: Tento průvodce popisuje, jak přispívat na web docs.microsoft.com, který obsahuje dokumentaci Microsoftu.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 04/17/2018
ms.openlocfilehash: 4a9a7573a62cfc7d5187b90de7e1fe147825273e
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712848"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Průvodce pro přispěvatele na web Microsoft Docs – přehled

Vítá vás Průvodce pro přispěvatele na webu [docs.microsoft.com](https://docs.microsoft.com) (Docs)!

Některé sady naší dokumentace jsou dostupné jako Open Source hostovaný na GitHubu. Tento model si přisvojuje stále více týmů v Microsoftu. Dokonce i sady dokumentů, které nejsou celé dostupné jako Open Source, mají veřejná úložiště, ve kterých můžete zadávat žádosti o přijetí změn. Komunikace mezi produktovými inženýry, týmy pro obsah a našimi zákazníky je tak jednodušší a efektivnější. Práce v otevřeném prostředí poskytuje několik výhod:

- Plánování úložišť Open Source se provádí otevřeně, což umožňuje získávat zpětnou vazbu o tom, které dokumenty jsou nejvíce žádané.
- Revize úložišť Open Source se provádějí otevřeně, takže je možné v naší nové verzi publikovat nejužitečnější obsah.
- Aktualizace úložišť Open Source se provádějí otevřeně, takže průběžné vylepšování obsahu je jednodušší.

Aby to bylo ještě jednodušší, uživatelské prostředí na webu [docs.microsoft.com](https://docs.microsoft.com) přímo integruje pracovní postupy [GitHubu](https://github.com). Můžete začít [úpravami dokumentu, který si prohlížíte](#quick-edits-to-existing-documents). Případně můžete pomoct s [revizemi nových témat](#review-open-prs) nebo s [vytvářením užitečných položek problémů](#create-quality-issues).

> [!IMPORTANT]
> Všechna úložiště, která se publikují na docs.microsoft.com, přijala [pravidla chování pro Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/) nebo [pravidla chování pro .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Další informace najdete v [častých otázkách k pravidlům chování](https://opensource.microsoft.com/codeofconduct/faq/). Se svými dotazy nebo připomínkami se můžete také obrátit na [opencode@microsoft.com](mailto:opencode@microsoft.com) nebo [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Na menší opravy nebo vysvětlení k dokumentaci a ukázkám kódu ve veřejných úložištích se vztahují [podmínky použití pro docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Nové nebo výrazné změny vygenerují v žádosti o přijetí změn komentář, abyste odeslali online licenční smlouvu s přispěvatelem (CLA), pokud nejste zaměstnancem Microsoftu. Potřebujeme, abyste tento online formulář vyplnili. Teprve pak vaši žádost o přijetí změn můžeme revidovat a přijmout.

## <a name="quick-edits-to-existing-documents"></a>Rychlé úpravy existujících dokumentů

Rychlé úpravy zjednodušují proces oznamování a oprav drobných chyb a vynechávek v dokumentech. I přes veškeré úsilí můžou v našich publikovaných dokumentech zůstat drobné gramatické a pravopisné chyby. Je sice možné oznamovat tyto chyby tak, že vytvoříte položky problémů, když ale vytvoříte žádost o přijetí změn, bude oprava těchto chyb rychlejší a jednodušší. Téměř u každého článku se zobrazuje tlačítko pro úpravy, které je znázorněno na následujícím obrázku. Kliknutím na **Edit** (Upravit) se dostanete na zdrojový soubor na GitHubu.

![Umístění odkazu pro úpravy](./media/index/edit-article.png)

Pak klikněte na ikonu tužky, která je znázorněna na následujícím obrázku, abyste mohli článek upravit.

![Umístění ikony tužky](./media/index/edit-icon.png)

> [!NOTE]
> Pokud je ikona tužky šedá, je nutné, abyste se přihlásili ke svému účtu GitHub nebo abyste si vytvořili nový účet.

Proveďte příslušné změny ve webovém editoru. Kliknutím na kartu **Preview changes** (Náhled změn) můžete zkontrolovat formátování jednotlivých změn.

Po provedení změn se posuňte do dolní části stránky. Zadejte název a popis pro vaši žádost o přijetí změn a klikněte na tlačítko **Propose file change** (Navrhnout změnu souboru), jak je znázorněno na následujícím obrázku:

![navržení změny](./media/index/submit-pull-request.png)

Teď, když jste navrhli změnu, musíte požádat vlastníky úložiště, aby vaši změnu „přijali“ do svého úložiště. K tomu slouží takzvaná „žádost o přijetí změn“. Když jste kliknuli na **Propose file change** (Navrhnout změnu souboru) v obrázku výše, měli byste se dostat na novou stránku, která vypadá jako na následujícím obrázku:

![vytvoření žádosti o přijetí změn](media/index/create-pull-request.png)

Klikněte na **Create pull request** (Vytvořit žádost o přijetí změn), zadejte název (a volitelně popis) této žádosti o přijetí změn a pak znovu klikněte na **Create pull request**.

A to je vše! Členové týmu pro obsah provedou revizi a sloučení vaší žádosti o přijetí změn. Pokud jste provedli větší změny, je možné, že dostanete zpětnou vazbu vyžadující nějaké změny.

Uživatelské rozhraní GitHubu pro úpravy se přizpůsobuje podle oprávnění uživatele v daném úložišti. Předchozí obrázky jsou přesné pro přispěvatele, kteří nemají oprávnění k zápisu do cílového úložiště. GitHub automaticky vytvoří ve vašem účtu fork cílového úložiště. Pokud máte oprávnění k zápisu do cílového úložiště, GitHub vytvoří v cílovém úložišti novou větev. Název větve má formát **\<GitHubId\>-patch-n** a používá vaše ID pro GitHub a číselný identifikátor pro větev opravy.

Žádosti o přijetí změn používáme pro všechny změny, tedy i od přispěvatelů, kteří mají oprávnění k zápisu. U většiny úložišť je větev `master` chráněná, takže aktualizace je nutné odesílat jako žádosti o přijetí změn.

Prostředí pro úpravy v prohlížeči je nejvhodnější pro drobné nebo málo časté změny. Pokud provádíte velké příspěvky nebo používáte pokročilé funkce Git (třeba správu větví nebo pokročilé řešení konfliktů při sloučení), potřebujete [vytvořit fork úložiště a pracovat místně](how-to-write-workflows-major.md).

> [!NOTE]
> Pokud je to povolené, můžete článek upravit v **libovolném jazyce**, přičemž podle typu úpravy se stane následující:
> 1. Jakákoli schválená jazyková změna zároveň pomůže vylepšit náš modul strojového překladu.
> 2. Jakákoli úprava, která podstatně změní obsah článku, se zpracuje interně a změna se odešle do stejného článku v angličtině, takže pokud bude schválena, lokalizuje se do všech jazyků.
> Vámi navržená vylepšení tedy pozitivně ovlivní nejen články ve vašem vlastním jazyce, ale také ve všech dostupných jazycích.

## <a name="review-open-prs"></a>Revize otevřených žádostí o přijetí změn

S novými tématy se můžete seznámit před jejich publikováním tak, že zkontrolujete aktuálně otevřené žádosti o přijetí změn. Revize se řídí procesem [toku GitHubu](https://guides.github.com/introduction/flow/). Ve veřejných úložištích můžete vidět navrhované aktualizace a nové články. Seznamte se s nimi a přidejte svoje komentáře. Podívejte se na libovolné z našich úložišť dokumentů a zkontrolujte otevřené žádosti o přijetí změn v oblastech, které vás zajímají. Zpětná vazba komunity na navrhované aktualizace pomáhá celé komunitě.

## <a name="create-quality-issues"></a>Vytváření užitečných položek problémů

Naše dokumenty jsou výsledkem nepřetržitě probíhající práce. Vhodně vytvořené položky problémů pomáhají zaměřit naše úsilí na to, co má pro komunitu nejvyšší prioritu. Čím více podrobností zadáte, tím je položka problému užitečnější. Sdělte nám, co jste hledali. Sdělte nám, jaké termíny jste při hledání použili. Pokud nemůžete zahájit práci, sdělte nám, jak se chcete s neznámou technologií začít seznamovat.

Položky problémů umožňují zahájit konverzaci o tom, co je potřeba udělat. Tým pro obsah bude na tyto položky problémů reagovat návrhy, co můžeme přidat, a požádá vás o váš názor. Až vytvoříme koncept, požádáme vás o [revizi dané žádosti o přijetí změn](#review-open-prs).

## <a name="get-more-involved"></a>Zapojte se více

Další témata vám pomáhají začít produktivně přispívat na web Microsoft Docs. Vysvětlují, jak používat úložiště GitHub, nástroje Markdown a rozšíření používaná na platformě Microsoft Docs.
