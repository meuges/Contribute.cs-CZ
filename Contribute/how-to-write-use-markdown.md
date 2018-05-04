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
ms.openlocfilehash: 96d00abc052c3b23ca62201dccdbe590a927e72d
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="6cb0a-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="6cb0a-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="6cb0a-104">Články na docs.microsoft.com jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="6cb0a-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="6cb0a-106">Protože je obsah Docs uložený v GitHubu, může používat nadstavbu Markdownu zvanou [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), která poskytuje další funkce pro běžné potřeby formátování.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="6cb0a-107">Kromě toho platforma OPS (Open Publishing Services) implementuje rozšíření DFM (DocFX Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="6cb0a-107">Additionally, Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="6cb0a-108">DFM je s GFM (GitHub Flavored Markdown) vysoce kompatibilní a přidává možnosti podporující funkce specifické pro Docs.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="6cb0a-109">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="6cb0a-110">Nadpis</span><span class="sxs-lookup"><span data-stu-id="6cb0a-110">Headings</span></span>

<span data-ttu-id="6cb0a-111">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="6cb0a-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="6cb0a-112">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="6cb0a-112">Bold and italic text</span></span>

<span data-ttu-id="6cb0a-113">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-113">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="6cb0a-114">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-114">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="6cb0a-115">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-115">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="6cb0a-116">Seznamy</span><span class="sxs-lookup"><span data-stu-id="6cb0a-116">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="6cb0a-117">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="6cb0a-117">Unordered list</span></span>

<span data-ttu-id="6cb0a-118">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-118">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="6cb0a-119">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-119">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="6cb0a-120">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-120">will be rendered as:</span></span>

- <span data-ttu-id="6cb0a-121">List item 1</span><span class="sxs-lookup"><span data-stu-id="6cb0a-121">List item 1</span></span>
- <span data-ttu-id="6cb0a-122">List item 2</span><span class="sxs-lookup"><span data-stu-id="6cb0a-122">List item 2</span></span>
- <span data-ttu-id="6cb0a-123">List item 3</span><span class="sxs-lookup"><span data-stu-id="6cb0a-123">List item 3</span></span>

<span data-ttu-id="6cb0a-124">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-124">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="6cb0a-125">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-125">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="6cb0a-126">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-126">will be rendered as:</span></span>

- <span data-ttu-id="6cb0a-127">List item 1</span><span class="sxs-lookup"><span data-stu-id="6cb0a-127">List item 1</span></span>
  - <span data-ttu-id="6cb0a-128">List item A</span><span class="sxs-lookup"><span data-stu-id="6cb0a-128">List item A</span></span>
  - <span data-ttu-id="6cb0a-129">List item B</span><span class="sxs-lookup"><span data-stu-id="6cb0a-129">List item B</span></span>
- <span data-ttu-id="6cb0a-130">List item 2</span><span class="sxs-lookup"><span data-stu-id="6cb0a-130">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="6cb0a-131">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="6cb0a-131">Ordered list</span></span>

<span data-ttu-id="6cb0a-132">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-132">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="6cb0a-133">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-133">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="6cb0a-134">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-134">will be rendered as:</span></span>

1. <span data-ttu-id="6cb0a-135">First instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-135">First instruction</span></span>
2. <span data-ttu-id="6cb0a-136">Second instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-136">Second instruction</span></span>
3. <span data-ttu-id="6cb0a-137">Third instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-137">Third instruction</span></span>

<span data-ttu-id="6cb0a-138">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-138">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="6cb0a-139">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-139">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="6cb0a-140">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-140">will be rendered as:</span></span>

1. <span data-ttu-id="6cb0a-141">First instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-141">First instruction</span></span>
    1. <span data-ttu-id="6cb0a-142">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-142">Sub-instruction</span></span>
    2. <span data-ttu-id="6cb0a-143">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-143">Sub-instruction</span></span>
2. <span data-ttu-id="6cb0a-144">Second instruction</span><span class="sxs-lookup"><span data-stu-id="6cb0a-144">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="6cb0a-145">Tables</span><span class="sxs-lookup"><span data-stu-id="6cb0a-145">Tables</span></span>

<span data-ttu-id="6cb0a-146">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-146">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="6cb0a-147">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="6cb0a-147">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="6cb0a-148">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-148">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="6cb0a-149">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-149">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="6cb0a-150">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-150">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="6cb0a-151">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-151">will be rendered as:</span></span>

