---
title: Balíček pro vytváření obsahu na webu Docs pro Visual Studio Code
description: Tento článek popisuje balíček rozšíření pro Visual Studio Code, který usnadňuje vytváření obsahu v jazyce Markdown pro docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336392"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Balíček pro vytváření obsahu na webu Docs pro VS Code

Balíček pro vytváření obsahu na webu Docs je kolekce rozšíření nástroje VS Code, který vám pomůže s vytvářením obsahu v jazyce Markdown pro docs.microsoft.com. Balíček je [dostupný na VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) a obsahuje následující rozšíření:

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Poskytuje pomoc při vytváření obsahu v Markdownu pro web docs.microsoft.com (Docs), včetně podpory základního Markdownu a podpory vlastní syntaxe na webu Docs, jako jsou výstrahy, fragmenty kódu a nelokalizovaný text. Nově také obsahuje pomoc při vytváření YAML, například vkládání položek obsahu.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Oblíbený linter Markdownu od Davida Ansona, který pomáhá udržovat Markdown platný
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Kontrola pravopisu od firmy Street Side Software, která je plně offline.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Používá šablonu stylů CSS z webu docs.microsoft.com k přesnějšímu zobrazení náhledu Markdownu, včetně vlastního Markdownu.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Umožňuje uživatelům generovat moduly webu Learn a u nových souborů použít obsah, který představuje kostru Markdownu.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Umožňuje ověřování schémat a automatické dokončení YAML pro web Docs.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): Umožňuje autorům webu docs.microsoft.com komprimovat obrázky a měnit jejich velikost ve složkách a jednotlivých souborech.

## <a name="prerequisites-and-assumptions"></a>Požadavky a předpoklady

