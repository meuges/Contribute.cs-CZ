---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.date: 01/29/2019
ms.openlocfilehash: 5235189d11c8c20ac20c91572d8bafcf525fb7c0
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887291"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="86ed4-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="86ed4-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="86ed4-104">Články na [docs.microsoft.com](http://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="86ed4-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="86ed4-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="86ed4-106">Back-end webu docs.microsoft.com používá platformu OPS (Open Publishing Services), která podporuje markdown parsovaný prostřednictvím [Markdigu](https://github.com/lunet-io/markdig) a splňující standard [CommonMark](https://commonmark.org/) a která podporuje také [DFM (DocFX Flavored Markdown)](https://dotnet.github.io/docfx/).</span><span class="sxs-lookup"><span data-stu-id="86ed4-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="86ed4-107">Tyto varianty markdownu jsou z větší části kompatibilní s [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu a může tam být upravovaná.</span><span class="sxs-lookup"><span data-stu-id="86ed4-107">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="86ed4-108">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-108">Additional functionality is added through Markdown extensions.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="86ed4-109">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="86ed4-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="86ed4-110">Nadpis</span><span class="sxs-lookup"><span data-stu-id="86ed4-110">Headings</span></span>

<span data-ttu-id="86ed4-111">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="86ed4-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="86ed4-112">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="86ed4-112">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="86ed4-113">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="86ed4-113">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="86ed4-114">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-114">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="86ed4-115">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="86ed4-115">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="86ed4-116">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="86ed4-116">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="86ed4-117">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-117">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="86ed4-118">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="86ed4-118">Bold and italic text</span></span>

<span data-ttu-id="86ed4-119">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="86ed4-119">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="86ed4-120">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="86ed4-120">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="86ed4-121">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="86ed4-121">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="86ed4-122">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="86ed4-122">Blockquotes</span></span>

<span data-ttu-id="86ed4-123">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="86ed4-123">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="86ed4-124">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-124">The preceding example renders as follows:</span></span>

> <span data-ttu-id="86ed4-125">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="86ed4-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="86ed4-126">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="86ed4-127">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="86ed4-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="86ed4-128">Seznamy</span><span class="sxs-lookup"><span data-stu-id="86ed4-128">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="86ed4-129">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="86ed4-129">Unordered list</span></span>

<span data-ttu-id="86ed4-130">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-130">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="86ed4-131">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="86ed4-131">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="86ed4-132">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-132">will be rendered as:</span></span>

- <span data-ttu-id="86ed4-133">List item 1</span><span class="sxs-lookup"><span data-stu-id="86ed4-133">List item 1</span></span>
- <span data-ttu-id="86ed4-134">List item 2</span><span class="sxs-lookup"><span data-stu-id="86ed4-134">List item 2</span></span>
- <span data-ttu-id="86ed4-135">List item 3</span><span class="sxs-lookup"><span data-stu-id="86ed4-135">List item 3</span></span>

<span data-ttu-id="86ed4-136">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="86ed4-136">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="86ed4-137">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="86ed4-137">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="86ed4-138">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-138">will be rendered as:</span></span>

- <span data-ttu-id="86ed4-139">List item 1</span><span class="sxs-lookup"><span data-stu-id="86ed4-139">List item 1</span></span>
  - <span data-ttu-id="86ed4-140">List item A</span><span class="sxs-lookup"><span data-stu-id="86ed4-140">List item A</span></span>
  - <span data-ttu-id="86ed4-141">List item B</span><span class="sxs-lookup"><span data-stu-id="86ed4-141">List item B</span></span>
- <span data-ttu-id="86ed4-142">List item 2</span><span class="sxs-lookup"><span data-stu-id="86ed4-142">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="86ed4-143">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="86ed4-143">Ordered list</span></span>

<span data-ttu-id="86ed4-144">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="86ed4-144">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="86ed4-145">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="86ed4-145">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="86ed4-146">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-146">will be rendered as:</span></span>

1. <span data-ttu-id="86ed4-147">First instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-147">First instruction</span></span>
2. <span data-ttu-id="86ed4-148">Second instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-148">Second instruction</span></span>
3. <span data-ttu-id="86ed4-149">Third instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-149">Third instruction</span></span>

<span data-ttu-id="86ed4-150">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="86ed4-150">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="86ed4-151">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="86ed4-151">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="86ed4-152">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-152">will be rendered as:</span></span>

1. <span data-ttu-id="86ed4-153">First instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-153">First instruction</span></span>
   1. <span data-ttu-id="86ed4-154">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-154">Sub-instruction</span></span>
   2. <span data-ttu-id="86ed4-155">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-155">Sub-instruction</span></span>
2. <span data-ttu-id="86ed4-156">Second instruction</span><span class="sxs-lookup"><span data-stu-id="86ed4-156">Second instruction</span></span>

<span data-ttu-id="86ed4-157">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="86ed4-157">Note that we use '1.'</span></span> <span data-ttu-id="86ed4-158">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-158">for all entries.</span></span> <span data-ttu-id="86ed4-159">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-159">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="86ed4-160">Tables</span><span class="sxs-lookup"><span data-stu-id="86ed4-160">Tables</span></span>

<span data-ttu-id="86ed4-161">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="86ed4-161">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="86ed4-162">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="86ed4-162">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="86ed4-163">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="86ed4-163">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="86ed4-164">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="86ed4-164">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="86ed4-165">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="86ed4-165">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="86ed4-166">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-166">will be rendered as:</span></span>

| <span data-ttu-id="86ed4-167">Fun</span><span class="sxs-lookup"><span data-stu-id="86ed4-167">Fun</span></span>                  | <span data-ttu-id="86ed4-168">With</span><span class="sxs-lookup"><span data-stu-id="86ed4-168">With</span></span>                 | <span data-ttu-id="86ed4-169">Tables</span><span class="sxs-lookup"><span data-stu-id="86ed4-169">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="86ed4-170">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="86ed4-170">left-aligned column</span></span>  | <span data-ttu-id="86ed4-171">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="86ed4-171">right-aligned column</span></span> | <span data-ttu-id="86ed4-172">centered column</span><span class="sxs-lookup"><span data-stu-id="86ed4-172">centered column</span></span> |
| <span data-ttu-id="86ed4-173">$100</span><span class="sxs-lookup"><span data-stu-id="86ed4-173">$100</span></span>                 | <span data-ttu-id="86ed4-174">$100</span><span class="sxs-lookup"><span data-stu-id="86ed4-174">$100</span></span>                 | <span data-ttu-id="86ed4-175">$100</span><span class="sxs-lookup"><span data-stu-id="86ed4-175">$100</span></span>            |
| <span data-ttu-id="86ed4-176">$10</span><span class="sxs-lookup"><span data-stu-id="86ed4-176">$10</span></span>                  | <span data-ttu-id="86ed4-177">$10</span><span class="sxs-lookup"><span data-stu-id="86ed4-177">$10</span></span>                  | <span data-ttu-id="86ed4-178">$10</span><span class="sxs-lookup"><span data-stu-id="86ed4-178">$10</span></span>             |
| <span data-ttu-id="86ed4-179">$1</span><span class="sxs-lookup"><span data-stu-id="86ed4-179">$1</span></span>                   | <span data-ttu-id="86ed4-180">$1</span><span class="sxs-lookup"><span data-stu-id="86ed4-180">$1</span></span>                   | <span data-ttu-id="86ed4-181">$1</span><span class="sxs-lookup"><span data-stu-id="86ed4-181">$1</span></span>              |

<span data-ttu-id="86ed4-182">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="86ed4-182">For more information on creating tables, see:</span></span>

- <span data-ttu-id="86ed4-183">[Funkce zalamování tabulek](#table-wrapping) v Markdigu určená k formátování širokých tabulek</span><span class="sxs-lookup"><span data-stu-id="86ed4-183">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="86ed4-184">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="86ed4-184">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="86ed4-185">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="86ed4-185">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="86ed4-186">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="86ed4-186">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="86ed4-187">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="86ed4-187">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="86ed4-188">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="86ed4-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="86ed4-189">Odkazy</span><span class="sxs-lookup"><span data-stu-id="86ed4-189">Links</span></span>

<span data-ttu-id="86ed4-190">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="86ed4-190">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="86ed4-191">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="86ed4-191">For more information on linking, see:</span></span>

- <span data-ttu-id="86ed4-192">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="86ed4-192">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="86ed4-193">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="86ed4-193">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="86ed4-194">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="86ed4-194">Code snippets</span></span>

<span data-ttu-id="86ed4-195">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="86ed4-195">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="86ed4-196">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="86ed4-196">For details, see:</span></span>

- [<span data-ttu-id="86ed4-197">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="86ed4-197">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="86ed4-198">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="86ed4-198">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="86ed4-199">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-199">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="86ed4-200">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="86ed4-200">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="86ed4-201">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="86ed4-201">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="86ed4-202">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:</span><span class="sxs-lookup"><span data-stu-id="86ed4-202">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="86ed4-203">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="86ed4-203">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="86ed4-204">Název</span><span class="sxs-lookup"><span data-stu-id="86ed4-204">Name</span></span>|<span data-ttu-id="86ed4-205">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="86ed4-205">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="86ed4-206">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="86ed4-206">.NET Console</span></span>|<span data-ttu-id="86ed4-207">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="86ed4-207">dotnetcli</span></span>|
|<span data-ttu-id="86ed4-208">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="86ed4-208">ASP.NET (C#)</span></span>|<span data-ttu-id="86ed4-209">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="86ed4-209">aspx-csharp</span></span>|
|<span data-ttu-id="86ed4-210">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="86ed4-210">ASP.NET (VB)</span></span>|<span data-ttu-id="86ed4-211">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="86ed4-211">aspx-vb</span></span>|
|<span data-ttu-id="86ed4-212">AzCopy</span><span class="sxs-lookup"><span data-stu-id="86ed4-212">AzCopy</span></span>|<span data-ttu-id="86ed4-213">azcopy</span><span class="sxs-lookup"><span data-stu-id="86ed4-213">azcopy</span></span>|
|<span data-ttu-id="86ed4-214">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="86ed4-214">Azure CLI</span></span>|<span data-ttu-id="86ed4-215">azurecli</span><span class="sxs-lookup"><span data-stu-id="86ed4-215">azurecli</span></span>|
|<span data-ttu-id="86ed4-216">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="86ed4-216">Azure PowerShell</span></span>|<span data-ttu-id="86ed4-217">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="86ed4-217">azurepowershell</span></span>|
|<span data-ttu-id="86ed4-218">C++</span><span class="sxs-lookup"><span data-stu-id="86ed4-218">C++</span></span>|<span data-ttu-id="86ed4-219">cpp</span><span class="sxs-lookup"><span data-stu-id="86ed4-219">cpp</span></span>|
|<span data-ttu-id="86ed4-220">C++/CX</span><span class="sxs-lookup"><span data-stu-id="86ed4-220">C++/CX</span></span>|<span data-ttu-id="86ed4-221">cppcx</span><span class="sxs-lookup"><span data-stu-id="86ed4-221">cppcx</span></span>|
|<span data-ttu-id="86ed4-222">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="86ed4-222">C++/WinRT</span></span>|<span data-ttu-id="86ed4-223">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="86ed4-223">cppwinrt</span></span>|
|<span data-ttu-id="86ed4-224">C#</span><span class="sxs-lookup"><span data-stu-id="86ed4-224">C#</span></span>|<span data-ttu-id="86ed4-225">csharp</span><span class="sxs-lookup"><span data-stu-id="86ed4-225">csharp</span></span>|
|<span data-ttu-id="86ed4-226">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="86ed4-226">C# in browser</span></span>|<span data-ttu-id="86ed4-227">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="86ed4-227">csharp-interactive</span></span>|
|<span data-ttu-id="86ed4-228">Konzola</span><span class="sxs-lookup"><span data-stu-id="86ed4-228">Console</span></span>|<span data-ttu-id="86ed4-229">konzola</span><span class="sxs-lookup"><span data-stu-id="86ed4-229">console</span></span>|
|<span data-ttu-id="86ed4-230">CSHTML</span><span class="sxs-lookup"><span data-stu-id="86ed4-230">CSHTML</span></span>|<span data-ttu-id="86ed4-231">cshtml</span><span class="sxs-lookup"><span data-stu-id="86ed4-231">cshtml</span></span>|
|<span data-ttu-id="86ed4-232">DAX</span><span class="sxs-lookup"><span data-stu-id="86ed4-232">DAX</span></span>|<span data-ttu-id="86ed4-233">dax</span><span class="sxs-lookup"><span data-stu-id="86ed4-233">dax</span></span>|
|<span data-ttu-id="86ed4-234">Docker</span><span class="sxs-lookup"><span data-stu-id="86ed4-234">Docker</span></span>|<span data-ttu-id="86ed4-235">dockerfile</span><span class="sxs-lookup"><span data-stu-id="86ed4-235">dockerfile</span></span>|
|<span data-ttu-id="86ed4-236">F#</span><span class="sxs-lookup"><span data-stu-id="86ed4-236">F#</span></span>|<span data-ttu-id="86ed4-237">fsharp</span><span class="sxs-lookup"><span data-stu-id="86ed4-237">fsharp</span></span>|
|<span data-ttu-id="86ed4-238">Go</span><span class="sxs-lookup"><span data-stu-id="86ed4-238">Go</span></span>|<span data-ttu-id="86ed4-239">go</span><span class="sxs-lookup"><span data-stu-id="86ed4-239">go</span></span>|
|<span data-ttu-id="86ed4-240">HTML</span><span class="sxs-lookup"><span data-stu-id="86ed4-240">HTML</span></span>|<span data-ttu-id="86ed4-241">html</span><span class="sxs-lookup"><span data-stu-id="86ed4-241">html</span></span>|
|<span data-ttu-id="86ed4-242">HTTP</span><span class="sxs-lookup"><span data-stu-id="86ed4-242">HTTP</span></span>|<span data-ttu-id="86ed4-243">http</span><span class="sxs-lookup"><span data-stu-id="86ed4-243">http</span></span>|
|<span data-ttu-id="86ed4-244">Java</span><span class="sxs-lookup"><span data-stu-id="86ed4-244">Java</span></span>|<span data-ttu-id="86ed4-245">java</span><span class="sxs-lookup"><span data-stu-id="86ed4-245">java</span></span>|
|<span data-ttu-id="86ed4-246">JavaScript</span><span class="sxs-lookup"><span data-stu-id="86ed4-246">JavaScript</span></span>|<span data-ttu-id="86ed4-247">javascript</span><span class="sxs-lookup"><span data-stu-id="86ed4-247">javascript</span></span>|
|<span data-ttu-id="86ed4-248">JSON</span><span class="sxs-lookup"><span data-stu-id="86ed4-248">JSON</span></span>|<span data-ttu-id="86ed4-249">json</span><span class="sxs-lookup"><span data-stu-id="86ed4-249">json</span></span>|
|<span data-ttu-id="86ed4-250">Dotazovací jazyk Kusto</span><span class="sxs-lookup"><span data-stu-id="86ed4-250">Kusto Query Language</span></span>|<span data-ttu-id="86ed4-251">kusto</span><span class="sxs-lookup"><span data-stu-id="86ed4-251">kusto</span></span>|
|<span data-ttu-id="86ed4-252">Markdown</span><span class="sxs-lookup"><span data-stu-id="86ed4-252">Markdown</span></span>|<span data-ttu-id="86ed4-253">md</span><span class="sxs-lookup"><span data-stu-id="86ed4-253">md</span></span>|
|<span data-ttu-id="86ed4-254">Objective-C</span><span class="sxs-lookup"><span data-stu-id="86ed4-254">Objective-C</span></span>|<span data-ttu-id="86ed4-255">objc</span><span class="sxs-lookup"><span data-stu-id="86ed4-255">objc</span></span>|
|<span data-ttu-id="86ed4-256">OData</span><span class="sxs-lookup"><span data-stu-id="86ed4-256">OData</span></span>|<span data-ttu-id="86ed4-257">odata</span><span class="sxs-lookup"><span data-stu-id="86ed4-257">odata</span></span>|
|<span data-ttu-id="86ed4-258">PHP</span><span class="sxs-lookup"><span data-stu-id="86ed4-258">PHP</span></span>|<span data-ttu-id="86ed4-259">php</span><span class="sxs-lookup"><span data-stu-id="86ed4-259">php</span></span>|
|<span data-ttu-id="86ed4-260">PowerApps (oddělovač desetinných míst v podobě tečky)</span><span class="sxs-lookup"><span data-stu-id="86ed4-260">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="86ed4-261">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="86ed4-261">powerapps-dot</span></span>|
|<span data-ttu-id="86ed4-262">PowerApps (oddělovač desetinných míst v podobě čárky)</span><span class="sxs-lookup"><span data-stu-id="86ed4-262">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="86ed4-263">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="86ed4-263">powerapps-comma</span></span>|
|<span data-ttu-id="86ed4-264">PowerShell</span><span class="sxs-lookup"><span data-stu-id="86ed4-264">PowerShell</span></span>|<span data-ttu-id="86ed4-265">powershell</span><span class="sxs-lookup"><span data-stu-id="86ed4-265">powershell</span></span>|
|<span data-ttu-id="86ed4-266">Python</span><span class="sxs-lookup"><span data-stu-id="86ed4-266">Python</span></span>|<span data-ttu-id="86ed4-267">python</span><span class="sxs-lookup"><span data-stu-id="86ed4-267">python</span></span>|
|<span data-ttu-id="86ed4-268">Q#</span><span class="sxs-lookup"><span data-stu-id="86ed4-268">Q#</span></span>|<span data-ttu-id="86ed4-269">qsharp</span><span class="sxs-lookup"><span data-stu-id="86ed4-269">qsharp</span></span>|
|<span data-ttu-id="86ed4-270">R</span><span class="sxs-lookup"><span data-stu-id="86ed4-270">R</span></span>|<span data-ttu-id="86ed4-271">r</span><span class="sxs-lookup"><span data-stu-id="86ed4-271">r</span></span>|
|<span data-ttu-id="86ed4-272">Ruby</span><span class="sxs-lookup"><span data-stu-id="86ed4-272">Ruby</span></span>|<span data-ttu-id="86ed4-273">ruby</span><span class="sxs-lookup"><span data-stu-id="86ed4-273">ruby</span></span>|
|<span data-ttu-id="86ed4-274">SQL</span><span class="sxs-lookup"><span data-stu-id="86ed4-274">SQL</span></span>|<span data-ttu-id="86ed4-275">sql</span><span class="sxs-lookup"><span data-stu-id="86ed4-275">sql</span></span>|
|<span data-ttu-id="86ed4-276">Swift</span><span class="sxs-lookup"><span data-stu-id="86ed4-276">Swift</span></span>|<span data-ttu-id="86ed4-277">swift</span><span class="sxs-lookup"><span data-stu-id="86ed4-277">swift</span></span>|
|<span data-ttu-id="86ed4-278">TypeScript</span><span class="sxs-lookup"><span data-stu-id="86ed4-278">TypeScript</span></span>|<span data-ttu-id="86ed4-279">typescript</span><span class="sxs-lookup"><span data-stu-id="86ed4-279">typescript</span></span>|
|<span data-ttu-id="86ed4-280">VB</span><span class="sxs-lookup"><span data-stu-id="86ed4-280">VB</span></span>|<span data-ttu-id="86ed4-281">vb</span><span class="sxs-lookup"><span data-stu-id="86ed4-281">vb</span></span>|
|<span data-ttu-id="86ed4-282">XAML</span><span class="sxs-lookup"><span data-stu-id="86ed4-282">XAML</span></span>|<span data-ttu-id="86ed4-283">xaml</span><span class="sxs-lookup"><span data-stu-id="86ed4-283">xaml</span></span>|
|<span data-ttu-id="86ed4-284">XML</span><span class="sxs-lookup"><span data-stu-id="86ed4-284">XML</span></span>|<span data-ttu-id="86ed4-285">xml</span><span class="sxs-lookup"><span data-stu-id="86ed4-285">xml</span></span>|

<span data-ttu-id="86ed4-286">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="86ed4-286">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="86ed4-287">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="86ed4-287">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="86ed4-288">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="86ed4-288">Example: C\#</span></span>

<span data-ttu-id="86ed4-289">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="86ed4-289">__Markdown__</span></span>

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

<span data-ttu-id="86ed4-290">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="86ed4-290">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="86ed4-291">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="86ed4-291">Example: SQL</span></span>

<span data-ttu-id="86ed4-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="86ed4-292">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="86ed4-293">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="86ed4-293">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="86ed4-294">Vlastní rozšíření Markdownu od OPS</span><span class="sxs-lookup"><span data-stu-id="86ed4-294">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="86ed4-295">Platforma Open Publishing Services (OPS) implementuje analyzátor Markdig Parser pro Markdown, který je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="86ed4-295">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="86ed4-296">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="86ed4-296">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="86ed4-297">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="86ed4-297">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="86ed4-298">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="86ed4-298">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="86ed4-299">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="86ed4-299">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="86ed4-300">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="86ed4-300">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="86ed4-301">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="86ed4-301">Note blocks</span></span>
- <span data-ttu-id="86ed4-302">Vložené soubory</span><span class="sxs-lookup"><span data-stu-id="86ed4-302">Include files</span></span>
- <span data-ttu-id="86ed4-303">Voliče</span><span class="sxs-lookup"><span data-stu-id="86ed4-303">Selectors</span></span>
- <span data-ttu-id="86ed4-304">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="86ed4-304">Embedded videos</span></span>
- <span data-ttu-id="86ed4-305">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="86ed4-305">Code snippets/samples</span></span>

<span data-ttu-id="86ed4-306">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-306">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="86ed4-307">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="86ed4-307">Note blocks</span></span>

<span data-ttu-id="86ed4-308">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="86ed4-308">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="86ed4-309">POZNÁMKA</span><span class="sxs-lookup"><span data-stu-id="86ed4-309">NOTE</span></span>
- <span data-ttu-id="86ed4-310">VAROVÁNÍ</span><span class="sxs-lookup"><span data-stu-id="86ed4-310">WARNING</span></span>
- <span data-ttu-id="86ed4-311">TIP</span><span class="sxs-lookup"><span data-stu-id="86ed4-311">TIP</span></span>
- <span data-ttu-id="86ed4-312">DŮLEŽITÉ</span><span class="sxs-lookup"><span data-stu-id="86ed4-312">IMPORTANT</span></span>

<span data-ttu-id="86ed4-313">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="86ed4-313">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="86ed4-314">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="86ed4-314">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="86ed4-315">Příklady:</span><span class="sxs-lookup"><span data-stu-id="86ed4-315">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="86ed4-316">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-316">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="86ed4-317">Toto je POZNÁMKA.</span><span class="sxs-lookup"><span data-stu-id="86ed4-317">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="86ed4-318">Toto je VAROVÁNÍ.</span><span class="sxs-lookup"><span data-stu-id="86ed4-318">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="86ed4-319">Toto je TIP.</span><span class="sxs-lookup"><span data-stu-id="86ed4-319">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86ed4-320">Toto je DŮLEŽITÉ.</span><span class="sxs-lookup"><span data-stu-id="86ed4-320">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="86ed4-321">Soubory k zahrnutí</span><span class="sxs-lookup"><span data-stu-id="86ed4-321">Include files</span></span>

<span data-ttu-id="86ed4-322">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="86ed4-322">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="86ed4-323">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="86ed4-323">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="86ed4-324">K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="86ed4-324">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="86ed4-325">Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="86ed4-325">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="86ed4-326">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="86ed4-326">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="86ed4-327">Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="86ed4-327">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="86ed4-328">Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="86ed4-328">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="86ed4-329">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="86ed4-329">It can contain any valid Markdown.</span></span> <span data-ttu-id="86ed4-330">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="86ed4-330">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="86ed4-331">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="86ed4-331">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="86ed4-332">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="86ed4-332">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="86ed4-333">Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="86ed4-333">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="86ed4-334">Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="86ed4-334">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="86ed4-335">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-335">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="86ed4-336">Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-336">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="86ed4-337">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="86ed4-337">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="86ed4-338">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="86ed4-338">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="86ed4-339">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="86ed4-339">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="86ed4-340">Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-340">Don't embed include references within other include files.</span></span> <span data-ttu-id="86ed4-341">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="86ed4-341">They are not supported.</span></span>
- <span data-ttu-id="86ed4-342">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="86ed4-342">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="86ed4-343">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-343">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="86ed4-344">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="86ed4-344">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="86ed4-345">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-345">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="86ed4-346">Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="86ed4-346">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="86ed4-347">Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-347">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="86ed4-348">Nepoužívejte soubor k zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="86ed4-348">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="86ed4-349">Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="86ed4-349">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="86ed4-350">Příklad:</span><span class="sxs-lookup"><span data-stu-id="86ed4-350">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="86ed4-351">Voliče</span><span class="sxs-lookup"><span data-stu-id="86ed4-351">Selectors</span></span>

<span data-ttu-id="86ed4-352">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="86ed4-352">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="86ed4-353">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="86ed4-353">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="86ed4-354">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="86ed4-354">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="86ed4-355">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-355">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="86ed4-356">Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="86ed4-356">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="86ed4-357">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="86ed4-357">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="86ed4-358">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="86ed4-358">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="86ed4-359">Odkazy pro zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="86ed4-359">Code include references</span></span>

<span data-ttu-id="86ed4-360">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="86ed4-360">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="86ed4-361">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="86ed4-361">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="86ed4-362">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="86ed4-362">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="86ed4-363">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="86ed4-363">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="86ed4-364">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="86ed4-364">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="86ed4-365">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="86ed4-365">Alt text</span></span>

<span data-ttu-id="86ed4-366">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="86ed4-366">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="86ed4-367">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="86ed4-367">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="86ed4-368">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="86ed4-368">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="86ed4-369">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="86ed4-369">Apostrophes and quotation marks</span></span>

<span data-ttu-id="86ed4-370">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-370">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="86ed4-371">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-371">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="86ed4-372">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="86ed4-372">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="86ed4-373">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="86ed4-373">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="86ed4-374">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="86ed4-374">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="86ed4-375">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="86ed4-375">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="86ed4-376">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="86ed4-376">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="86ed4-377">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="86ed4-377">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="86ed4-378">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="86ed4-378">Angle brackets</span></span>

<span data-ttu-id="86ed4-379">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="86ed4-379">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="86ed4-380">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="86ed4-380">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="86ed4-381">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="86ed4-381">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="86ed4-382">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="86ed4-382">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="86ed4-383">Viz také:</span><span class="sxs-lookup"><span data-stu-id="86ed4-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="86ed4-384">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="86ed4-384">Markdown resources</span></span>

- [<span data-ttu-id="86ed4-385">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="86ed4-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="86ed4-386">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="86ed4-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="86ed4-387">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="86ed4-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="86ed4-388">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="86ed4-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