| <span data-ttu-id="6cb0a-152">Fun</span><span class="sxs-lookup"><span data-stu-id="6cb0a-152">Fun</span></span>                  | <span data-ttu-id="6cb0a-153">With</span><span class="sxs-lookup"><span data-stu-id="6cb0a-153">With</span></span>                 | <span data-ttu-id="6cb0a-154">Tables</span><span class="sxs-lookup"><span data-stu-id="6cb0a-154">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="6cb0a-155">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="6cb0a-155">left-aligned column</span></span>  | <span data-ttu-id="6cb0a-156">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="6cb0a-156">right-aligned column</span></span> | <span data-ttu-id="6cb0a-157">centered column</span><span class="sxs-lookup"><span data-stu-id="6cb0a-157">centered column</span></span> |
| <span data-ttu-id="6cb0a-158">$100</span><span class="sxs-lookup"><span data-stu-id="6cb0a-158">$100</span></span>                 | <span data-ttu-id="6cb0a-159">$100</span><span class="sxs-lookup"><span data-stu-id="6cb0a-159">$100</span></span>                 | <span data-ttu-id="6cb0a-160">$100</span><span class="sxs-lookup"><span data-stu-id="6cb0a-160">$100</span></span>            |
| <span data-ttu-id="6cb0a-161">$10</span><span class="sxs-lookup"><span data-stu-id="6cb0a-161">$10</span></span>                  | <span data-ttu-id="6cb0a-162">$10</span><span class="sxs-lookup"><span data-stu-id="6cb0a-162">$10</span></span>                  | <span data-ttu-id="6cb0a-163">$10</span><span class="sxs-lookup"><span data-stu-id="6cb0a-163">$10</span></span>             |
| <span data-ttu-id="6cb0a-164">$1</span><span class="sxs-lookup"><span data-stu-id="6cb0a-164">$1</span></span>                   | <span data-ttu-id="6cb0a-165">$1</span><span class="sxs-lookup"><span data-stu-id="6cb0a-165">$1</span></span>                   | <span data-ttu-id="6cb0a-166">$1</span><span class="sxs-lookup"><span data-stu-id="6cb0a-166">$1</span></span>              |

<span data-ttu-id="6cb0a-167">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-167">For more information on creating tables, see:</span></span>

