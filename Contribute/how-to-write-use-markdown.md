---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 21194c4bd6020d847b526a4d9544c826aa199e2a
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609515"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="0a7d6-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="0a7d6-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="0a7d6-104">Články na [docs.microsoft.com](http://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="0a7d6-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="0a7d6-106">Protože je obsah Docs uložený v GitHubu, může používat nadstavbu Markdownu zvanou [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), která poskytuje další funkce pro běžné potřeby formátování.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="0a7d6-107">Platforma OPS (Open Publishing Services) navíc implementuje Markdig Markdown Parser.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="0a7d6-108">Markdig je vysoce kompatibilní s GFM a přidává možnosti podporující funkce specifické pro Docs.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="0a7d6-109">Markdig je rozšiřitelný procesor Markdownu pro .NET, který je rychlý, výkonný a kompatibilní se syntaxí CommonMark.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="0a7d6-110">Lepší podpora komunity</span><span class="sxs-lookup"><span data-stu-id="0a7d6-110">Better community support</span></span>
* <span data-ttu-id="0a7d6-111">Lepší podpora standardů</span><span class="sxs-lookup"><span data-stu-id="0a7d6-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="0a7d6-112">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="0a7d6-113">Nadpis</span><span class="sxs-lookup"><span data-stu-id="0a7d6-113">Headings</span></span>

