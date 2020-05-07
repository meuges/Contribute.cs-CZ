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
# <a name="sort-selection"></a>Řazení výběru

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

Pokud v souboru Markdownu ( *\*.md*) provedete výběr, zobrazí se dvě položky místní nabídky. Klikněte pravým tlačítkem myši na vybraný text a otevřete místní nabídku. Zobrazí se nabídka s položkami podobná této:

:::image type="content" source="media/sort-selection-menu.png" alt-text="Místní nabídka pro výběr řazení":::

> [!TIP]
> Položky místní nabídky pro výběr řazení zůstávají skryté až do doby, než v textovém editoru sady Visual Studio Code provedete platný výběr.

## <a name="sort-selection-ascending-a-to-z"></a>Sort selection ascending (A to Z)

Když vyberete možnost **Sort selection ascending (A to Z)** (Seřadit výběr vzestupně (od A do Z)), seřadí se celý výběr ve vzestupném pořadí, a to abecedně od A do Z.

## <a name="sort-selection-descending-z-to-a"></a>Sort selection descending (Z to A)

Když vyberete možnost **Sort selection descending (Z to A)** (Seřadit výběr sestupně (od Z do A)), seřadí se celý výběr v sestupném pořadí, a to abecedně od Z do A.

## <a name="considerations"></a>Důležité informace

Podkladový mechanismus využívá řazení v *přirozeném jazyce*. To je výkonnější a komplexnější než standardní řazení. Podívejte se například na tuto tabulku:

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

Bez řazení v přirozeném jazyce by bylo pořadí sloupce `Column1` 1, 11, 2 atd. Mechanismus ale chápe, že 11 je větší než 2, takže seřadí položky vzestupně tímto způsobem:

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

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce:

[![Ukázka výběru řazení](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
