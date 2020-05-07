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
# <a name="reformat-markdown-tables"></a>Přeformátování tabulek Markdownu

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

Když v souboru Markdownu ( *\*.md*) vyberete celou tabulku, zobrazí se dvě položky místní nabídky pro formátování tabulky. Klikněte pravým tlačítkem myši na vybranou tabulku Markdownu a otevřete místní nabídku. Zobrazí se nabídka s položkami podobná této:

:::image type="content" source="media/reformat-table-menu.png" alt-text="Místní nabídka pro přeformátování tabulky":::

> [!TIP]
> Tuto funkci **není možné** použít v případě, že je vybráno více tabulek Markdownu. Slouží pro úpravy jen jedné tabulky. Aby fungovala správně, je také potřeba vybrat celou tabulku včetně záhlaví.

## <a name="consolidate-selected-table"></a>Consolidate selected table

Když vyberete možnost **Consolidate selected table** (Konsolidovat vybranou tabulku), sbalí se záhlaví a obsah tabulky tak, že se po obou stranách každé hodnoty bude nacházet jen jedna mezera.

## <a name="evenly-distribute-selected-table"></a>Evenly distribute selected table

Když vyberete možnost **Evenly distribute selected table** (Rovnoměrně rozmístit vybranou tabulku), vypočítá se v každém sloupci nejdelší hodnota a všechny ostatní hodnoty se odpovídajícím způsobem rozmístí pomocí mezer.

## <a name="considerations"></a>Důležité informace

Tato funkce nemá vliv na vykreslování tabulky, ale zlepšuje její čitelnost, takže se tabulka lépe udržuje. Zarovnání sloupců tabulky zůstane beze změny.

Podívejte se například na tuto tabulku:

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

Po „rovnoměrném rozmístění“:

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

Po „konsolidaci“:

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

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce:

[![Ukázka přeformátování tabulky](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
