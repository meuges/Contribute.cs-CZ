---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615828"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="5e791-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="5e791-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="5e791-104">Články na [docs.microsoft.com](http://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="5e791-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="5e791-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="5e791-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="5e791-106">Protože je obsah Docs uložený v GitHubu, může používat nadstavbu Markdownu zvanou [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), která poskytuje další funkce pro běžné potřeby formátování.</span><span class="sxs-lookup"><span data-stu-id="5e791-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="5e791-107">Platforma OPS (Open Publishing Services) navíc implementuje Markdig Markdown Parser.</span><span class="sxs-lookup"><span data-stu-id="5e791-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="5e791-108">Markdig je vysoce kompatibilní s GFM a přidává možnosti podporující funkce specifické pro Docs.</span><span class="sxs-lookup"><span data-stu-id="5e791-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="5e791-109">Markdig je rozšiřitelný procesor Markdownu pro .NET, který je rychlý, výkonný a kompatibilní se syntaxí CommonMark.</span><span class="sxs-lookup"><span data-stu-id="5e791-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="5e791-110">Lepší podpora komunity</span><span class="sxs-lookup"><span data-stu-id="5e791-110">Better community support</span></span>
* <span data-ttu-id="5e791-111">Lepší podpora standardů</span><span class="sxs-lookup"><span data-stu-id="5e791-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="5e791-112">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="5e791-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="5e791-113">Nadpis</span><span class="sxs-lookup"><span data-stu-id="5e791-113">Headings</span></span>

<span data-ttu-id="5e791-114">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="5e791-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="5e791-115">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="5e791-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="5e791-116">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="5e791-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="5e791-117">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="5e791-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="5e791-118">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="5e791-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="5e791-119">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="5e791-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="5e791-120">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="5e791-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="5e791-121">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="5e791-121">Bold and italic text</span></span>

<span data-ttu-id="5e791-122">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="5e791-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="5e791-123">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="5e791-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="5e791-124">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="5e791-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="5e791-125">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="5e791-125">Blockquotes</span></span>

<span data-ttu-id="5e791-126">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="5e791-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="5e791-127">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="5e791-128">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="5e791-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="5e791-129">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="5e791-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="5e791-130">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="5e791-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="5e791-131">Seznamy</span><span class="sxs-lookup"><span data-stu-id="5e791-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="5e791-132">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="5e791-132">Unordered list</span></span>

<span data-ttu-id="5e791-133">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="5e791-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="5e791-134">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="5e791-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="5e791-135">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-135">will be rendered as:</span></span>

- <span data-ttu-id="5e791-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="5e791-136">List item 1</span></span>
- <span data-ttu-id="5e791-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="5e791-137">List item 2</span></span>
- <span data-ttu-id="5e791-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="5e791-138">List item 3</span></span>

<span data-ttu-id="5e791-139">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="5e791-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="5e791-140">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="5e791-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="5e791-141">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-141">will be rendered as:</span></span>

- <span data-ttu-id="5e791-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="5e791-142">List item 1</span></span>
  - <span data-ttu-id="5e791-143">List item A</span><span class="sxs-lookup"><span data-stu-id="5e791-143">List item A</span></span>
  - <span data-ttu-id="5e791-144">List item B</span><span class="sxs-lookup"><span data-stu-id="5e791-144">List item B</span></span>
- <span data-ttu-id="5e791-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="5e791-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="5e791-146">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="5e791-146">Ordered list</span></span>

<span data-ttu-id="5e791-147">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="5e791-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="5e791-148">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="5e791-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="5e791-149">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-149">will be rendered as:</span></span>

1. <span data-ttu-id="5e791-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-150">First instruction</span></span>
2. <span data-ttu-id="5e791-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-151">Second instruction</span></span>
3. <span data-ttu-id="5e791-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-152">Third instruction</span></span>

<span data-ttu-id="5e791-153">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="5e791-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="5e791-154">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="5e791-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="5e791-155">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-155">will be rendered as:</span></span>

