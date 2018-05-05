---
title: Pracovní postup přispívání prostřednictvím GitHubu pro menší nebo občasné změny
description: Tento článek popisuje, jak používat pracovní postup „menších“ přispěvatelů k přispívání do článků na web docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>Pracovní postup přispívání prostřednictvím GitHubu pro menší nebo občasné změny

> [!IMPORTANT]
> Všechna úložiště, která se publikují na docs.microsoft.com, přijala buď [pravidla chování pro Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/), nebo [pravidla chování pro .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Další informace najdete v [častých otázkách k pravidlům chování](https://opensource.microsoft.com/codeofconduct/faq/). Se svými dotazy nebo připomínkami se můžete také obrátit na [opencode@microsoft.com](mailto:opencode@microsoft.com) nebo [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Na menší opravy nebo vysvětlení k dokumentaci a ukázkám kódu ve veřejných úložištích se vztahují [podmínky použití pro docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Nové nebo výrazné změny vygenerují v žádosti o přijetí změn komentář, abyste odeslali online licenční smlouvu s přispěvatelem (CLA), pokud nejste zaměstnancem Microsoftu. Potřebujeme, abyste tento online formulář vyplnili. Teprve pak vaši žádost o přijetí změn můžeme přijmout.

## <a name="overview"></a>Přehled

Tento pracovní postup je vhodný k provádění menších nebo občasných změn pomocí webového editoru Markdownu GitHubu. Editor GitHubu je omezený v tom, co můžete dělat, protože uživatelské rozhraní nepodporuje všechny operace a scénáře vytváření obsahu Git. Pokud potřebujete provést velké příspěvky nebo potřebujete podporu pokročilých funkcí Git (třeba správu větví nebo pokročilé řešení konfliktů při sloučení), přečtěte si [pracovní postup pro větší nebo dlouho probíhající změny](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Postup pro používání editoru GitHubu k navrhování změn

1. Najděte odpovídající úložiště GitHubu a soubor Markdownu článku. Můžete použít kteroukoli z těchto metod:

   - Najděte článek procházením souborů Markdownu v souvisejícím úložišti GitHubu.
   - Přejděte na článek na [docs.microsoft.com](https://docs.microsoft.com/) a vpravo nahoře na stránce zvolte odkaz pro **úpravy**.

     ![Umístění odkazu pro úpravy](./media/light-workflow/contributetogit.png)

2. Zvolením ikony tužky **Upravit tento soubor** přejděte do režimu úprav:

    ![Umístění ikony tužky](./media/light-workflow/editicon.png)

3. Poveďte změny pomocí Markdownu na kartě **Upravit soubor** a náhled změn můžete zobrazit na kartě **Náhled změn**. Používání editoru je celkem jasné, ale pokud potřebujete pomoc, přečtěte si tyto návody:

   - [Jak používat Markdown](how-to-write-use-markdown.md)
   - [Vytváření souborů na GitHubu](https://github.com/blog/1327-creating-files-on-github)
   - [Ukládání souborů v úložištích](https://github.com/blog/2105-upload-files-to-your-repositories)

4. Posuňte se na dolů konec stránky, kde uvidíte jednu z těchto možností:

   - **Navrhnout změnu souboru** – zobrazí se, když máte k úložišti přístup jenom pro čtení, třeba při [upravování souborů v úložišti jiného uživatele](https://help.github.com/articles/editing-files-in-another-user-s-repository/). V takovém případě GitHub vytvoří „opravnou“ větev ve vašem forku úložiště (a pokud fork neexistuje, automaticky ho vytvoří). Po výběru možnosti **Navrhnout změnu souboru** se zobrazí stránka **Srovnání změn**, abyste své změny mohli ověřit. Pak kliknutím na **Vytvořit žádost o přijetí změn** změny odešlete do fronty žádostí o přijetí změn a pokračujte na [další sekci](#pull-request-processing).

   - **Potvrdit změny** – zobrazí se, když máte k úložišti oprávnění k zápisu, třeba při [upravování souborů ve vlastním úložišti](https://help.github.com/articles/editing-files-in-your-repository/). V takovém případě vám dá GitHub dvě možnosti k uložení změn:

     - **Potvrdit přímo ve větvi `<branch-name>`**, kde `<branch-name>` je název větve, ve které jste byli, když jste použili tlačítko **Upravit**. Vaše změny se tím použijí přímo ve větvi, místo aby se použila žádost o přijetí změn. Tím máte všechno hotovo.

     - **Vytvořit novou větev pro toto potvrzení a zahájit žádost o přijetí změn** zobrazí výzvu k vytvoření nové větve s výchozím názvem. Po výběru možnosti **Navrhnout změnu souboru** se zobrazí stránka **Srovnání změn**, abyste své změny mohli ověřit. Pak kliknutím na **Vytvořit žádost o přijetí změn** změny odešlete do fronty žádostí o přijetí změn a pokračujte na [další sekci](#pull-request-processing).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Další kroky

- Pokud se chcete dozvědět víc o Markdownu, syntaxi rozšíření Markdownu a dalších tématech, pokračujte na články Základy psaní.
