---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 086972acaef9647709fbe43f07c07abde71c7d9f
ms.sourcegitcommit: fd92198ec2d0ce2d6687b6f1521a82b3fefc60e0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2020
ms.locfileid: "76111063"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Používání Markdownu pro vytváření článků na webu Docs

Články na [docs.microsoft.com](https://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí. Díky tomu se v oboru rychle stal standardem. Na webu Docs se používá [varianta Markdig](#markdown-flavor) jazyka Markdown.


## <a name="markdown-basics"></a>Základy Markdownu

### <a name="headings"></a>Nadpisy

K vytvoření nadpisu se používá znak hash (#):

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6. Příklady nadpisů první až čtvrté úrovně jsou použité výše.

V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.

Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně. Příklad: `# Async Programming in F# #`

Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.

### <a name="bold-and-italic-text"></a>Tučné písmo a kurzíva

Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:

```md
This text is **bold**.
```

Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:

```md
This text is *italic*.
```

Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a>Blokové citace

Blokové citace se vytvářejí pomocí znaku `>`:

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

Předchozí příklad se zobrazí takto:

> Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila. Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu. V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.

### <a name="lists"></a>Seznamy

#### <a name="unordered-list"></a>Neseřazený seznam

Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky. Například tento Markdown:

```md
- List item 1
- List item 2
- List item 3
```

se zobrazí takto:

- List item 1
- List item 2
- List item 3

Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte. Například tento Markdown:

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

se zobrazí takto:

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>Seřazený seznam

Na seřazený/stupňovaný seznam použijte odpovídající čísla. Například tento Markdown:

```md
1. First instruction
1. Second instruction
1. Third instruction
```

se zobrazí takto:

1. First instruction
2. Second instruction
3. Third instruction

Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte. Například tento Markdown:

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

se zobrazí takto:

1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction

Všimněte si, že jsme použili „1.“ pro všechny položky. Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.

### <a name="tables"></a>Tabulky

Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM. Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-). Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují. Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.

Například tento Markdown:

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Se zobrazí takto:

| Fun                  | With                 | Tabulky          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Další informace o vytváření tabulek:

- [Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu
- Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)
- [Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)
- [Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>Odkazy

Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:

 `[link text](file-name.md)`

Další informace o tvorbě odkazů:

- Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).
- Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.

### <a name="code-snippets"></a>Fragmenty kódu

Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami. Podrobnosti najdete tady:

- [Nativní podpora bloků kódu v Markdownu](https://daringfireball.net/projects/markdown/syntax#precode)
- [Podpora ohraničení kódu a zvýraznění syntaxe v GFM](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu. Obecný formát ohraničených bloků kódu je:

    ```alias
    ...
    your code goes in here
    ...
    ```

Alias za prvními třemi znaky (\`) definuje zvýraznění syntaxe, které se má použít. Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných popisků:

Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.

|Název|Popisek Markdownu|
|-----|-------|
|Konzola .NET|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|Bash|bash|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|C# v prohlížeči|csharp-interactive|
|Konzola|konzola|
|CSHTML|cshtml|
|DAX|dax|
|Docker|dockerfile|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Dotazovací jazyk Kusto|kusto|
|Markdown|md|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|protobuf|protobuf|
|PowerApps (oddělovač desetinných míst v podobě tečky)|powerapps-dot|
|PowerApps (oddělovač desetinných míst v podobě čárky)|powerapps-comma|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|R|r|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|XAML|xaml|
|XML|xml|

Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči. Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.

#### <a name="example-c"></a>Příklad: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Vykreslení__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Příklad: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Vykreslení__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a>Vlastní rozšíření Markdownu pro Docs

> [!NOTE]
> Docs.Microsoft.com (Docs) implementuje analyzátor Markdig Parser pro Markdown, který je ve velké míře kompatibilní s rozšířením GitHub Flavored Markdown (GFM). Markdig přidává v rozšířeních Markdownu některé další funkce. Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS. (Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)

Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy. Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:

- Bloky poznámek
- Vložené soubory
- Voliče
- Vložená videa
- Fragmenty/ukázky kódu

Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.

### <a name="note-blocks"></a>Bloky poznámek

Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:

- NOTE (POZNÁMKA)
- WARNING (VAROVÁNÍ)
- TIP
- IMPORTANT (DŮLEŽITÉ)

Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě. I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.

Příklady:

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

### <a name="include-files"></a>Soubory k zahrnutí

Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru. Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku. K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:

- Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.
- Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.
- Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.

Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md). Ty mohou obsahovat jakýkoli platný Markdown. Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště. Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.

Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:

- Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.
- Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl. Nepoužívejte je na nic menšího než větu.
- Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu. Vykreslí se až po zveřejnění.
- Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje. Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.
- Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí. Není to podporováno.
- Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media. Adresář multimédií nesmí ve svém kořenu obsahovat obrázky. Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.
- Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí. Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem. Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.
- Nepoužívejte soubor k zahrnutí jako jediný obsah článku.  Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.

Příklad:

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a>Voliče

Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami. Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře. V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.

Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí. Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.

Příklad voliče můžete vidět zde:

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).

### <a name="code-include-references"></a>Odkazy pro zahrnutí kódu

Rozšíření Markdownu pro fragmenty kódu na webu Docs umožňuje vkládat do článků ukázky kódu a vykreslovat je s barevným zvýrazňováním syntaxe specifického jazyka. Můžete zahrnout kód jak z aktuálního úložiště, tak z jiného úložiště. Níže uvedené pokyny poskytují přehled o tom, jak používat tuto funkci se sadou [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack). V editoru Visual Studio Code můžete zobrazit náhled fragmentů kódu otevřením okna **Preview** (Náhled). V náhledu nejsou k dispozici zvýrazňování a interaktivita.

> [!NOTE]
> Toto rozšíření nepodporuje zahrnutí kódu formou vložení do textu – to se provádí pomocí standardní konvence Markdownu, tedy tří znaků `.

#### <a name="code-from-current-repository"></a>Kód z aktuálního úložiště

1. V editoru Visual Studio Code stiskněte **Alt+M** nebo **Option+M** a vyberte Snippet (Fragment).
2. Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti). Pokud chcete vyhledávat místně, vyberte Full Local Search (Úplné místní vyhledávání).
3. Zadejte hledaný termín pro vyhledání souboru. Jakmile soubor najdete, vyberte ho.
4. Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu. Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).
5. Podle výběru z kroku 4 zadejte v případě potřeby hodnotu.

Zobrazení celého souboru kódu:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Zobrazení části souboru kódu zadáním čísel řádků:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Zobrazení části souboru kódu zadáním názvu fragmentu:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a>Kód z jiného úložiště

1. V editoru Visual Studio Code stiskněte **Alt+M** nebo **Option+M** a vyberte Snippet (Fragment).
2. Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti). Pokud chcete hledat v jiném úložišti, vyberte Cross-Repository Reference (Odkaz mezi úložišti).
3. Dostanete možnost vybrat úložiště, která jsou v *.openpublishing.publish.config.json*. Vyberte úložiště.
3. Zadejte hledaný termín pro vyhledání souboru. Jakmile soubor najdete, vyberte ho.
4. Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu. Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).
5. Podle výběru z kroku 5 zadejte v případě potřeby hodnotu.