Pokud chcete vkládat relativní odkazy, obrázky a další vložený obsah pomocí rozšíření Docs Markdown, musí být oborem pracovního prostoru nástroje VS Code kořen naklonovaného úložiště OPS (Open Publishing System). Pokud jste například naklonovali úložiště Docs do `C:\git\SomeDocsRepo\`, otevřete danou složku nebo podsložku v nástroji VS Code a vyberte **Soubor** > **Otevřít složku**, nebo zadejte `code C:\git\SomeDocsRepo\` na příkazovém řádku.

Určité syntaxe podporované rozšířením, například výstrahy a fragmenty kódu, představují vlastní Markdown pro OPS. Ten se nebude správně vykreslovat, dokud ho nepublikujete přes OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Použití rozšíření Docs Markdown

K nabídce **Docs Markdown** se dostanete tak, že stisknete <kbd>ALT+M</kbd>. Požadovaný příkaz vyberete kliknutím nebo pomocí šipek nahoru a dolů. Případně můžete zadáním textu spustit filtrování, a jakmile se v nabídce zvýrazní nabídka, kterou hledáte, stisknout klávesu <kbd>Enter</kbd>.

Aktuální seznam příkazů najdete v [souboru readme pro Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown).

## <a name="how-to-generate-a-master-redirect-file"></a>Vygenerování hlavního souboru přesměrování

Rozšíření Docs Markdown obsahuje skript, pomocí kterého lze vygenerovat nebo aktualizovat hlavní soubor přesměrování pro úložiště na základě metadat `redirect_url` v jednotlivých souborech. Tento skript vyhledá `redirect_url` v každém souboru Markdownu v úložišti, přidá metadata přesměrování do hlavního souboru přesměrování ( *.openpublishing.redirection.json*) pro toto úložiště a přesune přesměrované soubory do složky mimo ně. Spuštění skriptu:

1. Výběrem klávesy <kbd>F1</kbd> otevřete paletu příkazů nástroje VS Code.
2. Začněte zadávat „Docs: Generate...“
3. Vyberte příkaz `Docs: Generate master redirection file`.
4. Po dokončení skriptu se výsledky přesměrování zobrazí v podokně výstupů nástroje VS Code a odebrané soubory Markdownu se přidají do složky Docs Authoring\redirects ve výchozí cestě.
5. Zkontrolujte výsledky. Pokud jste s nimi spokojeni, odešlete žádost o přijetí změn, aby se úložiště aktualizovalo.

## <a name="how-to-assign-keyboard-shortcuts"></a>Přiřazení klávesových zkratek

1. Zadejte <kbd>CTRL+K</kbd> a potom <kbd>Ctrl+S</kbd>, aby se otevřel seznam **klávesových zkratek**.
1. Vyhledejte příkaz, například `formatBold`, pro který si chcete vytvořit svoji klávesovou zkratku.
1. Klikněte na znaménko plus, které se zobrazí vedle názvu příkazu, když na řádek najedete myší.
1. Jakmile se zobrazí nové okno pro zadání, napište klávesovou zkratku, kterou chcete spojit s konkrétním příkazem. Pokud chcete například použít běžnou zkratku pro zvýraznění tučně, zadejte <kbd>Ctrl+B</kbd>.
1. Do klávesové zkratky je vhodné vložit klauzuli `when`, aby nebyla dostupná v jiných souborech než v Markdownu. To uděláte tak, že otevřete soubor *keybindings.json* a pod název příkazu vložíte následující řádek (mezi řádky nezapomeňte uvést čárku):

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Dokončená vlastní klávesová zkratka by v souboru *keybindings.json* měla vypadat takto:

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > Umístěním klávesové zkratky do tohoto souboru přepíšete výchozí hodnoty.

1. Soubor *keybindings.json* uložte.

Další informace o klávesových zkratkách najdete v [dokumentaci k nástroji VS Code](https://code.visualstudio.com/docs/getstarted/keybindings).

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Zobrazení staršího panelu nástrojů Gauntlet

Uživatelé staršího rozšíření s kódovým názvem Gauntlet si mohou všimnout, že po instalaci rozšíření Docs Markdown se panel pro vytváření obsahu už nezobrazuje v dolní části okna nástroje VS Code. Důvodem je to, že panel nástrojů zabíral mnoho místa na stavovém řádku nástroje VS Code a neřídil se doporučenými postupy pro uživatelské prostředí rozšíření, a proto se v novém rozšíření už nepoužívá. Panel nástrojů si ale můžete volitelně zobrazit, když následujícím způsobem aktualizujete soubor settings.json v nástroji VS Code:

1. V nástroji VS Code přejděte na **Soubor** > **Předvolby** > **Nastavení** nebo vyberte <kbd>Ctrl+,</kbd>.
1. Pokud chcete změnit nastavení všech pracovních prostorů nástroje VS Code, vyberte **Uživatelská nastavení**. Pokud chcete změnit jen nastavení aktuálního pracovního prostoru, vyberte **Nastavení pracovního prostoru**.
1. Vyberte **Rozšíření** > **Docs Markdown Extension Configuration** (Konfigurace rozšíření Docs Markdown) a potom vyberte **Show the legacy toolbar in the bottom status bar** (Zobrazit starší panel nástrojů na spodním stavovém řádku).

   ![Nastavení zobrazení staršího panelu nástrojů v nástroji VS Code](docs-authoring/media/show-gauntlet-bar.png)

Jakmile výběr dokončíte, VS Code aktualizuje soubor *settings.json*. Potom vás systém vyzve, ať znovu načtete okno, aby se mohly změny projevit.

Novější příkazy přidané do rozšíření nebudou na tomto panelu nástrojů k dispozici.

## <a name="how-to-use-docs-templates"></a>Jak používat šablony dokumentů

Rozšíření Docs Article Templates umožňuje autorům stáhnout v nástroji VS Code šablonu Markdownu z centralizovaného úložiště a aplikovat ji na soubor. Šablony například pomáhají zajistit, aby články obsahovaly požadovaná metadata a aby se dodržovaly standardy týkající se obsahu. Šablony se spravují jako soubory Markdown ve veřejném úložišti GitHubu.

### <a name="to-apply-a-template-in-vs-code"></a>Použití šablony v nástroji VS Code

1. Zkontrolujte, že je nainstalované a povolené rozšíření Docs Article Templates.
1. Pokud nemáte nainstalované rozšíření Docs Markdown, stisknutím klávesy <kbd>F1</kbd> otevřete paletu příkazů, začněte do filtru psát „template“ a pak klikněte na `Docs: Template`. Pokud rozšíření Docs Markdown máte nainstalované, můžete pomocí palety příkazů nebo kliknutím na <kbd>Alt+M</kbd> vyvolat nabídku Docs Markdown QuickPick a v seznamu vybrat `Template`.
1. V zobrazeném seznamu vyberte požadovanou šablonu.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Přidání ID GitHubu a/nebo aliasu Microsoftu do nastavení nástroje VS Code

Rozšíření Templates podporuje tři dynamická pole metadat: author, ms.author a ms.date. To znamená, že když autor šablony tato pole použije v záhlaví metadat nějaké šablony Markdownu, při jejím použití se tato pole automaticky naplní ve vašem souboru následujícím způsobem:

| Pole metadat | Hodnota |
|--|--|
| `author` | Váš alias na GitHubu, pokud je zadané v souboru nastavení nástroje VS Code |
| `ms.author` | Váš alias Microsoftu, pokud je zadaný v souboru nastavení nástroje VS Code. Pokud nejste zaměstnancem Microsoftu, nechejte toto pole nezadané. |
| `ms.date` | Aktuální datum ve formátu `MM/DD/YYYY` podporovaném v Docs. Toto datum se při následné aktualizaci souboru neaktualizuje automaticky, takže je potřeba ho aktualizovat ručně. Slouží k označení aktuálnosti článků. |

### <a name="to-set-author-andor-msauthor"></a>Nastavení polí author a/nebo ms.author

1. V nástroji VS Code přejděte na **Soubor** > **Předvolby** > **Nastavení** nebo vyberte <kbd>Ctrl+,</kbd>.
1. Pokud chcete změnit nastavení všech pracovních prostorů nástroje VS Code, vyberte **uživatelská nastavení**. Pokud chcete změnit jen nastavení aktuálního pracovního prostoru, vyberte **nastavení pracovního prostoru**.
1. V podokně Výchozí nastavení vlevo najděte **konfiguraci rozšíření Docs Article Templates**, klikněte na ikonu tužky vedle požadovaného nastavení a pak klikněte na Nahradit v Nastavení.
1. Vedle se otevře podokno **uživatelských nastavení** s novou položkou v dolní části.
1. Přidejte svoje ID GitHubu nebo e-mailový alias Microsoftu a uložte tento soubor.
1. Možná budete muset nástroj VS Code zavřít a znovu spustit, aby se změny projevily.
1. Když teď použijete šablonu využívající dynamická pole, naplní se v záhlaví metadat automaticky vaše ID GitHubu a/nebo alias Microsoftu.

### <a name="to-make-a-new-template-available-in-vs-code"></a>Zpřístupnění nové šablony v nástroji VS Code

1. Vytvořte koncept šablony jako soubor Markdownu.
1. Odešlete žádost o přijetí změn do složky šablon úložiště [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates).

Tým webu docs.microsoft.com vaši šablonu zkontroluje a pokud bude splňovat pravidla pro styl webu docs.microsoft.com, žádost sloučí. Po sloučení bude šablona k dispozici všem uživatelům rozšíření Docs Article Templates.

## <a name="demo-several-features"></a>Ukázka několika funkcí

Níže najdete krátké video, které vás seznámí s několika funkcemi balíčku pro vytváření obsahu na webu Docs:

* **Soubory YAML**
  * Podpora pro „Docs: Link to file in repo“
* **Soubory Markdownu**
  * Možnost „Update "ms.date" Metadata Value“ v místní nabídce
  * Podpora automatického dokončování kódu pro identifikátory jazyka kódového plotu
  * Upozornění na nerozpoznané identifikátory jazyka kódového plotu / podpora automatických oprav
  * Seřazení výběru vzestupně (od A do Z)
  * Seřazení výběru sestupně (od Z do A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>Doba do zveřejnění příspěvku

Balíček pro vytváření obsahu na webu Docs je opensourcový a dostupný všem přispěvatelům s účtem na GitHubu. Na tomto projektu aktivně pracuje také určený interní tým Microsoftu. Ten sleduje potíže a žádosti o přijetí změn. Smlouva o úrovni služeb (SLA) a doba do provedení kontroly žádosti je aktuálně jeden týden. Tým se ale snaží proces postupně automatizovat a tím dobu zkrátit.

## <a name="next-steps"></a>Další kroky

Seznamte se i dalšími funkcemi balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).

* [Dokončení platných identifikátorů jazyka](docs-authoring/dev-lang-completion.md)
* [Komprese obrázků](docs-authoring/image-compression.md)
* [Aktualizace metadat](docs-authoring/metadata-updates.md)
* [Přeformátování tabulek](docs-authoring/reformat-table.md)
* [Nahrazení chytrých uvozovek](docs-authoring/smart-quote-replacement.md)
* [Řazení přesměrování](docs-authoring/sort-redirects.md)
* [Výběr řazení](docs-authoring/sort-selection.md)