1. <span data-ttu-id="5e791-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-156">First instruction</span></span>
   1. <span data-ttu-id="5e791-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-157">Sub-instruction</span></span>
   2. <span data-ttu-id="5e791-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-158">Sub-instruction</span></span>
2. <span data-ttu-id="5e791-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="5e791-159">Second instruction</span></span>

<span data-ttu-id="5e791-160">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="5e791-160">Note that we use '1.'</span></span> <span data-ttu-id="5e791-161">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="5e791-161">for all entries.</span></span> <span data-ttu-id="5e791-162">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="5e791-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="5e791-163">Tables</span><span class="sxs-lookup"><span data-stu-id="5e791-163">Tables</span></span>

<span data-ttu-id="5e791-164">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="5e791-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="5e791-165">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="5e791-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="5e791-166">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="5e791-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="5e791-167">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="5e791-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="5e791-168">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="5e791-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="5e791-169">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-169">will be rendered as:</span></span>

| <span data-ttu-id="5e791-170">Fun</span><span class="sxs-lookup"><span data-stu-id="5e791-170">Fun</span></span>                  | <span data-ttu-id="5e791-171">With</span><span class="sxs-lookup"><span data-stu-id="5e791-171">With</span></span>                 | <span data-ttu-id="5e791-172">Tables</span><span class="sxs-lookup"><span data-stu-id="5e791-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="5e791-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="5e791-173">left-aligned column</span></span>  | <span data-ttu-id="5e791-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="5e791-174">right-aligned column</span></span> | <span data-ttu-id="5e791-175">centered column</span><span class="sxs-lookup"><span data-stu-id="5e791-175">centered column</span></span> |
| <span data-ttu-id="5e791-176">$100</span><span class="sxs-lookup"><span data-stu-id="5e791-176">$100</span></span>                 | <span data-ttu-id="5e791-177">$100</span><span class="sxs-lookup"><span data-stu-id="5e791-177">$100</span></span>                 | <span data-ttu-id="5e791-178">$100</span><span class="sxs-lookup"><span data-stu-id="5e791-178">$100</span></span>            |
| <span data-ttu-id="5e791-179">$10</span><span class="sxs-lookup"><span data-stu-id="5e791-179">$10</span></span>                  | <span data-ttu-id="5e791-180">$10</span><span class="sxs-lookup"><span data-stu-id="5e791-180">$10</span></span>                  | <span data-ttu-id="5e791-181">$10</span><span class="sxs-lookup"><span data-stu-id="5e791-181">$10</span></span>             |
| <span data-ttu-id="5e791-182">$1</span><span class="sxs-lookup"><span data-stu-id="5e791-182">$1</span></span>                   | <span data-ttu-id="5e791-183">$1</span><span class="sxs-lookup"><span data-stu-id="5e791-183">$1</span></span>                   | <span data-ttu-id="5e791-184">$1</span><span class="sxs-lookup"><span data-stu-id="5e791-184">$1</span></span>              |

<span data-ttu-id="5e791-185">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="5e791-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="5e791-186">[Funkce zalamování tabulek](#table-wrapping) v Markdigu určená k formátování širokých tabulek</span><span class="sxs-lookup"><span data-stu-id="5e791-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="5e791-187">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="5e791-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="5e791-188">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="5e791-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="5e791-189">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="5e791-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="5e791-190">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="5e791-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="5e791-191">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="5e791-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="5e791-192">Odkazy</span><span class="sxs-lookup"><span data-stu-id="5e791-192">Links</span></span>

<span data-ttu-id="5e791-193">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="5e791-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="5e791-194">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="5e791-194">For more information on linking, see:</span></span>

- <span data-ttu-id="5e791-195">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="5e791-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="5e791-196">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="5e791-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="5e791-197">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="5e791-197">Code snippets</span></span>

<span data-ttu-id="5e791-198">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="5e791-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="5e791-199">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="5e791-199">For details, see:</span></span>

