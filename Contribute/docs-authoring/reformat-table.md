---
title: Přeformátování tabulek Markdownu – Balíček pro vytváření obsahu na webu Docs
description: Přečtěte si, jak používat různé funkce pro formátování tabulek Markdownu v balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336766"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="967ae-103">Přeformátování tabulek Markdownu</span><span class="sxs-lookup"><span data-stu-id="967ae-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="967ae-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="967ae-104">Summary</span></span>

<span data-ttu-id="967ae-105">Když v souboru Markdownu ( *\*.md*) vyberete celou tabulku, zobrazí se dvě položky místní nabídky pro formátování tabulky.</span><span class="sxs-lookup"><span data-stu-id="967ae-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="967ae-106">Klikněte pravým tlačítkem myši na vybranou tabulku Markdownu a otevřete místní nabídku.</span><span class="sxs-lookup"><span data-stu-id="967ae-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="967ae-107">Zobrazí se nabídka s položkami podobná této:</span><span class="sxs-lookup"><span data-stu-id="967ae-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Místní nabídka pro přeformátování tabulky":::

> [!TIP]
> <span data-ttu-id="967ae-109">Tuto funkci **není možné** použít v případě, že je vybráno více tabulek Markdownu. Slouží pro úpravy jen jedné tabulky.</span><span class="sxs-lookup"><span data-stu-id="967ae-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="967ae-110">Aby fungovala správně, je také potřeba vybrat celou tabulku včetně záhlaví.</span><span class="sxs-lookup"><span data-stu-id="967ae-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="967ae-111">Consolidate selected table</span><span class="sxs-lookup"><span data-stu-id="967ae-111">Consolidate selected table</span></span>

<span data-ttu-id="967ae-112">Když vyberete možnost **Consolidate selected table** (Konsolidovat vybranou tabulku), sbalí se záhlaví a obsah tabulky tak, že se po obou stranách každé hodnoty bude nacházet jen jedna mezera.</span><span class="sxs-lookup"><span data-stu-id="967ae-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="967ae-113">Evenly distribute selected table</span><span class="sxs-lookup"><span data-stu-id="967ae-113">Evenly distribute selected table</span></span>

<span data-ttu-id="967ae-114">Když vyberete možnost **Evenly distribute selected table** (Rovnoměrně rozmístit vybranou tabulku), vypočítá se v každém sloupci nejdelší hodnota a všechny ostatní hodnoty se odpovídajícím způsobem rozmístí pomocí mezer.</span><span class="sxs-lookup"><span data-stu-id="967ae-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="967ae-115">Důležité informace</span><span class="sxs-lookup"><span data-stu-id="967ae-115">Considerations</span></span>

<span data-ttu-id="967ae-116">Tato funkce nemá vliv na vykreslování tabulky, ale zlepšuje její čitelnost, takže se tabulka lépe udržuje.</span><span class="sxs-lookup"><span data-stu-id="967ae-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="967ae-117">Zarovnání sloupců tabulky zůstane beze změny.</span><span class="sxs-lookup"><span data-stu-id="967ae-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="967ae-118">Podívejte se například na tuto tabulku:</span><span class="sxs-lookup"><span data-stu-id="967ae-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="967ae-119">Po „rovnoměrném rozmístění“:</span><span class="sxs-lookup"><span data-stu-id="967ae-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="967ae-120">Po „konsolidaci“:</span><span class="sxs-lookup"><span data-stu-id="967ae-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="967ae-121">V praxi</span><span class="sxs-lookup"><span data-stu-id="967ae-121">In action</span></span>

<span data-ttu-id="967ae-122">Tady vidíte krátkou ukázku této funkce:</span><span class="sxs-lookup"><span data-stu-id="967ae-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="967ae-123">[![Ukázka přeformátování tabulky](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="967ae-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
