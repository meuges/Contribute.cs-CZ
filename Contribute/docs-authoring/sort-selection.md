---
title: Výběr řazení – Balíček pro vytváření obsahu na webu Docs
description: Přečtěte si, jak používat funkci Výběr řazení v balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336743"
---
# <a name="sort-selection"></a><span data-ttu-id="4930d-103">Řazení výběru</span><span class="sxs-lookup"><span data-stu-id="4930d-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="4930d-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="4930d-104">Summary</span></span>

<span data-ttu-id="4930d-105">Pokud v souboru Markdownu ( *\*.md*) provedete výběr, zobrazí se dvě položky místní nabídky.</span><span class="sxs-lookup"><span data-stu-id="4930d-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="4930d-106">Klikněte pravým tlačítkem myši na vybraný text a otevřete místní nabídku.</span><span class="sxs-lookup"><span data-stu-id="4930d-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="4930d-107">Zobrazí se nabídka s položkami podobná této:</span><span class="sxs-lookup"><span data-stu-id="4930d-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Místní nabídka pro výběr řazení":::

> [!TIP]
> <span data-ttu-id="4930d-109">Položky místní nabídky pro výběr řazení zůstávají skryté až do doby, než v textovém editoru sady Visual Studio Code provedete platný výběr.</span><span class="sxs-lookup"><span data-stu-id="4930d-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="4930d-110">Sort selection ascending (A to Z)</span><span class="sxs-lookup"><span data-stu-id="4930d-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="4930d-111">Když vyberete možnost **Sort selection ascending (A to Z)** (Seřadit výběr vzestupně (od A do Z)), seřadí se celý výběr ve vzestupném pořadí, a to abecedně od A do Z.</span><span class="sxs-lookup"><span data-stu-id="4930d-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="4930d-112">Sort selection descending (Z to A)</span><span class="sxs-lookup"><span data-stu-id="4930d-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="4930d-113">Když vyberete možnost **Sort selection descending (Z to A)** (Seřadit výběr sestupně (od Z do A)), seřadí se celý výběr v sestupném pořadí, a to abecedně od Z do A.</span><span class="sxs-lookup"><span data-stu-id="4930d-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="4930d-114">Důležité informace</span><span class="sxs-lookup"><span data-stu-id="4930d-114">Considerations</span></span>

<span data-ttu-id="4930d-115">Podkladový mechanismus využívá řazení v *přirozeném jazyce*.</span><span class="sxs-lookup"><span data-stu-id="4930d-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="4930d-116">To je výkonnější a komplexnější než standardní řazení.</span><span class="sxs-lookup"><span data-stu-id="4930d-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="4930d-117">Podívejte se například na tuto tabulku:</span><span class="sxs-lookup"><span data-stu-id="4930d-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="4930d-118">Bez řazení v přirozeném jazyce by bylo pořadí sloupce `Column1` 1, 11, 2 atd. Mechanismus ale chápe, že 11 je větší než 2, takže seřadí položky vzestupně tímto způsobem:</span><span class="sxs-lookup"><span data-stu-id="4930d-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="4930d-119">V praxi</span><span class="sxs-lookup"><span data-stu-id="4930d-119">In action</span></span>

<span data-ttu-id="4930d-120">Tady vidíte krátkou ukázku této funkce:</span><span class="sxs-lookup"><span data-stu-id="4930d-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="4930d-121">[![Ukázka výběru řazení](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="4930d-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
