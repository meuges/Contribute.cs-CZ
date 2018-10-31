---
title: Referenční informace k jazyku Markdown pro OPS a docs.microsoft.com
description: Průvodce platformou OPS pro Markdown a rozšíření DFM (DocFX Flavored Markdown)
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: e248eafb0247b200313ba198f2545eca947f5627
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805876"
---
# <a name="markdown-reference-for-ops"></a>Referenční informace k jazyku Markdown pro OPS

Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu. OPS podporuje pro Markdown standard CommonMark plus několik vlastních rozšíření navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com. Tento článek obsahuje referenční informace o používání jazyka Markdown v OPS pro docs.microsoft.com.

K vytváření Markdownu můžete použít libovolný textový editor. Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření OPS, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).

Platforma OPS přijala Markdig za standard pro všechna nová úložiště a starší úložiště se na Markdig migrují. Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).

## <a name="alerts-note-tip-important-caution-warning"></a>Výstrahy (Poznámka, Tip, Důležité, Pozor, Upozornění)

Výstrahy jsou rozšíření Markdownu specifické pro OPS určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu. Podporují se následující typy výstrah:

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

Tyto výstrahy vypadají na webu docs.microsoft.com takto:

> [!NOTE]
> Informace, kterých by si uživatel měl všimnout i při rychlém čtení

> [!TIP]
> Informace, které pomáhají uživateli lépe uspět

> [!IMPORTANT]
> Důležité informace potřebné k tomu, aby uživatel uspěl

> [!CAUTION]
> Negativní potenciální důsledky nějaké akce

> [!WARNING]
> Nebezpečné důsledky nějaké akce

## <a name="code-snippets"></a>Fragmenty kódu

Do souborů Markdown můžete začlenit fragmenty kódu:

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Nadpisy

OPS podporuje šest úrovní nadpisů Markdownu:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Mezi posledním symbolem `#` a textem nadpisu musí být mezera.
- Každý soubor Markdown musí mít právě jeden nadpis H1.
- Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.
- Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru. Nadpisy nižších úrovní nikoli, proto nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.
- Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění při sestavování.
- Odkazy na jednotlivé nadpisy v souboru můžete realizovat přes [záložky](#bookmark-links).

## <a name="html"></a>HTML

Ačkoli Markdown podporuje vložený kód HTML, pro publikování přes OPS se HTML nedoporučuje, přičemž až na omezený seznam hodnot způsobí chyby a upozornění při sestavování. <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a>Obrázky

Syntaxe pro začlenění obrázku:

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku. Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku. Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.

Obrázky by měly být uložené ve složce `/media` v sadě dokumentace. Pro obrázky se standardně podporují tyto typy souborů:

- .jpg
- .png

Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json<!--add link to reference when available--> sady dokumentace.

## <a name="links"></a>Odkazy

OPS používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky. Typy odkazů jsou popsané v níže uvedených pododdílech.

> [!TIP]
> Balíček pro vytváření obsahu na webu Docs pro VS Code vám může pomoci vkládat relativní odkazy a záložky bez nudného určování cest.

> [!IMPORTANT]
> Do odkazů na weby Microsoftu nezačleňujte kódy národního prostředí, například cs-cz. Pevně zakódované kódy národního prostředí zabraňují zobrazení lokalizovaného obsahu, což je pro uživatele v jiných národních prostředích nepříjemná zkušenost, a způsobují významné náklady na lokalizaci. Při kopírování adresy URL z prohlížeče se kód národního prostředí zkopíruje, takže ho při vytváření odkazu musíte ručně odstranit. Použijte například tento odkaz:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Nikoli tento odkaz:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Relativní odkazy na soubory ve stejné sadě dokumentace

Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru. V OPS můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace. Relativní cesta má následující syntaxi:

```markdown
[link text](../../folder/filename.md)
```

`../` označuje jednu úroveň výše v hierarchii.

- Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.
- K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace. Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.
- OPS podporuje speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md). Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace. Během sestavování se ověří a přeloží i tento druh cesty.

> [!IMPORTANT]
> Do relativní cesty začleňte příponu souboru. Při sestavování se ověřuje existence cílového souboru v této relativní cestě. Pokud relativní cesta neobsahuje příponu souboru, při sestavování se pravděpodobně nahlásí upozornění nebo přerušený hypertextový odkaz. Použijte například tento odkaz:
>
> `[link text](../../folder/filename.md)`
>
> Nikoli tento odkaz:
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a>Absolutní odkazy na jiné soubory v OPS

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Nezačleňujte příponu souboru (.md). Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.

