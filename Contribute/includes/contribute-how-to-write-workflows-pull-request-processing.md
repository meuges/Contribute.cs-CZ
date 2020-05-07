---
ms.openlocfilehash: 9cb0ba651d40d2834081d32443a8fd2b1152003d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "53286102"
---
## <a name="pull-request-processing"></a>Zpracování žádosti o přijetí změn

Předchozí oddíl vás provedl procesem odeslání navrhovaných změn, kdy se tyto změny seskupí do nové žádosti o přijetí změn, která se přidá do fronty žádostí o přijetí změn v cílovém úložišti. Žádost o přijetí změn umožňuje model spolupráce na GitHubu, a to tak, že se vyžádá přijetí změn z vaší pracovní větve a jejich sloučení do další větve. Ve většině případů je tou další větví výchozí/hlavní větev v hlavním úložišti.

### <a name="validation"></a>Ověřování

Před sloučením žádosti o přijetí změn do její cílové větve se může vyžadovat, aby prošla jedním nebo více procesy ověřování. Procesy ověřování se mohou lišit v závislosti na rozsahu navrhovaných změn a pravidlech cílového úložiště. Po odeslání žádosti o přijetí změn se většinou provede jedna nebo několik z následujících akcí:

- **Slučitelnost**: Nejdříve se na GitHubu provede základní test slučitelnosti, který ověří, jestli změny navrhované ve vaší větvi nejsou v konfliktu s cílovou větví. Pokud žádost o přijetí změn neprojde tímto testem úspěšně, je nutné před pokračováním procesu upravit obsah, který konflikt způsobuje.
- **Smlouva CLA**: Pokud přispíváte do veřejného úložiště, nejste zaměstnancem Microsoftu a jedná se o první odeslání žádosti o přijetí změn do daného úložiště, můžete být v závislosti na rozsahu navrhovaných změn požádáni o vyplnění krátké licenční smlouvy s přispěvatelem (CLA). Po odsouhlasení smlouvy CLA se vaše žádost o přijetí změn zpracuje.
- **Popisky**: K žádosti o přijetí změn se automaticky přiřazují popisky, které označují stav žádosti o přijetí změn během procesu ověřování. Například nové žádosti o přijetí změn mohou automaticky dostat popisek „neslučovat“, který indikuje, že pro danou žádost o přijetí změn se ještě neprovedlo ověření, posouzení ani schválení.
- **Ověření a sestavení**: Automatizované kontroly ověřují, zda vaše změny projdou ověřovacími testy. Ověřovací testy mohou zobrazit upozornění nebo chyby, které vyžadují, abyste před sloučením žádosti o přijetí změn provedli změny v jednom nebo více souborech. Výsledky ověřovacího testu se k žádosti o přijetí změn přidávají jako komentář pro kontrolu a můžete je dostat také e-mailem.
- **Příprava**: Stránky článku ovlivněné vašimi změnami se po úspěšném ověření a sestavení automaticky nasadí do přípravného prostředí pro posouzení. V komentáři k žádosti o přijetí změn se zobrazí adresy URL náhledu.
- **Automatické sloučení**: Pokud žádost o přijetí změn projde ověřovacím testováním úspěšně a splňuje určitá kritéria, může se sloučit automaticky. V takovém případě nemusíte provádět žádnou další akci.

### <a name="review-and-sign-off"></a>Posouzení a schválení

Po dokončení všech akcí zpracování žádosti o přijetí změn byste měli posoudit výsledky (komentáře k žádosti o přijetí změn, adresy URL náhledu atd.) a určit, jestli budou před schválením pro sloučení nutné další změny v souborech. Pokud kontrolor žádostí o přijetí změn vaši žádost posoudil a našel nějaké nevyřízené problémy nebo otázky, které je potřeba před sloučením vyřešit, může svůj názor vyjádřit prostřednictvím komentářů.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Když je žádost o přijetí změn bez problémů a proběhlo schválení, sloučí se změny do nadřazené větve a žádost o přijetí změn se zavře.

### <a name="publishing"></a>Publikování

Upozorňujeme, že změny se mohou zahrnout do dalšího plánovaného spuštění publikování až poté, co žádost o přijetí změn sloučí kontrolor. Žádosti o přijetí změn se obvykle posuzují a slučují v pořadí, ve kterém se odeslaly. Pokud vaše žádost o přijetí změn vyžaduje sloučení pro konkrétní spuštění publikování, bude potřeba, abyste se s kontrolorem předem domluvili a zajistili tak, že se sloučení provede před publikováním.

Po schválení a sloučení příspěvků přebere příspěvky proces publikování na docs.microsoft.com. Časy publikování se můžou lišit v závislosti na týmu, který spravuje úložiště, do něhož přispíváte. Články publikované pod následujícími cestami se obvykle nasazují od pondělí do pátku přibližně v 10:30 a 15:30 (místní čas Tichomoří):

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Po publikování může trvat až 45 minut, než se články zobrazí online. Po publikování článku můžete svoje změny ověřit na příslušné adrese URL: `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
