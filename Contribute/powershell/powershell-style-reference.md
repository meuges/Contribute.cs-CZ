---
title: Zvláštní pokyny týkající se psaní referenčních rutin
description: V tomto článku jsou zvláštní pravidla platná pro formátování vzorového kódu v PowerShellu. Pravidla platí pro obecné články s příklady i pro referenční rutiny.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290281"
---
# <a name="updating-reference-articles"></a><span data-ttu-id="bd3a1-104">Aktualizace referenčních článků</span><span class="sxs-lookup"><span data-stu-id="bd3a1-104">Updating reference articles</span></span>

<span data-ttu-id="bd3a1-105">Články s referenčními rutinami mají zvláštní strukturu.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="bd3a1-106">Tuto strukturu definuje [PlatyPS][].</span><span class="sxs-lookup"><span data-stu-id="bd3a1-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="bd3a1-107">PlatyPS je nástroj, který se používá ke generování nápovědy k rutinám v modulech PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="bd3a1-108">PlatyPS vytvoří pro rutinu základní soubor Markdown.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="bd3a1-109">Po úpravě souborů Markdown se PlatyPS použije k vytvoření souborů nápovědy MAML používaných rutinou `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="bd3a1-110">V PlatyPS je pevně naprogramované schéma referenčních rutin zapsaných do kódu.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="bd3a1-111">Dokument [platyPS.schema.md][] se pokouší tuto strukturu popsat.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="bd3a1-112">Při porušení schématu dochází k chybám sestavení, které je potřeba opravit, abychom mohli příspěvek přijmout.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="bd3a1-113">Obecné pokyny</span><span class="sxs-lookup"><span data-stu-id="bd3a1-113">General guidelines</span></span>

- <span data-ttu-id="bd3a1-114">Neodebírejte žádné struktury záhlaví.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="bd3a1-115">PlatyPS očekává zvláštní sadu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="bd3a1-116">Záhlaví **Input type** (Typ vstupu) a **Output type** (Typ výstupu) musí být určitého typu.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="bd3a1-117">Pokud rutina nemá vstup nebo nevrací hodnotu, použijte hodnotu „None“ (Žádný).</span><span class="sxs-lookup"><span data-stu-id="bd3a1-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="bd3a1-118">Oplocené bloky kódu jsou povolené jenom v oddílu [Příklady](#format-for-examples).</span><span class="sxs-lookup"><span data-stu-id="bd3a1-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="bd3a1-119">Vložené části kódu můžete použít v kterémkoli odstavci.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="bd3a1-120">Formátování souborů About_</span><span class="sxs-lookup"><span data-stu-id="bd3a1-120">Formatting About_ files</span></span>

<span data-ttu-id="bd3a1-121">Soubory `About_*` nyní zpracovává převaděč [Pandoc][] místo nástroje PlatyPS.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="bd3a1-122">Soubory `About_*` jsou formátované tak, aby byly zajistily co největší kompatibilitu se všemi verzemi PowerShellu a publikačními nástroji.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="bd3a1-123">Neměňte prosím formátování souborů `about_*`, aniž byste se přihlásili jako údržbáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="bd3a1-124">Základní pravidla formátování:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="bd3a1-125">Omezte řádky na 80 znaků.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="bd3a1-126">Bloky kódu, uvozovky bloku a tabulky jsou omezené na 76 znaků, protože Pandoc tyto části při převodu odsadí o čtyři mezery.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="bd3a1-127">Tabulky se musejí vejít do 76 znaků.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="bd3a1-128">Ručně zabalte obsah buněk, který je na více řádků.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="bd3a1-129">Na každém řádku používejte úvodní a závěrečné znaky `|`.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="bd3a1-130">Funkční příklad viz [about_Comparison_Operators][about-example].</span><span class="sxs-lookup"><span data-stu-id="bd3a1-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="bd3a1-131">Při použití speciálních znaků `\`, `$`, `` ` `` a `<` převaděče Pandoc:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="bd3a1-132">V záhlaví musí být tyto znaky uvozeny počátečním znakem `\`.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="bd3a1-133">V odstavci musí být tyto znaky dány do rozsahů kódu.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="bd3a1-134">Například:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="bd3a1-135">Formátování příkladů</span><span class="sxs-lookup"><span data-stu-id="bd3a1-135">Format for examples</span></span>

<span data-ttu-id="bd3a1-136">Ve schématu PlatyPS je záhlaví **EXAMPLES** v záhlaví H2 a každý příklad představuje záhlaví H3.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="bd3a1-137">V příkladu schéma nedovoluje, aby byly bloky kódu odděleny odstavci.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="bd3a1-138">Platné schéma:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="bd3a1-139">Očíslujte každý příklad a přidejte stručný nadpis.</span><span class="sxs-lookup"><span data-stu-id="bd3a1-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="bd3a1-140">Například:</span><span class="sxs-lookup"><span data-stu-id="bd3a1-140">For example:</span></span>

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org