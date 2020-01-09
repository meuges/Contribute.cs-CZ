---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: 1f43cecb450c988e4f546aa5ecc5907061521f34
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188288"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="10ff9-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="10ff9-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="10ff9-104">Články na [docs.microsoft.com](https://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="10ff9-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="10ff9-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="10ff9-106">Na webu Docs se používá [varianta Markdig](#markdown-flavor) jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="10ff9-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="10ff9-107">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="10ff9-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="10ff9-108">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="10ff9-108">Headings</span></span>

<span data-ttu-id="10ff9-109">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="10ff9-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="10ff9-110">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="10ff9-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="10ff9-111">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="10ff9-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="10ff9-112">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="10ff9-113">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="10ff9-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="10ff9-114">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="10ff9-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="10ff9-115">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="10ff9-116">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="10ff9-116">Bold and italic text</span></span>

<span data-ttu-id="10ff9-117">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="10ff9-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="10ff9-118">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="10ff9-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="10ff9-119">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="10ff9-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="10ff9-120">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="10ff9-120">Blockquotes</span></span>

<span data-ttu-id="10ff9-121">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="10ff9-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="10ff9-122">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="10ff9-123">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="10ff9-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="10ff9-124">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="10ff9-125">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="10ff9-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="10ff9-126">Seznamy</span><span class="sxs-lookup"><span data-stu-id="10ff9-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="10ff9-127">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="10ff9-127">Unordered list</span></span>

<span data-ttu-id="10ff9-128">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="10ff9-129">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="10ff9-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="10ff9-130">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-130">will be rendered as:</span></span>

- <span data-ttu-id="10ff9-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="10ff9-131">List item 1</span></span>
- <span data-ttu-id="10ff9-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="10ff9-132">List item 2</span></span>
- <span data-ttu-id="10ff9-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="10ff9-133">List item 3</span></span>

<span data-ttu-id="10ff9-134">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="10ff9-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="10ff9-135">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="10ff9-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="10ff9-136">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-136">will be rendered as:</span></span>

- <span data-ttu-id="10ff9-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="10ff9-137">List item 1</span></span>
  - <span data-ttu-id="10ff9-138">List item A</span><span class="sxs-lookup"><span data-stu-id="10ff9-138">List item A</span></span>
  - <span data-ttu-id="10ff9-139">List item B</span><span class="sxs-lookup"><span data-stu-id="10ff9-139">List item B</span></span>
- <span data-ttu-id="10ff9-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="10ff9-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="10ff9-141">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="10ff9-141">Ordered list</span></span>

<span data-ttu-id="10ff9-142">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="10ff9-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="10ff9-143">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="10ff9-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="10ff9-144">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-144">will be rendered as:</span></span>

1. <span data-ttu-id="10ff9-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-145">First instruction</span></span>
2. <span data-ttu-id="10ff9-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-146">Second instruction</span></span>
3. <span data-ttu-id="10ff9-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-147">Third instruction</span></span>

<span data-ttu-id="10ff9-148">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="10ff9-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="10ff9-149">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="10ff9-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="10ff9-150">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-150">will be rendered as:</span></span>

1. <span data-ttu-id="10ff9-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-151">First instruction</span></span>
   1. <span data-ttu-id="10ff9-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-152">Sub-instruction</span></span>
   2. <span data-ttu-id="10ff9-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-153">Sub-instruction</span></span>
2. <span data-ttu-id="10ff9-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="10ff9-154">Second instruction</span></span>

<span data-ttu-id="10ff9-155">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="10ff9-155">Note that we use '1.'</span></span> <span data-ttu-id="10ff9-156">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-156">for all entries.</span></span> <span data-ttu-id="10ff9-157">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="10ff9-158">Tabulky</span><span class="sxs-lookup"><span data-stu-id="10ff9-158">Tables</span></span>

<span data-ttu-id="10ff9-159">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="10ff9-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="10ff9-160">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="10ff9-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="10ff9-161">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="10ff9-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="10ff9-162">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="10ff9-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="10ff9-163">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="10ff9-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="10ff9-164">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-164">Will be rendered as:</span></span>