<span data-ttu-id="0a7d6-114">K vytvoření nadpisu se používá znak mřížky (#):</span><span class="sxs-lookup"><span data-stu-id="0a7d6-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="0a7d6-115">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="0a7d6-116">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="0a7d6-117">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="0a7d6-118">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="0a7d6-119">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="0a7d6-120">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="0a7d6-121">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="0a7d6-121">Bold and italic text</span></span>

<span data-ttu-id="0a7d6-122">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="0a7d6-123">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="0a7d6-124">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="0a7d6-125">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="0a7d6-125">Blockquotes</span></span>

<span data-ttu-id="0a7d6-126">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="0a7d6-127">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="0a7d6-128">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="0a7d6-129">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="0a7d6-130">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="0a7d6-131">Seznamy</span><span class="sxs-lookup"><span data-stu-id="0a7d6-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="0a7d6-132">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="0a7d6-132">Unordered list</span></span>

<span data-ttu-id="0a7d6-133">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="0a7d6-134">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="0a7d6-135">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-135">will be rendered as:</span></span>

- <span data-ttu-id="0a7d6-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="0a7d6-136">List item 1</span></span>
- <span data-ttu-id="0a7d6-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="0a7d6-137">List item 2</span></span>
- <span data-ttu-id="0a7d6-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="0a7d6-138">List item 3</span></span>

<span data-ttu-id="0a7d6-139">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0a7d6-140">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="0a7d6-141">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-141">will be rendered as:</span></span>

- <span data-ttu-id="0a7d6-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="0a7d6-142">List item 1</span></span>
  - <span data-ttu-id="0a7d6-143">List item A</span><span class="sxs-lookup"><span data-stu-id="0a7d6-143">List item A</span></span>
  - <span data-ttu-id="0a7d6-144">List item B</span><span class="sxs-lookup"><span data-stu-id="0a7d6-144">List item B</span></span>
- <span data-ttu-id="0a7d6-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="0a7d6-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="0a7d6-146">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="0a7d6-146">Ordered list</span></span>

<span data-ttu-id="0a7d6-147">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="0a7d6-148">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="0a7d6-149">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-149">will be rendered as:</span></span>

1. <span data-ttu-id="0a7d6-150">First instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-150">First instruction</span></span>
2. <span data-ttu-id="0a7d6-151">Second instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-151">Second instruction</span></span>
3. <span data-ttu-id="0a7d6-152">Third instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-152">Third instruction</span></span>

<span data-ttu-id="0a7d6-153">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="0a7d6-154">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="0a7d6-155">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-155">will be rendered as:</span></span>

1. <span data-ttu-id="0a7d6-156">First instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-156">First instruction</span></span>
   1. <span data-ttu-id="0a7d6-157">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-157">Sub-instruction</span></span>
   2. <span data-ttu-id="0a7d6-158">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-158">Sub-instruction</span></span>
2. <span data-ttu-id="0a7d6-159">Second instruction</span><span class="sxs-lookup"><span data-stu-id="0a7d6-159">Second instruction</span></span>

<span data-ttu-id="0a7d6-160">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="0a7d6-160">Note that we use '1.'</span></span> <span data-ttu-id="0a7d6-161">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-161">for all entries.</span></span> <span data-ttu-id="0a7d6-162">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="0a7d6-163">Tables</span><span class="sxs-lookup"><span data-stu-id="0a7d6-163">Tables</span></span>

<span data-ttu-id="0a7d6-164">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="0a7d6-165">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="0a7d6-166">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="0a7d6-167">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="0a7d6-168">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="0a7d6-169">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-169">will be rendered as:</span></span>

| <span data-ttu-id="0a7d6-170">Fun</span><span class="sxs-lookup"><span data-stu-id="0a7d6-170">Fun</span></span>                  | <span data-ttu-id="0a7d6-171">With</span><span class="sxs-lookup"><span data-stu-id="0a7d6-171">With</span></span>                 | <span data-ttu-id="0a7d6-172">Tables</span><span class="sxs-lookup"><span data-stu-id="0a7d6-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="0a7d6-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="0a7d6-173">left-aligned column</span></span>  | <span data-ttu-id="0a7d6-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="0a7d6-174">right-aligned column</span></span> | <span data-ttu-id="0a7d6-175">centered column</span><span class="sxs-lookup"><span data-stu-id="0a7d6-175">centered column</span></span> |
| <span data-ttu-id="0a7d6-176">$100</span><span class="sxs-lookup"><span data-stu-id="0a7d6-176">$100</span></span>                 | <span data-ttu-id="0a7d6-177">$100</span><span class="sxs-lookup"><span data-stu-id="0a7d6-177">$100</span></span>                 | <span data-ttu-id="0a7d6-178">$100</span><span class="sxs-lookup"><span data-stu-id="0a7d6-178">$100</span></span>            |
| <span data-ttu-id="0a7d6-179">$10</span><span class="sxs-lookup"><span data-stu-id="0a7d6-179">$10</span></span>                  | <span data-ttu-id="0a7d6-180">$10</span><span class="sxs-lookup"><span data-stu-id="0a7d6-180">$10</span></span>                  | <span data-ttu-id="0a7d6-181">$10</span><span class="sxs-lookup"><span data-stu-id="0a7d6-181">$10</span></span>             |
| <span data-ttu-id="0a7d6-182">$1</span><span class="sxs-lookup"><span data-stu-id="0a7d6-182">$1</span></span>                   | <span data-ttu-id="0a7d6-183">$1</span><span class="sxs-lookup"><span data-stu-id="0a7d6-183">$1</span></span>                   | <span data-ttu-id="0a7d6-184">$1</span><span class="sxs-lookup"><span data-stu-id="0a7d6-184">$1</span></span>              |

<span data-ttu-id="0a7d6-185">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="0a7d6-186">[Funkce zalamování tabulek](#table-wrapping) v Markdigu určená k formátování širokých tabulek</span><span class="sxs-lookup"><span data-stu-id="0a7d6-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="0a7d6-187">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="0a7d6-188">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="0a7d6-189">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="0a7d6-190">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="0a7d6-191">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="0a7d6-192">Odkazy</span><span class="sxs-lookup"><span data-stu-id="0a7d6-192">Links</span></span>

<span data-ttu-id="0a7d6-193">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="0a7d6-194">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-194">For more information on linking, see:</span></span>

- <span data-ttu-id="0a7d6-195">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="0a7d6-196">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="0a7d6-197">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-197">Code snippets</span></span>

<span data-ttu-id="0a7d6-198">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="0a7d6-199">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-199">For details, see:</span></span>

- [<span data-ttu-id="0a7d6-200">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-200">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="0a7d6-201">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="0a7d6-201">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="0a7d6-202">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="0a7d6-203">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="0a7d6-204">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="0a7d6-205">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných označení:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="0a7d6-206">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="0a7d6-207">Název</span><span class="sxs-lookup"><span data-stu-id="0a7d6-207">Name</span></span>|<span data-ttu-id="0a7d6-208">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="0a7d6-209">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="0a7d6-209">.NET Console</span></span>|<span data-ttu-id="0a7d6-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="0a7d6-210">dotnetcli</span></span>|
|<span data-ttu-id="0a7d6-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-211">ASP.NET (C#)</span></span>|<span data-ttu-id="0a7d6-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="0a7d6-212">aspx-csharp</span></span>|
|<span data-ttu-id="0a7d6-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-213">ASP.NET (VB)</span></span>|<span data-ttu-id="0a7d6-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="0a7d6-214">aspx-vb</span></span>|
|<span data-ttu-id="0a7d6-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="0a7d6-215">AzCopy</span></span>|<span data-ttu-id="0a7d6-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="0a7d6-216">azcopy</span></span>|
|<span data-ttu-id="0a7d6-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="0a7d6-217">Azure CLI</span></span>|<span data-ttu-id="0a7d6-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="0a7d6-218">azurecli</span></span>|
|<span data-ttu-id="0a7d6-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a7d6-219">Azure PowerShell</span></span>|<span data-ttu-id="0a7d6-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="0a7d6-220">azurepowershell</span></span>|
|<span data-ttu-id="0a7d6-221">C++</span><span class="sxs-lookup"><span data-stu-id="0a7d6-221">C++</span></span>|<span data-ttu-id="0a7d6-222">cpp</span><span class="sxs-lookup"><span data-stu-id="0a7d6-222">cpp</span></span>|
|<span data-ttu-id="0a7d6-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="0a7d6-223">C++/CX</span></span>|<span data-ttu-id="0a7d6-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="0a7d6-224">cppcx</span></span>|
|<span data-ttu-id="0a7d6-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="0a7d6-225">C++/WinRT</span></span>|<span data-ttu-id="0a7d6-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="0a7d6-226">cppwinrt</span></span>|
|<span data-ttu-id="0a7d6-227">C#</span><span class="sxs-lookup"><span data-stu-id="0a7d6-227">C#</span></span>|<span data-ttu-id="0a7d6-228">csharp</span><span class="sxs-lookup"><span data-stu-id="0a7d6-228">csharp</span></span>|
|<span data-ttu-id="0a7d6-229">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="0a7d6-229">C# in browser</span></span>|<span data-ttu-id="0a7d6-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="0a7d6-230">csharp-interactive</span></span>|
|<span data-ttu-id="0a7d6-231">Konzola</span><span class="sxs-lookup"><span data-stu-id="0a7d6-231">Console</span></span>|<span data-ttu-id="0a7d6-232">konzola</span><span class="sxs-lookup"><span data-stu-id="0a7d6-232">console</span></span>|
|<span data-ttu-id="0a7d6-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="0a7d6-233">CSHTML</span></span>|<span data-ttu-id="0a7d6-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="0a7d6-234">cshtml</span></span>|
|<span data-ttu-id="0a7d6-235">DAX</span><span class="sxs-lookup"><span data-stu-id="0a7d6-235">DAX</span></span>|<span data-ttu-id="0a7d6-236">dax</span><span class="sxs-lookup"><span data-stu-id="0a7d6-236">dax</span></span>|
|<span data-ttu-id="0a7d6-237">F#</span><span class="sxs-lookup"><span data-stu-id="0a7d6-237">F#</span></span>|<span data-ttu-id="0a7d6-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="0a7d6-238">fsharp</span></span>|
|<span data-ttu-id="0a7d6-239">Go</span><span class="sxs-lookup"><span data-stu-id="0a7d6-239">Go</span></span>|<span data-ttu-id="0a7d6-240">go</span><span class="sxs-lookup"><span data-stu-id="0a7d6-240">go</span></span>|
|<span data-ttu-id="0a7d6-241">HTML</span><span class="sxs-lookup"><span data-stu-id="0a7d6-241">HTML</span></span>|<span data-ttu-id="0a7d6-242">html</span><span class="sxs-lookup"><span data-stu-id="0a7d6-242">html</span></span>|
|<span data-ttu-id="0a7d6-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="0a7d6-243">HTTP</span></span>|<span data-ttu-id="0a7d6-244">http</span><span class="sxs-lookup"><span data-stu-id="0a7d6-244">http</span></span>|
|<span data-ttu-id="0a7d6-245">Java</span><span class="sxs-lookup"><span data-stu-id="0a7d6-245">Java</span></span>|<span data-ttu-id="0a7d6-246">java</span><span class="sxs-lookup"><span data-stu-id="0a7d6-246">java</span></span>|
|<span data-ttu-id="0a7d6-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="0a7d6-247">JavaScript</span></span>|<span data-ttu-id="0a7d6-248">javascript</span><span class="sxs-lookup"><span data-stu-id="0a7d6-248">javascript</span></span>|
|<span data-ttu-id="0a7d6-249">JSON</span><span class="sxs-lookup"><span data-stu-id="0a7d6-249">JSON</span></span>|<span data-ttu-id="0a7d6-250">json</span><span class="sxs-lookup"><span data-stu-id="0a7d6-250">json</span></span>|
|<span data-ttu-id="0a7d6-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="0a7d6-251">Markdown</span></span>|<span data-ttu-id="0a7d6-252">md</span><span class="sxs-lookup"><span data-stu-id="0a7d6-252">md</span></span>|
|<span data-ttu-id="0a7d6-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="0a7d6-253">NodeJS</span></span>|<span data-ttu-id="0a7d6-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="0a7d6-254">nodejs</span></span>|
|<span data-ttu-id="0a7d6-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="0a7d6-255">Objective-C</span></span>|<span data-ttu-id="0a7d6-256">objc</span><span class="sxs-lookup"><span data-stu-id="0a7d6-256">objc</span></span>|
|<span data-ttu-id="0a7d6-257">OData</span><span class="sxs-lookup"><span data-stu-id="0a7d6-257">OData</span></span>|<span data-ttu-id="0a7d6-258">odata</span><span class="sxs-lookup"><span data-stu-id="0a7d6-258">odata</span></span>|
|<span data-ttu-id="0a7d6-259">PHP</span><span class="sxs-lookup"><span data-stu-id="0a7d6-259">PHP</span></span>|<span data-ttu-id="0a7d6-260">php</span><span class="sxs-lookup"><span data-stu-id="0a7d6-260">php</span></span>|
|<span data-ttu-id="0a7d6-261">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="0a7d6-261">Power Apps Formula</span></span>|<span data-ttu-id="0a7d6-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="0a7d6-262">powerappsfl</span></span>|
|<span data-ttu-id="0a7d6-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a7d6-263">PowerShell</span></span>|<span data-ttu-id="0a7d6-264">powershell</span><span class="sxs-lookup"><span data-stu-id="0a7d6-264">powershell</span></span>|
|<span data-ttu-id="0a7d6-265">Python</span><span class="sxs-lookup"><span data-stu-id="0a7d6-265">Python</span></span>|<span data-ttu-id="0a7d6-266">python</span><span class="sxs-lookup"><span data-stu-id="0a7d6-266">python</span></span>|
|<span data-ttu-id="0a7d6-267">Q#</span><span class="sxs-lookup"><span data-stu-id="0a7d6-267">Q#</span></span>|<span data-ttu-id="0a7d6-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="0a7d6-268">qsharp</span></span>|
|<span data-ttu-id="0a7d6-269">R</span><span class="sxs-lookup"><span data-stu-id="0a7d6-269">R</span></span>|<span data-ttu-id="0a7d6-270">r</span><span class="sxs-lookup"><span data-stu-id="0a7d6-270">r</span></span>|
|<span data-ttu-id="0a7d6-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="0a7d6-271">Ruby</span></span>|<span data-ttu-id="0a7d6-272">ruby</span><span class="sxs-lookup"><span data-stu-id="0a7d6-272">ruby</span></span>|
|<span data-ttu-id="0a7d6-273">SQL</span><span class="sxs-lookup"><span data-stu-id="0a7d6-273">SQL</span></span>|<span data-ttu-id="0a7d6-274">sql</span><span class="sxs-lookup"><span data-stu-id="0a7d6-274">sql</span></span>|
|<span data-ttu-id="0a7d6-275">Swift</span><span class="sxs-lookup"><span data-stu-id="0a7d6-275">Swift</span></span>|<span data-ttu-id="0a7d6-276">swift</span><span class="sxs-lookup"><span data-stu-id="0a7d6-276">swift</span></span>|
|<span data-ttu-id="0a7d6-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="0a7d6-277">TypeScript</span></span>|<span data-ttu-id="0a7d6-278">typescript</span><span class="sxs-lookup"><span data-stu-id="0a7d6-278">typescript</span></span>|
|<span data-ttu-id="0a7d6-279">VB</span><span class="sxs-lookup"><span data-stu-id="0a7d6-279">VB</span></span>|<span data-ttu-id="0a7d6-280">vb</span><span class="sxs-lookup"><span data-stu-id="0a7d6-280">vb</span></span>|
|<span data-ttu-id="0a7d6-281">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="0a7d6-281">VSTS CLI</span></span>|<span data-ttu-id="0a7d6-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="0a7d6-282">vstscli</span></span>|
|<span data-ttu-id="0a7d6-283">XAML</span><span class="sxs-lookup"><span data-stu-id="0a7d6-283">XAML</span></span>|<span data-ttu-id="0a7d6-284">xaml</span><span class="sxs-lookup"><span data-stu-id="0a7d6-284">xaml</span></span>|
|<span data-ttu-id="0a7d6-285">XML</span><span class="sxs-lookup"><span data-stu-id="0a7d6-285">XML</span></span>|<span data-ttu-id="0a7d6-286">xml</span><span class="sxs-lookup"><span data-stu-id="0a7d6-286">xml</span></span>|

<span data-ttu-id="0a7d6-287">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="0a7d6-288">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="0a7d6-289">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="0a7d6-289">Example: C\#</span></span>

<span data-ttu-id="0a7d6-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0a7d6-290">__Markdown__</span></span>

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

<span data-ttu-id="0a7d6-291">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="0a7d6-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="0a7d6-292">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="0a7d6-292">Example: SQL</span></span>

<span data-ttu-id="0a7d6-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="0a7d6-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="0a7d6-294">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="0a7d6-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="0a7d6-295">Vlastní rozšíření Markdownu od OPS</span><span class="sxs-lookup"><span data-stu-id="0a7d6-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="0a7d6-296">Platforma Open Publishing Services (OPS) implementuje analyzátor Markdig Parser pro Markdown, který je vysoce kompatibilní s rozšířením GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="0a7d6-297">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="0a7d6-298">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="0a7d6-299">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="0a7d6-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="0a7d6-300">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="0a7d6-301">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="0a7d6-302">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="0a7d6-302">Note blocks</span></span>
- <span data-ttu-id="0a7d6-303">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="0a7d6-303">Includes</span></span>
- <span data-ttu-id="0a7d6-304">Voliče</span><span class="sxs-lookup"><span data-stu-id="0a7d6-304">Selectors</span></span>
- <span data-ttu-id="0a7d6-305">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="0a7d6-305">Embedded videos</span></span>
- <span data-ttu-id="0a7d6-306">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-306">Code snippets/samples</span></span>

<span data-ttu-id="0a7d6-307">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="0a7d6-308">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="0a7d6-308">Note blocks</span></span>

<span data-ttu-id="0a7d6-309">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="0a7d6-310">POZNÁMKA</span><span class="sxs-lookup"><span data-stu-id="0a7d6-310">NOTE</span></span>
- <span data-ttu-id="0a7d6-311">VAROVÁNÍ</span><span class="sxs-lookup"><span data-stu-id="0a7d6-311">WARNING</span></span>
- <span data-ttu-id="0a7d6-312">TIP</span><span class="sxs-lookup"><span data-stu-id="0a7d6-312">TIP</span></span>
- <span data-ttu-id="0a7d6-313">DŮLEŽITÉ</span><span class="sxs-lookup"><span data-stu-id="0a7d6-313">IMPORTANT</span></span>

<span data-ttu-id="0a7d6-314">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="0a7d6-315">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="0a7d6-316">Příklady:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-316">Examples:</span></span>

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

<span data-ttu-id="0a7d6-317">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="0a7d6-318">Toto je POZNÁMKA.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="0a7d6-319">Toto je VAROVÁNÍ.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="0a7d6-320">Toto je TIP.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a7d6-321">Toto je DŮLEŽITÉ.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-321">This is IMPORTANT</span></span>

### <a name="includes"></a><span data-ttu-id="0a7d6-322">Zahrnutí</span><span class="sxs-lookup"><span data-stu-id="0a7d6-322">Includes</span></span>

<span data-ttu-id="0a7d6-323">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="0a7d6-324">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="0a7d6-325">K dispozici jsou tři typy zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-325">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="0a7d6-326">Vložení: umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="0a7d6-327">Blok: umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="0a7d6-328">Obrázek: takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="0a7d6-329">Zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-329">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="0a7d6-330">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="0a7d6-331">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="0a7d6-332">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="0a7d6-333">Tady jsou požadavky a důležité informace týkající se zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-333">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="0a7d6-334">Zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-334">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="0a7d6-335">Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-335">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="0a7d6-336">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="0a7d6-337">Zahrnuté soubory se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-337">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="0a7d6-338">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="0a7d6-339">Dbejte na to, aby byl všechen text v zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-339">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="0a7d6-340">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="0a7d6-341">Nevkládejte zahrnutí do jiných zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-341">Don't embed includes within other includes.</span></span> <span data-ttu-id="0a7d6-342">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-342">They are not supported.</span></span>
- <span data-ttu-id="0a7d6-343">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="0a7d6-344">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="0a7d6-345">Pokud zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-345">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="0a7d6-346">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="0a7d6-347">Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-347">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="0a7d6-348">Multimediální soubor uložte do složky multimédií spojené se zahrnutím.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-348">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="0a7d6-349">Nepoužívejte zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-349">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="0a7d6-350">Zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-350">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="0a7d6-351">Příklad:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="0a7d6-352">Voliče</span><span class="sxs-lookup"><span data-stu-id="0a7d6-352">Selectors</span></span>

<span data-ttu-id="0a7d6-353">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="0a7d6-354">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="0a7d6-355">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="0a7d6-356">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="0a7d6-357">Pak můžete na zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-357">Then you can reference that include in all your articles that use the same selector.</span></span>

<span data-ttu-id="0a7d6-358">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="0a7d6-359">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="0a7d6-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-includes"></a><span data-ttu-id="0a7d6-360">Zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-360">Code includes</span></span>

<span data-ttu-id="0a7d6-361">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="0a7d6-362">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="0a7d6-363">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="0a7d6-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="0a7d6-364">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="0a7d6-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="0a7d6-365">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="0a7d6-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="0a7d6-366">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="0a7d6-366">Alt text</span></span>

<span data-ttu-id="0a7d6-367">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="0a7d6-368">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="0a7d6-369">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="0a7d6-370">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="0a7d6-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="0a7d6-371">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="0a7d6-372">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="0a7d6-373">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="0a7d6-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="0a7d6-374">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="0a7d6-375">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="0a7d6-376">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="0a7d6-377">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="0a7d6-378">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="0a7d6-379">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="0a7d6-379">Angle brackets</span></span>

<span data-ttu-id="0a7d6-380">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="0a7d6-381">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="0a7d6-382">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="0a7d6-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="0a7d6-383">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="0a7d6-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="0a7d6-384">Viz také:</span><span class="sxs-lookup"><span data-stu-id="0a7d6-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="0a7d6-385">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="0a7d6-385">Markdown resources</span></span>

- [<span data-ttu-id="0a7d6-386">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-386">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="0a7d6-387">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="0a7d6-387">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="0a7d6-388">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="0a7d6-388">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="0a7d6-389">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="0a7d6-389">The Markdown Guide</span></span>](https://www.markdownguide.org/)