- <span data-ttu-id="6cb0a-168">Funkce [zalamování tabulek](#table-wrapping) DFM, která může pomoct při formátování širokých tabulek</span><span class="sxs-lookup"><span data-stu-id="6cb0a-168">The DFM [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="6cb0a-169">[Organizování informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-169">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="6cb0a-170">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="6cb0a-170">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="6cb0a-171">Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda</span><span class="sxs-lookup"><span data-stu-id="6cb0a-171">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="6cb0a-172">Markdown Extra od Michela Fortina</span><span class="sxs-lookup"><span data-stu-id="6cb0a-172">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="6cb0a-173">Převedení HTML tabulek na Markdown</span><span class="sxs-lookup"><span data-stu-id="6cb0a-173">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="6cb0a-174">Odkazy</span><span class="sxs-lookup"><span data-stu-id="6cb0a-174">Links</span></span>

<span data-ttu-id="6cb0a-175">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-175">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="6cb0a-176">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-176">For more information on linking, see:</span></span>

- <span data-ttu-id="6cb0a-177">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="6cb0a-177">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="6cb0a-178">Podrobnosti o další syntaxi odkazů, kterou umožňuje DFM, najdete v sekci [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-178">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that DFM provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="6cb0a-179">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-179">Code snippets</span></span>

<span data-ttu-id="6cb0a-180">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-180">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="6cb0a-181">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-181">For details, see:</span></span>

- [<span data-ttu-id="6cb0a-182">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-182">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="6cb0a-183">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="6cb0a-183">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="6cb0a-184">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-184">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="6cb0a-185">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-185">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="6cb0a-186">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-186">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="6cb0a-187">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-187">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="6cb0a-188">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-188">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="6cb0a-189">Název</span><span class="sxs-lookup"><span data-stu-id="6cb0a-189">Name</span></span>|<span data-ttu-id="6cb0a-190">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-190">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="6cb0a-191">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="6cb0a-191">.NET Console</span></span>|<span data-ttu-id="6cb0a-192">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="6cb0a-192">dotnetcli</span></span>|
|<span data-ttu-id="6cb0a-193">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="6cb0a-193">ASP.NET (C#)</span></span>|<span data-ttu-id="6cb0a-194">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="6cb0a-194">aspx-csharp</span></span>|
|<span data-ttu-id="6cb0a-195">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="6cb0a-195">ASP.NET (VB)</span></span>|<span data-ttu-id="6cb0a-196">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="6cb0a-196">aspx-vb</span></span>|
|<span data-ttu-id="6cb0a-197">AzCopy</span><span class="sxs-lookup"><span data-stu-id="6cb0a-197">AzCopy</span></span>|<span data-ttu-id="6cb0a-198">azcopy</span><span class="sxs-lookup"><span data-stu-id="6cb0a-198">azcopy</span></span>|
|<span data-ttu-id="6cb0a-199">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="6cb0a-199">Azure CLI</span></span>|<span data-ttu-id="6cb0a-200">azurecli</span><span class="sxs-lookup"><span data-stu-id="6cb0a-200">azurecli</span></span>|
|<span data-ttu-id="6cb0a-201">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6cb0a-201">Azure PowerShell</span></span>|<span data-ttu-id="6cb0a-202">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="6cb0a-202">azurepowershell</span></span>|
|<span data-ttu-id="6cb0a-203">C++</span><span class="sxs-lookup"><span data-stu-id="6cb0a-203">C++</span></span>|<span data-ttu-id="6cb0a-204">cpp</span><span class="sxs-lookup"><span data-stu-id="6cb0a-204">cpp</span></span>|
|<span data-ttu-id="6cb0a-205">C++/CX</span><span class="sxs-lookup"><span data-stu-id="6cb0a-205">C++/CX</span></span>|<span data-ttu-id="6cb0a-206">cppcx</span><span class="sxs-lookup"><span data-stu-id="6cb0a-206">cppcx</span></span>|
|<span data-ttu-id="6cb0a-207">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="6cb0a-207">C++/WinRT</span></span>|<span data-ttu-id="6cb0a-208">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="6cb0a-208">cppwinrt</span></span>|
|<span data-ttu-id="6cb0a-209">C#</span><span class="sxs-lookup"><span data-stu-id="6cb0a-209">C#</span></span>|<span data-ttu-id="6cb0a-210">csharp</span><span class="sxs-lookup"><span data-stu-id="6cb0a-210">csharp</span></span>|
|<span data-ttu-id="6cb0a-211">CSHTML</span><span class="sxs-lookup"><span data-stu-id="6cb0a-211">CSHTML</span></span>|<span data-ttu-id="6cb0a-212">cshtml</span><span class="sxs-lookup"><span data-stu-id="6cb0a-212">cshtml</span></span>|
|<span data-ttu-id="6cb0a-213">DAX</span><span class="sxs-lookup"><span data-stu-id="6cb0a-213">DAX</span></span>|<span data-ttu-id="6cb0a-214">dax</span><span class="sxs-lookup"><span data-stu-id="6cb0a-214">dax</span></span>|
|<span data-ttu-id="6cb0a-215">F#</span><span class="sxs-lookup"><span data-stu-id="6cb0a-215">F#</span></span>|<span data-ttu-id="6cb0a-216">fsharp</span><span class="sxs-lookup"><span data-stu-id="6cb0a-216">fsharp</span></span>|
|<span data-ttu-id="6cb0a-217">Go</span><span class="sxs-lookup"><span data-stu-id="6cb0a-217">Go</span></span>|<span data-ttu-id="6cb0a-218">go</span><span class="sxs-lookup"><span data-stu-id="6cb0a-218">go</span></span>|
|<span data-ttu-id="6cb0a-219">HTML</span><span class="sxs-lookup"><span data-stu-id="6cb0a-219">HTML</span></span>|<span data-ttu-id="6cb0a-220">html</span><span class="sxs-lookup"><span data-stu-id="6cb0a-220">html</span></span>|
|<span data-ttu-id="6cb0a-221">HTTP</span><span class="sxs-lookup"><span data-stu-id="6cb0a-221">HTTP</span></span>|<span data-ttu-id="6cb0a-222">http</span><span class="sxs-lookup"><span data-stu-id="6cb0a-222">http</span></span>|
|<span data-ttu-id="6cb0a-223">Java</span><span class="sxs-lookup"><span data-stu-id="6cb0a-223">Java</span></span>|<span data-ttu-id="6cb0a-224">java</span><span class="sxs-lookup"><span data-stu-id="6cb0a-224">java</span></span>|
|<span data-ttu-id="6cb0a-225">JavaScript</span><span class="sxs-lookup"><span data-stu-id="6cb0a-225">JavaScript</span></span>|<span data-ttu-id="6cb0a-226">javascript</span><span class="sxs-lookup"><span data-stu-id="6cb0a-226">javascript</span></span>|
|<span data-ttu-id="6cb0a-227">JSON</span><span class="sxs-lookup"><span data-stu-id="6cb0a-227">JSON</span></span>|<span data-ttu-id="6cb0a-228">json</span><span class="sxs-lookup"><span data-stu-id="6cb0a-228">json</span></span>|
|<span data-ttu-id="6cb0a-229">Markdown</span><span class="sxs-lookup"><span data-stu-id="6cb0a-229">Markdown</span></span>|<span data-ttu-id="6cb0a-230">md</span><span class="sxs-lookup"><span data-stu-id="6cb0a-230">md</span></span>|
|<span data-ttu-id="6cb0a-231">NodeJS</span><span class="sxs-lookup"><span data-stu-id="6cb0a-231">NodeJS</span></span>|<span data-ttu-id="6cb0a-232">nodejs</span><span class="sxs-lookup"><span data-stu-id="6cb0a-232">nodejs</span></span>|
|<span data-ttu-id="6cb0a-233">Objective-C</span><span class="sxs-lookup"><span data-stu-id="6cb0a-233">Objective-C</span></span>|<span data-ttu-id="6cb0a-234">objc</span><span class="sxs-lookup"><span data-stu-id="6cb0a-234">objc</span></span>|
|<span data-ttu-id="6cb0a-235">OData</span><span class="sxs-lookup"><span data-stu-id="6cb0a-235">OData</span></span>|<span data-ttu-id="6cb0a-236">odata</span><span class="sxs-lookup"><span data-stu-id="6cb0a-236">odata</span></span>|
|<span data-ttu-id="6cb0a-237">PHP</span><span class="sxs-lookup"><span data-stu-id="6cb0a-237">PHP</span></span>|<span data-ttu-id="6cb0a-238">php</span><span class="sxs-lookup"><span data-stu-id="6cb0a-238">php</span></span>|
|<span data-ttu-id="6cb0a-239">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="6cb0a-239">Power Apps Formula</span></span>|<span data-ttu-id="6cb0a-240">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="6cb0a-240">powerappsfl</span></span>|
|<span data-ttu-id="6cb0a-241">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6cb0a-241">PowerShell</span></span>|<span data-ttu-id="6cb0a-242">powershell</span><span class="sxs-lookup"><span data-stu-id="6cb0a-242">powershell</span></span>|
|<span data-ttu-id="6cb0a-243">Python</span><span class="sxs-lookup"><span data-stu-id="6cb0a-243">Python</span></span>|<span data-ttu-id="6cb0a-244">python</span><span class="sxs-lookup"><span data-stu-id="6cb0a-244">python</span></span>|
|<span data-ttu-id="6cb0a-245">Q#</span><span class="sxs-lookup"><span data-stu-id="6cb0a-245">Q#</span></span>|<span data-ttu-id="6cb0a-246">qsharp</span><span class="sxs-lookup"><span data-stu-id="6cb0a-246">qsharp</span></span>|
|<span data-ttu-id="6cb0a-247">Ruby</span><span class="sxs-lookup"><span data-stu-id="6cb0a-247">Ruby</span></span>|<span data-ttu-id="6cb0a-248">ruby</span><span class="sxs-lookup"><span data-stu-id="6cb0a-248">ruby</span></span>|
|<span data-ttu-id="6cb0a-249">SQL</span><span class="sxs-lookup"><span data-stu-id="6cb0a-249">SQL</span></span>|<span data-ttu-id="6cb0a-250">sql</span><span class="sxs-lookup"><span data-stu-id="6cb0a-250">sql</span></span>|
|<span data-ttu-id="6cb0a-251">Swift</span><span class="sxs-lookup"><span data-stu-id="6cb0a-251">Swift</span></span>|<span data-ttu-id="6cb0a-252">swift</span><span class="sxs-lookup"><span data-stu-id="6cb0a-252">swift</span></span>|
|<span data-ttu-id="6cb0a-253">TypeScript</span><span class="sxs-lookup"><span data-stu-id="6cb0a-253">TypeScript</span></span>|<span data-ttu-id="6cb0a-254">typescript</span><span class="sxs-lookup"><span data-stu-id="6cb0a-254">typescript</span></span>|
|<span data-ttu-id="6cb0a-255">VB</span><span class="sxs-lookup"><span data-stu-id="6cb0a-255">VB</span></span>|<span data-ttu-id="6cb0a-256">vb</span><span class="sxs-lookup"><span data-stu-id="6cb0a-256">vb</span></span>|
|<span data-ttu-id="6cb0a-257">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="6cb0a-257">VSTS CLI</span></span>|<span data-ttu-id="6cb0a-258">vstscli</span><span class="sxs-lookup"><span data-stu-id="6cb0a-258">vstscli</span></span>|
|<span data-ttu-id="6cb0a-259">XAML</span><span class="sxs-lookup"><span data-stu-id="6cb0a-259">XAML</span></span>|<span data-ttu-id="6cb0a-260">xaml</span><span class="sxs-lookup"><span data-stu-id="6cb0a-260">xaml</span></span>|
|<span data-ttu-id="6cb0a-261">XML</span><span class="sxs-lookup"><span data-stu-id="6cb0a-261">XML</span></span>|<span data-ttu-id="6cb0a-262">xml</span><span class="sxs-lookup"><span data-stu-id="6cb0a-262">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="6cb0a-263">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="6cb0a-263">Example: C\#</span></span>

<span data-ttu-id="6cb0a-264">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="6cb0a-264">__Markdown__</span></span>

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

<span data-ttu-id="6cb0a-265">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="6cb0a-265">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="6cb0a-266">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="6cb0a-266">Example: SQL</span></span>

<span data-ttu-id="6cb0a-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="6cb0a-267">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="6cb0a-268">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="6cb0a-268">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="6cb0a-269">Vlastní rozšíření Markdownu od OPS</span><span class="sxs-lookup"><span data-stu-id="6cb0a-269">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="6cb0a-270">Platforma OPS (Open Publishing Services) implementuje rozšíření DFM (DocFX Flavored Markdown), které je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="6cb0a-270">Open Publishing Services (OPS) implements DocFX Flavored Markdown (DFM), which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="6cb0a-271">Rozšíření DFM přidává prostřednictvím rozšíření Markdownu další funkce.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-271">DFM adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="6cb0a-272">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-272">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="6cb0a-273">(Podívejte se třeba na„Rozšíření DFM a Markdownu“ a „Fragmenty kódu“ v obsahu.)</span><span class="sxs-lookup"><span data-stu-id="6cb0a-273">(For example, see "DFM and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="6cb0a-274">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-274">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="6cb0a-275">Na bohatší formátování používají články funkce DFM jako:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-275">For richer formatting, articles can use DFM features such as:</span></span>

- <span data-ttu-id="6cb0a-276">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="6cb0a-276">Note blocks</span></span>
- <span data-ttu-id="6cb0a-277">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="6cb0a-277">Includes</span></span>
- <span data-ttu-id="6cb0a-278">Voliče</span><span class="sxs-lookup"><span data-stu-id="6cb0a-278">Selectors</span></span>
- <span data-ttu-id="6cb0a-279">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="6cb0a-279">Embedded videos</span></span>
- <span data-ttu-id="6cb0a-280">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-280">Code snippets/samples</span></span>

<span data-ttu-id="6cb0a-281">Kompletní seznam najdete v částech „Rozšíření DFM a Markdownu“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-281">For the complete list, refer to "DFM and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="6cb0a-282">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="6cb0a-282">Note blocks</span></span>

<span data-ttu-id="6cb0a-283">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-283">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="6cb0a-284">POZNÁMKA</span><span class="sxs-lookup"><span data-stu-id="6cb0a-284">NOTE</span></span>
- <span data-ttu-id="6cb0a-285">VAROVÁNÍ</span><span class="sxs-lookup"><span data-stu-id="6cb0a-285">WARNING</span></span>
- <span data-ttu-id="6cb0a-286">TIP</span><span class="sxs-lookup"><span data-stu-id="6cb0a-286">TIP</span></span>
- <span data-ttu-id="6cb0a-287">DŮLEŽITÉ</span><span class="sxs-lookup"><span data-stu-id="6cb0a-287">IMPORTANT</span></span>

<span data-ttu-id="6cb0a-288">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-288">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="6cb0a-289">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-289">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="6cb0a-290">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="6cb0a-290">Includes</span></span>

<span data-ttu-id="6cb0a-291">Když máte opakovaně použitelný text nebo soubory obrázků, které je potřeba zahrnout do souborů článků, můžete použít odkaz na soubor „zahrnutí“ prostřednictvím funkce DFM k zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-291">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the DFM file include feature.</span></span> <span data-ttu-id="6cb0a-292">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-292">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="6cb0a-293">K dispozici jsou tři typy zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-293">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="6cb0a-294">Vložení: umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-294">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="6cb0a-295">Blok: umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-295">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="6cb0a-296">Obrázek: takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-296">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="6cb0a-297">Zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="6cb0a-297">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="6cb0a-298">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-298">It can contain any valid Markdown.</span></span> <span data-ttu-id="6cb0a-299">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-299">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="6cb0a-300">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-300">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="6cb0a-301">Tady jsou požadavky a důležité informace týkající se zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-301">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="6cb0a-302">Zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-302">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="6cb0a-303">Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-303">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="6cb0a-304">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-304">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="6cb0a-305">Zahrnutí se nevykreslí v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních DFM.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-305">Includes won't be rendered in the GitHub rendered view of your article, because they rely on DFM extensions.</span></span> <span data-ttu-id="6cb0a-306">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-306">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="6cb0a-307">Dbejte na to, aby byl všechen text v zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-307">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="6cb0a-308">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-308">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="6cb0a-309">Nevkládejte zahrnutí do jiných zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-309">Don't embed includes within other includes.</span></span> <span data-ttu-id="6cb0a-310">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-310">They are not supported.</span></span>
- <span data-ttu-id="6cb0a-311">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-311">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="6cb0a-312">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-312">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="6cb0a-313">Pokud zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-313">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="6cb0a-314">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-314">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="6cb0a-315">Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-315">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="6cb0a-316">Multimediální soubor uložte do složky multimédií spojené se zahrnutím.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-316">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="6cb0a-317">Nepoužívejte zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-317">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="6cb0a-318">Zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-318">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="6cb0a-319">Voliče</span><span class="sxs-lookup"><span data-stu-id="6cb0a-319">Selectors</span></span>

<span data-ttu-id="6cb0a-320">Voliče používejte v technických článcích, když vytváříte více charakterů stejného článku, abyste vyřešili rozdíly v implementaci pro různé technologie nebo platformy.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-320">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="6cb0a-321">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-321">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="6cb0a-322">V DFM jsou v současnosti dva různé typy voličů – jednoduchý a vícenásobný volič.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-322">There are currently two different types of selectors in DFM, a single selector and a multi-selector.</span></span>

<span data-ttu-id="6cb0a-323">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-323">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="6cb0a-324">Pak můžete na zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-324">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="6cb0a-325">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-325">Code snippets</span></span>

<span data-ttu-id="6cb0a-326">DFM podporuje zahrnutí kódu do článku prostřednictvím svého rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-326">DFM supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="6cb0a-327">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-327">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="6cb0a-328">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="6cb0a-328">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="6cb0a-329">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="6cb0a-329">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="6cb0a-330">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="6cb0a-330">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="6cb0a-331">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="6cb0a-331">Alt text</span></span>

<span data-ttu-id="6cb0a-332">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-332">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="6cb0a-333">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-333">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="6cb0a-334">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-334">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="6cb0a-335">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="6cb0a-335">Apostrophes and quotation marks</span></span>

<span data-ttu-id="6cb0a-336">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-336">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="6cb0a-337">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-337">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="6cb0a-338">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="6cb0a-338">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="6cb0a-339">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="6cb0a-339">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="6cb0a-340">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="6cb0a-340">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="6cb0a-341">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="6cb0a-341">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="6cb0a-342">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="6cb0a-342">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="6cb0a-343">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="6cb0a-343">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="6cb0a-344">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="6cb0a-344">Angle brackets</span></span>

<span data-ttu-id="6cb0a-345">Pokud v textu (ne kódu) v souboru používáte ostré závorky, třeba k vyznačení zástupného symbolu, musíte pro ně použít kód.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-345">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="6cb0a-346">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="6cb0a-346">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="6cb0a-347">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="6cb0a-347">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="6cb0a-348">Viz také</span><span class="sxs-lookup"><span data-stu-id="6cb0a-348">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="6cb0a-349">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="6cb0a-349">Markdown resources</span></span>

- [<span data-ttu-id="6cb0a-350">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-350">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="6cb0a-351">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="6cb0a-351">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="6cb0a-352">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="6cb0a-352">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