- [<span data-ttu-id="5e791-200">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="5e791-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="5e791-201">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="5e791-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="5e791-202">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="5e791-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="5e791-203">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="5e791-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="5e791-204">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="5e791-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="5e791-205">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:</span><span class="sxs-lookup"><span data-stu-id="5e791-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="5e791-206">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="5e791-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="5e791-207">Název</span><span class="sxs-lookup"><span data-stu-id="5e791-207">Name</span></span>|<span data-ttu-id="5e791-208">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="5e791-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="5e791-209">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="5e791-209">.NET Console</span></span>|<span data-ttu-id="5e791-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="5e791-210">dotnetcli</span></span>|
|<span data-ttu-id="5e791-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="5e791-211">ASP.NET (C#)</span></span>|<span data-ttu-id="5e791-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="5e791-212">aspx-csharp</span></span>|
|<span data-ttu-id="5e791-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="5e791-213">ASP.NET (VB)</span></span>|<span data-ttu-id="5e791-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="5e791-214">aspx-vb</span></span>|
|<span data-ttu-id="5e791-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="5e791-215">AzCopy</span></span>|<span data-ttu-id="5e791-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="5e791-216">azcopy</span></span>|
|<span data-ttu-id="5e791-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5e791-217">Azure CLI</span></span>|<span data-ttu-id="5e791-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="5e791-218">azurecli</span></span>|
|<span data-ttu-id="5e791-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e791-219">Azure PowerShell</span></span>|<span data-ttu-id="5e791-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="5e791-220">azurepowershell</span></span>|
|<span data-ttu-id="5e791-221">C++</span><span class="sxs-lookup"><span data-stu-id="5e791-221">C++</span></span>|<span data-ttu-id="5e791-222">cpp</span><span class="sxs-lookup"><span data-stu-id="5e791-222">cpp</span></span>|
|<span data-ttu-id="5e791-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="5e791-223">C++/CX</span></span>|<span data-ttu-id="5e791-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="5e791-224">cppcx</span></span>|
|<span data-ttu-id="5e791-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="5e791-225">C++/WinRT</span></span>|<span data-ttu-id="5e791-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="5e791-226">cppwinrt</span></span>|
|<span data-ttu-id="5e791-227">C#</span><span class="sxs-lookup"><span data-stu-id="5e791-227">C#</span></span>|<span data-ttu-id="5e791-228">csharp</span><span class="sxs-lookup"><span data-stu-id="5e791-228">csharp</span></span>|
|<span data-ttu-id="5e791-229">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="5e791-229">C# in browser</span></span>|<span data-ttu-id="5e791-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="5e791-230">csharp-interactive</span></span>|
|<span data-ttu-id="5e791-231">Konzola</span><span class="sxs-lookup"><span data-stu-id="5e791-231">Console</span></span>|<span data-ttu-id="5e791-232">konzola</span><span class="sxs-lookup"><span data-stu-id="5e791-232">console</span></span>|
|<span data-ttu-id="5e791-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="5e791-233">CSHTML</span></span>|<span data-ttu-id="5e791-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="5e791-234">cshtml</span></span>|
|<span data-ttu-id="5e791-235">DAX</span><span class="sxs-lookup"><span data-stu-id="5e791-235">DAX</span></span>|<span data-ttu-id="5e791-236">dax</span><span class="sxs-lookup"><span data-stu-id="5e791-236">dax</span></span>|
|<span data-ttu-id="5e791-237">F#</span><span class="sxs-lookup"><span data-stu-id="5e791-237">F#</span></span>|<span data-ttu-id="5e791-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="5e791-238">fsharp</span></span>|
|<span data-ttu-id="5e791-239">Go</span><span class="sxs-lookup"><span data-stu-id="5e791-239">Go</span></span>|<span data-ttu-id="5e791-240">go</span><span class="sxs-lookup"><span data-stu-id="5e791-240">go</span></span>|
|<span data-ttu-id="5e791-241">HTML</span><span class="sxs-lookup"><span data-stu-id="5e791-241">HTML</span></span>|<span data-ttu-id="5e791-242">html</span><span class="sxs-lookup"><span data-stu-id="5e791-242">html</span></span>|
|<span data-ttu-id="5e791-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="5e791-243">HTTP</span></span>|<span data-ttu-id="5e791-244">http</span><span class="sxs-lookup"><span data-stu-id="5e791-244">http</span></span>|
|<span data-ttu-id="5e791-245">Java</span><span class="sxs-lookup"><span data-stu-id="5e791-245">Java</span></span>|<span data-ttu-id="5e791-246">java</span><span class="sxs-lookup"><span data-stu-id="5e791-246">java</span></span>|
|<span data-ttu-id="5e791-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5e791-247">JavaScript</span></span>|<span data-ttu-id="5e791-248">javascript</span><span class="sxs-lookup"><span data-stu-id="5e791-248">javascript</span></span>|
|<span data-ttu-id="5e791-249">JSON</span><span class="sxs-lookup"><span data-stu-id="5e791-249">JSON</span></span>|<span data-ttu-id="5e791-250">json</span><span class="sxs-lookup"><span data-stu-id="5e791-250">json</span></span>|
|<span data-ttu-id="5e791-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="5e791-251">Markdown</span></span>|<span data-ttu-id="5e791-252">md</span><span class="sxs-lookup"><span data-stu-id="5e791-252">md</span></span>|
|<span data-ttu-id="5e791-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="5e791-253">NodeJS</span></span>|<span data-ttu-id="5e791-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="5e791-254">nodejs</span></span>|
|<span data-ttu-id="5e791-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="5e791-255">Objective-C</span></span>|<span data-ttu-id="5e791-256">objc</span><span class="sxs-lookup"><span data-stu-id="5e791-256">objc</span></span>|
|<span data-ttu-id="5e791-257">OData</span><span class="sxs-lookup"><span data-stu-id="5e791-257">OData</span></span>|<span data-ttu-id="5e791-258">odata</span><span class="sxs-lookup"><span data-stu-id="5e791-258">odata</span></span>|
|<span data-ttu-id="5e791-259">PHP</span><span class="sxs-lookup"><span data-stu-id="5e791-259">PHP</span></span>|<span data-ttu-id="5e791-260">php</span><span class="sxs-lookup"><span data-stu-id="5e791-260">php</span></span>|
|<span data-ttu-id="5e791-261">PowerApps (oddělovač desetinných míst v podobě tečky)</span><span class="sxs-lookup"><span data-stu-id="5e791-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="5e791-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="5e791-262">powerapps-dot</span></span>|
|<span data-ttu-id="5e791-263">PowerApps (oddělovač desetinných míst v podobě čárky)</span><span class="sxs-lookup"><span data-stu-id="5e791-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="5e791-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="5e791-264">powerapps-comma</span></span>|
|<span data-ttu-id="5e791-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e791-265">PowerShell</span></span>|<span data-ttu-id="5e791-266">powershell</span><span class="sxs-lookup"><span data-stu-id="5e791-266">powershell</span></span>|
|<span data-ttu-id="5e791-267">Python</span><span class="sxs-lookup"><span data-stu-id="5e791-267">Python</span></span>|<span data-ttu-id="5e791-268">python</span><span class="sxs-lookup"><span data-stu-id="5e791-268">python</span></span>|
|<span data-ttu-id="5e791-269">Q#</span><span class="sxs-lookup"><span data-stu-id="5e791-269">Q#</span></span>|<span data-ttu-id="5e791-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="5e791-270">qsharp</span></span>|
|<span data-ttu-id="5e791-271">R</span><span class="sxs-lookup"><span data-stu-id="5e791-271">R</span></span>|<span data-ttu-id="5e791-272">r</span><span class="sxs-lookup"><span data-stu-id="5e791-272">r</span></span>|
|<span data-ttu-id="5e791-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="5e791-273">Ruby</span></span>|<span data-ttu-id="5e791-274">ruby</span><span class="sxs-lookup"><span data-stu-id="5e791-274">ruby</span></span>|
|<span data-ttu-id="5e791-275">SQL</span><span class="sxs-lookup"><span data-stu-id="5e791-275">SQL</span></span>|<span data-ttu-id="5e791-276">sql</span><span class="sxs-lookup"><span data-stu-id="5e791-276">sql</span></span>|
|<span data-ttu-id="5e791-277">Swift</span><span class="sxs-lookup"><span data-stu-id="5e791-277">Swift</span></span>|<span data-ttu-id="5e791-278">swift</span><span class="sxs-lookup"><span data-stu-id="5e791-278">swift</span></span>|
|<span data-ttu-id="5e791-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="5e791-279">TypeScript</span></span>|<span data-ttu-id="5e791-280">typescript</span><span class="sxs-lookup"><span data-stu-id="5e791-280">typescript</span></span>|
|<span data-ttu-id="5e791-281">VB</span><span class="sxs-lookup"><span data-stu-id="5e791-281">VB</span></span>|<span data-ttu-id="5e791-282">vb</span><span class="sxs-lookup"><span data-stu-id="5e791-282">vb</span></span>|
|<span data-ttu-id="5e791-283">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="5e791-283">VSTS CLI</span></span>|<span data-ttu-id="5e791-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="5e791-284">vstscli</span></span>|
|<span data-ttu-id="5e791-285">XAML</span><span class="sxs-lookup"><span data-stu-id="5e791-285">XAML</span></span>|<span data-ttu-id="5e791-286">xaml</span><span class="sxs-lookup"><span data-stu-id="5e791-286">xaml</span></span>|
|<span data-ttu-id="5e791-287">XML</span><span class="sxs-lookup"><span data-stu-id="5e791-287">XML</span></span>|<span data-ttu-id="5e791-288">xml</span><span class="sxs-lookup"><span data-stu-id="5e791-288">xml</span></span>|

<span data-ttu-id="5e791-289">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="5e791-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="5e791-290">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="5e791-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="5e791-291">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="5e791-291">Example: C\#</span></span>

<span data-ttu-id="5e791-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="5e791-292">__Markdown__</span></span>

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

<span data-ttu-id="5e791-293">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="5e791-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="5e791-294">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="5e791-294">Example: SQL</span></span>

<span data-ttu-id="5e791-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="5e791-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="5e791-296">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="5e791-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="5e791-297">Vlastní rozšíření Markdownu od OPS</span><span class="sxs-lookup"><span data-stu-id="5e791-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="5e791-298">Platforma Open Publishing Services (OPS) implementuje analyzátor Markdig Parser pro Markdown, který je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="5e791-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="5e791-299">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="5e791-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="5e791-300">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="5e791-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="5e791-301">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="5e791-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="5e791-302">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="5e791-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="5e791-303">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="5e791-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="5e791-304">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="5e791-304">Note blocks</span></span>
- <span data-ttu-id="5e791-305">Vložené soubory</span><span class="sxs-lookup"><span data-stu-id="5e791-305">Include files</span></span>
- <span data-ttu-id="5e791-306">Voliče</span><span class="sxs-lookup"><span data-stu-id="5e791-306">Selectors</span></span>
- <span data-ttu-id="5e791-307">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="5e791-307">Embedded videos</span></span>
- <span data-ttu-id="5e791-308">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="5e791-308">Code snippets/samples</span></span>

<span data-ttu-id="5e791-309">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="5e791-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="5e791-310">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="5e791-310">Note blocks</span></span>

<span data-ttu-id="5e791-311">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="5e791-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="5e791-312">POZNÁMKA</span><span class="sxs-lookup"><span data-stu-id="5e791-312">NOTE</span></span>
- <span data-ttu-id="5e791-313">VAROVÁNÍ</span><span class="sxs-lookup"><span data-stu-id="5e791-313">WARNING</span></span>
- <span data-ttu-id="5e791-314">TIP</span><span class="sxs-lookup"><span data-stu-id="5e791-314">TIP</span></span>
- <span data-ttu-id="5e791-315">DŮLEŽITÉ</span><span class="sxs-lookup"><span data-stu-id="5e791-315">IMPORTANT</span></span>

<span data-ttu-id="5e791-316">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="5e791-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="5e791-317">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="5e791-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="5e791-318">Příklady:</span><span class="sxs-lookup"><span data-stu-id="5e791-318">Examples:</span></span>

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

<span data-ttu-id="5e791-319">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="5e791-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="5e791-320">Toto je POZNÁMKA.</span><span class="sxs-lookup"><span data-stu-id="5e791-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="5e791-321">Toto je VAROVÁNÍ.</span><span class="sxs-lookup"><span data-stu-id="5e791-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="5e791-322">Toto je TIP.</span><span class="sxs-lookup"><span data-stu-id="5e791-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e791-323">Toto je DŮLEŽITÉ.</span><span class="sxs-lookup"><span data-stu-id="5e791-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="5e791-324">Soubory k zahrnutí</span><span class="sxs-lookup"><span data-stu-id="5e791-324">Include files</span></span>

<span data-ttu-id="5e791-325">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="5e791-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="5e791-326">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="5e791-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="5e791-327">K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="5e791-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="5e791-328">Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="5e791-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="5e791-329">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="5e791-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="5e791-330">Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="5e791-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="5e791-331">Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="5e791-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="5e791-332">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="5e791-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="5e791-333">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="5e791-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="5e791-334">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="5e791-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="5e791-335">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="5e791-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="5e791-336">Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="5e791-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="5e791-337">Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="5e791-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="5e791-338">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="5e791-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="5e791-339">Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="5e791-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="5e791-340">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="5e791-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="5e791-341">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="5e791-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="5e791-342">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="5e791-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="5e791-343">Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="5e791-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="5e791-344">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="5e791-344">They are not supported.</span></span>
- <span data-ttu-id="5e791-345">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="5e791-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="5e791-346">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="5e791-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="5e791-347">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="5e791-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="5e791-348">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="5e791-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="5e791-349">Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="5e791-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="5e791-350">Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="5e791-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="5e791-351">Nepoužívejte soubor k zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="5e791-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="5e791-352">Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="5e791-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="5e791-353">Příklad:</span><span class="sxs-lookup"><span data-stu-id="5e791-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="5e791-354">Voliče</span><span class="sxs-lookup"><span data-stu-id="5e791-354">Selectors</span></span>

<span data-ttu-id="5e791-355">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="5e791-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="5e791-356">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="5e791-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="5e791-357">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="5e791-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="5e791-358">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="5e791-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="5e791-359">Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="5e791-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="5e791-360">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="5e791-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="5e791-361">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="5e791-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="5e791-362">Odkazy pro zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="5e791-362">Code include references</span></span>

<span data-ttu-id="5e791-363">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="5e791-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="5e791-364">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="5e791-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="5e791-365">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="5e791-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="5e791-366">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="5e791-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="5e791-367">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="5e791-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="5e791-368">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="5e791-368">Alt text</span></span>

<span data-ttu-id="5e791-369">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="5e791-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="5e791-370">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="5e791-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="5e791-371">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="5e791-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="5e791-372">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="5e791-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="5e791-373">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="5e791-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="5e791-374">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="5e791-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="5e791-375">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="5e791-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="5e791-376">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="5e791-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="5e791-377">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="5e791-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="5e791-378">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="5e791-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="5e791-379">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="5e791-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="5e791-380">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="5e791-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="5e791-381">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="5e791-381">Angle brackets</span></span>

<span data-ttu-id="5e791-382">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="5e791-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="5e791-383">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="5e791-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="5e791-384">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="5e791-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="5e791-385">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="5e791-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="5e791-386">Viz také:</span><span class="sxs-lookup"><span data-stu-id="5e791-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="5e791-387">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="5e791-387">Markdown resources</span></span>

- [<span data-ttu-id="5e791-388">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="5e791-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="5e791-389">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="5e791-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="5e791-390">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="5e791-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="5e791-391">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="5e791-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
