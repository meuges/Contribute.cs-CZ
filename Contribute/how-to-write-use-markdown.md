---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/23/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Používání Markdownu pro vytváření článků na webu Docs

Články na docs.microsoft.com jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí. Díky tomu se v oboru rychle stal standardem.

Protože je obsah Docs uložený v GitHubu, může používat nadstavbu Markdownu zvanou [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), která poskytuje další funkce pro běžné potřeby formátování. Platforma OPS (Open Publishing Services) navíc implementuje Markdig Markdown Parser. Markdig je vysoce kompatibilní s rozšířením GitHub Flavored Markdown (GFM) a přidává možnosti podporující funkce specifické pro Docs.

* Markdig je rozšiřitelný procesor Markdownu pro .NET, který je rychlý, výkonný a kompatibilní se syntaxí CommonMark.
* https://github.com/lunet-io/markdig
* Lepší podpora komunity
* Lepší podpora standardů

## <a name="markdown-basics"></a>Základy Markdownu

### <a name="headings"></a>Nadpis

K vytvoření nadpisu se používá znak hash (#):

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>Tučné písmo a kurzíva

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
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>Seznamy

#### <a name="unordered-list"></a>Neseřazený seznam

Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky. Například tento Markdown:

```markdown
- List item 1
- List item 2
- List item 3
```

se zobrazí takto:

- List item 1
- List item 2
- List item 3

Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte. Například tento Markdown:

```markdown
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

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

se zobrazí takto:

1. First instruction
2. Second instruction
3. Third instruction

Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte. Například tento Markdown:

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

se zobrazí takto:

1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction

### <a name="tables"></a>Tables

Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM. Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-). Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují. Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.

Například tento Markdown:

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

se zobrazí takto:

| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

Další informace o vytváření tabulek:

- [Funkce zalamování tabulek](#table-wrapping) v Markdigu určená k formátování širokých tabulek
- [Organizování informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu
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

Alias za prvními třemi znaky „`“ definuje použité zvýraznění syntaxe. Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:

Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.

|Název|Popisek Markdownu|
|-----|-------|
|Konzola .NET|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

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

## <a name="ops-custom-markdown-extensions"></a>Vlastní rozšíření Markdownu od OPS

> [!NOTE]
> Platforma Open Publishing Services (OPS) implementuje analyzátor Markdig Parser pro Markdown, který je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown). Markdig přidává v rozšířeních Markdownu některé další funkce. Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS. (Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)

Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy. Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:

- Bloky poznámek
- Zahrnutí
- Voliče
- Vložená videa
- Fragmenty/ukázky kódu

Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.

### <a name="note-blocks"></a>Bloky poznámek

Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:

- POZNÁMKA
- VAROVÁNÍ
- TIP
- DŮLEŽITÉ

Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě. I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.

### <a name="includes"></a>Zahrnutí

Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru. Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku. K dispozici jsou tři typy zahrnutí, které vám pomůžou znovu použít obsah:

- Vložení: umožňuje znovu použít běžný vložený fragment textu v jiné větě.
- Blok: umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.
- Obrázek: takto se v Docs implementuje standardní zahrnutí obrázků.

Zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md). Ty mohou obsahovat jakýkoli platný Markdown. Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště. Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.

Tady jsou požadavky a důležité informace týkající se zahrnutí:

- Zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.
- Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl. Nepoužívejte je na nic menšího než větu.
- Zahrnuté soubory se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu. Vykreslí se až po zveřejnění.
- Dbejte na to, aby byl všechen text v zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na zahrnutí odkazuje. Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.
- Nevkládejte zahrnutí do jiných zahrnutí. Není to podporováno.
- Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media. Adresář multimédií nesmí ve svém kořenu obsahovat obrázky. Pokud zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.
- Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí. Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem. Multimediální soubor uložte do složky multimédií spojené se zahrnutím.
- Nepoužívejte zahrnutí jako jediný obsah článku.  Zahrnutí mají být doplněním obsahu ve zbytku článku.

### <a name="selectors"></a>Voliče

Voliče používejte v technických článcích, když vytváříte více charakterů stejného článku, abyste vyřešili rozdíly v implementaci pro různé technologie nebo platformy. Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře. V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.

Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do zahrnutí. Pak můžete na zahrnutí odkázat ve všech článcích, které stejný volič používají.

### <a name="code-snippets"></a>Fragmenty kódu

Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu. To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:

- Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště
- Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích

## <a name="gotchas-and-troubleshooting"></a>Možná úskalí a řešení potíží

### <a name="alt-text"></a>Alternativní text

Alternativní text, který obsahuje podtržítka, se správně nezobrazí. Třeba místo použití tohoto:

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Napište takto před podtržítka zpětné lomítko:

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrofy a uvozovky

Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky. Pro ty je nutné použít kód nebo je změnit na základní uvozovky. Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s

Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:

- Levá (otevírací) uvozovka: `&#8220;`
- Pravá (uzavírací) uvozovka: `&#8221;`
- Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`
- Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`

### <a name="angle-brackets"></a>Ostré závorky

Pokud v textu (ne kódu) v souboru používáte ostré závorky, třeba k vyznačení zástupného symbolu, musíte pro ně použít kód. Jinak je Markdown bude považovat za značku HTML.

Například `<script name>` přepište kódem jako `&lt;script name&gt;`

## <a name="see-also"></a>Viz také

### <a name="markdown-resources"></a>Prostředky pro Markdown

- [Úvod do Markdownu](https://daringfireball.net/projects/markdown/syntax)
- [Tahák pro Markdown v Docs](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Základy Markdownu v GitHubu](https://help.github.com/articles/markdown-basics/)
