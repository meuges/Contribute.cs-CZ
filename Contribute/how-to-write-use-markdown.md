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
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="667e7-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="667e7-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="667e7-104">Články na docs.microsoft.com jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="667e7-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="667e7-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="667e7-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="667e7-106">Protože je obsah Docs uložený v GitHubu, může používat nadstavbu Markdownu zvanou [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), která poskytuje další funkce pro běžné potřeby formátování.</span><span class="sxs-lookup"><span data-stu-id="667e7-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="667e7-107">Platforma OPS (Open Publishing Services) navíc implementuje Markdig Markdown Parser.</span><span class="sxs-lookup"><span data-stu-id="667e7-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="667e7-108">Markdig je vysoce kompatibilní s rozšířením GitHub Flavored Markdown (GFM) a přidává možnosti podporující funkce specifické pro Docs.</span><span class="sxs-lookup"><span data-stu-id="667e7-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="667e7-109">Markdig je rozšiřitelný procesor Markdownu pro .NET, který je rychlý, výkonný a kompatibilní se syntaxí CommonMark.</span><span class="sxs-lookup"><span data-stu-id="667e7-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="667e7-110">Lepší podpora komunity</span><span class="sxs-lookup"><span data-stu-id="667e7-110">Better community support</span></span>
* <span data-ttu-id="667e7-111">Lepší podpora standardů</span><span class="sxs-lookup"><span data-stu-id="667e7-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="667e7-112">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="667e7-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="667e7-113">Nadpis</span><span class="sxs-lookup"><span data-stu-id="667e7-113">Headings</span></span>

<span data-ttu-id="667e7-114">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="667e7-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="667e7-115">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="667e7-115">Bold and italic text</span></span>

<span data-ttu-id="667e7-116">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="667e7-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="667e7-117">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="667e7-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="667e7-118">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="667e7-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="667e7-119">Seznamy</span><span class="sxs-lookup"><span data-stu-id="667e7-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="667e7-120">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="667e7-120">Unordered list</span></span>

<span data-ttu-id="667e7-121">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="667e7-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="667e7-122">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="667e7-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="667e7-123">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="667e7-123">will be rendered as:</span></span>

- <span data-ttu-id="667e7-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="667e7-124">List item 1</span></span>
- <span data-ttu-id="667e7-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="667e7-125">List item 2</span></span>
- <span data-ttu-id="667e7-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="667e7-126">List item 3</span></span>

<span data-ttu-id="667e7-127">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="667e7-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="667e7-128">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="667e7-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="667e7-129">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="667e7-129">will be rendered as:</span></span>

- <span data-ttu-id="667e7-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="667e7-130">List item 1</span></span>
  - <span data-ttu-id="667e7-131">List item A</span><span class="sxs-lookup"><span data-stu-id="667e7-131">List item A</span></span>
  - <span data-ttu-id="667e7-132">List item B</span><span class="sxs-lookup"><span data-stu-id="667e7-132">List item B</span></span>
- <span data-ttu-id="667e7-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="667e7-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="667e7-134">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="667e7-134">Ordered list</span></span>

<span data-ttu-id="667e7-135">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="667e7-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="667e7-136">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="667e7-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="667e7-137">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="667e7-137">will be rendered as:</span></span>

1. <span data-ttu-id="667e7-138">First instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-138">First instruction</span></span>
2. <span data-ttu-id="667e7-139">Second instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-139">Second instruction</span></span>
3. <span data-ttu-id="667e7-140">Third instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-140">Third instruction</span></span>

<span data-ttu-id="667e7-141">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="667e7-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="667e7-142">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="667e7-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="667e7-143">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="667e7-143">will be rendered as:</span></span>

1. <span data-ttu-id="667e7-144">First instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-144">First instruction</span></span>
    1. <span data-ttu-id="667e7-145">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-145">Sub-instruction</span></span>
    2. <span data-ttu-id="667e7-146">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-146">Sub-instruction</span></span>
2. <span data-ttu-id="667e7-147">Second instruction</span><span class="sxs-lookup"><span data-stu-id="667e7-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="667e7-148">Tables</span><span class="sxs-lookup"><span data-stu-id="667e7-148">Tables</span></span>

<span data-ttu-id="667e7-149">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="667e7-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="667e7-150">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="667e7-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="667e7-151">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="667e7-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="667e7-152">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="667e7-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="667e7-153">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="667e7-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="667e7-154">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="667e7-154">will be rendered as:</span></span>

