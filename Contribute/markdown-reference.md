---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624731"
---
# <a name="docs-markdown-reference"></a>Referenční informace k jazyku Markdown pro Docs

Tento článek obsahuje referenční informace o psaní jazyka Markdown pro docs.microsoft.com.

[Markdown](https://daringfireball.net/projects/markdown/) je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu. Web Docs podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig). Podporuje také vlastní rozšíření Markdownu, které na webu poskytuje bohatší obsah.

Markdown sice můžete psát v jakémkoliv textovém editoru, doporučujeme ale použít [Visual Studio Code](https://code.visualstudio.com/) s [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack). Balíček pro vytváření obsahu na webu Docs obsahuje nástroje pro úpravy a funkci náhledu, díky které se můžete podívat, jak bude váš článek po publikování na webu Docs vypadat.

## <a name="alerts-note-tip-important-caution-warning"></a>Výstrahy – Note (Poznámka), Tip, Important (Důležité), Caution (Pozor), Warning (Upozornění)

Výstrahy představují rozšíření Markdownu určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu. Podporují se následující typy výstrah:

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
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>Ostré závorky

Pokud v textu v souboru používáte ostré závorky, třeba k vyznačení zástupného symbolu, musíte pro ně použít kód. Jinak je Markdown bude považovat za značku HTML.

Například `<script name>` přepište kódem jako `&lt;script name&gt;` nebo `\<script name>`.

Hranaté závorky nemusí být uvozené v textu formátovaném jako vložený kód ani v blocích kódu.

## <a name="apostrophes-and-quotation-marks"></a>Apostrofy a uvozovky

Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky. Pro ty je nutné použít kód nebo je změnit na základní uvozovky. Jinak se při publikování souboru zobrazí nějak takto: Itâ&euro;&trade;s

Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:

- Levá (otevírací) uvozovka: `&#8220;`
- Pravá (uzavírací) uvozovka: `&#8221;`
- Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`
- Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`

## <a name="blockquotes"></a>Blokové citace

Blokové citace se vytvářejí pomocí znaku `>`:

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

Předchozí příklad se zobrazí takto:

> This is a blockquote. It is usually rendered indented and with a different background color.

## <a name="bold-and-italic-text"></a>Tučné písmo a kurzíva

Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:

```markdown
This text is **bold**.
```

Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:

```markdown
This text is *italic*.
```

Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Fragmenty kódu

Markdown pro Docs podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami. Podrobnosti najdete v tématu věnovaném [přidávání kódu na webu Docs](code-in-docs.md).

## <a name="columns"></a>Sloupce

Rozšíření Markdownu pro **sloupce** umožňuje autorům webu Docs přidávat rozložení obsahu založená na sloupcích, která jsou flexibilnější a výkonnější než základní tabulky Markdownu (ty se hodí jen pro skutečná tabulková data). Můžete přidat až čtyři sloupce a pomocí volitelného atributu `span` spojit dva nebo více sloupců.

Syntaxe pro sloupce je následující:

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

Sloupce by měly obsahovat jen základní Markdown, a to včetně obrázků. Záhlaví, tabulky, tabulátory ani další složité struktury nevkládejte. Mimo sloupec nesmí být na řádku žádný obsah.

Tento Markdown například vytvoří jeden sloupec, který pokrývá dvě šířky sloupců, a jeden standardní sloupec (bez `span`):

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

Toto se zobrazí takto:

:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>Nadpisy

Web Docs podporuje šest úrovní nadpisů Markdownu:

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Mezi posledním symbolem `#` a textem nadpisu musí být mezera.
- Každý soubor Markdownu musí mít právě jeden nadpis H1.
- Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.
- Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru. Nadpisy nižších úrovní nikoliv, takže nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.
- Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění sestavení.
- Odkazy na jednotlivé nadpisy v souboru můžete realizovat pomocí [odkazů na záložky](how-to-write-links.md#explicit-anchor-links).

## <a name="html"></a>HTML

Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.

## <a name="images"></a>Obrázky

Pro obrázky se standardně podporují tyto typy souborů:

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>Standardní konceptuální obrázky (výchozí Markdown)

Základní syntaxe Markdownu pro vložení obrázku je následující:

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

`<alt text>` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku. Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku. Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.

Podtržítka se v alternativním textu zobrazí správně jen tehdy, pokud je uvedete předponou zpětného lomítka (`\_`). Jako alternativní text ale nepoužívejte zkopírovaný název souborů. Například namísto tohoto:

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Napište toto:

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Standardní konceptuální obrázky (Markdown pro Docs)

Vlastní rozšíření `:::image:::` pro web Docs podporuje standardní obrázky, složité obrázky a ikony.

I když u standardních obrázků bude i nadále fungovat starší syntaxe Markdownu, doporučujeme použít toto nové rozšíření, protože podporuje výkonnější funkce, jako je specifikace rozsahu lokalizace, která se liší od nadřazeného tématu. V budoucnu budou k dispozici i další pokročilé funkce, například možnost výběru ze sdílené galerie obrázků namísto specifikace místního obrázku. Nová syntaxe vypadá takto:

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

V případě výchozího `type="content"` se vyžaduje `source` i `alt-text`.

### <a name="complex-images-with-long-descriptions"></a>Složité obrázky s dlouhými popisy

Díky tomuto rozšíření můžete také přidávat obrázky s dlouhým popisem, který přečte čtečka obrazovky, ale vizuálně se na publikované stránce nevykreslí. Dlouhé popisy představují požadavek na přístupnost u složitých obrázků (například grafů). Syntaxe je následující:

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

V případě `type="complex"` se vyžaduje `source`, `alt-text`, dlouhý popis i značka `:::image-end:::`.

### <a name="specifying-loc-scope"></a>Specifikace rozsahu lokalizace

Někdy se rozsah lokalizace obrázku liší od rozsahu článku nebo modulu, který ho obsahuje. To může způsobit potíže uživatelům z různých částí světa – například pokud se snímek obrazovky s produktem omylem lokalizuje do jazyka, v němž není produkt k dispozici. Chcete-li tomu zabránit, můžete v obrázcích typu `content` a `complex` zadat volitelný atribut `loc-scope`.

### <a name="icons"></a>Ikony

Rozšíření pro obrázky podporuje ikony, které neobsahují alternativní text a slouží jako dekorativní obrázky. Syntaxe pro ikony je následující:

```Markdown
:::image type="icon" source="<folderPath>":::
```

V případě výchozího `type="icon"` je potřeba specifikovat jen `source`.

## <a name="included-markdown-files"></a>Zahrnuté soubory Markdownu

Tam, kde se mají soubory Markdownu opakovat ve více článcích, můžete použít soubor k zahrnutí. Tato funkce říká webu Docs, že má v době sestavování nahradit odkaz obsahem zahrnutého souboru. Soubory k zahrnutí můžete používat dvěma způsoby:

- Vložení: Umožňuje znovu použít běžný vložený fragment textu v rámci věty.
- Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.

Soubor k zahrnutí typu Vložení nebo Blok je soubor Markdownu (.md). Ty mohou obsahovat jakýkoli platný Markdown. Zahrnuté soubory se obvykle nachází ve společném podadresáři *includes* v kořenovém adresáři úložiště. Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.

### <a name="includes-syntax"></a>Zahrnutá syntaxe

Soubor typu Blok má vlastní řádek:

```markdown
[!INCLUDE [<title>](<filepath>)]
```

Soubor typu Vložení je součástí řádku:

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

`<title>` představuje název souboru a `<filepath>` relativní cestu k souboru. `INCLUDE` musí být velkými písmeny a před `<title>` se musí nacházet čárka.

Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:

- Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl. Nepoužívejte je na nic menšího než větu.
- Zahrnuté soubory se nevykreslí v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních pro Docs. Vykreslí se až po zveřejnění.
- Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor odkazuje. Ignorováním tohoto pravidla vznikne v článku nepřeložitelný řetězec.
- Nevkládejte zahrnuté soubory do jiných zahrnutých souborů.
- Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>` */includes/media*. Adresář *media* nesmí ve svém kořenu obsahovat obrázky. Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář *media* není potřeba.
- Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí. Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem. Multimediální soubor uložte do složky multimédií spojené se zahrnutím.
- Nepoužívejte zahrnutí jako jediný obsah článku.  Zahrnutí mají být doplněním obsahu ve zbytku článku.

## <a name="links"></a>Odkazy

Informace o syntaxi odkazů najdete v tématu [Použití odkazů v dokumentaci](how-to-write-links.md).

## <a name="lists-numbered-bulleted-checklist"></a>Seznamy (číslované, odrážkové, kontrolní)

### <a name="numbered-list"></a>Číslovaný seznam

Při vytváření číslovaného seznamu můžete všude použít jedničky (1). Ty se při publikování zobrazí jako sekvenční seznam ve vzestupném pořadí. Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat ručně.

Nepoužívejte v seznamech ani vnořených seznamech písmena. Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena. Například:

```markdown
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

Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` nebo `*` následovaný mezerou:

```markdown
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

Ať už se rozhodnete pro `-` nebo `*`, používejte jeden typ syntaxe konzistentně v rámci celého článku.

### <a name="checklist"></a>Kontrolní seznam

Kontrolní seznamy jsou webu Docs dostupné jen při použití vlastního rozšíření Markdownu:

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Tento příklad se na webu Docs zobrazí takto:

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku. Nepřidávejte do svých článků náhodné kontrolní seznamy.

## <a name="next-step-action"></a>Akce dalšího kroku

K přidání tlačítka akce dalšího kroku na stránky Docs můžete použít vlastní rozšíření.

Syntaxe je následující:

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Například:

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Toto se zobrazí takto:

> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)

V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku. Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.

## <a name="non-localized-strings"></a>Nelokalizované řetězce

Pomocí vlastního rozšíření Markdownu `no-loc` můžete identifikovat řetězce obsahu, které má proces lokalizace ignorovat.

Ve všech příslušných řetězcích se budou rozlišovat velká a malá písmena, což znamená, že musí být specifikované naprosto přesně, aby se mohly ignorovat.

Pokud chcete řetězec označit jako nelokalizovaný, použijte tuto syntaxi:

```markdown
:::no-loc text="String":::
```

Například v následujícím příkladu se během procesu lokalizace bude ignorovat jen jedna instance `Document`:

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> K uvození speciálních znaků použijte `\`:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

Pomocí metadat v hlavičce YAML můžete také označit jako nelokalizované všechny instance řetězce v aktuálním souboru Markdownu:

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> Nelokalizovaná metadata se v souboru *docfx.json* nepodporují jako globální metadata. Lokalizační kanál nečte soubor *docfx.json*, takže je potřeba tato metadata přidat do každého ze zdrojových souborů.

V následujícím příkladu bude proces lokalizace ignorovat slovo `title` jak v `Document` metadat, tak i v hlavičce Markdownu.

V `description` metadat a v hlavním obsahu Markdownu se slovo `document` lokalizuje, protože nezačíná velkým písmenem `D`.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>Voliče

Voliče jsou prvky uživatelského rozhraní, které umožňují uživateli přepínat mezi různými variantami jednoho článku. Využívají se v některých sadách dokumentace k řešení rozdílné implementace napříč technologiemi a platformami. Voliče se zpravidla nejvíce hodí pro obsah určený pro vývojářské mobilní platformy.

Protože do každého souboru článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí. Pak můžete na daný soubor k zahrnutí odkázat ve všech souborech článků, které daný volič používají.

K dispozici jsou dva typy voličů – jednoduchý a vícenásobný volič.

### <a name="single-selector"></a>Jeden selektor

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

...se zobrazí takto:

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Vícenásobný selektor

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

...se zobrazí takto:

> [!div class="op_multi_selector" title1="Platforma" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows Universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>Dolní index a horní index

Dolní a horní index používejte jen tam, kde jsou potřeba k zajištění technické přesnosti, například v článcích o matematických vzorcích. Nepoužívejte je v nestandardních stylech, jako jsou poznámky pod čarou.

V obou případech použijte HTML:

```html
Hello <sub>This is subscript!</sub>
```

Toto se zobrazí takto:

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Toto se zobrazí takto:

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Tabulky

Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky. Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:

```markdown
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

Sloupce můžete zarovnat pomocí dvojtečky:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Se vykreslí takto:

| Fun                  | With                 | Tabulky          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!
>
> You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).

### <a name="line-breaks-within-words-in-any-table-cell"></a>Konce řádků ve slovech v libovolných buňkách tabulky

Dlouhá slova v markdownové tabulce můžou způsobit, že bude tabulka zasahovat do navigace napravo a stane se nečitelnou. Tento problém vyřešíte tak, že webu Docs umožníte při zobrazování automaticky vkládat konce řádků do slov tam, kde je to potřeba. Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.

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
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Konce řádků ve slovech v buňkách druhého sloupce tabulky

Je možné, že budete potřebovat automaticky vkládat konce řádků do slov jen ve druhém sloupci tabulky. Pokud chcete konce řádků omezit právě jen na druhý sloupec, použijte třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.

### <a name="data-matrix-tables"></a>Tabulky matic dat

Tabulka matic dat má záhlaví a vážený první sloupec. Výsledkem je matice s prázdnou buňkou v levém horním rohu. Dokumentace (Docs) obsahuje vlastní Markdown pro tabulky matic dat:

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

Každá položka v prvním sloupci musí být naformátovaná jako tučná (`**bold**`); jinak tabulky nebudou přístupné pro čtečky obrazovky ani platné pro dokumentaci (Docs).

### <a name="html-tables"></a>Tabulky HTML

Tabulky HTML se na webu docs.microsoft.com nedoporučují. Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.
