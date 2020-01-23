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
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="7ffe8-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="7ffe8-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="7ffe8-104">Články na [docs.microsoft.com](https://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="7ffe8-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="7ffe8-106">Na webu Docs se používá [varianta Markdig](#markdown-flavor) jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="7ffe8-107">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="7ffe8-108">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-108">Headings</span></span>

<span data-ttu-id="7ffe8-109">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="7ffe8-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="7ffe8-110">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="7ffe8-111">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="7ffe8-112">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="7ffe8-113">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="7ffe8-114">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="7ffe8-115">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="7ffe8-116">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="7ffe8-116">Bold and italic text</span></span>

<span data-ttu-id="7ffe8-117">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="7ffe8-118">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="7ffe8-119">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="7ffe8-120">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="7ffe8-120">Blockquotes</span></span>

<span data-ttu-id="7ffe8-121">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="7ffe8-122">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="7ffe8-123">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="7ffe8-124">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="7ffe8-125">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="7ffe8-126">Seznamy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="7ffe8-127">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="7ffe8-127">Unordered list</span></span>

<span data-ttu-id="7ffe8-128">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="7ffe8-129">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="7ffe8-130">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-130">will be rendered as:</span></span>

- <span data-ttu-id="7ffe8-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="7ffe8-131">List item 1</span></span>
- <span data-ttu-id="7ffe8-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="7ffe8-132">List item 2</span></span>
- <span data-ttu-id="7ffe8-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="7ffe8-133">List item 3</span></span>

<span data-ttu-id="7ffe8-134">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7ffe8-135">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="7ffe8-136">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-136">will be rendered as:</span></span>

- <span data-ttu-id="7ffe8-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="7ffe8-137">List item 1</span></span>
  - <span data-ttu-id="7ffe8-138">List item A</span><span class="sxs-lookup"><span data-stu-id="7ffe8-138">List item A</span></span>
  - <span data-ttu-id="7ffe8-139">List item B</span><span class="sxs-lookup"><span data-stu-id="7ffe8-139">List item B</span></span>
- <span data-ttu-id="7ffe8-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="7ffe8-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="7ffe8-141">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="7ffe8-141">Ordered list</span></span>

<span data-ttu-id="7ffe8-142">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="7ffe8-143">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="7ffe8-144">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-144">will be rendered as:</span></span>

1. <span data-ttu-id="7ffe8-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-145">First instruction</span></span>
2. <span data-ttu-id="7ffe8-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-146">Second instruction</span></span>
3. <span data-ttu-id="7ffe8-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-147">Third instruction</span></span>

<span data-ttu-id="7ffe8-148">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="7ffe8-149">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="7ffe8-150">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-150">will be rendered as:</span></span>

1. <span data-ttu-id="7ffe8-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-151">First instruction</span></span>
   1. <span data-ttu-id="7ffe8-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-152">Sub-instruction</span></span>
   2. <span data-ttu-id="7ffe8-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-153">Sub-instruction</span></span>
2. <span data-ttu-id="7ffe8-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="7ffe8-154">Second instruction</span></span>

<span data-ttu-id="7ffe8-155">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="7ffe8-155">Note that we use '1.'</span></span> <span data-ttu-id="7ffe8-156">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-156">for all entries.</span></span> <span data-ttu-id="7ffe8-157">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="7ffe8-158">Tabulky</span><span class="sxs-lookup"><span data-stu-id="7ffe8-158">Tables</span></span>

<span data-ttu-id="7ffe8-159">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="7ffe8-160">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="7ffe8-161">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="7ffe8-162">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="7ffe8-163">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="7ffe8-164">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-164">Will be rendered as:</span></span>

| <span data-ttu-id="7ffe8-165">Fun</span><span class="sxs-lookup"><span data-stu-id="7ffe8-165">Fun</span></span>                  | <span data-ttu-id="7ffe8-166">With</span><span class="sxs-lookup"><span data-stu-id="7ffe8-166">With</span></span>                 | <span data-ttu-id="7ffe8-167">Tabulky</span><span class="sxs-lookup"><span data-stu-id="7ffe8-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="7ffe8-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="7ffe8-168">left-aligned column</span></span>  | <span data-ttu-id="7ffe8-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="7ffe8-169">right-aligned column</span></span> | <span data-ttu-id="7ffe8-170">centered column</span><span class="sxs-lookup"><span data-stu-id="7ffe8-170">centered column</span></span> |
| <span data-ttu-id="7ffe8-171">$100</span><span class="sxs-lookup"><span data-stu-id="7ffe8-171">$100</span></span>                 | <span data-ttu-id="7ffe8-172">$100</span><span class="sxs-lookup"><span data-stu-id="7ffe8-172">$100</span></span>                 | <span data-ttu-id="7ffe8-173">$100</span><span class="sxs-lookup"><span data-stu-id="7ffe8-173">$100</span></span>            |
| <span data-ttu-id="7ffe8-174">$10</span><span class="sxs-lookup"><span data-stu-id="7ffe8-174">$10</span></span>                  | <span data-ttu-id="7ffe8-175">$10</span><span class="sxs-lookup"><span data-stu-id="7ffe8-175">$10</span></span>                  | <span data-ttu-id="7ffe8-176">$10</span><span class="sxs-lookup"><span data-stu-id="7ffe8-176">$10</span></span>             |
| <span data-ttu-id="7ffe8-177">$1</span><span class="sxs-lookup"><span data-stu-id="7ffe8-177">$1</span></span>                   | <span data-ttu-id="7ffe8-178">$1</span><span class="sxs-lookup"><span data-stu-id="7ffe8-178">$1</span></span>                   | <span data-ttu-id="7ffe8-179">$1</span><span class="sxs-lookup"><span data-stu-id="7ffe8-179">$1</span></span>              |

<span data-ttu-id="7ffe8-180">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="7ffe8-181">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="7ffe8-182">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="7ffe8-183">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="7ffe8-184">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="7ffe8-185">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="7ffe8-186">Odkazy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-186">Links</span></span>

<span data-ttu-id="7ffe8-187">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="7ffe8-188">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-188">For more information on linking, see:</span></span>

- <span data-ttu-id="7ffe8-189">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="7ffe8-190">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="7ffe8-191">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-191">Code snippets</span></span>

<span data-ttu-id="7ffe8-192">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="7ffe8-193">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-193">For details, see:</span></span>

- [<span data-ttu-id="7ffe8-194">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="7ffe8-195">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="7ffe8-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="7ffe8-196">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="7ffe8-197">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="7ffe8-198">Alias za prvními třemi znaky (\`) definuje zvýraznění syntaxe, které se má použít.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="7ffe8-199">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných popisků:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="7ffe8-200">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="7ffe8-201">Název</span><span class="sxs-lookup"><span data-stu-id="7ffe8-201">Name</span></span>|<span data-ttu-id="7ffe8-202">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="7ffe8-203">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="7ffe8-203">.NET Console</span></span>|<span data-ttu-id="7ffe8-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="7ffe8-204">dotnetcli</span></span>|
|<span data-ttu-id="7ffe8-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-205">ASP.NET (C#)</span></span>|<span data-ttu-id="7ffe8-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-206">aspx-csharp</span></span>|
|<span data-ttu-id="7ffe8-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-207">ASP.NET (VB)</span></span>|<span data-ttu-id="7ffe8-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="7ffe8-208">aspx-vb</span></span>|
|<span data-ttu-id="7ffe8-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-209">AzCopy</span></span>|<span data-ttu-id="7ffe8-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-210">azcopy</span></span>|
|<span data-ttu-id="7ffe8-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="7ffe8-211">Azure CLI</span></span>|<span data-ttu-id="7ffe8-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="7ffe8-212">azurecli</span></span>|
|<span data-ttu-id="7ffe8-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ffe8-213">Azure PowerShell</span></span>|<span data-ttu-id="7ffe8-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="7ffe8-214">azurepowershell</span></span>|
|<span data-ttu-id="7ffe8-215">Bash</span><span class="sxs-lookup"><span data-stu-id="7ffe8-215">Bash</span></span>|<span data-ttu-id="7ffe8-216">bash</span><span class="sxs-lookup"><span data-stu-id="7ffe8-216">bash</span></span>|
|<span data-ttu-id="7ffe8-217">C++</span><span class="sxs-lookup"><span data-stu-id="7ffe8-217">C++</span></span>|<span data-ttu-id="7ffe8-218">cpp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-218">cpp</span></span>|
|<span data-ttu-id="7ffe8-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="7ffe8-219">C++/CX</span></span>|<span data-ttu-id="7ffe8-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="7ffe8-220">cppcx</span></span>|
|<span data-ttu-id="7ffe8-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="7ffe8-221">C++/WinRT</span></span>|<span data-ttu-id="7ffe8-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="7ffe8-222">cppwinrt</span></span>|
|<span data-ttu-id="7ffe8-223">C#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-223">C#</span></span>|<span data-ttu-id="7ffe8-224">csharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-224">csharp</span></span>|
|<span data-ttu-id="7ffe8-225">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="7ffe8-225">C# in browser</span></span>|<span data-ttu-id="7ffe8-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="7ffe8-226">csharp-interactive</span></span>|
|<span data-ttu-id="7ffe8-227">Konzola</span><span class="sxs-lookup"><span data-stu-id="7ffe8-227">Console</span></span>|<span data-ttu-id="7ffe8-228">konzola</span><span class="sxs-lookup"><span data-stu-id="7ffe8-228">console</span></span>|
|<span data-ttu-id="7ffe8-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-229">CSHTML</span></span>|<span data-ttu-id="7ffe8-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-230">cshtml</span></span>|
|<span data-ttu-id="7ffe8-231">DAX</span><span class="sxs-lookup"><span data-stu-id="7ffe8-231">DAX</span></span>|<span data-ttu-id="7ffe8-232">dax</span><span class="sxs-lookup"><span data-stu-id="7ffe8-232">dax</span></span>|
|<span data-ttu-id="7ffe8-233">Docker</span><span class="sxs-lookup"><span data-stu-id="7ffe8-233">Docker</span></span>|<span data-ttu-id="7ffe8-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="7ffe8-234">dockerfile</span></span>|
|<span data-ttu-id="7ffe8-235">F#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-235">F#</span></span>|<span data-ttu-id="7ffe8-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-236">fsharp</span></span>|
|<span data-ttu-id="7ffe8-237">Go</span><span class="sxs-lookup"><span data-stu-id="7ffe8-237">Go</span></span>|<span data-ttu-id="7ffe8-238">go</span><span class="sxs-lookup"><span data-stu-id="7ffe8-238">go</span></span>|
|<span data-ttu-id="7ffe8-239">HTML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-239">HTML</span></span>|<span data-ttu-id="7ffe8-240">html</span><span class="sxs-lookup"><span data-stu-id="7ffe8-240">html</span></span>|
|<span data-ttu-id="7ffe8-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="7ffe8-241">HTTP</span></span>|<span data-ttu-id="7ffe8-242">http</span><span class="sxs-lookup"><span data-stu-id="7ffe8-242">http</span></span>|
|<span data-ttu-id="7ffe8-243">Java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-243">Java</span></span>|<span data-ttu-id="7ffe8-244">java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-244">java</span></span>|
|<span data-ttu-id="7ffe8-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-245">JavaScript</span></span>|<span data-ttu-id="7ffe8-246">javascript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-246">javascript</span></span>|
|<span data-ttu-id="7ffe8-247">JSON</span><span class="sxs-lookup"><span data-stu-id="7ffe8-247">JSON</span></span>|<span data-ttu-id="7ffe8-248">json</span><span class="sxs-lookup"><span data-stu-id="7ffe8-248">json</span></span>|
|<span data-ttu-id="7ffe8-249">Dotazovací jazyk Kusto</span><span class="sxs-lookup"><span data-stu-id="7ffe8-249">Kusto Query Language</span></span>|<span data-ttu-id="7ffe8-250">kusto</span><span class="sxs-lookup"><span data-stu-id="7ffe8-250">kusto</span></span>|
|<span data-ttu-id="7ffe8-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="7ffe8-251">Markdown</span></span>|<span data-ttu-id="7ffe8-252">md</span><span class="sxs-lookup"><span data-stu-id="7ffe8-252">md</span></span>|
|<span data-ttu-id="7ffe8-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="7ffe8-253">Objective-C</span></span>|<span data-ttu-id="7ffe8-254">objc</span><span class="sxs-lookup"><span data-stu-id="7ffe8-254">objc</span></span>|
|<span data-ttu-id="7ffe8-255">OData</span><span class="sxs-lookup"><span data-stu-id="7ffe8-255">OData</span></span>|<span data-ttu-id="7ffe8-256">odata</span><span class="sxs-lookup"><span data-stu-id="7ffe8-256">odata</span></span>|
|<span data-ttu-id="7ffe8-257">PHP</span><span class="sxs-lookup"><span data-stu-id="7ffe8-257">PHP</span></span>|<span data-ttu-id="7ffe8-258">php</span><span class="sxs-lookup"><span data-stu-id="7ffe8-258">php</span></span>|
|<span data-ttu-id="7ffe8-259">protobuf</span><span class="sxs-lookup"><span data-stu-id="7ffe8-259">protobuf</span></span>|<span data-ttu-id="7ffe8-260">protobuf</span><span class="sxs-lookup"><span data-stu-id="7ffe8-260">protobuf</span></span>|
|<span data-ttu-id="7ffe8-261">PowerApps (oddělovač desetinných míst v podobě tečky)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="7ffe8-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="7ffe8-262">powerapps-dot</span></span>|
|<span data-ttu-id="7ffe8-263">PowerApps (oddělovač desetinných míst v podobě čárky)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="7ffe8-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="7ffe8-264">powerapps-comma</span></span>|
|<span data-ttu-id="7ffe8-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ffe8-265">PowerShell</span></span>|<span data-ttu-id="7ffe8-266">powershell</span><span class="sxs-lookup"><span data-stu-id="7ffe8-266">powershell</span></span>|
|<span data-ttu-id="7ffe8-267">Python</span><span class="sxs-lookup"><span data-stu-id="7ffe8-267">Python</span></span>|<span data-ttu-id="7ffe8-268">python</span><span class="sxs-lookup"><span data-stu-id="7ffe8-268">python</span></span>|
|<span data-ttu-id="7ffe8-269">Q#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-269">Q#</span></span>|<span data-ttu-id="7ffe8-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-270">qsharp</span></span>|
|<span data-ttu-id="7ffe8-271">R</span><span class="sxs-lookup"><span data-stu-id="7ffe8-271">R</span></span>|<span data-ttu-id="7ffe8-272">r</span><span class="sxs-lookup"><span data-stu-id="7ffe8-272">r</span></span>|
|<span data-ttu-id="7ffe8-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="7ffe8-273">Ruby</span></span>|<span data-ttu-id="7ffe8-274">ruby</span><span class="sxs-lookup"><span data-stu-id="7ffe8-274">ruby</span></span>|
|<span data-ttu-id="7ffe8-275">SQL</span><span class="sxs-lookup"><span data-stu-id="7ffe8-275">SQL</span></span>|<span data-ttu-id="7ffe8-276">sql</span><span class="sxs-lookup"><span data-stu-id="7ffe8-276">sql</span></span>|
|<span data-ttu-id="7ffe8-277">Swift</span><span class="sxs-lookup"><span data-stu-id="7ffe8-277">Swift</span></span>|<span data-ttu-id="7ffe8-278">swift</span><span class="sxs-lookup"><span data-stu-id="7ffe8-278">swift</span></span>|
|<span data-ttu-id="7ffe8-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-279">TypeScript</span></span>|<span data-ttu-id="7ffe8-280">typescript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-280">typescript</span></span>|
|<span data-ttu-id="7ffe8-281">VB</span><span class="sxs-lookup"><span data-stu-id="7ffe8-281">VB</span></span>|<span data-ttu-id="7ffe8-282">vb</span><span class="sxs-lookup"><span data-stu-id="7ffe8-282">vb</span></span>|
|<span data-ttu-id="7ffe8-283">XAML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-283">XAML</span></span>|<span data-ttu-id="7ffe8-284">xaml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-284">xaml</span></span>|
|<span data-ttu-id="7ffe8-285">XML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-285">XML</span></span>|<span data-ttu-id="7ffe8-286">xml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-286">xml</span></span>|

<span data-ttu-id="7ffe8-287">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="7ffe8-288">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="7ffe8-289">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-289">Example: C\#</span></span>

<span data-ttu-id="7ffe8-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7ffe8-290">__Markdown__</span></span>

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

<span data-ttu-id="7ffe8-291">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="7ffe8-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="7ffe8-292">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="7ffe8-292">Example: SQL</span></span>

<span data-ttu-id="7ffe8-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="7ffe8-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="7ffe8-294">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="7ffe8-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="7ffe8-295">Vlastní rozšíření Markdownu pro Docs</span><span class="sxs-lookup"><span data-stu-id="7ffe8-295">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="7ffe8-296">Docs.Microsoft.com (Docs) implementuje analyzátor Markdig Parser pro Markdown, který je ve velké míře kompatibilní s rozšířením GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-296">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="7ffe8-297">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="7ffe8-298">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="7ffe8-299">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="7ffe8-300">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="7ffe8-301">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="7ffe8-302">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="7ffe8-302">Note blocks</span></span>
- <span data-ttu-id="7ffe8-303">Vložené soubory</span><span class="sxs-lookup"><span data-stu-id="7ffe8-303">Include files</span></span>
- <span data-ttu-id="7ffe8-304">Voliče</span><span class="sxs-lookup"><span data-stu-id="7ffe8-304">Selectors</span></span>
- <span data-ttu-id="7ffe8-305">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="7ffe8-305">Embedded videos</span></span>
- <span data-ttu-id="7ffe8-306">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-306">Code snippets/samples</span></span>

<span data-ttu-id="7ffe8-307">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="7ffe8-308">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="7ffe8-308">Note blocks</span></span>

<span data-ttu-id="7ffe8-309">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="7ffe8-310">NOTE (POZNÁMKA)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-310">NOTE</span></span>
- <span data-ttu-id="7ffe8-311">WARNING (VAROVÁNÍ)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-311">WARNING</span></span>
- <span data-ttu-id="7ffe8-312">TIP</span><span class="sxs-lookup"><span data-stu-id="7ffe8-312">TIP</span></span>
- <span data-ttu-id="7ffe8-313">IMPORTANT (DŮLEŽITÉ)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-313">IMPORTANT</span></span>

<span data-ttu-id="7ffe8-314">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="7ffe8-315">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="7ffe8-316">Příklady:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-316">Examples:</span></span>

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

<span data-ttu-id="7ffe8-317">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-317">These alerts look like this on docs.microsoft.com:</span></span>

![Ukazuje, jak výstrahy v předchozím příkladu vypadají na publikované stránce Docs s různými ikonami a barvami.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="7ffe8-319">Soubory k zahrnutí</span><span class="sxs-lookup"><span data-stu-id="7ffe8-319">Include files</span></span>

<span data-ttu-id="7ffe8-320">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-320">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="7ffe8-321">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-321">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="7ffe8-322">K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-322">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="7ffe8-323">Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-323">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="7ffe8-324">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-324">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="7ffe8-325">Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-325">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="7ffe8-326">Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-326">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="7ffe8-327">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-327">It can contain any valid Markdown.</span></span> <span data-ttu-id="7ffe8-328">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-328">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="7ffe8-329">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-329">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="7ffe8-330">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-330">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="7ffe8-331">Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-331">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="7ffe8-332">Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-332">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="7ffe8-333">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-333">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="7ffe8-334">Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-334">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="7ffe8-335">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-335">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="7ffe8-336">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-336">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="7ffe8-337">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-337">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="7ffe8-338">Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-338">Don't embed include references within other include files.</span></span> <span data-ttu-id="7ffe8-339">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-339">They are not supported.</span></span>
- <span data-ttu-id="7ffe8-340">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-340">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="7ffe8-341">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-341">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="7ffe8-342">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-342">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="7ffe8-343">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-343">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="7ffe8-344">Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-344">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="7ffe8-345">Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-345">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="7ffe8-346">Nepoužívejte soubor k zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-346">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="7ffe8-347">Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-347">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="7ffe8-348">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-348">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="7ffe8-349">Voliče</span><span class="sxs-lookup"><span data-stu-id="7ffe8-349">Selectors</span></span>

<span data-ttu-id="7ffe8-350">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-350">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="7ffe8-351">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-351">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="7ffe8-352">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-352">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="7ffe8-353">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-353">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="7ffe8-354">Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-354">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="7ffe8-355">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-355">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="7ffe8-356">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-356">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="7ffe8-357">Odkazy pro zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-357">Code include references</span></span>

<span data-ttu-id="7ffe8-358">Rozšíření Markdownu pro fragmenty kódu na webu Docs umožňuje vkládat do článků ukázky kódu a vykreslovat je s barevným zvýrazňováním syntaxe specifického jazyka.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-358">The Docs code snippet Markdown extension allows you to embed code samples in your articles and render them with language-specific syntax coloring.</span></span> <span data-ttu-id="7ffe8-359">Můžete zahrnout kód jak z aktuálního úložiště, tak z jiného úložiště.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-359">You can include code from either the current repository or another repository.</span></span> <span data-ttu-id="7ffe8-360">Níže uvedené pokyny poskytují přehled o tom, jak používat tuto funkci se sadou [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-360">The instructions below provides an overview of how to use the feature with the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span> <span data-ttu-id="7ffe8-361">V editoru Visual Studio Code můžete zobrazit náhled fragmentů kódu otevřením okna **Preview** (Náhled).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-361">In Visual Studio Code, you can preview the code snippets by opening **Preview**.</span></span> <span data-ttu-id="7ffe8-362">V náhledu nejsou k dispozici zvýrazňování a interaktivita.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-362">Highlighting and interactivity are not available in preview.</span></span>

> [!NOTE]
> <span data-ttu-id="7ffe8-363">Toto rozšíření nepodporuje zahrnutí kódu formou vložení do textu – to se provádí pomocí standardní konvence Markdownu, tedy tří znaků \`.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-363">The extension does not support including code content within it inline – this is to be done through the standard triple-tick Markdown convention.</span></span>

#### <a name="code-from-current-repository"></a><span data-ttu-id="7ffe8-364">Kód z aktuálního úložiště</span><span class="sxs-lookup"><span data-stu-id="7ffe8-364">Code from current repository</span></span>

1. <span data-ttu-id="7ffe8-365">V editoru Visual Studio Code stiskněte **Alt+M** nebo **Option+M** a vyberte Snippet (Fragment).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-365">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="7ffe8-366">Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-366">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="7ffe8-367">Pokud chcete vyhledávat místně, vyberte Full Local Search (Úplné místní vyhledávání).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-367">To search locally, select Full Local Search.</span></span>
3. <span data-ttu-id="7ffe8-368">Zadejte hledaný termín pro vyhledání souboru.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-368">Enter a search term to find the file.</span></span> <span data-ttu-id="7ffe8-369">Jakmile soubor najdete, vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-369">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="7ffe8-370">Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-370">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="7ffe8-371">Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-371">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="7ffe8-372">Podle výběru z kroku 4 zadejte v případě potřeby hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-372">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="7ffe8-373">Zobrazení celého souboru kódu:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-373">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="7ffe8-374">Zobrazení části souboru kódu zadáním čísel řádků:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-374">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="7ffe8-375">Zobrazení části souboru kódu zadáním názvu fragmentu:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-375">Display part of a code file by a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

#### <a name="code-from-another-repository"></a><span data-ttu-id="7ffe8-376">Kód z jiného úložiště</span><span class="sxs-lookup"><span data-stu-id="7ffe8-376">Code from another repository</span></span>

1. <span data-ttu-id="7ffe8-377">V editoru Visual Studio Code stiskněte **Alt+M** nebo **Option+M** a vyberte Snippet (Fragment).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-377">In Visual Studio Code, click **Alt + M** or **Option + M** and select Snippet.</span></span>
2. <span data-ttu-id="7ffe8-378">Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-378">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="7ffe8-379">Pokud chcete hledat v jiném úložišti, vyberte Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-379">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="7ffe8-380">Dostanete možnost vybrat úložiště, která jsou v *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-380">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="7ffe8-381">Vyberte úložiště.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-381">Select a repository.</span></span>
3. <span data-ttu-id="7ffe8-382">Zadejte hledaný termín pro vyhledání souboru.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-382">Enter a search term to find the file.</span></span> <span data-ttu-id="7ffe8-383">Jakmile soubor najdete, vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-383">Once you’ve found the file, select the file.</span></span>
4. <span data-ttu-id="7ffe8-384">Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-384">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="7ffe8-385">Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-385">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="7ffe8-386">Podle výběru z kroku 5 zadejte v případě potřeby hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-386">Based on your selection from Step 5, provide a value if necessary.</span></span>

<span data-ttu-id="7ffe8-387">Váš odkaz na fragment bude vypadat nějak takto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-387">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

#### <a name="path-to-code-file"></a><span data-ttu-id="7ffe8-388">Cesta k souboru kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-388">Path to code file</span></span>

<span data-ttu-id="7ffe8-389">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-389">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="7ffe8-390">Příklad je z úložiště dokumentů ASP.NET, soubor článku [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-390">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="7ffe8-391">Na soubor kódu odkazuje relativní cesta k [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) ve stejném úložišti.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-391">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

#### <a name="selected-line-numbers"></a><span data-ttu-id="7ffe8-392">Vybraná čísla řádků</span><span class="sxs-lookup"><span data-stu-id="7ffe8-392">Selected line numbers</span></span>

<span data-ttu-id="7ffe8-393">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-393">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="7ffe8-394">Tento příklad zobrazí jenom řádky 2 až 24 a 26 ze souboru kódu *StudentController.cs*.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-394">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="7ffe8-395">Dejte raději přednost fragmentům před pevnými čísly řádků, jak je vysvětleno v další části.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-395">Prefer snippets over hard-coded line numbers, as explained in the next section.</span></span>

#### <a name="named-snippet"></a><span data-ttu-id="7ffe8-396">Pojmenovaný fragment</span><span class="sxs-lookup"><span data-stu-id="7ffe8-396">Named snippet</span></span>

<span data-ttu-id="7ffe8-397">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-397">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="7ffe8-398">Pro název používejte jenom písmena a podtržítka.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-398">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="7ffe8-399">V příkladu je zobrazený oddíl `snippet_Create` souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-399">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="7ffe8-400">Soubor kódu pro tento příklad má oblast C# s názvem `snippet_Create`:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-400">The code file for this example has a C# region named `snippet_Create`:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="7ffe8-401">Vždy, když je to možné, odkazujte na pojmenovanou část a nezadávejte čísla řádků.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-401">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="7ffe8-402">S odkazy na čísla řádků je třeba zacházet opatrně, protože soubory kódu se nevyhnutelně mění tak, že dochází ke změnám čísel řádků.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-402">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="7ffe8-403">Takové změny vám lehce uniknou.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-403">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="7ffe8-404">Ve vašem článku se nakonec začnou zobrazovat chybné řádky a vy nebudete mít potuchy, že se něco změnilo.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-404">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

#### <a name="highlighting-selected-lines"></a><span data-ttu-id="7ffe8-405">Zvýraznění vybraných řádků</span><span class="sxs-lookup"><span data-stu-id="7ffe8-405">Highlighting selected lines</span></span>

<span data-ttu-id="7ffe8-406">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-406">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="7ffe8-407">V příkladu jsou zvýrazněné řádky 2 a 5, počítáno od začátku zobrazeného fragmentu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-407">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="7ffe8-408">(Čísla zvýrazněných řádků se nepočítají od začátku souboru kódu.) Jinými slovy jsou zvýrazněné řádky 3 a 6 ze souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-408">(Line numbers to highlight don't count from the start of the code file.) In other words, lines 3 and 6 of the code file are highlighted.</span></span>

#### <a name="interactive-code-snippets"></a><span data-ttu-id="7ffe8-409">Interaktivní fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-409">Interactive code snippets</span></span>

<span data-ttu-id="7ffe8-410">Interaktivní režim můžete povolit pro fragmenty kódu, které jsou zahrnuté odkazem.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-410">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="7ffe8-411">Tady jsou příklady:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-411">Here are examples:</span></span>

```markdown
:::code language="powershell" source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code language="bash" source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="7ffe8-412">Pokud chcete tuto funkci zapnout pro konkrétní blok kódu, použijte atribut `interactive`.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-412">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="7ffe8-413">Dostupné hodnoty atributu jsou:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-413">The available attribute values are:</span></span>

- <span data-ttu-id="7ffe8-414">`cloudshell-powershell` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-414">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
- <span data-ttu-id="7ffe8-415">`cloudshell-bash` – povolí Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-415">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
- <span data-ttu-id="7ffe8-416">`try-dotnet` – povolí Try .NET.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-416">`try-dotnet` - Enables Try .NET</span></span>
- <span data-ttu-id="7ffe8-417">`try-dotnet-class` – povolí Try .NET s generováním tříd.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-417">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
- <span data-ttu-id="7ffe8-418">`try-dotnet-method` – povolí Try .NET s generováním metod.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-418">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="7ffe8-419">Existují páry hodnot atributů `language` a `interactive`, které jsou kompatibilní.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-419">There are pairs of `language` and `interactive` that are compatible.</span></span> <span data-ttu-id="7ffe8-420">Pokud má například atribut `interactive` hodnotu `try-dotnet`, musí být jako jazyk zadaný `csharp`.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-420">For example, if `interactive` is `try-dotnet`, the language must be `csharp`.</span></span> <span data-ttu-id="7ffe8-421">Podobně bude atribut `cloudshell-powershell` fungovat jenom s jazykem `powershell` a atribut `cloudshell-bash` s jazykem `bash`.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-421">Similarly, `cloudshell-powershell` would only work with `powershell` and `cloudshell-bash` would work only with `bash` as the language.</span></span>

<span data-ttu-id="7ffe8-422">Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-422">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

<span data-ttu-id="7ffe8-423">[Try .NET](https://github.com/dotnet/try) umožňuje interaktivní spouštění kódu .NET (C#) v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-423">[Try .NET](https://github.com/dotnet/try) enables interactive execution of .NET code (C#) in the browser.</span></span> <span data-ttu-id="7ffe8-424">Pro Try .NET existují tři možnosti interaktivity: `try-dotnet`, `try-dotnet-class` a `try-dotnet-method`.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-424">For Try .NET, there are three options for interactivity: `try-dotnet`, `try-dotnet-class`, and `try-dotnet-method`.</span></span> <span data-ttu-id="7ffe8-425">Použití těchto možností nevyžaduje žádnou další konfiguraci v rámci fragmentu kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-425">Use of these options require no additional configuration within the code snippet.</span></span> <span data-ttu-id="7ffe8-426">Ve výchozím nastavení jsou v současnosti dostupné tyto obory názvů:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-426">The namespaces currently available by default are:</span></span>

- <span data-ttu-id="7ffe8-427">System</span><span class="sxs-lookup"><span data-stu-id="7ffe8-427">System</span></span>
- <span data-ttu-id="7ffe8-428">System.Linq</span><span class="sxs-lookup"><span data-stu-id="7ffe8-428">System.Linq</span></span>
- <span data-ttu-id="7ffe8-429">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="7ffe8-429">System.Collections.Generic</span></span>
- <span data-ttu-id="7ffe8-430">System.Text</span><span class="sxs-lookup"><span data-stu-id="7ffe8-430">System.Text</span></span>
- <span data-ttu-id="7ffe8-431">System.Globalization</span><span class="sxs-lookup"><span data-stu-id="7ffe8-431">System.Globalization</span></span>
- <span data-ttu-id="7ffe8-432">System.Text.RegularExpressions</span><span class="sxs-lookup"><span data-stu-id="7ffe8-432">System.Text.RegularExpressions</span></span>

<span data-ttu-id="7ffe8-433">Hodnota atributu `try-dotnet` umožňuje uživatelům spustit kód C# v prohlížeči bez nutnosti zabalit kód do jakéhokoli vlastního kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-433">The `try-dotnet` attribute value enables users to run C# code in the browser without the need to wrap the code in any custom code.</span></span>

<span data-ttu-id="7ffe8-434">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-434">Example:</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" interactive="try-dotnet":::
```

<span data-ttu-id="7ffe8-435">Hodnota `try-dotnet-class` aplikuje u kódu předaného interaktivní komponentě generování na úrovni třídy.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-435">The `try-dotnet-class` value applies class-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-class":::
```

<span data-ttu-id="7ffe8-436">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-436">Example:</span></span>

<span data-ttu-id="7ffe8-437">Fragment kódu bez aplikovaného generování tříd</span><span class="sxs-lookup"><span data-stu-id="7ffe8-437">Code Snippet without Class Scaffolding Applied</span></span>

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

<span data-ttu-id="7ffe8-438">Fragment kódu s aplikovaným generováním tříd</span><span class="sxs-lookup"><span data-stu-id="7ffe8-438">Code Snippet with Class Scaffolding Applied</span></span>

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

<span data-ttu-id="7ffe8-439">Hodnota `try-dotnet-method` aplikuje u kódu předaného interaktivní komponentě generování na úrovni metody.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-439">The `try-dotnet-method` value applies method-level scaffolding to the code passed to the interactive component.</span></span>

```md
:::code language="csharp" source="relative/path/source.cs" id="snippet-tag" interactive="try-dotnet-method":::
```

<span data-ttu-id="7ffe8-440">Příklad:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-440">Example:</span></span>

<span data-ttu-id="7ffe8-441">Fragment kódu bez aplikovaného generování metod</span><span class="sxs-lookup"><span data-stu-id="7ffe8-441">Code Snippet without Method Scaffolding Applied</span></span>

```md
/*Print some string in C#*/

Console.WriteLine("Hello C#.);
```

<span data-ttu-id="7ffe8-442">Fragment kódu s aplikovaným generováním metod</span><span class="sxs-lookup"><span data-stu-id="7ffe8-442">Code Snippet with Method Scaffolding Applied</span></span>

```md
public static void Main(string args[]) {

/*Print some string in C#*/

Console.WriteLine("Hello C#.);
}
```

#### <a name="snippet-syntax-reference"></a><span data-ttu-id="7ffe8-443">Přehled syntaxe fragmentů</span><span class="sxs-lookup"><span data-stu-id="7ffe8-443">Snippet syntax reference</span></span>

<span data-ttu-id="7ffe8-444">Na fragmenty kódu uložené v úložišti můžete odkazovat pomocí zadaného jazyka kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-444">You can reference code snippets stored in your repo by using the specified code language.</span></span> <span data-ttu-id="7ffe8-445">Obsah specifikované cesty kódu se rozbalí a zahrne do vašeho souboru.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-445">The content of the specified code path will be expanded and included in your file.</span></span>

<span data-ttu-id="7ffe8-446">Struktura složek fragmentů kódu není nijak omezená.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-446">There aren't restrictions on the folder structure of code snippets.</span></span> <span data-ttu-id="7ffe8-447">Fragmenty kódu můžete spravovat jako běžný zdrojový kód.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-447">You can manage the code snippets as normal source code.</span></span>

<span data-ttu-id="7ffe8-448">Syntaxe:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-448">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="7ffe8-449">Tato syntaxe je blokové rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-449">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="7ffe8-450">Musíte ji použít na samostatném řádku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-450">It must be used on its own line.</span></span>

- <span data-ttu-id="7ffe8-451">`<language>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-451">`<language>` (*optional*)</span></span>
  - <span data-ttu-id="7ffe8-452">Jazyk fragmentu kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-452">Language of the code snippet.</span></span> <span data-ttu-id="7ffe8-453">Další informace najdete v části [Podporované jazyky](#supported-languages) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-453">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

- <span data-ttu-id="7ffe8-454">`<path>` (*povinné*)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-454">`<path>` (*mandatory*)</span></span>
  - <span data-ttu-id="7ffe8-455">Relativní cesta v systému souborů označující soubor fragmentu kódu, na který se má odkazovat</span><span class="sxs-lookup"><span data-stu-id="7ffe8-455">Relative path in the file system that indicates the code snippet file to reference.</span></span>

- <span data-ttu-id="7ffe8-456">`<attribute>` a `<attribute-value>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="7ffe8-456">`<attribute>` and `<attribute-value>` (*optional*)</span></span>
  - <span data-ttu-id="7ffe8-457">Společně se používají pro zadání, jak se má kód ze souboru načítat:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-457">Used together to specify how the code should be retrieved from the file:</span></span>
    - <span data-ttu-id="7ffe8-458">`range`: `1,3-5` Rozsah řádků.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-458">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="7ffe8-459">Tento příklad zahrnuje řádky 1, 3, 4 a 5.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-459">This example includes lines 1, 3, 4, and 5.</span></span>
    - <span data-ttu-id="7ffe8-460">`id`: `snippet_Create` ID fragmentu, který se má vložit ze souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-460">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="7ffe8-461">Tato hodnota nemůže existovat současně s rozsahem.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-461">This value cannot co-exist with range.</span></span>
    - <span data-ttu-id="7ffe8-462">`highlight`: `2-4,6` Rozsah a/nebo čísla řádků, které se mají zvýraznit ve vygenerovaném fragmentu kódu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-462">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="7ffe8-463">Číslování je relativní vzhledem k samotnému fragmentu kódu, nikoli k importovanému rozsahu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-463">The numbering is relative to the code snippet itself, not the imported range.</span></span>
    - <span data-ttu-id="7ffe8-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Hodnota řetězce určuje, jaké druhy interaktivity jsou povolené.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-464">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>

#### <a name="supported-languages"></a><span data-ttu-id="7ffe8-465">Podporované jazyky</span><span class="sxs-lookup"><span data-stu-id="7ffe8-465">Supported languages</span></span>

|<span data-ttu-id="7ffe8-466">Name</span><span class="sxs-lookup"><span data-stu-id="7ffe8-466">Name</span></span>|<span data-ttu-id="7ffe8-467">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-467">Markdown label</span></span>|
|-----|-------|
|<span data-ttu-id="7ffe8-468">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="7ffe8-468">.NET Core CLI</span></span>|`dotnetcli`|
|<span data-ttu-id="7ffe8-469">ASP.NET s C#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-469">ASP.NET with C#</span></span>|`aspx-csharp`|
|<span data-ttu-id="7ffe8-470">ASP.NET s VB</span><span class="sxs-lookup"><span data-stu-id="7ffe8-470">ASP.NET with VB</span></span>|`aspx-vb`|
|<span data-ttu-id="7ffe8-471">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="7ffe8-471">Azure CLI</span></span>|`azurecli`|
|<span data-ttu-id="7ffe8-472">Azure CLI v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="7ffe8-472">Azure CLI in browser</span></span>|`azurecli-interactive`|
|<span data-ttu-id="7ffe8-473">Azure PowerShell v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="7ffe8-473">Azure PowerShell in browser</span></span>|`azurepowershell-interactive`|
|<span data-ttu-id="7ffe8-474">AzCopy</span><span class="sxs-lookup"><span data-stu-id="7ffe8-474">AzCopy</span></span>|`azcopy`|
|<span data-ttu-id="7ffe8-475">Bash</span><span class="sxs-lookup"><span data-stu-id="7ffe8-475">Bash</span></span>|`bash`|
|<span data-ttu-id="7ffe8-476">C++</span><span class="sxs-lookup"><span data-stu-id="7ffe8-476">C++</span></span>|`cpp`|
|<span data-ttu-id="7ffe8-477">C#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-477">C#</span></span>|`csharp`|
|<span data-ttu-id="7ffe8-478">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="7ffe8-478">C# in browser</span></span>|`csharp-interactive`|
|<span data-ttu-id="7ffe8-479">Konzola</span><span class="sxs-lookup"><span data-stu-id="7ffe8-479">Console</span></span>|`console`|
|<span data-ttu-id="7ffe8-480">CSHTML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-480">CSHTML</span></span>|`cshtml`|
|<span data-ttu-id="7ffe8-481">DAX</span><span class="sxs-lookup"><span data-stu-id="7ffe8-481">DAX</span></span>|`dax`|
|<span data-ttu-id="7ffe8-482">Docker</span><span class="sxs-lookup"><span data-stu-id="7ffe8-482">Docker</span></span>|`Dockerfile`|
|<span data-ttu-id="7ffe8-483">F#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-483">F#</span></span>|`fsharp`|
|<span data-ttu-id="7ffe8-484">HTML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-484">HTML</span></span>|`html`|
|<span data-ttu-id="7ffe8-485">Java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-485">Java</span></span>|`java`|
|<span data-ttu-id="7ffe8-486">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-486">JavaScript</span></span>|`javascript`|
|<span data-ttu-id="7ffe8-487">JSON</span><span class="sxs-lookup"><span data-stu-id="7ffe8-487">JSON</span></span>|`json`|
|<span data-ttu-id="7ffe8-488">Dotazovací jazyk Kusto</span><span class="sxs-lookup"><span data-stu-id="7ffe8-488">Kusto Query Language</span></span>|`kusto`|
|<span data-ttu-id="7ffe8-489">Markdown</span><span class="sxs-lookup"><span data-stu-id="7ffe8-489">Markdown</span></span>|`md`|
|<span data-ttu-id="7ffe8-490">Objective-C</span><span class="sxs-lookup"><span data-stu-id="7ffe8-490">Objective-C</span></span>|`objc`|
|<span data-ttu-id="7ffe8-491">PHP</span><span class="sxs-lookup"><span data-stu-id="7ffe8-491">PHP</span></span>|`php`|
|<span data-ttu-id="7ffe8-492">PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ffe8-492">PowerShell</span></span>|`powershell`|
|<span data-ttu-id="7ffe8-493">Power Query M</span><span class="sxs-lookup"><span data-stu-id="7ffe8-493">Power Query M</span></span>|`powerquery-m`|
|<span data-ttu-id="7ffe8-494">protobuf</span><span class="sxs-lookup"><span data-stu-id="7ffe8-494">protobuf</span></span>|`protobuf`|
|<span data-ttu-id="7ffe8-495">Python</span><span class="sxs-lookup"><span data-stu-id="7ffe8-495">Python</span></span>|`python`|
|<span data-ttu-id="7ffe8-496">Ruby</span><span class="sxs-lookup"><span data-stu-id="7ffe8-496">Ruby</span></span>|`ruby`|
|<span data-ttu-id="7ffe8-497">SQL</span><span class="sxs-lookup"><span data-stu-id="7ffe8-497">SQL</span></span>|`sql`|
|<span data-ttu-id="7ffe8-498">Swift</span><span class="sxs-lookup"><span data-stu-id="7ffe8-498">Swift</span></span>|`swift`|
|<span data-ttu-id="7ffe8-499">VB</span><span class="sxs-lookup"><span data-stu-id="7ffe8-499">VB</span></span>|`vb`|
|<span data-ttu-id="7ffe8-500">XAML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-500">XAML</span></span>|`xaml`|
|<span data-ttu-id="7ffe8-501">XML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-501">XML</span></span>|`xml`|
|<span data-ttu-id="7ffe8-502">YAML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-502">YAML</span></span>|`yml`|

#### <a name="code-extensions"></a><span data-ttu-id="7ffe8-503">Rozšíření kódu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-503">Code extensions</span></span>

|<span data-ttu-id="7ffe8-504">Name</span><span class="sxs-lookup"><span data-stu-id="7ffe8-504">Name</span></span>|<span data-ttu-id="7ffe8-505">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-505">Markdown label</span></span>|<span data-ttu-id="7ffe8-506">Přípona souboru</span><span class="sxs-lookup"><span data-stu-id="7ffe8-506">File extension</span></span>|
|-----|-------|-----|
|<span data-ttu-id="7ffe8-507">C#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-507">C#</span></span>|<span data-ttu-id="7ffe8-508">csharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-508">csharp</span></span>|<span data-ttu-id="7ffe8-509">.cs, .csx</span><span class="sxs-lookup"><span data-stu-id="7ffe8-509">.cs, .csx</span></span>|
|<span data-ttu-id="7ffe8-510">C++</span><span class="sxs-lookup"><span data-stu-id="7ffe8-510">C++</span></span>|<span data-ttu-id="7ffe8-511">cpp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-511">cpp</span></span>|<span data-ttu-id="7ffe8-512">.cpp, .h</span><span class="sxs-lookup"><span data-stu-id="7ffe8-512">.cpp, .h</span></span>|
|<span data-ttu-id="7ffe8-513">F#</span><span class="sxs-lookup"><span data-stu-id="7ffe8-513">F#</span></span>|<span data-ttu-id="7ffe8-514">fsharp</span><span class="sxs-lookup"><span data-stu-id="7ffe8-514">fsharp</span></span>|<span data-ttu-id="7ffe8-515">.fs</span><span class="sxs-lookup"><span data-stu-id="7ffe8-515">.fs</span></span>|
|<span data-ttu-id="7ffe8-516">Java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-516">Java</span></span>|<span data-ttu-id="7ffe8-517">java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-517">java</span></span>|<span data-ttu-id="7ffe8-518">.java</span><span class="sxs-lookup"><span data-stu-id="7ffe8-518">.java</span></span>|
|<span data-ttu-id="7ffe8-519">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-519">JavaScript</span></span>|<span data-ttu-id="7ffe8-520">javascript</span><span class="sxs-lookup"><span data-stu-id="7ffe8-520">javascript</span></span>|<span data-ttu-id="7ffe8-521">.js</span><span class="sxs-lookup"><span data-stu-id="7ffe8-521">.js</span></span>|
|<span data-ttu-id="7ffe8-522">Python</span><span class="sxs-lookup"><span data-stu-id="7ffe8-522">Python</span></span>|<span data-ttu-id="7ffe8-523">python</span><span class="sxs-lookup"><span data-stu-id="7ffe8-523">python</span></span>|<span data-ttu-id="7ffe8-524">.py</span><span class="sxs-lookup"><span data-stu-id="7ffe8-524">.py</span></span>|
|<span data-ttu-id="7ffe8-525">SQL</span><span class="sxs-lookup"><span data-stu-id="7ffe8-525">SQL</span></span>|<span data-ttu-id="7ffe8-526">sql</span><span class="sxs-lookup"><span data-stu-id="7ffe8-526">sql</span></span>|<span data-ttu-id="7ffe8-527">.sql</span><span class="sxs-lookup"><span data-stu-id="7ffe8-527">.sql</span></span>|
|<span data-ttu-id="7ffe8-528">VB</span><span class="sxs-lookup"><span data-stu-id="7ffe8-528">VB</span></span>|<span data-ttu-id="7ffe8-529">vb</span><span class="sxs-lookup"><span data-stu-id="7ffe8-529">vb</span></span>|<span data-ttu-id="7ffe8-530">.vb</span><span class="sxs-lookup"><span data-stu-id="7ffe8-530">.vb</span></span>|
|<span data-ttu-id="7ffe8-531">XAML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-531">XAML</span></span>|<span data-ttu-id="7ffe8-532">xaml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-532">xaml</span></span>|<span data-ttu-id="7ffe8-533">.xaml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-533">.xaml</span></span>|
|<span data-ttu-id="7ffe8-534">XML</span><span class="sxs-lookup"><span data-stu-id="7ffe8-534">XML</span></span>|<span data-ttu-id="7ffe8-535">xml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-535">xml</span></span>|<span data-ttu-id="7ffe8-536">.xml</span><span class="sxs-lookup"><span data-stu-id="7ffe8-536">.xml</span></span>|

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="7ffe8-537">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="7ffe8-537">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="7ffe8-538">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="7ffe8-538">Alt text</span></span>

<span data-ttu-id="7ffe8-539">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-539">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="7ffe8-540">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-540">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="7ffe8-541">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-541">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="7ffe8-542">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="7ffe8-542">Apostrophes and quotation marks</span></span>

<span data-ttu-id="7ffe8-543">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-543">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="7ffe8-544">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-544">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="7ffe8-545">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="7ffe8-545">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="7ffe8-546">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-546">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="7ffe8-547">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-547">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="7ffe8-548">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-548">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="7ffe8-549">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-549">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="7ffe8-550">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-550">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="7ffe8-551">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="7ffe8-551">Angle brackets</span></span>

<span data-ttu-id="7ffe8-552">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-552">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="7ffe8-553">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-553">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="7ffe8-554">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-554">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="7ffe8-555">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="7ffe8-555">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="7ffe8-556">Varianta Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-556">Markdown flavor</span></span>

<span data-ttu-id="7ffe8-557">Backend webu docs.microsoft.com podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="7ffe8-557">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="7ffe8-558">Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-558">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="7ffe8-559">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="7ffe8-559">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ffe8-560">Viz také:</span><span class="sxs-lookup"><span data-stu-id="7ffe8-560">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="7ffe8-561">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="7ffe8-561">Markdown resources</span></span>

- [<span data-ttu-id="7ffe8-562">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-562">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="7ffe8-563">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="7ffe8-563">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="7ffe8-564">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="7ffe8-564">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="7ffe8-565">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="7ffe8-565">The Markdown Guide</span></span>](https://www.markdownguide.org/)
