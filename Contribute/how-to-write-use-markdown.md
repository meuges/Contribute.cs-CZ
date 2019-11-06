---
title: Používání Markdownu pro vytváření článků na webu Docs
description: Tento článek poskytuje základní a referenční informace o jazyku Markdown, který slouží k vytváření článků publikovaných na docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: ffc44f07929890ef17b3878ba389dfeea82691a6
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592472"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="04009-103">Používání Markdownu pro vytváření článků na webu Docs</span><span class="sxs-lookup"><span data-stu-id="04009-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="04009-104">Články na [docs.microsoft.com](https://docs.microsoft.com) jsou psané jednoduchým jazykem využívajícím značky, který se nazývá [Markdown](https://daringfireball.net/projects/markdown/) a snadno se čte i učí.</span><span class="sxs-lookup"><span data-stu-id="04009-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="04009-105">Díky tomu se v oboru rychle stal standardem.</span><span class="sxs-lookup"><span data-stu-id="04009-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="04009-106">Na webu Docs se používá [varianta Markdig](#markdown-flavor) jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="04009-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="04009-107">Základy Markdownu</span><span class="sxs-lookup"><span data-stu-id="04009-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="04009-108">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="04009-108">Headings</span></span>

<span data-ttu-id="04009-109">K vytvoření nadpisu se používá znak hash (#):</span><span class="sxs-lookup"><span data-stu-id="04009-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="04009-110">Nadpisy by se měly vytvářet stylem atx, kdy se na začátku řádku použije 1 až 6 znaků mřížky (#), které označují nadpis odpovídající úrovním nadpisů HTML H1 až H6.</span><span class="sxs-lookup"><span data-stu-id="04009-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="04009-111">Příklady nadpisů první až čtvrté úrovně jsou použité výše.</span><span class="sxs-lookup"><span data-stu-id="04009-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="04009-112">V tématu **musí** být jen jeden nadpis první úrovně (H1), který se zobrazí jako nadpis stránky.</span><span class="sxs-lookup"><span data-stu-id="04009-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="04009-113">Pokud nadpis končí znakem `#`, musíte na konec přidat znak `#` navíc, aby se nadpis zobrazil správně.</span><span class="sxs-lookup"><span data-stu-id="04009-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="04009-114">Příklad: `# Async Programming in F# #`</span><span class="sxs-lookup"><span data-stu-id="04009-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="04009-115">Nadpisy druhé úrovně vygenerují obsah stránky, který se zobrazí v oddílu „V tomto článku“ pod nadpisem stránky.</span><span class="sxs-lookup"><span data-stu-id="04009-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="04009-116">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="04009-116">Bold and italic text</span></span>

<span data-ttu-id="04009-117">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="04009-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="04009-118">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="04009-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="04009-119">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="04009-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="04009-120">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="04009-120">Blockquotes</span></span>

<span data-ttu-id="04009-121">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="04009-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="04009-122">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="04009-123">Sucho nyní panovalo deset miliónů let a nadvláda těchto strašných ještěrů trvala dlouho, než skončila.</span><span class="sxs-lookup"><span data-stu-id="04009-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="04009-124">Zde na rovníku, na kontinentu, který bude jednou známý jako Afrika, dosáhl boj o holou existenci nového vrcholu krutosti, přičemž vítěz zatím nebyl v dohledu.</span><span class="sxs-lookup"><span data-stu-id="04009-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="04009-125">V této pusté a vyprahlé krajině se mohlo dařit jen malým, hbitým nebo krutým tvorům.</span><span class="sxs-lookup"><span data-stu-id="04009-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="04009-126">Seznamy</span><span class="sxs-lookup"><span data-stu-id="04009-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="04009-127">Neseřazený seznam</span><span class="sxs-lookup"><span data-stu-id="04009-127">Unordered list</span></span>

<span data-ttu-id="04009-128">Na neseřazený seznam / seznam s odrážkami můžete použít hvězdičky nebo spojovníky.</span><span class="sxs-lookup"><span data-stu-id="04009-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="04009-129">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="04009-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="04009-130">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-130">will be rendered as:</span></span>

- <span data-ttu-id="04009-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="04009-131">List item 1</span></span>
- <span data-ttu-id="04009-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="04009-132">List item 2</span></span>
- <span data-ttu-id="04009-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="04009-133">List item 3</span></span>

<span data-ttu-id="04009-134">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="04009-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="04009-135">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="04009-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="04009-136">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-136">will be rendered as:</span></span>

- <span data-ttu-id="04009-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="04009-137">List item 1</span></span>
  - <span data-ttu-id="04009-138">List item A</span><span class="sxs-lookup"><span data-stu-id="04009-138">List item A</span></span>
  - <span data-ttu-id="04009-139">List item B</span><span class="sxs-lookup"><span data-stu-id="04009-139">List item B</span></span>
- <span data-ttu-id="04009-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="04009-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="04009-141">Seřazený seznam</span><span class="sxs-lookup"><span data-stu-id="04009-141">Ordered list</span></span>

<span data-ttu-id="04009-142">Na seřazený/stupňovaný seznam použijte odpovídající čísla.</span><span class="sxs-lookup"><span data-stu-id="04009-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="04009-143">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="04009-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="04009-144">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-144">will be rendered as:</span></span>

1. <span data-ttu-id="04009-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="04009-145">First instruction</span></span>
2. <span data-ttu-id="04009-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="04009-146">Second instruction</span></span>
3. <span data-ttu-id="04009-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="04009-147">Third instruction</span></span>

<span data-ttu-id="04009-148">Pokud chcete seznam vnořit do jiného seznamu, podřízené položky seznamu odsaďte.</span><span class="sxs-lookup"><span data-stu-id="04009-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="04009-149">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="04009-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="04009-150">se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-150">will be rendered as:</span></span>

1. <span data-ttu-id="04009-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="04009-151">First instruction</span></span>
   1. <span data-ttu-id="04009-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="04009-152">Sub-instruction</span></span>
   2. <span data-ttu-id="04009-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="04009-153">Sub-instruction</span></span>
2. <span data-ttu-id="04009-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="04009-154">Second instruction</span></span>

<span data-ttu-id="04009-155">Všimněte si, že jsme použili „1.“</span><span class="sxs-lookup"><span data-stu-id="04009-155">Note that we use '1.'</span></span> <span data-ttu-id="04009-156">pro všechny položky.</span><span class="sxs-lookup"><span data-stu-id="04009-156">for all entries.</span></span> <span data-ttu-id="04009-157">Usnadňuje to zjištění rozdílů, pokud pozdější vložené soubory obsahují nové kroky nebo odebírají existující kroky.</span><span class="sxs-lookup"><span data-stu-id="04009-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="04009-158">Tabulky</span><span class="sxs-lookup"><span data-stu-id="04009-158">Tables</span></span>

<span data-ttu-id="04009-159">Tabulky nejsou součástí základní specifikace Markdownu, ale podporuje je GFM.</span><span class="sxs-lookup"><span data-stu-id="04009-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="04009-160">Tabulky můžete vytvářet pomocí svislé čáry (|) a spojovníku (-).</span><span class="sxs-lookup"><span data-stu-id="04009-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="04009-161">Spojovníky vytvářejí záhlaví každého sloupce, zatímco svislé čáry jednotlivé sloupce oddělují.</span><span class="sxs-lookup"><span data-stu-id="04009-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="04009-162">Aby se tabulka správně vykreslila, přidejte před ni prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="04009-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="04009-163">Například tento Markdown:</span><span class="sxs-lookup"><span data-stu-id="04009-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="04009-164">Se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="04009-164">Will be rendered as:</span></span>

| <span data-ttu-id="04009-165">Fun</span><span class="sxs-lookup"><span data-stu-id="04009-165">Fun</span></span>                  | <span data-ttu-id="04009-166">With</span><span class="sxs-lookup"><span data-stu-id="04009-166">With</span></span>                 | <span data-ttu-id="04009-167">Tabulky</span><span class="sxs-lookup"><span data-stu-id="04009-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="04009-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="04009-168">left-aligned column</span></span>  | <span data-ttu-id="04009-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="04009-169">right-aligned column</span></span> | <span data-ttu-id="04009-170">centered column</span><span class="sxs-lookup"><span data-stu-id="04009-170">centered column</span></span> |
| <span data-ttu-id="04009-171">$100</span><span class="sxs-lookup"><span data-stu-id="04009-171">$100</span></span>                 | <span data-ttu-id="04009-172">$100</span><span class="sxs-lookup"><span data-stu-id="04009-172">$100</span></span>                 | <span data-ttu-id="04009-173">$100</span><span class="sxs-lookup"><span data-stu-id="04009-173">$100</span></span>            |
| <span data-ttu-id="04009-174">$10</span><span class="sxs-lookup"><span data-stu-id="04009-174">$10</span></span>                  | <span data-ttu-id="04009-175">$10</span><span class="sxs-lookup"><span data-stu-id="04009-175">$10</span></span>                  | <span data-ttu-id="04009-176">$10</span><span class="sxs-lookup"><span data-stu-id="04009-176">$10</span></span>             |
| <span data-ttu-id="04009-177">$1</span><span class="sxs-lookup"><span data-stu-id="04009-177">$1</span></span>                   | <span data-ttu-id="04009-178">$1</span><span class="sxs-lookup"><span data-stu-id="04009-178">$1</span></span>                   | <span data-ttu-id="04009-179">$1</span><span class="sxs-lookup"><span data-stu-id="04009-179">$1</span></span>              |

<span data-ttu-id="04009-180">Další informace o vytváření tabulek:</span><span class="sxs-lookup"><span data-stu-id="04009-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="04009-181">[Uspořádání informací pomocí tabulek](https://help.github.com/articles/organizing-information-with-tables/) v GitHubu</span><span class="sxs-lookup"><span data-stu-id="04009-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="04009-182">Webová aplikace [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) (Generátor tabulek v Markdownu)</span><span class="sxs-lookup"><span data-stu-id="04009-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="04009-183">[Markdown Cheatsheet (Tahák pro Markdown) od Adama Pritcharda](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span><span class="sxs-lookup"><span data-stu-id="04009-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="04009-184">[Markdown Extra od Michela Fortina](https://michelf.ca/projects/php-markdown/extra/#table)</span><span class="sxs-lookup"><span data-stu-id="04009-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="04009-185">[Převedení HTML tabulek na Markdown](https://jmalarcon.github.io/markdowntables/)</span><span class="sxs-lookup"><span data-stu-id="04009-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="04009-186">Odkazy</span><span class="sxs-lookup"><span data-stu-id="04009-186">Links</span></span>

<span data-ttu-id="04009-187">Syntaxe Markdownu pro vložený odkaz se skládá z části `[link text]`, což je text, který bude tvořit hypertextový odkaz, následované částí `(file-name.md)`, což je adresa URL nebo název souboru, na které se odkazuje:</span><span class="sxs-lookup"><span data-stu-id="04009-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="04009-188">Další informace o tvorbě odkazů:</span><span class="sxs-lookup"><span data-stu-id="04009-188">For more information on linking, see:</span></span>

- <span data-ttu-id="04009-189">Podrobnosti o základní podpoře odkazů v Markdownu najdete v [průvodci syntaxí Markdownu](https://daringfireball.net/projects/markdown/syntax#link).</span><span class="sxs-lookup"><span data-stu-id="04009-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="04009-190">Podrobnosti o další syntaxi odkazů, které nabízí Markdig, najdete v oddílu [Odkazy](how-to-write-links.md) tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="04009-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="04009-191">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="04009-191">Code snippets</span></span>

<span data-ttu-id="04009-192">Markdown podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="04009-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="04009-193">Podrobnosti najdete tady:</span><span class="sxs-lookup"><span data-stu-id="04009-193">For details, see:</span></span>

- [<span data-ttu-id="04009-194">Nativní podpora bloků kódu v Markdownu</span><span class="sxs-lookup"><span data-stu-id="04009-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="04009-195">Podpora ohraničení kódu a zvýraznění syntaxe v GFM</span><span class="sxs-lookup"><span data-stu-id="04009-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="04009-196">Ohraničené bloky kódu představují snadný způsob, jak umožnit zvýraznění syntaxe pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="04009-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="04009-197">Obecný formát ohraničených bloků kódu je:</span><span class="sxs-lookup"><span data-stu-id="04009-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="04009-198">Alias za prvními třemi znaky „\`“ definuje použité zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="04009-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="04009-199">Tady je seznam běžně používaných programovacích jazyků v obsahu na webu Docs a příslušných popisků:</span><span class="sxs-lookup"><span data-stu-id="04009-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="04009-200">Tyto jazyky podporují popisné názvy a většina z nich umožňuje zvýrazňování jazyka.</span><span class="sxs-lookup"><span data-stu-id="04009-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="04009-201">Název</span><span class="sxs-lookup"><span data-stu-id="04009-201">Name</span></span>|<span data-ttu-id="04009-202">Popisek Markdownu</span><span class="sxs-lookup"><span data-stu-id="04009-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="04009-203">Konzola .NET</span><span class="sxs-lookup"><span data-stu-id="04009-203">.NET Console</span></span>|<span data-ttu-id="04009-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="04009-204">dotnetcli</span></span>|
|<span data-ttu-id="04009-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="04009-205">ASP.NET (C#)</span></span>|<span data-ttu-id="04009-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="04009-206">aspx-csharp</span></span>|
|<span data-ttu-id="04009-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="04009-207">ASP.NET (VB)</span></span>|<span data-ttu-id="04009-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="04009-208">aspx-vb</span></span>|
|<span data-ttu-id="04009-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="04009-209">AzCopy</span></span>|<span data-ttu-id="04009-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="04009-210">azcopy</span></span>|
|<span data-ttu-id="04009-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="04009-211">Azure CLI</span></span>|<span data-ttu-id="04009-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="04009-212">azurecli</span></span>|
|<span data-ttu-id="04009-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="04009-213">Azure PowerShell</span></span>|<span data-ttu-id="04009-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="04009-214">azurepowershell</span></span>|
|<span data-ttu-id="04009-215">Bash</span><span class="sxs-lookup"><span data-stu-id="04009-215">Bash</span></span>|<span data-ttu-id="04009-216">bash</span><span class="sxs-lookup"><span data-stu-id="04009-216">bash</span></span>|
|<span data-ttu-id="04009-217">C++</span><span class="sxs-lookup"><span data-stu-id="04009-217">C++</span></span>|<span data-ttu-id="04009-218">cpp</span><span class="sxs-lookup"><span data-stu-id="04009-218">cpp</span></span>|
|<span data-ttu-id="04009-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="04009-219">C++/CX</span></span>|<span data-ttu-id="04009-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="04009-220">cppcx</span></span>|
|<span data-ttu-id="04009-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="04009-221">C++/WinRT</span></span>|<span data-ttu-id="04009-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="04009-222">cppwinrt</span></span>|
|<span data-ttu-id="04009-223">C#</span><span class="sxs-lookup"><span data-stu-id="04009-223">C#</span></span>|<span data-ttu-id="04009-224">csharp</span><span class="sxs-lookup"><span data-stu-id="04009-224">csharp</span></span>|
|<span data-ttu-id="04009-225">C# v prohlížeči</span><span class="sxs-lookup"><span data-stu-id="04009-225">C# in browser</span></span>|<span data-ttu-id="04009-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="04009-226">csharp-interactive</span></span>|
|<span data-ttu-id="04009-227">Konzola</span><span class="sxs-lookup"><span data-stu-id="04009-227">Console</span></span>|<span data-ttu-id="04009-228">konzola</span><span class="sxs-lookup"><span data-stu-id="04009-228">console</span></span>|
|<span data-ttu-id="04009-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="04009-229">CSHTML</span></span>|<span data-ttu-id="04009-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="04009-230">cshtml</span></span>|
|<span data-ttu-id="04009-231">DAX</span><span class="sxs-lookup"><span data-stu-id="04009-231">DAX</span></span>|<span data-ttu-id="04009-232">dax</span><span class="sxs-lookup"><span data-stu-id="04009-232">dax</span></span>|
|<span data-ttu-id="04009-233">Docker</span><span class="sxs-lookup"><span data-stu-id="04009-233">Docker</span></span>|<span data-ttu-id="04009-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="04009-234">dockerfile</span></span>|
|<span data-ttu-id="04009-235">F#</span><span class="sxs-lookup"><span data-stu-id="04009-235">F#</span></span>|<span data-ttu-id="04009-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="04009-236">fsharp</span></span>|
|<span data-ttu-id="04009-237">Go</span><span class="sxs-lookup"><span data-stu-id="04009-237">Go</span></span>|<span data-ttu-id="04009-238">go</span><span class="sxs-lookup"><span data-stu-id="04009-238">go</span></span>|
|<span data-ttu-id="04009-239">HTML</span><span class="sxs-lookup"><span data-stu-id="04009-239">HTML</span></span>|<span data-ttu-id="04009-240">html</span><span class="sxs-lookup"><span data-stu-id="04009-240">html</span></span>|
|<span data-ttu-id="04009-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="04009-241">HTTP</span></span>|<span data-ttu-id="04009-242">http</span><span class="sxs-lookup"><span data-stu-id="04009-242">http</span></span>|
|<span data-ttu-id="04009-243">Java</span><span class="sxs-lookup"><span data-stu-id="04009-243">Java</span></span>|<span data-ttu-id="04009-244">java</span><span class="sxs-lookup"><span data-stu-id="04009-244">java</span></span>|
|<span data-ttu-id="04009-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04009-245">JavaScript</span></span>|<span data-ttu-id="04009-246">javascript</span><span class="sxs-lookup"><span data-stu-id="04009-246">javascript</span></span>|
|<span data-ttu-id="04009-247">JSON</span><span class="sxs-lookup"><span data-stu-id="04009-247">JSON</span></span>|<span data-ttu-id="04009-248">json</span><span class="sxs-lookup"><span data-stu-id="04009-248">json</span></span>|
|<span data-ttu-id="04009-249">Dotazovací jazyk Kusto</span><span class="sxs-lookup"><span data-stu-id="04009-249">Kusto Query Language</span></span>|<span data-ttu-id="04009-250">kusto</span><span class="sxs-lookup"><span data-stu-id="04009-250">kusto</span></span>|
|<span data-ttu-id="04009-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="04009-251">Markdown</span></span>|<span data-ttu-id="04009-252">md</span><span class="sxs-lookup"><span data-stu-id="04009-252">md</span></span>|
|<span data-ttu-id="04009-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="04009-253">Objective-C</span></span>|<span data-ttu-id="04009-254">objc</span><span class="sxs-lookup"><span data-stu-id="04009-254">objc</span></span>|
|<span data-ttu-id="04009-255">OData</span><span class="sxs-lookup"><span data-stu-id="04009-255">OData</span></span>|<span data-ttu-id="04009-256">odata</span><span class="sxs-lookup"><span data-stu-id="04009-256">odata</span></span>|
|<span data-ttu-id="04009-257">PHP</span><span class="sxs-lookup"><span data-stu-id="04009-257">PHP</span></span>|<span data-ttu-id="04009-258">php</span><span class="sxs-lookup"><span data-stu-id="04009-258">php</span></span>|
|<span data-ttu-id="04009-259">PowerApps (oddělovač desetinných míst v podobě tečky)</span><span class="sxs-lookup"><span data-stu-id="04009-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="04009-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="04009-260">powerapps-dot</span></span>|
|<span data-ttu-id="04009-261">PowerApps (oddělovač desetinných míst v podobě čárky)</span><span class="sxs-lookup"><span data-stu-id="04009-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="04009-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="04009-262">powerapps-comma</span></span>|
|<span data-ttu-id="04009-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="04009-263">PowerShell</span></span>|<span data-ttu-id="04009-264">powershell</span><span class="sxs-lookup"><span data-stu-id="04009-264">powershell</span></span>|
|<span data-ttu-id="04009-265">Python</span><span class="sxs-lookup"><span data-stu-id="04009-265">Python</span></span>|<span data-ttu-id="04009-266">python</span><span class="sxs-lookup"><span data-stu-id="04009-266">python</span></span>|
|<span data-ttu-id="04009-267">Q#</span><span class="sxs-lookup"><span data-stu-id="04009-267">Q#</span></span>|<span data-ttu-id="04009-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="04009-268">qsharp</span></span>|
|<span data-ttu-id="04009-269">R</span><span class="sxs-lookup"><span data-stu-id="04009-269">R</span></span>|<span data-ttu-id="04009-270">r</span><span class="sxs-lookup"><span data-stu-id="04009-270">r</span></span>|
|<span data-ttu-id="04009-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="04009-271">Ruby</span></span>|<span data-ttu-id="04009-272">ruby</span><span class="sxs-lookup"><span data-stu-id="04009-272">ruby</span></span>|
|<span data-ttu-id="04009-273">SQL</span><span class="sxs-lookup"><span data-stu-id="04009-273">SQL</span></span>|<span data-ttu-id="04009-274">sql</span><span class="sxs-lookup"><span data-stu-id="04009-274">sql</span></span>|
|<span data-ttu-id="04009-275">Swift</span><span class="sxs-lookup"><span data-stu-id="04009-275">Swift</span></span>|<span data-ttu-id="04009-276">swift</span><span class="sxs-lookup"><span data-stu-id="04009-276">swift</span></span>|
|<span data-ttu-id="04009-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="04009-277">TypeScript</span></span>|<span data-ttu-id="04009-278">typescript</span><span class="sxs-lookup"><span data-stu-id="04009-278">typescript</span></span>|
|<span data-ttu-id="04009-279">VB</span><span class="sxs-lookup"><span data-stu-id="04009-279">VB</span></span>|<span data-ttu-id="04009-280">vb</span><span class="sxs-lookup"><span data-stu-id="04009-280">vb</span></span>|
|<span data-ttu-id="04009-281">XAML</span><span class="sxs-lookup"><span data-stu-id="04009-281">XAML</span></span>|<span data-ttu-id="04009-282">xaml</span><span class="sxs-lookup"><span data-stu-id="04009-282">xaml</span></span>|
|<span data-ttu-id="04009-283">XML</span><span class="sxs-lookup"><span data-stu-id="04009-283">XML</span></span>|<span data-ttu-id="04009-284">xml</span><span class="sxs-lookup"><span data-stu-id="04009-284">xml</span></span>|

<span data-ttu-id="04009-285">Název `csharp-interactive` určuje jazyk C# a možnost spuštění ukázek v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="04009-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="04009-286">Tyto fragmenty kódu se kompilují a spouští v kontejneru Dockeru a výsledky spuštění tohoto programu se zobrazují v okně prohlížeče uživatele.</span><span class="sxs-lookup"><span data-stu-id="04009-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="04009-287">Příklad: C\#</span><span class="sxs-lookup"><span data-stu-id="04009-287">Example: C\#</span></span>

<span data-ttu-id="04009-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="04009-288">__Markdown__</span></span>

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

<span data-ttu-id="04009-289">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="04009-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="04009-290">Příklad: SQL</span><span class="sxs-lookup"><span data-stu-id="04009-290">Example: SQL</span></span>

<span data-ttu-id="04009-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="04009-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="04009-292">__Vykreslení__</span><span class="sxs-lookup"><span data-stu-id="04009-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="04009-293">Vlastní rozšíření Markdownu pro Docs</span><span class="sxs-lookup"><span data-stu-id="04009-293">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="04009-294">Docs.Microsoft.com (Docs) implementuje analyzátor Markdig Parser pro Markdown, který je ve velké míře kompatibilní s rozšířením GitHub Flavored Markdown (GFM).</span><span class="sxs-lookup"><span data-stu-id="04009-294">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="04009-295">Markdig přidává v rozšířeních Markdownu některé další funkce.</span><span class="sxs-lookup"><span data-stu-id="04009-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="04009-296">Tento průvodce tak jako referenční informace zahrnuje vybrané články z úplného průvodce vytvářením obsahu OPS.</span><span class="sxs-lookup"><span data-stu-id="04009-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="04009-297">(Podívejte se v obsahu například na „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“.)</span><span class="sxs-lookup"><span data-stu-id="04009-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="04009-298">Články Docs používají GFM na většinu formátování, jako jsou odstavce, odkazy, seznamy a nadpisy.</span><span class="sxs-lookup"><span data-stu-id="04009-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="04009-299">Ke složitějšímu formátování článků můžete používat třeba tyto funkce Markdigu:</span><span class="sxs-lookup"><span data-stu-id="04009-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="04009-300">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="04009-300">Note blocks</span></span>
- <span data-ttu-id="04009-301">Vložené soubory</span><span class="sxs-lookup"><span data-stu-id="04009-301">Include files</span></span>
- <span data-ttu-id="04009-302">Voliče</span><span class="sxs-lookup"><span data-stu-id="04009-302">Selectors</span></span>
- <span data-ttu-id="04009-303">Vložená videa</span><span class="sxs-lookup"><span data-stu-id="04009-303">Embedded videos</span></span>
- <span data-ttu-id="04009-304">Fragmenty/ukázky kódu</span><span class="sxs-lookup"><span data-stu-id="04009-304">Code snippets/samples</span></span>

<span data-ttu-id="04009-305">Kompletní seznam funkcí najdete v tématech „Rozšíření Markdig a Markdown“ a „Fragmenty kódu“ v obsahu.</span><span class="sxs-lookup"><span data-stu-id="04009-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="04009-306">Bloky poznámek</span><span class="sxs-lookup"><span data-stu-id="04009-306">Note blocks</span></span>

<span data-ttu-id="04009-307">Můžete vybírat ze čtyř typů bloků poznámek k přitažení pozornosti ke konkrétnímu obsahu:</span><span class="sxs-lookup"><span data-stu-id="04009-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="04009-308">NOTE (POZNÁMKA)</span><span class="sxs-lookup"><span data-stu-id="04009-308">NOTE</span></span>
- <span data-ttu-id="04009-309">WARNING (VAROVÁNÍ)</span><span class="sxs-lookup"><span data-stu-id="04009-309">WARNING</span></span>
- <span data-ttu-id="04009-310">TIP</span><span class="sxs-lookup"><span data-stu-id="04009-310">TIP</span></span>
- <span data-ttu-id="04009-311">IMPORTANT (DŮLEŽITÉ)</span><span class="sxs-lookup"><span data-stu-id="04009-311">IMPORTANT</span></span>

<span data-ttu-id="04009-312">Obecně by se bloky poznámek měly používat střídmě, protože můžou působit rušivě.</span><span class="sxs-lookup"><span data-stu-id="04009-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="04009-313">I když bloky poznámek podporují také bloky kódu, obrázky, seznamy a odkazy, snažte se, aby byly jednoduché a nekomplikované.</span><span class="sxs-lookup"><span data-stu-id="04009-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="04009-314">Příklady:</span><span class="sxs-lookup"><span data-stu-id="04009-314">Examples:</span></span>

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

<span data-ttu-id="04009-315">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="04009-315">These alerts look like this on docs.microsoft.com:</span></span>

![Ukazuje, jak výstrahy v předchozím příkladu vypadají na publikované stránce Docs s různými ikonami a barvami.](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="04009-317">Soubory k zahrnutí</span><span class="sxs-lookup"><span data-stu-id="04009-317">Include files</span></span>

<span data-ttu-id="04009-318">Pokud máte opakovaně použitelný text nebo soubory obrázků, které chcete zahrnout do souborů s články, použijte odkaz na zahrnutý soubor prostřednictvím funkce Markdigu pro zahrnutí souboru.</span><span class="sxs-lookup"><span data-stu-id="04009-318">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="04009-319">Tato funkce platformě OPS říká, aby daný soubor zahrnula do vašeho souboru článku při jeho vytvoření, a soubor se tak stal součástí vašeho publikovaného článku.</span><span class="sxs-lookup"><span data-stu-id="04009-319">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="04009-320">K dispozici jsou tři typy odkazů pro zahrnutí, které vám pomůžou znovu použít obsah:</span><span class="sxs-lookup"><span data-stu-id="04009-320">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="04009-321">Vložení: Umožňuje znovu použít běžný vložený fragment textu v jiné větě.</span><span class="sxs-lookup"><span data-stu-id="04009-321">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="04009-322">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="04009-322">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="04009-323">Obrázek: Takto se v Docs implementuje standardní zahrnutí obrázků.</span><span class="sxs-lookup"><span data-stu-id="04009-323">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="04009-324">Soubor k zahrnutí typu Vložení nebo Blok je jenom prostý soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="04009-324">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="04009-325">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="04009-325">It can contain any valid Markdown.</span></span> <span data-ttu-id="04009-326">Všechny soubory zahrnutí Markdownu musí být umístěné ve [společném podadresáři `/includes`](git-github-fundamentals.md#includes-subdirectory) v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="04009-326">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="04009-327">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="04009-327">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="04009-328">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="04009-328">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="04009-329">Soubor k zahrnutí použijte, kdykoli potřebujete, aby se stejný text zobrazoval ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="04009-329">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="04009-330">Odkazy pro zahrnutí typu Blok používejte pro větší obsah, třeba pro jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="04009-330">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="04009-331">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="04009-331">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="04009-332">Odkazy pro zahrnutí se nebudou vykreslovat v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních Markdigu.</span><span class="sxs-lookup"><span data-stu-id="04009-332">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="04009-333">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="04009-333">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="04009-334">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor k zahrnutí odkazuje.</span><span class="sxs-lookup"><span data-stu-id="04009-334">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="04009-335">Ignorováním tohoto pravidla vznikne nepřeložitelný řetězec, který naruší lokalizované použití.</span><span class="sxs-lookup"><span data-stu-id="04009-335">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="04009-336">Nevkládejte odkazy pro zahrnutí do jiných souborů k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="04009-336">Don't embed include references within other include files.</span></span> <span data-ttu-id="04009-337">Není to podporováno.</span><span class="sxs-lookup"><span data-stu-id="04009-337">They are not supported.</span></span>
- <span data-ttu-id="04009-338">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="04009-338">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="04009-339">Adresář multimédií nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="04009-339">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="04009-340">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář multimédií není potřeba.</span><span class="sxs-lookup"><span data-stu-id="04009-340">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="04009-341">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="04009-341">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="04009-342">Pro každý soubor k zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="04009-342">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="04009-343">Multimediální soubor uložte do složky multimédií spojené s příslušným souborem k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="04009-343">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="04009-344">Nepoužívejte soubor k zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="04009-344">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="04009-345">Soubory k zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="04009-345">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="04009-346">Příklad:</span><span class="sxs-lookup"><span data-stu-id="04009-346">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="04009-347">Voliče</span><span class="sxs-lookup"><span data-stu-id="04009-347">Selectors</span></span>

<span data-ttu-id="04009-348">Voliče používejte v technických článcích, když vytváříte více variant stejného článku, které objasňují rozdíly v implementaci mezi různými technologiemi nebo platformami.</span><span class="sxs-lookup"><span data-stu-id="04009-348">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="04009-349">Typicky se to nejvíce hodí na náš obsah pro mobilní platformy pro vývojáře.</span><span class="sxs-lookup"><span data-stu-id="04009-349">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="04009-350">V Markdigu jsou v současnosti dva různé typy voličů: jednoduchý a vícenásobný.</span><span class="sxs-lookup"><span data-stu-id="04009-350">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="04009-351">Protože do každého článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="04009-351">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="04009-352">Pak můžete na daný soubor k zahrnutí odkázat ve všech článcích, které stejný volič používají.</span><span class="sxs-lookup"><span data-stu-id="04009-352">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="04009-353">Příklad voliče můžete vidět zde:</span><span class="sxs-lookup"><span data-stu-id="04009-353">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="04009-354">Příklad toho, jak se voliče používají v praxi, můžete vidět v [dokumentaci k Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="04009-354">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="04009-355">Odkazy pro zahrnutí kódu</span><span class="sxs-lookup"><span data-stu-id="04009-355">Code include references</span></span>

<span data-ttu-id="04009-356">Markdig podporuje rozšířené zahrnutí kódu do článku prostřednictvím rozšíření pro fragmenty kódu.</span><span class="sxs-lookup"><span data-stu-id="04009-356">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="04009-357">To poskytuje pokročilé vykreslení, které vychází z funkcí GFM, jako například výběr programovacího jazyka a barvy syntaxe. Navíc nabízí užitečné funkce jako:</span><span class="sxs-lookup"><span data-stu-id="04009-357">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="04009-358">Zahrnutí centralizovaných ukázek/fragmentů kódu z externího úložiště</span><span class="sxs-lookup"><span data-stu-id="04009-358">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="04009-359">Uživatelské rozhraní s kartami k zobrazení více verzí ukázek kódu v různých jazycích</span><span class="sxs-lookup"><span data-stu-id="04009-359">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="04009-360">Možná úskalí a řešení potíží</span><span class="sxs-lookup"><span data-stu-id="04009-360">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="04009-361">Alternativní text</span><span class="sxs-lookup"><span data-stu-id="04009-361">Alt text</span></span>

<span data-ttu-id="04009-362">Alternativní text, který obsahuje podtržítka, se správně nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="04009-362">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="04009-363">Třeba místo použití tohoto:</span><span class="sxs-lookup"><span data-stu-id="04009-363">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="04009-364">Napište takto před podtržítka zpětné lomítko:</span><span class="sxs-lookup"><span data-stu-id="04009-364">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="04009-365">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="04009-365">Apostrophes and quotation marks</span></span>

<span data-ttu-id="04009-366">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="04009-366">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="04009-367">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="04009-367">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="04009-368">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="04009-368">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="04009-369">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="04009-369">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="04009-370">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="04009-370">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="04009-371">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="04009-371">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="04009-372">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="04009-372">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="04009-373">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="04009-373">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="04009-374">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="04009-374">Angle brackets</span></span>

<span data-ttu-id="04009-375">K označování zástupných symbolů se běžně používají ostré závorky.</span><span class="sxs-lookup"><span data-stu-id="04009-375">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="04009-376">Když to uděláte v textu (nikoli v kódu), musíte ostré závorky zakódovat.</span><span class="sxs-lookup"><span data-stu-id="04009-376">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="04009-377">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="04009-377">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="04009-378">Například `<script name>` přepište kódem jako `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="04009-378">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="04009-379">Varianta Markdownu</span><span class="sxs-lookup"><span data-stu-id="04009-379">Markdown flavor</span></span>

<span data-ttu-id="04009-380">Backend webu docs.microsoft.com podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="04009-380">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="04009-381">Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat.</span><span class="sxs-lookup"><span data-stu-id="04009-381">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="04009-382">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="04009-382">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="04009-383">Viz také:</span><span class="sxs-lookup"><span data-stu-id="04009-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="04009-384">Prostředky pro Markdown</span><span class="sxs-lookup"><span data-stu-id="04009-384">Markdown resources</span></span>

- [<span data-ttu-id="04009-385">Úvod do Markdownu</span><span class="sxs-lookup"><span data-stu-id="04009-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="04009-386">Tahák pro Markdown v Docs</span><span class="sxs-lookup"><span data-stu-id="04009-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="04009-387">Základy Markdownu v GitHubu</span><span class="sxs-lookup"><span data-stu-id="04009-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="04009-388">Příručka pro Markdown</span><span class="sxs-lookup"><span data-stu-id="04009-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