| <span data-ttu-id="10ff9-165">Fun</span><span class="sxs-lookup"><span data-stu-id="10ff9-165">Fun</span></span>                  | <span data-ttu-id="10ff9-166">With</span><span class="sxs-lookup"><span data-stu-id="10ff9-166">With</span></span>                 | <span data-ttu-id="10ff9-167">Tabulky</span><span class="sxs-lookup"><span data-stu-id="10ff9-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="10ff9-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="10ff9-168">left-aligned column</span></span>  | <span data-ttu-id="10ff9-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="10ff9-169">right-aligned column</span></span> | <span data-ttu-id="10ff9-170">centered column</span><span class="sxs-lookup"><span data-stu-id="10ff9-170">centered column</span></span> |
| <span data-ttu-id="10ff9-171">$100</span><span class="sxs-lookup"><span data-stu-id="10ff9-171">$100</span></span>                 | <span data-ttu-id="10ff9-172">$100</span><span class="sxs-lookup"><span data-stu-id="10ff9-172">$100</span></span>                 | <span data-ttu-id="10ff9-173">$100</span><span class="sxs-lookup"><span data-stu-id="10ff9-173">$100</span></span>            |
| <span data-ttu-id="10ff9-174">$10</span><span class="sxs-lookup"><span data-stu-id="10ff9-174">$10</span></span>                  | <span data-ttu-id="10ff9-175">$10</span><span class="sxs-lookup"><span data-stu-id="10ff9-175">$10</span></span>                  | <span data-ttu-id="10ff9-176">$10</span><span class="sxs-lookup"><span data-stu-id="10ff9-176">$10</span></span>             |
| <span data-ttu-id="10ff9-177">$1</span><span class="sxs-lookup"><span data-stu-id="10ff9-177">$1</span></span>                   | <span data-ttu-id="10ff9-178">$1</span><span class="sxs-lookup"><span data-stu-id="10ff9-178">$1</span></span>                   | <span data-ttu-id="10ff9-179">$1</span><span class="sxs-lookup"><span data-stu-id="10ff9-179">$1</span></span>              |

<span data-ttu-id="10ff9-180">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="10ff9-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="10ff9-181">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="10ff9-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="10ff9-182">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="10ff9-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="10ff9-183">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="10ff9-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="10ff9-184">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="10ff9-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="10ff9-185">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="10ff9-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="10ff9-186">Odkazy</span><span class="sxs-lookup"><span data-stu-id="10ff9-186">Links</span></span>

<span data-ttu-id="10ff9-187">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="10ff9-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="10ff9-188">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="10ff9-188">For more information on linking, see:</span></span>

- <span data-ttu-id="10ff9-189">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="10ff9-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="10ff9-190">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="10ff9-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="10ff9-191">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="10ff9-191">Code snippets</span></span>

<span data-ttu-id="10ff9-192">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="10ff9-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="10ff9-193">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="10ff9-193">For details, see:</span></span>