### <a name="links-to-external-sites"></a>Odkazy na externí weby

```markdown
[Microsoft](https://www.microsoft.com)
```

Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).

### <a name="bookmark-links"></a>Odkazy na záložky

Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Odkaz na záložku u nadpisu v aktuálním souboru:

```markdown
[Managed Disks](#managed-disks)
```

Použijte mřížku následovanou textem nadpisu s odebranou interpunkcí a mezerami nahrazenými pomlčkami.

### <a name="explicit-anchor-links"></a>Explicitní odkazy na ukotvení

Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek. V obecných souborech Markdown použijte výše popsané záložky. Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:

`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`

Pro odkaz na explicitní ukotvení použijte následující syntaxi:

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Křížové odkazy XREF

K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).

> [!NOTE]
> K odkazování na stránky s referencemi rozhraní API v jiných sadách dokumentace potřebujete do souboru `docfx.json` přidat konfiguraci `xrefService`.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

Identifikátor odpovídá plně kvalifikované třídě a názvu člena. Pokud za UID přidáte *, představuje tento odkaz stránku přetížení, nikoli konkrétní rozhraní API. `List<T>.BinarySearch*` použijte například k odkazu na stránku metody BinarySearch místo odkazu na konkrétní přetížení, jako je `List<T>.BinarySearch(T, IComparer<T>)`.

Můžete použít jednu z následujících syntaxí:

- Automatický odkaz: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  Nepovinný parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu. Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.

- Odkaz Markdownu: `[link text](xref:UID)`
  
  Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.

Příklady:

- `<xref:System.String>` se zobrazí jako „String“.
- `<xref:System.String?displayProperty=nameWithType>` se zobrazí jako „System.String“.
- `[String class](xref:System.String)` se zobrazí jako „třída String“.

V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID. <!-- ? -->Nejlepším způsobem, jak najít UID pro rozhraní API, je zobrazit zdrojový kód stránky API, na kterou chcete odkázat, a najít hodnotu ms.assetid. Hodnoty jednotlivých přetížení se ve zdroji nezobrazují. Pracujeme na tom, abychom v budoucnu měli lepší systém.