Váš odkaz na fragment bude vypadat nějak takto:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a>Cesta k souboru kódu

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Příklad je z úložiště dokumentů ASP.NET, soubor článku [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Na soubor kódu odkazuje relativní cesta k [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) ve stejném úložišti.

#### <a name="selected-line-numbers"></a>Vybraná čísla řádků

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Tento příklad zobrazí jenom řádky 2 až 24 a 26 ze souboru kódu *StudentController.cs*.

Dejte raději přednost fragmentům před pevnými čísly řádků, jak je vysvětleno v další části.

#### <a name="named-snippet"></a>Pojmenovaný fragment

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Pro název používejte jenom písmena a podtržítka.

V příkladu je zobrazený oddíl `snippet_Create` souboru kódu. Soubor kódu pro tento příklad má oblast C# s názvem `snippet_Create`:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Vždy, když je to možné, odkazujte na pojmenovanou část a nezadávejte čísla řádků. S odkazy na čísla řádků je třeba zacházet opatrně, protože soubory kódu se nevyhnutelně mění tak, že dochází ke změnám čísel řádků.
Takové změny vám lehce uniknou. Ve vašem článku se nakonec začnou zobrazovat chybné řádky a vy nebudete mít potuchy, že se něco změnilo.

#### <a name="highlighting-selected-lines"></a>Zvýraznění vybraných řádků

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

V příkladu jsou zvýrazněné řádky 2 a 5, počítáno od začátku zobrazeného fragmentu. (Čísla zvýrazněných řádků se nepočítají od začátku souboru kódu.) Jinými slovy jsou zvýrazněné řádky 3 a 6 ze souboru kódu.

#### <a name="interactive-code-snippets"></a>Interaktivní fragmenty kódu

Interaktivní režim můžete povolit pro fragmenty kódu, které jsou zahrnuté odkazem. Tady jsou příklady:

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

Pokud chcete tuto funkci zapnout pro konkrétní blok kódu, použijte atribut `interactive`. Dostupné hodnoty atributu jsou:

- `cloudshell-powershell` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.
- `cloudshell-bash` – povolí Azure Cloud Shell.
- `try-dotnet` – povolí Try .NET.
- `try-dotnet-class` – povolí Try .NET s generováním tříd.
- `try-dotnet-method` – povolí Try .NET s generováním metod.

Existují páry hodnot atributů `language` a `interactive`, které jsou kompatibilní. Pokud má například atribut `interactive` hodnotu `try-dotnet`, musí být jako jazyk zadaný `csharp`. Podobně bude atribut `cloudshell-powershell` fungovat jenom s jazykem `powershell` a atribut `cloudshell-bash` s jazykem `bash`.

Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.

[Try .NET](https://github.com/dotnet/try) umožňuje interaktivní spouštění kódu .NET (C#) v prohlížeči. Pro Try .NET existují tři možnosti interaktivity: `try-dotnet`, `try-dotnet-class` a `try-dotnet-method`. Použití těchto možností nevyžaduje žádnou další konfiguraci v rámci fragmentu kódu. Ve výchozím nastavení jsou v současnosti dostupné tyto obory názvů:

- System
- System.Linq
- System.Collections.Generic
- System.Text
- System.Globalization
- System.Text.RegularExpressions

Hodnota atributu `try-dotnet` umožňuje uživatelům spustit kód C# v prohlížeči bez nutnosti zabalit kód do jakéhokoli vlastního kódu.

Příklad:

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

Hodnota `try-dotnet-class` aplikuje u kódu předaného interaktivní komponentě generování na úrovni třídy.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

Příklad:

Fragment kódu bez aplikovaného generování tříd

```md
public static void Main()
    {  
        // Specify the data source.  
        int[] scores = new int[] { 97, 92, 81, 60 };        // Define the query expression.

        IEnumerable<int> scoreQuery =
            from score in scores  
            where score > 80  
            select score;

        // Execute the query.  
        foreach (int i in scoreQuery)
        {  
            Console.Write(i + " ");
        }
    }  
}
```

Fragment kódu s aplikovaným generováním tříd

```md
class NameOfClass {

   public static void Main()
    {
        // Specify the data source.
        int[] scores = new int[] { 97, 92, 81, 60 };

        // Define the query expression.
        IEnumerable<int> scoreQuery =
            from score in scores
            where score > 80
            select score;

        // Execute the query.
        foreach (int i in scoreQuery)
        {
            Console.Write(i + " ");
        }
    }  
}
```

Hodnota `try-dotnet-method` aplikuje u kódu předaného interaktivní komponentě generování na úrovni metody.

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

Příklad:

Fragment kódu bez aplikovaného generování metod

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

Fragment kódu s aplikovaným generováním metod

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a>Přehled syntaxe fragmentů

Na fragmenty kódu uložené v úložišti můžete odkazovat pomocí zadaného jazyka kódu. Obsah specifikované cesty kódu se rozbalí a zahrne do vašeho souboru.

Struktura složek fragmentů kódu není nijak omezená. Fragmenty kódu můžete spravovat jako běžný zdrojový kód.

Syntaxe:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Tato syntaxe je blokové rozšíření Markdownu. Musíte ji použít na samostatném řádku.

- `<language>` (*volitelné*)
  - Jazyk fragmentu kódu. Další informace najdete v části [Podporované jazyky](#supported-languages) dále v tomto článku.

- `<path>` (*povinné*)
  - Relativní cesta v systému souborů označující soubor fragmentu kódu, na který se má odkazovat

- `<attribute>` a `<attribute-value>` (*volitelné*)
  - Společně se používají pro zadání, jak se má kód ze souboru načítat:
    - `range`: `1,3-5` Rozsah řádků. Tento příklad zahrnuje řádky 1, 3, 4 a 5.
    - `id`: `snippet_Create` ID fragmentu, který se má vložit ze souboru kódu. Tato hodnota nemůže existovat současně s rozsahem.
    - `highlight`: `2-4,6` Rozsah a/nebo čísla řádků, které se mají zvýraznit ve vygenerovaném fragmentu kódu. Číslování je relativní vzhledem k samotnému fragmentu kódu, nikoli k importovanému rozsahu.
    - `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Hodnota řetězce určuje, jaké druhy interaktivity jsou povolené.

#### <a name="supported-languages"></a>Podporované jazyky

|Name|Popisek Markdownu|
|-----|-------|
|.NET Core CLI|`dotnetcli`|
|ASP.NET s C#|`aspx-csharp`|
|ASP.NET s VB|`aspx-vb`|
|Azure CLI|`azurecli`|
|Azure CLI v prohlížeči|`azurecli-interactive`|
|Azure PowerShell v prohlížeči|`azurepowershell-interactive`|
|AzCopy|`azcopy`|
|Bash|`bash`|
|C++|`cpp`|
|C#|`csharp`|
|C# v prohlížeči|`csharp-interactive`|
|Konzola|`console`|
|CSHTML|`cshtml`|
|DAX|`dax`|
|Docker|`Dockerfile`|
|F#|`fsharp`|
|HTML|`html`|
|Java|`java`|
|JavaScript|`javascript`|
|JSON|`json`|
|Dotazovací jazyk Kusto|`kusto`|
|Markdown|`md`|
|Objective-C|`objc`|
|PHP|`php`|
|PowerShell|`powershell`|
|Power Query M|`powerquery-m`|
|protobuf|`protobuf`|
|Python|`python`|
|Ruby|`ruby`|
|SQL|`sql`|
|Swift|`swift`|
|VB|`vb`|
|XAML|`xaml`|
|XML|`xml`|
|YAML|`yml`|

#### <a name="code-extensions"></a>Rozšíření kódu

|Name|Popisek Markdownu|Přípona souboru|
|-----|-------|-----|
|C#|csharp|.cs, .csx|
|C++|cpp|.cpp, .h|
|F#|fsharp|.fs|
|Java|java|.java|
|JavaScript|javascript|.js|
|Python|python|.py|
|SQL|sql|.sql|
|VB|vb|.vb|
|XAML|xaml|.xaml|
|XML|xml|.xml|

## <a name="gotchas-and-troubleshooting"></a>Možná úskalí a řešení potíží

### <a name="alt-text"></a>Alternativní text

Alternativní text, který obsahuje podtržítka, se správně nezobrazí. Třeba místo použití tohoto:

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Napište takto před podtržítka zpětné lomítko:

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrofy a uvozovky

Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky. Pro ty je nutné použít kód nebo je změnit na základní uvozovky. Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s

Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:

- Levá (otevírací) uvozovka: `&#8220;`
- Pravá (uzavírací) uvozovka: `&#8221;`
- Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`
- Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`

### <a name="angle-brackets"></a>Ostré závorky

K označování zástupných symbolů se běžně používají ostré závorky. Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat. Jinak je Markdown bude považovat za značku HTML.

Například `<script name>` přepište kódem jako `&lt;script name&gt;`

## <a name="markdown-flavor"></a>Varianta Markdownu

Backend webu docs.microsoft.com podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig). Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat. Další funkce se přidávají prostřednictvím rozšíření Markdownu.

## <a name="see-also"></a>Viz také:

### <a name="markdown-resources"></a>Prostředky pro Markdown

- [Úvod do Markdownu](https://daringfireball.net/projects/markdown/syntax)
- [Tahák pro Markdown v Docs](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Základy Markdownu v GitHubu](https://help.github.com/articles/markdown-basics/)
- [Příručka pro Markdown](https://www.markdownguide.org/)