- [<span data-ttu-id="10ff9-194">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="10ff9-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="10ff9-195">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="10ff9-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="10ff9-196">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="10ff9-197">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="10ff9-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="10ff9-198">Alias za prvními třemi znaky (\`) definuje zvýraznění syntaxe, které se má použít.</span><span class="sxs-lookup"><span data-stu-id="10ff9-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="10ff9-199">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných popisků:</span><span class="sxs-lookup"><span data-stu-id="10ff9-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="10ff9-200">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="10ff9-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="10ff9-201">Název</span><span class="sxs-lookup"><span data-stu-id="10ff9-201">Name</span></span>|<span data-ttu-id="10ff9-202">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="10ff9-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="10ff9-203">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="10ff9-203">.NET Console</span></span>|<span data-ttu-id="10ff9-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="10ff9-204">dotnetcli</span></span>|
|<span data-ttu-id="10ff9-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="10ff9-205">ASP.NET (C#)</span></span>|<span data-ttu-id="10ff9-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="10ff9-206">aspx-csharp</span></span>|
|<span data-ttu-id="10ff9-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="10ff9-207">ASP.NET (VB)</span></span>|<span data-ttu-id="10ff9-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="10ff9-208">aspx-vb</span></span>|
|<span data-ttu-id="10ff9-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="10ff9-209">AzCopy</span></span>|<span data-ttu-id="10ff9-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="10ff9-210">azcopy</span></span>|
|<span data-ttu-id="10ff9-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="10ff9-211">Azure CLI</span></span>|<span data-ttu-id="10ff9-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="10ff9-212">azurecli</span></span>|
|<span data-ttu-id="10ff9-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="10ff9-213">Azure PowerShell</span></span>|<span data-ttu-id="10ff9-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="10ff9-214">azurepowershell</span></span>|
|<span data-ttu-id="10ff9-215">Bash</span><span class="sxs-lookup"><span data-stu-id="10ff9-215">Bash</span></span>|<span data-ttu-id="10ff9-216">bash</span><span class="sxs-lookup"><span data-stu-id="10ff9-216">bash</span></span>|
|<span data-ttu-id="10ff9-217">C++</span><span class="sxs-lookup"><span data-stu-id="10ff9-217">C++</span></span>|<span data-ttu-id="10ff9-218">cpp</span><span class="sxs-lookup"><span data-stu-id="10ff9-218">cpp</span></span>|
|<span data-ttu-id="10ff9-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="10ff9-219">C++/CX</span></span>|<span data-ttu-id="10ff9-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="10ff9-220">cppcx</span></span>|
|<span data-ttu-id="10ff9-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="10ff9-221">C++/WinRT</span></span>|<span data-ttu-id="10ff9-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="10ff9-222">cppwinrt</span></span>|
|<span data-ttu-id="10ff9-223">C#</span><span class="sxs-lookup"><span data-stu-id="10ff9-223">C#</span></span>|<span data-ttu-id="10ff9-224">csharp</span><span class="sxs-lookup"><span data-stu-id="10ff9-224">csharp</span></span>|
|<span data-ttu-id="10ff9-225">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="10ff9-225">C# in browser</span></span>|<span data-ttu-id="10ff9-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="10ff9-226">csharp-interactive</span></span>|
|<span data-ttu-id="10ff9-227">Konzola</span><span class="sxs-lookup"><span data-stu-id="10ff9-227">Console</span></span>|<span data-ttu-id="10ff9-228">konzola</span><span class="sxs-lookup"><span data-stu-id="10ff9-228">console</span></span>|
|<span data-ttu-id="10ff9-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="10ff9-229">CSHTML</span></span>|<span data-ttu-id="10ff9-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="10ff9-230">cshtml</span></span>|
|<span data-ttu-id="10ff9-231">DAX</span><span class="sxs-lookup"><span data-stu-id="10ff9-231">DAX</span></span>|<span data-ttu-id="10ff9-232">dax</span><span class="sxs-lookup"><span data-stu-id="10ff9-232">dax</span></span>|
|<span data-ttu-id="10ff9-233">Docker</span><span class="sxs-lookup"><span data-stu-id="10ff9-233">Docker</span></span>|<span data-ttu-id="10ff9-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="10ff9-234">dockerfile</span></span>|
|<span data-ttu-id="10ff9-235">F#</span><span class="sxs-lookup"><span data-stu-id="10ff9-235">F#</span></span>|<span data-ttu-id="10ff9-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="10ff9-236">fsharp</span></span>|
|<span data-ttu-id="10ff9-237">Go</span><span class="sxs-lookup"><span data-stu-id="10ff9-237">Go</span></span>|<span data-ttu-id="10ff9-238">go</span><span class="sxs-lookup"><span data-stu-id="10ff9-238">go</span></span>|
|<span data-ttu-id="10ff9-239">HTML</span><span class="sxs-lookup"><span data-stu-id="10ff9-239">HTML</span></span>|<span data-ttu-id="10ff9-240">html</span><span class="sxs-lookup"><span data-stu-id="10ff9-240">html</span></span>|
|<span data-ttu-id="10ff9-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="10ff9-241">HTTP</span></span>|<span data-ttu-id="10ff9-242">http</span><span class="sxs-lookup"><span data-stu-id="10ff9-242">http</span></span>|
|<span data-ttu-id="10ff9-243">Java</span><span class="sxs-lookup"><span data-stu-id="10ff9-243">Java</span></span>|<span data-ttu-id="10ff9-244">java</span><span class="sxs-lookup"><span data-stu-id="10ff9-244">java</span></span>|
|<span data-ttu-id="10ff9-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="10ff9-245">JavaScript</span></span>|<span data-ttu-id="10ff9-246">javascript</span><span class="sxs-lookup"><span data-stu-id="10ff9-246">javascript</span></span>|
|<span data-ttu-id="10ff9-247">JSON</span><span class="sxs-lookup"><span data-stu-id="10ff9-247">JSON</span></span>|<span data-ttu-id="10ff9-248">json</span><span class="sxs-lookup"><span data-stu-id="10ff9-248">json</span></span>|
|<span data-ttu-id="10ff9-249">Dotazovací jazyk Kusto</span><span class="sxs-lookup"><span data-stu-id="10ff9-249">Kusto Query Language</span></span>|<span data-ttu-id="10ff9-250">kusto</span><span class="sxs-lookup"><span data-stu-id="10ff9-250">kusto</span></span>|
|<span data-ttu-id="10ff9-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="10ff9-251">Markdown</span></span>|<span data-ttu-id="10ff9-252">md</span><span class="sxs-lookup"><span data-stu-id="10ff9-252">md</span></span>|
|<span data-ttu-id="10ff9-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="10ff9-253">Objective-C</span></span>|<span data-ttu-id="10ff9-254">objc</span><span class="sxs-lookup"><span data-stu-id="10ff9-254">objc</span></span>|
|<span data-ttu-id="10ff9-255">OData</span><span class="sxs-lookup"><span data-stu-id="10ff9-255">OData</span></span>|<span data-ttu-id="10ff9-256">odata</span><span class="sxs-lookup"><span data-stu-id="10ff9-256">odata</span></span>|
|<span data-ttu-id="10ff9-257">PHP</span><span class="sxs-lookup"><span data-stu-id="10ff9-257">PHP</span></span>|<span data-ttu-id="10ff9-258">php</span><span class="sxs-lookup"><span data-stu-id="10ff9-258">php</span></span>|
|<span data-ttu-id="10ff9-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="10ff9-259">protobuf</span></span>|<span data-ttu-id="10ff9-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="10ff9-260">protobuf</span></span>|
|<span data-ttu-id="10ff9-261">PowerApps (oddělovač desetinných míst v podobě tečky)</span><span class="sxs-lookup"><span data-stu-id="10ff9-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="10ff9-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="10ff9-262">powerapps-dot</span></span>|
|<span data-ttu-id="10ff9-263">PowerApps (oddělovač desetinných míst v podobě čárky)</span><span class="sxs-lookup"><span data-stu-id="10ff9-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="10ff9-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="10ff9-264">powerapps-comma</span></span>|
|<span data-ttu-id="10ff9-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="10ff9-265">PowerShell</span></span>|<span data-ttu-id="10ff9-266">powershell</span><span class="sxs-lookup"><span data-stu-id="10ff9-266">powershell</span></span>|
|<span data-ttu-id="10ff9-267">Python</span><span class="sxs-lookup"><span data-stu-id="10ff9-267">Python</span></span>|<span data-ttu-id="10ff9-268">python</span><span class="sxs-lookup"><span data-stu-id="10ff9-268">python</span></span>|
|<span data-ttu-id="10ff9-269">Q#</span><span class="sxs-lookup"><span data-stu-id="10ff9-269">Q#</span></span>|<span data-ttu-id="10ff9-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="10ff9-270">qsharp</span></span>|
|<span data-ttu-id="10ff9-271">R</span><span class="sxs-lookup"><span data-stu-id="10ff9-271">R</span></span>|<span data-ttu-id="10ff9-272">r</span><span class="sxs-lookup"><span data-stu-id="10ff9-272">r</span></span>|
|<span data-ttu-id="10ff9-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="10ff9-273">Ruby</span></span>|<span data-ttu-id="10ff9-274">ruby</span><span class="sxs-lookup"><span data-stu-id="10ff9-274">ruby</span></span>|
|<span data-ttu-id="10ff9-275">SQL</span><span class="sxs-lookup"><span data-stu-id="10ff9-275">SQL</span></span>|<span data-ttu-id="10ff9-276">sql</span><span class="sxs-lookup"><span data-stu-id="10ff9-276">sql</span></span>|
|<span data-ttu-id="10ff9-277">Swift</span><span class="sxs-lookup"><span data-stu-id="10ff9-277">Swift</span></span>|<span data-ttu-id="10ff9-278">swift</span><span class="sxs-lookup"><span data-stu-id="10ff9-278">swift</span></span>|
|<span data-ttu-id="10ff9-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="10ff9-279">TypeScript</span></span>|<span data-ttu-id="10ff9-280">typescript</span><span class="sxs-lookup"><span data-stu-id="10ff9-280">typescript</span></span>|
|<span data-ttu-id="10ff9-281">VB</span><span class="sxs-lookup"><span data-stu-id="10ff9-281">VB</span></span>|<span data-ttu-id="10ff9-282">vb</span><span class="sxs-lookup"><span data-stu-id="10ff9-282">vb</span></span>|
|<span data-ttu-id="10ff9-283">XAML</span><span class="sxs-lookup"><span data-stu-id="10ff9-283">XAML</span></span>|<span data-ttu-id="10ff9-284">xaml</span><span class="sxs-lookup"><span data-stu-id="10ff9-284">xaml</span></span>|
|<span data-ttu-id="10ff9-285">XML</span><span class="sxs-lookup"><span data-stu-id="10ff9-285">XML</span></span>|<span data-ttu-id="10ff9-286">xml</span><span class="sxs-lookup"><span data-stu-id="10ff9-286">xml</span></span>|

<span data-ttu-id="10ff9-287">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="10ff9-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="10ff9-288">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="10ff9-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="10ff9-289">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="10ff9-289">Example: C\#</span></span>

<span data-ttu-id="10ff9-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="10ff9-290">__Markdown__</span></span>

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

<span data-ttu-id="10ff9-291">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="10ff9-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="10ff9-292">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="10ff9-292">Example: SQL</span></span>

<span data-ttu-id="10ff9-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="10ff9-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="10ff9-294">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="10ff9-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="10ff9-295">Vlastní rozšíření Markdownu pro Docs</span><span class="sxs-lookup"><span data-stu-id="10ff9-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="10ff9-296">Docs.Microsoft.com (Docs) implementuje analyzátor Markdig Parser pro Markdown, který je ve velké míře kompatibilní s rozšířením GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="10ff9-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="10ff9-297">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="10ff9-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="10ff9-298">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="10ff9-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="10ff9-299">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="10ff9-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="10ff9-300">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="10ff9-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="10ff9-301">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="10ff9-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="10ff9-302">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="10ff9-302">Note blocks</span></span>
- <span data-ttu-id="10ff9-303">Vložené soubory</span><span class="sxs-lookup"><span data-stu-id="10ff9-303">Include files</span></span>
- <span data-ttu-id="10ff9-304">Voliče</span><span class="sxs-lookup"><span data-stu-id="10ff9-304">Selectors</span></span>
- <span data-ttu-id="10ff9-305">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="10ff9-305">Embedded videos</span></span>
- <span data-ttu-id="10ff9-306">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="10ff9-306">Code snippets/samples</span></span>

<span data-ttu-id="10ff9-307">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="10ff9-308">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="10ff9-308">Note blocks</span></span>

<span data-ttu-id="10ff9-309">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="10ff9-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="10ff9-310">NOTE (POZNÁMKA)</span><span class="sxs-lookup"><span data-stu-id="10ff9-310">NOTE</span></span>
- <span data-ttu-id="10ff9-311">WARNING (VAROVÁNÍ)</span><span class="sxs-lookup"><span data-stu-id="10ff9-311">WARNING</span></span>
- <span data-ttu-id="10ff9-312">TIP</span><span class="sxs-lookup"><span data-stu-id="10ff9-312">TIP</span></span>
- <span data-ttu-id="10ff9-313">IMPORTANT (DŮLEŽITÉ)</span><span class="sxs-lookup"><span data-stu-id="10ff9-313">IMPORTANT</span></span>

<span data-ttu-id="10ff9-314">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="10ff9-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="10ff9-315">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="10ff9-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="10ff9-316">Příklady:</span><span class="sxs-lookup"><span data-stu-id="10ff9-316">Examples:</span></span>

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

<span data-ttu-id="10ff9-317">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-317">These alerts look like this on docs.microsoft.com:</span></span>

![Ukazuje, jak výstrahy v předchozím příkladu vypadají na publikované stránce Docs s různými ikonami a barvami.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="10ff9-319">Soubory k zahrnutí</span><span class="sxs-lookup"><span data-stu-id="10ff9-319">Include files</span></span>

<span data-ttu-id="10ff9-320">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="10ff9-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="10ff9-321">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="10ff9-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="10ff9-322">K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="10ff9-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="10ff9-323">Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="10ff9-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="10ff9-324">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="10ff9-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="10ff9-325">Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="10ff9-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="10ff9-326">Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="10ff9-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="10ff9-327">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="10ff9-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="10ff9-328">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="10ff9-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="10ff9-329">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="10ff9-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="10ff9-330">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="10ff9-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="10ff9-331">Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="10ff9-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="10ff9-332">Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="10ff9-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="10ff9-333">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="10ff9-334">Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="10ff9-335">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="10ff9-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="10ff9-336">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="10ff9-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="10ff9-337">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="10ff9-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="10ff9-338">Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="10ff9-339">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="10ff9-339">They are not supported.</span></span>
- <span data-ttu-id="10ff9-340">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="10ff9-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="10ff9-341">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="10ff9-342">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="10ff9-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="10ff9-343">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="10ff9-344">Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="10ff9-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="10ff9-345">Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="10ff9-346">Nepoužívejte soubor k zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="10ff9-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="10ff9-347">Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="10ff9-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="10ff9-348">Příklad:</span><span class="sxs-lookup"><span data-stu-id="10ff9-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="10ff9-349">Voliče</span><span class="sxs-lookup"><span data-stu-id="10ff9-349">Selectors</span></span>

<span data-ttu-id="10ff9-350">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="10ff9-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="10ff9-351">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="10ff9-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="10ff9-352">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="10ff9-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="10ff9-353">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="10ff9-354">Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="10ff9-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="10ff9-355">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="10ff9-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="10ff9-356">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="10ff9-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="10ff9-357">Odkazy pro zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="10ff9-357">Code include references</span></span>

<span data-ttu-id="10ff9-358">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-358">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="10ff9-359">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="10ff9-359">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="10ff9-360">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="10ff9-360">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="10ff9-361">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="10ff9-361">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="10ff9-362">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="10ff9-362">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="10ff9-363">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="10ff9-363">Alt text</span></span>

<span data-ttu-id="10ff9-364">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="10ff9-364">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="10ff9-365">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="10ff9-365">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="10ff9-366">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="10ff9-366">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="10ff9-367">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="10ff9-367">Apostrophes and quotation marks</span></span>

<span data-ttu-id="10ff9-368">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-368">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="10ff9-369">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-369">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="10ff9-370">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="10ff9-370">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="10ff9-371">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="10ff9-371">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="10ff9-372">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="10ff9-372">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="10ff9-373">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="10ff9-373">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="10ff9-374">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="10ff9-374">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="10ff9-375">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="10ff9-375">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="10ff9-376">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="10ff9-376">Angle brackets</span></span>

<span data-ttu-id="10ff9-377">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="10ff9-377">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="10ff9-378">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="10ff9-378">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="10ff9-379">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="10ff9-379">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="10ff9-380">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="10ff9-380">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="10ff9-381">Varianta Markdownu</span><span class="sxs-lookup"><span data-stu-id="10ff9-381">Markdown flavor</span></span>

<span data-ttu-id="10ff9-382">Backend webu docs.microsoft.com podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="10ff9-382">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="10ff9-383">Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat.</span><span class="sxs-lookup"><span data-stu-id="10ff9-383">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="10ff9-384">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="10ff9-384">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="10ff9-385">Viz také:</span><span class="sxs-lookup"><span data-stu-id="10ff9-385">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="10ff9-386">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="10ff9-386">Markdown resources</span></span>

- [<span data-ttu-id="10ff9-387">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="10ff9-387">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="10ff9-388">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="10ff9-388">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="10ff9-389">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="10ff9-389">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="10ff9-390">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="10ff9-390">The Markdown Guide</span></span>](https://www.markdownguide.org/)