| <span data-ttu-id="667e7-155">Fun</span><span class="sxs-lookup"><span data-stu-id="667e7-155">Fun</span></span>                  | <span data-ttu-id="667e7-156">With</span><span class="sxs-lookup"><span data-stu-id="667e7-156">With</span></span>                 | <span data-ttu-id="667e7-157">Tables</span><span class="sxs-lookup"><span data-stu-id="667e7-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="667e7-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="667e7-158">left-aligned column</span></span>  | <span data-ttu-id="667e7-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="667e7-159">right-aligned column</span></span> | <span data-ttu-id="667e7-160">centered column</span><span class="sxs-lookup"><span data-stu-id="667e7-160">centered column</span></span> |
| <span data-ttu-id="667e7-161">$100</span><span class="sxs-lookup"><span data-stu-id="667e7-161">$100</span></span>                 | <span data-ttu-id="667e7-162">$100</span><span class="sxs-lookup"><span data-stu-id="667e7-162">$100</span></span>                 | <span data-ttu-id="667e7-163">$100</span><span class="sxs-lookup"><span data-stu-id="667e7-163">$100</span></span>            |
| <span data-ttu-id="667e7-164">$10</span><span class="sxs-lookup"><span data-stu-id="667e7-164">$10</span></span>                  | <span data-ttu-id="667e7-165">$10</span><span class="sxs-lookup"><span data-stu-id="667e7-165">$10</span></span>                  | <span data-ttu-id="667e7-166">$10</span><span class="sxs-lookup"><span data-stu-id="667e7-166">$10</span></span>             |
| <span data-ttu-id="667e7-167">$1</span><span class="sxs-lookup"><span data-stu-id="667e7-167">$1</span></span>                   | <span data-ttu-id="667e7-168">$1</span><span class="sxs-lookup"><span data-stu-id="667e7-168">$1</span></span>                   | <span data-ttu-id="667e7-169">$1</span><span class="sxs-lookup"><span data-stu-id="667e7-169">$1</span></span>              |

