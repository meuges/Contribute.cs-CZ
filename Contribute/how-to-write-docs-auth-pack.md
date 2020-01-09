---
title: Balíček pro vytváření obsahu na webu Docs pro Visual Studio Code
description: Tento článek popisuje balíček rozšíření pro Visual Studio Code, který usnadňuje vytváření obsahu v jazyce Markdown pro docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 10/22/2018
ms.openlocfilehash: 1552ecc3e17e52439a7faa72973813099ce4d253
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188299"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Balíček pro vytváření obsahu na webu Docs pro VS Code

Balíček pro vytváření obsahu na webu Docs je kolekce rozšíření nástroje Visual Studio Code, která vám pomohou s vytvářením obsahu v jazyce Markdown pro docs.microsoft.com. Balíček je [dostupný na VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) a obsahuje následující rozšíření:

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Oblíbený linter Markdownu od Davida Ansona, který pomáhá dodržovat osvědčené postupy Markdownu.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): Kontrola pravopisu od firmy Street Side Software, která je plně offline.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Používá šablonu stylů CSS z webu docs.microsoft.com k přesnějšímu zobrazení náhledu Markdownu, včetně vlastního Markdownu.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Poskytuje pomoc při vytváření obsahu v Markdownu pro docs.microsoft.com v systému OPS (Open Publishing System), včetně podpory základního Markdownu a podpory vlastní syntaxe Markdownu v OPS. Ve zbývající části tématu se popisuje rozšíření Markdown Docs.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Umožňuje uživatelům u nových souborů použít obsah, který představuje kostru Markdownu.

## <a name="prerequisites-and-assumptions"></a>Požadavky a předpoklady

Pokud chcete přesně vkládat relativní odkazy, obrázky a další vložený obsah pomocí rozšíření Docs Markdown, musí být oborem pracovního prostoru nástroje VS Code kořen naklonovaného úložiště OPS (Open Publishing System).

Určité syntaxe podporované rozšířením, například výstrahy a fragmenty kódu, představují vlastní Markdown pro OPS a nebudou se správně vykreslovat, dokud je nepublikujete přes OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Použití rozšíření Docs Markdown

K nabídce Docs Markdown se dostanete tak, že stisknete `ALT+M`. Kliknutím nebo klávesami se šipkami nahoru a dolů můžete vybrat požadovanou funkci. Můžete ale také začít psát a spustit filtrování. Jakmile se požadovaná funkce zvýrazní v nabídce, stačí stisknout `ENTER`. K dispozici jsou následující funkce:

|Funkce     |Description           |
|-------------|----------------------|
|Náhled      |Zobrazí náhled aktivního tématu ve vedlejším okně pomocí rozšíření Docs Preview. Tato možnost je dostupná jen v případě, že je nainstalované rozšíření Docs Preview.|
|Tučné         |Formátuje text **tučně**.|
|Kurzíva       |Formátuje text jako *kurzívu*.|
|Kód         |Pokud vyberete jeden nebo žádný řádek, formátuje text jako `inline code`.<br><br>Pokud vyberete více řádků, formátuje je jako ohraničený blok kódu a umožní vám volitelně vybrat programovací jazyk podporovaný systémem OPS.|
|Výstrah        |Vloží poznámku, důležitou informaci, upozornění nebo tip.<br><br>Nejprve vyberte z nabídky výstrahu a potom její typ. Pokud jste už nějaký text vybrali, umístí se do vybrané syntaxe výstrahy. Pokud jste žádný text nevybrali, nová výstraha se vloží se zástupným textem.|
|Číslovaný seznam|Vloží nový číslovaný seznam.<br><br> Pokud vyberete více řádků, bude každý z nich představovat položku seznamu. Všimněte si, že se v Markdownu číslované seznamy zobrazují všechny jako 1, ale na docs.microsoft.com se zobrazí očíslované posloupně a u vnořených seznamů označené písmeny. Vnořený číslovaný seznam vytvoříte tak, že požadované položky odsadíte od nadřazeného seznamu pomocí tabulátoru.|
|Seznam s odrážkami|Vloží nový seznam s odrážkami.|
|Tabulka        |Vloží tabulkovou strukturu Markdownu.<br><br>Po výběru příkazu k vytvoření tabulky zadejte počet sloupců a řádků ve formátu sloupce:řádky, například 3:4. Všimněte si, že maximální počet sloupců, které můžete zadat prostřednictvím tohoto rozšíření, je 5, což je doporučený maximální počet s ohledem na čitelnost.|
|Odkaz na soubor v úložišti|Vloží relativní odkaz na jiný soubor v aktuálním úložišti. Po výběru této možnosti začněte psát do okna příkazu, aby se začaly filtrovat soubory podle názvu, a potom vyberte požadovaný soubor. Pokud jste předtím vybrali text, stane se z něho text odkazu. V opačném případě se jako text odkazu použije H1 cílového souboru.|
|Odkaz na webovou stránku    |Vloží odkaz na webovou stránku. Po výběru této možnosti vložte nebo napište do příkazového okna identifikátor URI. `https://` je povinné. Pokud jste předtím vybrali text, stane se z něho text odkazu. V opačném případě se jako text odkazu použije identifikátor URI.|
|Odkaz na nadpis     |Vytvoří odkaz na záložku v aktuálním souboru nebo jiném souboru v úložišti.<br>`Bookmark in this file`: Vyberte položku ze seznamu nadpisů v aktuálním souboru, aby se vložila správně naformátovaná záložka.<br>`Bookmark in another file`: Nejprve filtrujte soubory podle jejich názvu, vyberte soubor, na který chcete vytvořit odkaz, a potom ve vybraném souboru vyberte odpovídající nadpis.|
|Obrázek        |Zadejte alternativní text (vyžadovaný z důvodu usnadnění) a vyberte ho. Potom zavolejte tento příkaz, aby se vyfiltroval seznam podporovaných souborů obrázků v úložišti, a vyberte požadovaný soubor. Pokud jste při volání tohoto příkazu neměli vybraný alternativní text, zobrazí se výzva k jeho výběru, než budete moci vybrat soubor obrázku.|
|Vložený soubor      |Vyhledá soubor, který se má vložit do aktuálního souboru.|
|Fragment kódu      |Vyhledá fragment kódu v úložišti, který se má vložit do aktuálního souboru.|
|Video        |Přidá vložené video.|
|Šablona     |Vytvoří nový soubor a použije šablonu Markdownu. Další informace najdete v části [Šablony](#how-to-use-docs-templates) níže.|

## <a name="how-to-assign-keyboard-shortcuts"></a>Přiřazení klávesových zkratek

1. Zadejte `CTRL+K` a potom `CTRL+S`, aby se otevřel seznam klávesových zkratek.
1. Vyhledejte příkaz, například `formatBold`, pro který si chcete vytvořit svoji klávesovou zkratku.
1. Klikněte na znaménko plus, které se zobrazí vedle názvu příkazu, když na řádek najedete myší.
1. Jakmile se zobrazí nové okno pro zadání, napište klávesovou zkratku, kterou chcete spojit s konkrétním příkazem. Pokud chcete například použít běžnou zkratku pro zvýraznění tučně, zadejte `ctrl+b`.
1. Do klávesové zkratky je vhodné vložit klauzuli `when`, aby nebyla dostupná v jiných souborech než v Markdownu. To uděláte tak, že otevřete soubor *keybindings.json* a pod název příkazu vložíte následující řádek (mezi řádky nezapomeňte uvést čárku):
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Dokončená vlastní klávesová zkratka by v souboru keybindings.json měla vypadat takto:

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Soubor keybindings.json uložte.

Další informace najdete v tématu věnovaném [klávesovým zkratkám](https://code.visualstudio.com/docs/getstarted/keybindings) v dokumentaci k nástroji VS Code.

## <a name="how-to-show-the-legacy-toolbar"></a>Jak zobrazit zastaralý panel nástrojů

Uživatelé předběžné verze rozšíření si všimnou, že po instalaci rozšíření Docs Markdown se panel pro vytváření obsahu už nezobrazuje v dolní části okna nástroje VS Code. Důvodem je to, že panel nástrojů zabíral příliš mnoho místa na stavovém řádku nástroje VS Code a neřídil se doporučenými postupy pro uživatelské prostředí rozšíření, a proto se v novém rozšíření už nepoužívá. Panel nástrojů si ale můžete volitelně zobrazit, když následujícím způsobem aktualizujete soubor settings.json v nástroji VS Code:

1. V nástroji VS Code přejděte na Soubor -> Předvolby -> Nastavení (`CTRL+Comma`).
1. Pokud chcete změnit nastavení všech pracovních prostorů nástroje VS Code, vyberte Uživatelská nastavení. Pokud chcete změnit nastavení pouze aktuálního pracovního prostoru, vyberte Nastavení pracovního prostoru.
1. V podokně Výchozí nastavení vyhledejte část týkající se konfigurace rozšíření pro vytváření obsahu pro web Docs a vyberte ikonu tužky vedle požadovaného nastavení. Zobrazí se výzva k výběru možnosti `true` nebo `false`. Po výběru požadované možnosti VS Code automaticky přidá hodnotu do souboru settings.json a zobrazí výzvu k opakovanému načtení okna, aby se změny projevily.

## <a name="how-to-use-docs-templates"></a>Jak používat šablony dokumentů

Rozšíření Docs Article Templates umožňuje autorům stáhnout v nástroji VS Code šablonu Markdownu z centralizovaného úložiště a aplikovat ji na soubor. Šablony například pomáhají zajistit, aby články obsahovaly požadovaná metadata a aby se dodržovaly standardy týkající se obsahu. Šablony se spravují jako soubory Markdown ve veřejném úložišti GitHubu.

### <a name="to-apply-a-template-in-vs-code"></a>Použití šablony v nástroji VS Code

1. Pokud nemáte nainstalované rozšíření Docs Markdown, stisknutím klávesy F1 otevřete paletu příkazů, začněte do filtru psát „template“ a pak klikněte na `Docs: Template`. Pokud máte rozšíření Docs Markdown nainstalované, můžete pomocí palety příkazů nebo kliknutím na `Alt+M` vyvolat nabídku Docs Markdown QuickPick a v seznamu vybrat `Template`.
1. V zobrazeném seznamu vyberte požadovanou šablonu.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Přidání ID GitHubu a/nebo aliasu Microsoftu do nastavení nástroje VS Code

Rozšíření Templates podporuje tři dynamická pole metadat: author, ms.author a ms.date. To znamená, že když autor šablony tato pole použije v záhlaví metadat nějaké šablony Markdownu, při jejím použití se tato pole automaticky naplní ve vašem souboru následujícím způsobem:

|Metadata  |Hodnota|
|----------|---------------|
|author    |Vaše ID GitHubu, pokud je zadané v souboru nastavení nástroje VS Code.|
|ms.author |Váš alias Microsoftu, pokud je zadaný v souboru nastavení nástroje VS Code. Pokud nejste zaměstnancem Microsoftu, nechejte toto pole nezadané.|
|ms.date   |Aktuální datum ve formátu MM/DD/RRRR podporovaném v Docs. Toto datum se při následné aktualizaci souboru neaktualizuje automaticky. Ruční aktualizací hodnoty ms.date musíte vyznačit nejnovější datum publikování na webu docs.microsoft.com.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>Nastavení polí author (ID GitHubu) a/nebo ms.author (alias Microsoftu)

1. V nástroji VS Code přejděte na Soubor -> Předvolby -> Nastavení (`CTRL+Comma`).
1. Pokud chcete změnit nastavení všech pracovních prostorů nástroje VS Code, vyberte Uživatelská nastavení. Pokud chcete změnit jen nastavení aktuálního pracovního prostoru, vyberte Nastavení pracovního prostoru.
1. V podokně Výchozí nastavení vlevo najděte konfiguraci rozšíření Docs Article Templates, klikněte na ikonu tužky vedle požadovaného nastavení a pak klikněte na Nahradit v Nastavení.
1. Vedle se otevře podokno Uživatelská nastavení s novou položkou v dolní části.
1. Přidejte svoje ID GitHubu nebo e-mailový alias Microsoftu a uložte tento soubor.
1. Možná budete muset nástroj VS Code zavřít a znovu spustit, aby se změny projevily.
1. Když teď použijete šablonu využívající dynamická pole, naplní se v záhlaví metadat automaticky vaše ID GitHubu a/nebo alias Microsoftu.
