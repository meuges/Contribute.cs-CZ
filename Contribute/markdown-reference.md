---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592567"
---
# <a name="markdown-reference"></a>Referenční informace k jazyku Markdown

Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu. Platforma Docs podporuje standard CommonMark pro Markdown plus několik vlastních rozšíření navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com. Tento článek obsahuje referenční informace o používání jazyka Markdown pro docs.microsoft.com.

K vytváření Markdownu můžete použít libovolný textový editor. Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření Docs, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).

Web Docs používá modul Markdig Markdown. Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).

## <a name="alerts-note-tip-important-caution-warning"></a>Výstrahy – Note (Poznámka), Tip, Important (Důležité), Caution (Pozor), Warning (Upozornění)

Výstrahy jsou rozšíření Docs Markdown určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu. Podporují se následující typy výstrah:

```md
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

![Ukazuje, jak výstrahy v předchozím příkladu vypadají na publikované stránce Docs s různými ikonami a barvami.](media/alerts-rendering.png)

## <a name="code-snippets"></a>Fragmenty kódu

Do souborů Markdown můžete začlenit fragmenty kódu:

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>Nadpisy

Web Docs podporuje šest úrovní nadpisů Markdownu:

```md
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

Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.

## <a name="images"></a>Obrázky

Syntaxe pro začlenění obrázku:

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku. Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku. Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.

Obrázky by měly být uložené ve složce `/media` v sadě dokumentace. Pro obrázky se standardně podporují tyto typy souborů:

- .jpg
- .png

Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json<!--add link to reference when available--> pro sadu dokumentace.

## <a name="links"></a>Odkazy

Web Docs používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky. Typy odkazů jsou popsané v níže uvedených pododdílech.

> [!TIP]
> The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!

> [!IMPORTANT]
> Do not include locale codes, such as en-us, in your links to Microsoft sites. Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs. When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link. For example, use:
>
> `[Microsoft](https://www.microsoft.com)`
>
> Not:
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Relativní odkazy na soubory ve stejné sadě dokumentace

Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru. Na webu Docs můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace. Relativní cesta má následující syntaxi:

```md
[link text](../../folder/filename.md)
```

`../` označuje jednu úroveň výše v hierarchii.

- Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.
- K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace. Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.
- Web Docs podporuje také speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md). Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace. Během sestavování se ověří a přeloží i tento druh cesty.

> [!IMPORTANT]
> Include the file extension in the relative path. Build validates the existence of the target file of that relative path. If relative path does not include file extension, it is likely build will report a warning of broken link. For example, use:
>
> `[link text](../../folder/filename.md)`
>
> Not:
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Relativní odkazy na jiné soubory na webu Docs

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

Nezačleňujte příponu souboru (.md). Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.

### <a name="links-to-external-sites"></a>Odkazy na externí weby

```md
[Microsoft](https://www.microsoft.com)
```

Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).

### <a name="bookmark-links"></a>Odkazy na záložky

Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti. Například:

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

Odkaz na záložku u nadpisu v aktuálním souboru:

```md
[Managed Disks](#managed-disks)
```

Použijte znak hash (`#`) a za ním slova nadpisu. Pokud chcete změnit text nadpisu na text odkazu:
- Použijte jenom malá písmena.
- Odeberte interpunkci.
- Nahraďte mezery pomlčkami.

Pokud máte například nadpis „2.2 Otázky zabezpečení“, pak text odkazu na záložku bude „#22-otázky-zabezpečení“.

### <a name="explicit-anchor-links"></a>Explicitní odkazy na ukotvení

Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek. V obecných souborech Markdown použijte výše popsané záložky. Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:

`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`

Pro odkaz na explicitní ukotvení použijte následující syntaxi:

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Křížové odkazy XREF

K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).

> [!NOTE]
> To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.
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

V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID. <!-- ? -->Nejlepším způsobem, jak najít identifikátor UID pro rozhraní API, je zobrazit zdroj stránky API, kterou chcete propojit, a najít hodnotu ms.assetid. Hodnoty jednotlivých přetížení se ve zdroji nezobrazují. Pracujeme na tom, abychom v budoucnu měli lepší systém.

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

Nepoužívejte v seznamech ani vnořených seznamech písmena. Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena. Například:

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Toto se zobrazí takto:

1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)

### <a name="bulleted-list"></a>Seznam s odrážkami

Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Toto se zobrazí takto:

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

### <a name="checklist"></a>Kontrolní seznam

Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:

```md
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

Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku. Nepřidávejte do svých článků náhodné kontrolní seznamy.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Akce dalšího kroku

K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.

Syntaxe je následující:

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Například:

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Toto se zobrazí takto:

> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)

V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku. Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.

## <a name="section-definition"></a>Definice oddílu

<!-- more info about this would be helpful! -->
Je možné, že budete potřebovat nadefinovat oddíl. Tato syntaxe se nejčastěji používá pro tabulky kódu.
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

## <a name="selectors"></a>Voliče

<!-- could be more clear! -->
Volič neboli selektor můžete použít, když chcete připojit různé stránky pro stejný článek. Čtenáři pak můžou přepínat mezi těmito stránkami.

> [!NOTE]
> This extension works differently between docs.microsoft.com and MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

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

> [!div class="op_multi_selector" title1="Platforma" title2="Back-end"]
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

## <a name="tables"></a>Tabulky

Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky. Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Toto se zobrazí takto:

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

Můžete také vytvořit tabulku bez záhlaví. Příklad vytvoření seznamu s více sloupci:

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

Toto se zobrazí takto:

|   |   |
| - | - |
| This | table |
| has no | header |

Sloupce můžete zarovnat pomocí dvojtečky:

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Se vykreslí takto:

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!
>
> You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> This only works on the docs.microsoft.com site.

Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou. Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit. Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.

Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Zobrazí se takto:

> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> This only works on the docs.microsoft.com site.

Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova. Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.

### <a name="html-tables"></a>Tabulky HTML

Tabulky HTML se na webu docs.microsoft.com nedoporučují. Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Videa

### <a name="embedding-videos-into-a-markdown-page"></a>Vkládání videí na stránku Markdownu

Platforma Docs v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:

- YouTube
- Channel9
- Vlastní systém Microsoftu „One Player“

Můžete vložit video s následující syntaxí a Docs ho zobrazí.

```md
> [!VIDEO <embedded_video_link>]
```

Příklad:

```md
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
> The CH9 video URL should start with `https` and end with `/player`. Otherwise, it will embed the whole page instead of the video only.

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

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