<span data-ttu-id="667e7-170">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="667e7-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="667e7-171">[Funkce zalamování tabulek](#table-wrapping) v Markdigu určená k formátování širokých tabulek</span><span class="sxs-lookup"><span data-stu-id="667e7-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="667e7-172">[Organizování informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="667e7-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="667e7-173">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="667e7-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="667e7-174">Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda</span><span class="sxs-lookup"><span data-stu-id="667e7-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="667e7-175">Markdown Extra od Michela Fortina</span><span class="sxs-lookup"><span data-stu-id="667e7-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="667e7-176">Převedení HTML tabulek na Markdown</span><span class="sxs-lookup"><span data-stu-id="667e7-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="667e7-177">Odkazy</span><span class="sxs-lookup"><span data-stu-id="667e7-177">Links</span></span>

<span data-ttu-id="667e7-178">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="667e7-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="667e7-179">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="667e7-179">For more information on linking, see:</span></span>

- <span data-ttu-id="667e7-180">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="667e7-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="667e7-181">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="667e7-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="667e7-182">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="667e7-182">Code snippets</span></span>

<span data-ttu-id="667e7-183">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="667e7-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="667e7-184">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="667e7-184">For details, see:</span></span>

- [<span data-ttu-id="667e7-185">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="667e7-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="667e7-186">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="667e7-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="667e7-187">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="667e7-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="667e7-188">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="667e7-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="667e7-189">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="667e7-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="667e7-190">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:</span><span class="sxs-lookup"><span data-stu-id="667e7-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="667e7-191">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="667e7-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="667e7-192">Název</span><span class="sxs-lookup"><span data-stu-id="667e7-192">Name</span></span>|<span data-ttu-id="667e7-193">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="667e7-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="667e7-194">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="667e7-194">.NET Console</span></span>|<span data-ttu-id="667e7-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="667e7-195">dotnetcli</span></span>|
|<span data-ttu-id="667e7-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="667e7-196">ASP.NET (C#)</span></span>|<span data-ttu-id="667e7-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="667e7-197">aspx-csharp</span></span>|
|<span data-ttu-id="667e7-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="667e7-198">ASP.NET (VB)</span></span>|<span data-ttu-id="667e7-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="667e7-199">aspx-vb</span></span>|
|<span data-ttu-id="667e7-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="667e7-200">AzCopy</span></span>|<span data-ttu-id="667e7-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="667e7-201">azcopy</span></span>|
|<span data-ttu-id="667e7-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="667e7-202">Azure CLI</span></span>|<span data-ttu-id="667e7-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="667e7-203">azurecli</span></span>|
|<span data-ttu-id="667e7-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="667e7-204">Azure PowerShell</span></span>|<span data-ttu-id="667e7-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="667e7-205">azurepowershell</span></span>|
|<span data-ttu-id="667e7-206">C++</span><span class="sxs-lookup"><span data-stu-id="667e7-206">C++</span></span>|<span data-ttu-id="667e7-207">cpp</span><span class="sxs-lookup"><span data-stu-id="667e7-207">cpp</span></span>|
|<span data-ttu-id="667e7-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="667e7-208">C++/CX</span></span>|<span data-ttu-id="667e7-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="667e7-209">cppcx</span></span>|
|<span data-ttu-id="667e7-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="667e7-210">C++/WinRT</span></span>|<span data-ttu-id="667e7-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="667e7-211">cppwinrt</span></span>|
|<span data-ttu-id="667e7-212">C#</span><span class="sxs-lookup"><span data-stu-id="667e7-212">C#</span></span>|<span data-ttu-id="667e7-213">csharp</span><span class="sxs-lookup"><span data-stu-id="667e7-213">csharp</span></span>|
|<span data-ttu-id="667e7-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="667e7-214">CSHTML</span></span>|<span data-ttu-id="667e7-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="667e7-215">cshtml</span></span>|
|<span data-ttu-id="667e7-216">DAX</span><span class="sxs-lookup"><span data-stu-id="667e7-216">DAX</span></span>|<span data-ttu-id="667e7-217">dax</span><span class="sxs-lookup"><span data-stu-id="667e7-217">dax</span></span>|
|<span data-ttu-id="667e7-218">F#</span><span class="sxs-lookup"><span data-stu-id="667e7-218">F#</span></span>|<span data-ttu-id="667e7-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="667e7-219">fsharp</span></span>|
|<span data-ttu-id="667e7-220">Go</span><span class="sxs-lookup"><span data-stu-id="667e7-220">Go</span></span>|<span data-ttu-id="667e7-221">go</span><span class="sxs-lookup"><span data-stu-id="667e7-221">go</span></span>|
|<span data-ttu-id="667e7-222">HTML</span><span class="sxs-lookup"><span data-stu-id="667e7-222">HTML</span></span>|<span data-ttu-id="667e7-223">html</span><span class="sxs-lookup"><span data-stu-id="667e7-223">html</span></span>|
|<span data-ttu-id="667e7-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="667e7-224">HTTP</span></span>|<span data-ttu-id="667e7-225">http</span><span class="sxs-lookup"><span data-stu-id="667e7-225">http</span></span>|
|<span data-ttu-id="667e7-226">Java</span><span class="sxs-lookup"><span data-stu-id="667e7-226">Java</span></span>|<span data-ttu-id="667e7-227">java</span><span class="sxs-lookup"><span data-stu-id="667e7-227">java</span></span>|
|<span data-ttu-id="667e7-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="667e7-228">JavaScript</span></span>|<span data-ttu-id="667e7-229">javascript</span><span class="sxs-lookup"><span data-stu-id="667e7-229">javascript</span></span>|
|<span data-ttu-id="667e7-230">JSON</span><span class="sxs-lookup"><span data-stu-id="667e7-230">JSON</span></span>|<span data-ttu-id="667e7-231">json</span><span class="sxs-lookup"><span data-stu-id="667e7-231">json</span></span>|
|<span data-ttu-id="667e7-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="667e7-232">Markdown</span></span>|<span data-ttu-id="667e7-233">md</span><span class="sxs-lookup"><span data-stu-id="667e7-233">md</span></span>|
|<span data-ttu-id="667e7-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="667e7-234">NodeJS</span></span>|<span data-ttu-id="667e7-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="667e7-235">nodejs</span></span>|
|<span data-ttu-id="667e7-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="667e7-236">Objective-C</span></span>|<span data-ttu-id="667e7-237">objc</span><span class="sxs-lookup"><span data-stu-id="667e7-237">objc</span></span>|
|<span data-ttu-id="667e7-238">OData</span><span class="sxs-lookup"><span data-stu-id="667e7-238">OData</span></span>|<span data-ttu-id="667e7-239">odata</span><span class="sxs-lookup"><span data-stu-id="667e7-239">odata</span></span>|
|<span data-ttu-id="667e7-240">PHP</span><span class="sxs-lookup"><span data-stu-id="667e7-240">PHP</span></span>|<span data-ttu-id="667e7-241">php</span><span class="sxs-lookup"><span data-stu-id="667e7-241">php</span></span>|
|<span data-ttu-id="667e7-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="667e7-242">Power Apps Formula</span></span>|<span data-ttu-id="667e7-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="667e7-243">powerappsfl</span></span>|
|<span data-ttu-id="667e7-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="667e7-244">PowerShell</span></span>|<span data-ttu-id="667e7-245">powershell</span><span class="sxs-lookup"><span data-stu-id="667e7-245">powershell</span></span>|
|<span data-ttu-id="667e7-246">Python</span><span class="sxs-lookup"><span data-stu-id="667e7-246">Python</span></span>|<span data-ttu-id="667e7-247">python</span><span class="sxs-lookup"><span data-stu-id="667e7-247">python</span></span>|
|<span data-ttu-id="667e7-248">Q#</span><span class="sxs-lookup"><span data-stu-id="667e7-248">Q#</span></span>|<span data-ttu-id="667e7-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="667e7-249">qsharp</span></span>|
|<span data-ttu-id="667e7-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="667e7-250">Ruby</span></span>|<span data-ttu-id="667e7-251">ruby</span><span class="sxs-lookup"><span data-stu-id="667e7-251">ruby</span></span>|
|<span data-ttu-id="667e7-252">SQL</span><span class="sxs-lookup"><span data-stu-id="667e7-252">SQL</span></span>|<span data-ttu-id="667e7-253">sql</span><span class="sxs-lookup"><span data-stu-id="667e7-253">sql</span></span>|
|<span data-ttu-id="667e7-254">Swift</span><span class="sxs-lookup"><span data-stu-id="667e7-254">Swift</span></span>|<span data-ttu-id="667e7-255">swift</span><span class="sxs-lookup"><span data-stu-id="667e7-255">swift</span></span>|
|<span data-ttu-id="667e7-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="667e7-256">TypeScript</span></span>|<span data-ttu-id="667e7-257">typescript</span><span class="sxs-lookup"><span data-stu-id="667e7-257">typescript</span></span>|
|<span data-ttu-id="667e7-258">VB</span><span class="sxs-lookup"><span data-stu-id="667e7-258">VB</span></span>|<span data-ttu-id="667e7-259">vb</span><span class="sxs-lookup"><span data-stu-id="667e7-259">vb</span></span>|
|<span data-ttu-id="667e7-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="667e7-260">VSTS CLI</span></span>|<span data-ttu-id="667e7-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="667e7-261">vstscli</span></span>|
|<span data-ttu-id="667e7-262">XAML</span><span class="sxs-lookup"><span data-stu-id="667e7-262">XAML</span></span>|<span data-ttu-id="667e7-263">xaml</span><span class="sxs-lookup"><span data-stu-id="667e7-263">xaml</span></span>|
|<span data-ttu-id="667e7-264">XML</span><span class="sxs-lookup"><span data-stu-id="667e7-264">XML</span></span>|<span data-ttu-id="667e7-265">xml</span><span class="sxs-lookup"><span data-stu-id="667e7-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="667e7-266">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="667e7-266">Example: C\#</span></span>

<span data-ttu-id="667e7-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="667e7-267">__Markdown__</span></span>

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

<span data-ttu-id="667e7-268">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="667e7-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="667e7-269">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="667e7-269">Example: SQL</span></span>

<span data-ttu-id="667e7-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="667e7-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="667e7-271">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="667e7-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="667e7-272">Vlastní rozšíření Markdownu od OPS</span><span class="sxs-lookup"><span data-stu-id="667e7-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="667e7-273">Platforma Open Publishing Services (OPS) implementuje analyzátor Markdig Parser pro Markdown, který je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="667e7-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="667e7-274">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="667e7-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="667e7-275">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="667e7-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="667e7-276">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="667e7-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="667e7-277">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="667e7-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="667e7-278">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="667e7-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="667e7-279">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="667e7-279">Note blocks</span></span>
- <span data-ttu-id="667e7-280">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="667e7-280">Includes</span></span>
- <span data-ttu-id="667e7-281">Voliče</span><span class="sxs-lookup"><span data-stu-id="667e7-281">Selectors</span></span>
- <span data-ttu-id="667e7-282">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="667e7-282">Embedded videos</span></span>
- <span data-ttu-id="667e7-283">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="667e7-283">Code snippets/samples</span></span>

<span data-ttu-id="667e7-284">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="667e7-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="667e7-285">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="667e7-285">Note blocks</span></span>

<span data-ttu-id="667e7-286">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="667e7-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="667e7-287">POZNÁMKA</span><span class="sxs-lookup"><span data-stu-id="667e7-287">NOTE</span></span>
- <span data-ttu-id="667e7-288">VAROVÁNÍ</span><span class="sxs-lookup"><span data-stu-id="667e7-288">WARNING</span></span>
- <span data-ttu-id="667e7-289">TIP</span><span class="sxs-lookup"><span data-stu-id="667e7-289">TIP</span></span>
- <span data-ttu-id="667e7-290">DŮLEŽITÉ</span><span class="sxs-lookup"><span data-stu-id="667e7-290">IMPORTANT</span></span>

<span data-ttu-id="667e7-291">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="667e7-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="667e7-292">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="667e7-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="667e7-293">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="667e7-293">Includes</span></span>

<span data-ttu-id="667e7-294">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="667e7-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="667e7-295">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="667e7-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="667e7-296">K dispozici jsou tři typy zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="667e7-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="667e7-297">Vložení: umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="667e7-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="667e7-298">Blok: umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="667e7-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="667e7-299">Obrázek: takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="667e7-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="667e7-300">Zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="667e7-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="667e7-301">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="667e7-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="667e7-302">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="667e7-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="667e7-303">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="667e7-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="667e7-304">Tady jsou požadavky a důležité informace týkající se zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="667e7-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="667e7-305">Zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="667e7-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="667e7-306">Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="667e7-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="667e7-307">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="667e7-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="667e7-308">Zahrnuté soubory se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="667e7-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="667e7-309">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="667e7-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="667e7-310">Dbejte na to, aby byl všechen text v zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="667e7-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="667e7-311">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="667e7-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="667e7-312">Nevkládejte zahrnutí do jiných zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="667e7-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="667e7-313">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="667e7-313">They are not supported.</span></span>
- <span data-ttu-id="667e7-314">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="667e7-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="667e7-315">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="667e7-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="667e7-316">Pokud zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="667e7-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="667e7-317">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="667e7-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="667e7-318">Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="667e7-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="667e7-319">Multimediální soubor uložte do složky multimédií spojené se zahrnutím.</span><span class="sxs-lookup"><span data-stu-id="667e7-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="667e7-320">Nepoužívejte zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="667e7-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="667e7-321">Zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="667e7-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="667e7-322">Voliče</span><span class="sxs-lookup"><span data-stu-id="667e7-322">Selectors</span></span>

<span data-ttu-id="667e7-323">Voliče používejte v technických článcích, když vytváříte více charakterů stejného článku, abyste vyřešili rozdíly v implementaci pro různé technologie nebo platformy.</span><span class="sxs-lookup"><span data-stu-id="667e7-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="667e7-324">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="667e7-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="667e7-325">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="667e7-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="667e7-326">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="667e7-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="667e7-327">Pak můžete na zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="667e7-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="667e7-328">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="667e7-328">Code snippets</span></span>

<span data-ttu-id="667e7-329">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="667e7-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="667e7-330">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="667e7-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="667e7-331">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="667e7-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="667e7-332">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="667e7-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="667e7-333">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="667e7-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="667e7-334">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="667e7-334">Alt text</span></span>

<span data-ttu-id="667e7-335">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="667e7-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="667e7-336">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="667e7-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="667e7-337">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="667e7-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="667e7-338">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="667e7-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="667e7-339">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="667e7-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="667e7-340">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="667e7-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="667e7-341">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="667e7-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="667e7-342">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="667e7-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="667e7-343">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="667e7-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="667e7-344">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="667e7-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="667e7-345">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="667e7-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="667e7-346">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="667e7-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="667e7-347">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="667e7-347">Angle brackets</span></span>

<span data-ttu-id="667e7-348">Pokud v textu (ne kódu) v souboru používáte ostré závorky, třeba k vyznačení zástupného symbolu, musíte pro ně použít kód.</span><span class="sxs-lookup"><span data-stu-id="667e7-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="667e7-349">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="667e7-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="667e7-350">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="667e7-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="667e7-351">Viz také</span><span class="sxs-lookup"><span data-stu-id="667e7-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="667e7-352">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="667e7-352">Markdown resources</span></span>

- [<span data-ttu-id="667e7-353">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="667e7-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="667e7-354">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="667e7-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="667e7-355">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="667e7-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
