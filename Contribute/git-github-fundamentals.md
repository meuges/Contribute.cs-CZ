---
title: Základy Gitu a GitHubu pro dokumentaci
description: Tento článek poskytuje přehled úložišť Git a GitHub a způsob uspořádání obsahu a konvence vytváření názvů pro web docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 5f7f90b69953e23833906202c739d2168b139d7e
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="git-and-github-essentials-for-docs"></a>Základy Gitu a GitHubu pro web Docs

## <a name="overview"></a>Přehled

Jako přispěvatelé k obsahu na webu Docs budete používat více nástrojů a procesů. Budete pracovat souběžně s ostatními přispěvateli na stejném projektu, možná na úplně stejném obsahu, dokonce i ve stejnou dobu. To vše umožňuje software Gitu a GitHubu.

Git je open-sourcový systém správy verzí. Usnadňuje tento typ spolupráce na projektech prostřednictvím *distribuovaného systému správy verzí* souborů umístěných v *úložištích*. Git v podstatě umožňuje u daného úložiště integrovat proudy práce provedené několika přispěvateli v průběhu času.

GitHub je webová hostitelská služba pro úložiště Git, včetně těch, která se používají k ukládání obsahu webu [docs.microsoft.com](https://docs.microsoft.com). U každého projektu GitHub hostuje hlavní úložiště, ze kterého můžou přispěvatelé vytvářet kopie pro vlastní potřebu.

## <a name="git"></a>Git

Pokud už centralizované systémy správy verzí znáte (například Team Foundation Server, SharePoint nebo Visual SourceSafe), všimnete si, že Git pro podporu svého distribuovaného modelu používá jedinečný pracovní postup a terminologii pro přispěvatele. Například neexistuje zamykání souborů, které je běžně spojené s operacemi rezervovat a vrátit se změnami. Git se ve skutečnosti zajímá o změny i na nižší úrovni a porovnává soubory bajt po bajtu.

Git také k ukládání a správě obsahu pro projekt používá strukturu úrovní:

- *Úložiště*: *úložiště* je nejvyšší jednotka pro ukládání dat. Úložiště obsahuje jednu nebo více větví.
- *Větev*: jednotka úložiště obsahující soubory a složky, které tvoří sadu obsahu projektu. Větve oddělují toky práce (obvykle označované jako verze). Příspěvky se vždy provádějí do konkrétní větve. Všechna úložiště obsahují výchozí větev (která se obvykle označuje jako „hlavní“) a jednu nebo víc větví určených ke sloučení s hlavní větví. Hlavní větev slouží jako aktuální verze a „jediný zdroj pravdy“ pro projekt. Je nadřazenou větví, ze které se vytvářejí všechny ostatní větve v úložišti.

Přispěvatelé při práci s Gitem aktualizují a upravují úložiště jak na místní úrovni, tak na úrovni GitHubu:

- Místně prostřednictvím nástrojů jako je konzola Git Bash, která podporuje příkazy Gitu pro správu místních úložišť a komunikaci s úložišti GitHub.
- Prostřednictvím webu [www.github.com](https://www.github.com), který integruje Git pro účely správy sloučení příspěvků, které se přenášejí zpět do hlavního úložiště.

## <a name="github"></a>GitHub

> [!NOTE]
> Články s pokyny na webu Docs jsou sice založené na používání GitHubu, ale některé týmy používají k hostování úložišť Git službu Visual Studio Team Service. Klient Visual Studio Team Explorer poskytuje pro interakci s úložišti Team Service grafické uživatelské rozhraní, které je alternativou k používání příkazů Git pomocí příkazového řádku.
> </br>
> Mnoho z následujících článků s pokyny bylo také vyvinuto pomocí osvědčených postupů po několika letech zkušeností s hostováním obsahu služby Azure v GitHubu. V některých úložištích Docs je možná budete potřebovat.

Všechny pracovní postupy začínají i končí na úrovni GitHubu, kde se nachází hlavní úložiště všech projektů Docs. Kopie, které přispěvatelé vytvářejí pro vlastní potřebu, jsou distribuované na víc počítačů. Tyto kopie se nakonec sloučí zpět do hlavního úložiště GitHub projektu.

### <a name="directory-organization"></a>Organizace adresáře

Jak jsme už zmínili, výchozí/hlavní větev projektu slouží jako aktuální verze obsahu projektu. Obsah v hlavní větvi (a ve větvích z ní vytvořených) přibližně odpovídá uspořádání článků na odpovídajících stránkách webu Docs. Podadresáře se používají k oddělení podobného obsahu (jako jsou služby) a multimediálního obsahu (jako jsou obrázky) a „zahrnují“ soubory (které umožňují opakované použití obsahu).

Hlavní adresář `articles` obvykle najdete v kořenovém adresáři úložiště. Adresář článků obsahuje sadu podadresářů. Články v podadresářích jsou formátované jako soubory Markdownu, které používají příponu *.md*. Některá úložiště podporující více služeb používají obecný podadresář `/articles`, jako například úložiště [https://github.com/microsoft/Azure-Docs](https://github.com/microsoft/Azure-Docs). Jiná můžou použít název specifický pro službu, jako například úložiště [https://github.com/microsoft/IntuneDocs](https://github.com/microsoft/IntuneDocs), které používá `/IntuneDocs`.

V kořenové složce tohoto adresáře naleznete obecné články související s obecným fungováním služby nebo produktu. Obvykle pak také najdete další řady podadresářů, které odpovídají příslušným funkcím/službám nebo běžným scénářům. Třeba články o „virtuálním počítači“ Azure jsou v podadresáři `/virtual-machines`, zatímco články o „porozumění a prozkoumání“ Intune jsou v podadresáři `/understand-explore`.

### <a name="media-subdirectory"></a>Podadresář Media

Adresář každého článku obsahuje podadresář `/media` pro odpovídající soubory médií. Soubory médií obsahují obrázky používané v článcích, které odkazují na obrázky.

### <a name="includes-subdirectory"></a>Podadresář Includes

Pokud máme nějaký opakovaně použitelný obsah, který je sdílený dvěma nebo více články, je umístěný v podadresáři `/includes` hlavního adresáře `articles`. Do souboru Markdownu, který používá příslušný soubor zahrnutí, se na místo, kde se na tento soubor má odkazovat, umístí odpovídající rozšíření Markdownu pro „zahrnutí“.

Další pokyny najdete v části článku [Jak používat Markdown: Zahrnutí](how-to-write-use-markdown.md#includes).

### <a name="markdown-file-template"></a>Šablona souboru Markdown

Kořenový adresář každého úložiště obvykle pro pohodlnější používání obsahuje soubor šablony Markdownu s názvem `template.md`. Tento soubor šablony můžete použít jako „výchozí soubor“, pokud potřebujete vytvořit nový článek k odeslání do úložiště. Tento soubor obsahuje:

- **Záhlaví metadat** v horní části souboru, vymezené dvěma řádky tvořenými třemi spojovníky. Obsahuje různé značky používané ke sledování informací týkajících se článku. Metadata článku umožňují některé funkce, jako je uvedení autora, uvedení přispěvatele, popis cesty a popisy článku. Zahrnují také optimalizaci pro vyhledávače (SEO) a procesy vytváření sestav, které Microsoft používá k vyhodnocení výkonu obsahu. Metadata jsou tedy důležitá.
- **Sekci metadat** popisující různé hodnoty a značky metadat. Pokud si nejste jistí, jaké hodnoty je třeba pro sekci metadat použít, můžete ji nechat prázdnou nebo přidat komentář začínající hashtagem (#). Kontrolor žádostí o přijetí změn pro příslušné úložiště pak tuto sekci zkontroluje a dokončí.
- Různé **příklady použití formátu Markdown** pro formátování prvků článku.
- Obecné **pokyny týkající se použití rozšíření Markdownu**, která můžete použít pro různé typy výstrah
- Příklady **vložení videa** pomocí iframe
- Obecné **pokyny týkající se použití rozšíření docs.microsoft.com**, která můžete použít pro speciální ovládací prvky, jako jsou tlačítka a selektory

## <a name="pull-requests"></a>Žádosti o přijetí změn

*Žádost o přijetí změn* představuje pohodlný způsob pro přispěvatele, jak navrhnout sadu změn, které se mají použít na výchozí větev. Změny (označované také jako *potvrzení*) jsou uložené ve větvi přispěvatele. GitHub tak může dopad jejich *sloučení* s výchozí větví nejdřív namodelovat. Žádost o přijetí změn také slouží jako mechanismus, který poskytne přispěvateli zpětnou vazbu z procesu sestavení a ověření, od recenzenta žádostí o přijetí změn nebo z dotazů položených před sloučením s výchozí větví.

Existují dva způsoby, jak pomocí žádosti o přijetí změn přispívat, a to podle velikosti změn, které chcete navrhnout. Budeme se tím podrobně zabývat později v oddílech [pracovního postupu pro GitHub](how-to-write-workflows-major.md) tohoto průvodce.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
