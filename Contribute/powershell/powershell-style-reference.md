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
# <a name="updating-reference-articles"></a>Aktualizace referenčních článků

Články s referenčními rutinami mají zvláštní strukturu. Tuto strukturu definuje [PlatyPS][].
PlatyPS je nástroj, který se používá ke generování nápovědy k rutinám v modulech PowerShellu. PlatyPS vytvoří pro rutinu základní soubor Markdown. Po úpravě souborů Markdown se PlatyPS použije k vytvoření souborů nápovědy MAML používaných rutinou `Get-Help`.

V PlatyPS je pevně naprogramované schéma referenčních rutin zapsaných do kódu. Dokument [platyPS.schema.md][] se pokouší tuto strukturu popsat. Při porušení schématu dochází k chybám sestavení, které je potřeba opravit, abychom mohli příspěvek přijmout.

## <a name="general-guidelines"></a>Obecné pokyny

- Neodebírejte žádné struktury záhlaví. PlatyPS očekává zvláštní sadu záhlaví.
- Záhlaví **Input type** (Typ vstupu) a **Output type** (Typ výstupu) musí být určitého typu. Pokud rutina nemá vstup nebo nevrací hodnotu, použijte hodnotu „None“ (Žádný).
- Oplocené bloky kódu jsou povolené jenom v oddílu [Příklady](#format-for-examples).
- Vložené části kódu můžete použít v kterémkoli odstavci.

## <a name="formatting-about_-files"></a>Formátování souborů About_

Soubory `About_*` nyní zpracovává převaděč [Pandoc][] místo nástroje PlatyPS. Soubory `About_*` jsou formátované tak, aby byly zajistily co největší kompatibilitu se všemi verzemi PowerShellu a publikačními nástroji.
Neměňte prosím formátování souborů `about_*`, aniž byste se přihlásili jako údržbáři úložiště.

Základní pravidla formátování:

- Omezte řádky na 80 znaků.
- Bloky kódu, uvozovky bloku a tabulky jsou omezené na 76 znaků, protože Pandoc tyto části při převodu odsadí o čtyři mezery.
- Tabulky se musejí vejít do 76 znaků.
  - Ručně zabalte obsah buněk, který je na více řádků.
  - Na každém řádku používejte úvodní a závěrečné znaky `|`.
  - Funkční příklad viz [about_Comparison_Operators][about-example].
- Při použití speciálních znaků `\`, `$`, `` ` `` a `<` převaděče Pandoc:
  - V záhlaví musí být tyto znaky uvozeny počátečním znakem `\`.
  - V odstavci musí být tyto znaky dány do rozsahů kódu. Například:

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Formátování příkladů

Ve schématu PlatyPS je záhlaví **EXAMPLES** v záhlaví H2 a každý příklad představuje záhlaví H3.

V příkladu schéma nedovoluje, aby byly bloky kódu odděleny odstavci. Platné schéma:

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Očíslujte každý příklad a přidejte stručný nadpis.

Například:

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