Pokud UID obsahuje speciální znaky \`, \# nebo \*, musí být hodnota UID uvedena ve formátu HTML `%60`, `%23` a `%2A` v uvedeném pořadí. Někdy v tomto formátu uvidíte i závorky, není to ale povinné.

Příklady:

- System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.
- System.Exception.\#ctor se změní na `System.Exception.%23ctor`.
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Seznamy (číslované, odrážkové, kontrolní)

### <a name="numbered-list"></a>Číslovaný seznam

Při vytváření číslovaného seznamu můžete všude použít jedničky (1), které se při publikování zobrazí jako sekvenční seznam. Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat.

Nepoužívejte v seznamech ani vnořených seznamech písmena. Při publikování přes OPS se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena. Například:

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Toto se zobrazí takto:

1. Toto je
1. nadřazený číslovaný seznam
   1. a toto je
   1. vnořený číslovaný seznam
1. (konec)

### <a name="bulleted-list"></a>Seznam s odrážkami

Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Toto se zobrazí takto:

- Toto je
- nadřazený seznam s odrážkami
  - a toto je
  - vnořený seznam s odrážkami
- Hotovo!

### <a name="checklist"></a>Kontrolní seznam

Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Tento příklad se na webu docs.microsoft.com zobrazí takto:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Kontrolní seznamy můžete použít na začátku nebo na konci článku k sumarizaci toho, „co se naučíte“ nebo „co jste se naučili“. Nepřidávejte do svých článků náhodné kontrolní seznamy.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Akce dalšího kroku

K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.

Syntaxe je následující:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Například:

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Toto se zobrazí takto:

> [!div class="nextstepaction"]
> [Informace o základním stylu](style-quick-start.md)

V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku. Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.

## <a name="section-definition"></a>Definice oddílu

<!-- more info about this would be helpful! --> Je možné, že budete potřebovat nadefinovat oddíl. Tato syntaxe se nejčastěji používá pro tabulky kódu.
Prohlédněte si následující příklad:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Předchozí text Markdownu blokové citace se zobrazí takto:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Selektory

<!-- could be more clear! --> Selektor můžete použít, když chcete propojit různé stránky stejného článku. Čtenáři pak můžou přepínat mezi těmito stránkami.

> [!NOTE]
> Toto rozšíření funguje mezi weby docs.microsoft.com a MSDN různě. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Jeden selektor

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

...se zobrazí takto:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Vícenásobný selektor

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

...se zobrazí takto:

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a>Tabulky

Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky. Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Toto se zobrazí takto:

|Toto je   |jednoduché   |záhlaví tabulky|
|----------|-----------|------------|
|data     |tabulky       |zde        |
|ani nemusí|být pěkně   |zarovnaná!||

Můžete také vytvořit tabulku bez záhlaví. Příklad vytvoření seznamu s více sloupci:

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

Toto se zobrazí takto:

|   |   |
| - | - |
| Tato | tabulka |
| nemá žádné | záhlaví |

Sloupce můžete zarovnat pomocí dvojtečky:

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Se vykreslí takto:

|                  |
|------------------|
|    zarovnání vpravo:|
|:zarovnání vlevo     |
|:na střed        :|

> [!TIP]
> Rozšíření pro vytváření obsahu na webu Docs pro VS Code usnadňuje přidávání základních tabulek Markdownu.
>
> Můžete také použít [online generátor tabulek](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Toto funguje jen na webu docs.microsoft.com.

Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou. Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit. Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.

Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Zobrazí se takto:

> [!div class="mx-tdBreakAll"]
> |Název|Syntaxe|Povinné pro tichou instalaci?|Popis|
> |-------------|----------|---------|---------|
> |Tichá instalace|/quiet|Ano|Spustí instalační program bez zobrazení uživatelského rozhraní a výzev.|
> |Bez restartování|/norestart|Ne|Potlačí všechny pokusy o restartování. Ve výchozím nastavení zobrazí uživatelské rozhraní před restartováním výzvu.|
> |Nápověda|/help|Ne|Poskytuje nápovědu a stručné referenční informace. Zobrazí správné použití příkazu instalace včetně seznamu všech možností a chování.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Toto funguje jen na webu docs.microsoft.com.

Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova. Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.

### <a name="html-tables"></a>Tabulky HTML

Tabulky HTML se na webu docs.microsoft.com nedoporučují. Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Videa

### <a name="embedding-videos-into-a-markdown-page"></a>Vkládání videí na stránku Markdownu

OPS v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:

- YouTube
- Channel9
- Vlastní systém Microsoftu „One Player“

Můžete vložit video s následující syntaxí a OPS ho zobrazí.

```markdown
> [!VIDEO <embedded_video_link>]
```

Příklad:

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

...se zobrazí takto:

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

A na publikovaných stránkách se zobrazí takto:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> Adresa URL videa CH9 by měla začínat řetězcem `https` a končit řetězcem `/player`. V opačném případě totiž místo samotného videa vloží celou stránku.

### <a name="uploading-new-videos"></a>Nahrání nových videí

Všechna nová videa by měla být nahrána následujícím postupem:

1. Připojte se ke skupině **docs_video_users** na IDWEB.
1. Přejděte na adresu https://aka.ms/VideoUploadRequest a vyplňte podrobnosti o videu. Budete potřebovat zadat tyto údaje (žádné z nich nebudou veřejně viditelné):
    1. Název videa
    1. Seznam produktů/služeb, kterých se video týká
    1. Cílová stránka nebo (pokud tuto stránku ještě nemáte) sada dokumentace, kde bude video hostované
    1. Odkaz na soubor MP4 s videem (pokud ještě nevíte, kde bude soubor umístěný, můžete sem dočasně zadat: `\\scratch2\scratch\apex`). Soubory MP4 by měly mít rozlišení 720p nebo vyšší.
    1. Popis videa
1. Odešlete (uložte) tuto položku.
1. Video se nahraje během dvou pracovních dnů. Odkaz potřebný k vložení bude umístěn do pracovní položky, která vám bude *přeložena zpět*.
1. Jakmile získáte odkaz na video, zavřete tuto pracovní položku.
1. Odkaz na video pak můžete přidat do příspěvku pomocí této syntaxe:

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
