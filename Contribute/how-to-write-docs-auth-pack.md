---
title: Balíček pro vytváření obsahu na webu Docs pro VS Code
description: Tento článek popisuje balíček rozšíření pro VS Code, který usnadňuje vytváření obsahu v jazyce Markdown pro docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d0d61db2faf88598ecd2c800fb5fbe8df8ec44f5
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469571"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Balíček pro vytváření obsahu na webu Docs pro VS Code

Balíček pro vytváření obsahu na webu Docs je kolekce rozšíření nástroje VS Code, který vám pomůže s vytvářením obsahu v jazyce Markdown pro docs.microsoft.com. Balíček je [dostupný na VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) a obsahuje následující rozšíření:

- **DocFx:** Poskytuje náhled Markdownu specifický pro docs.microsoft.com. Další informace najdete tady: [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX).
- **markdownlint:** Oblíbený markdownový linter od Davida Ansona, který vám pomůže zajistit, že se Markdown řídí doporučenými postupy. Další informace najdete tady: [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).
- **Docs Markdown:** Poskytuje pomoc při vytváření obsahu v jazyce Markdown pro docs.microsoft.com v systému OPS (Open Publishing System), včetně základní podpory Markdownu pro vlastní markdownovou syntaxi v OPS. Ve zbývající části tématu se popisuje rozšíření Markdown Docs.

## <a name="prerequisites-and-assumptions"></a>Požadavky a předpoklady

Pokud chcete přesně vkládat relativní odkazy, obrázky a další obsah pomocí rozšíření Docs Markdown, musí být oborem pracovního prostoru nástroje VS Code kořen naklonovaného úložiště OPS.

Určité syntaxe podporované rozšířením, například výstrahy a fragmenty kódu, představují vlastní Markdown pro OPS a nebudou se správně vykreslovat, dokud je nepublikujete přes OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Použití rozšíření Docs Markdown

K nabídce Docs Markdown se dostanete tak, že zadáte `ALT+M`. Kliknutím nebo klávesami se šipkami nahoru a dolů můžete vybrat požadovanou funkci. Můžete ale také začít psát a spustit filtrování. Jakmile se požadovaná funkce zvýrazní v nabídce, stačí stisknout `ENTER`. K dispozici jsou následující funkce:

|Funkce     |Příkaz             |Popis           |
|-------------|--------------------|----------------------|
|Tučné         |`formatBold`        |Formátuje text **tučně**.|
|Kurzíva       |`formatItalic`      |Formátuje text jako *kurzívu*.|
|Kód         |`formatCode`        |Pokud vyberete jeden nebo žádný řádek, formátuje text jako `inline code`.<br><br>Pokud vyberete více řádků, formátuje je jako ohraničený blok kódu a umožní vám volitelně vybrat programovací jazyk podporovaný systémem OPS.|
|Výstrah        |`insertAlert`       |Vloží poznámku, důležitou informaci, upozornění nebo tip.<br><br>Nejprve vyberte z nabídky výstrahu a potom její typ. Pokud jste už nějaký text vybrali, umístí se do vybrané syntaxe výstrahy. Pokud jste žádný text nevybrali, nová výstraha se vloží se zástupným textem.|
|Číslovaný seznam|`insertNumberedList` |Vloží nový číslovaný seznam.<br><br> Pokud vyberete více řádků, bude každý z nich představovat položku seznamu. Všimněte si, že se v Markdownu číslované seznamy zobrazují všechny jako 1, ale na docs.microsoft.com se zobrazí očíslované posloupně a u vnořených seznamů označené písmeny. Vnořený číslovaný seznam vytvoříte tak, že požadované položky odsadíte od nadřazeného seznamu pomocí tabulátoru.|
|Seznam s odrážkami|`insertBulletedList` |Vloží nový seznam s odrážkami.|
|Tabulka        |`insertTable`        |Vloží tabulkovou strukturu Markdownu.<br><br>Po výběru příkazu k vytvoření tabulky zadejte počet sloupců a řádků ve formátu sloupce:řádky, například 3:4. Všimněte si, že maximální počet sloupců, které můžete zadat prostřednictvím tohoto rozšíření, je 5, což je doporučený maximální počet s ohledem na čitelnost.|
|Odkaz         |`selectLinkType`      |Vloží odkaz. Když vyberete teto příkaz, zobrazí se následující podnabídka.<br><br>`External`: Odkaz na webovou stránku pomocí identifikátoru URI. Musí obsahovat http nebo https.<br>`Internal`: Vloží relativní odkaz na jiný soubor ve stejném úložišti. Po výběru této možnosti začněte psát do okna příkazu, aby se začaly filtrovat soubory podle názvu, a potom vyberte požadovaný soubor. <br>`Bookmark in this file`: Vyberte záhlaví ze seznamu v aktuálním souboru, aby se vložila správně formátovaná záložka.<br>`Bookmark in another file`: Nejprve vyfiltrujte soubor podle názvu a vyberte soubor, na který chcete vytvořit odkaz, a potom ve vybraném souboru zvolte příslušné záhlaví.|
|Obrázek        |`insertImage`     |Zadejte alternativní text (vyžadovaný z důvodu usnadnění) a vyberte ho. Potom zavolejte tento příkaz, aby se vyfiltroval seznam podporovaných souborů obrázků v úložišti, a vyberte požadovaný soubor. Pokud jste při volání tohoto příkazu neměli vybraný alternativní text, zobrazí se výzva k jeho výběru, než budete moci vybrat soubor obrázku.|
|Vložený soubor      |`insertInclude`   |Vyhledá soubor, který se má vložit do aktuálního souboru.|
|Fragment kódu      |`insertSnippet`   |Vyhledá fragment kódu v úložišti, který se má vložit do aktuálního souboru.|
|Video        |`insertVideo`     |Přidá vložené video.|
|Náhled      |`previewTopic`    |Zobrazí náhled aktivního tématu ve vedlejším souběžném okně pomocí rozšíření DocFX.  Pokud rozšíření DocFX není nainstalováno nebo je nainstalováno, ale je zakázáno, toto téma se nezobrazí.


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

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Zobrazení staršího panelu nástrojů Gauntlet

Uživatelé staršího rozšíření s kódovým názvem Gauntlet si mohou všimnout, že po instalaci rozšíření Docs Markdown se panel pro vytváření obsahu už nezobrazuje v dolní části okna nástroje VS Code. Důvodem je to, že panel nástrojů zabíral příliš mnoho místa na stavovém řádku nástroje VS Code a neřídil se doporučenými postupy pro uživatelské prostředí rozšíření, a proto se v novém rozšíření už nepoužívá. Panel nástrojů si ale můžete volitelně zobrazit, když následujícím způsobem aktualizujete soubor settings.json v nástroji VS Code:

1. V nástroji VS Code přejděte na Soubor -> Předvolby -> Nastavení (`CTRL+Comma`).
1. Pokud chcete změnit nastavení všech pracovních prostorů nástroje VS Code, vyberte Uživatelská nastavení. Pokud chcete změnit nastavení pouze aktuálního pracovního prostoru, vyberte Nastavení pracovního prostoru.
1. V podokně Výchozí nastavení vyhledejte část týkající se konfigurace rozšíření pro vytváření obsahu pro web Docs a vyberte ikonu tužky vedle požadovaného nastavení. Zobrazí se výzva k výběru možnosti `true` nebo `false`. Po výběru požadované možnosti VS Code automaticky přidá hodnotu do souboru settings.json a zobrazí výzvu k opakovanému načtení okna, aby se změny projevily.

## <a name="known-issues"></a>Známé problémy

- DocFX Preview: V systémech MacOS a Linux se v DocFX Preview nespouští náhled správně (u těchto platforem se náhled standardně přepne na VS Code Markdown).
- DocFx Preview: Na všech platformách se některé syntaxe, například odkazy xref (křížové odkazy) na rozhraní API, v náhledu správně nezobrazují a v některých případech zanechávají v obsahu mezery.
- Externí záložky: V Linuxu se seznam souborů sice zobrazí, ale nejsou k dispozici žádná záhlaví pro výběr.
- Vložené soubory: V Linuxu se seznam souborů sice zobrazí, ale po výběru se nepřidá žádný odkaz.
