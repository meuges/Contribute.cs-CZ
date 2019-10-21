---
title: Psaní příspěvků do úložišť dokumentace k PowerShellu
description: Tento článek popisuje úložiště, která tvoří dokumentaci k PowerShellu.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290166"
---
# <a name="contributing-to-powershell-documentation"></a>Přispívání do dokumentace k PowerShellu

Děkujeme vám za váš zájem o dokumentaci k PowerShellu.

Tento dokument vysvětluje postup přispívání do článků a vzorového kódu hostovaného na webu s dokumentací k PowerShellu. Příspěvky můžou být jednoduché, třeba oprava překlepu, nebo složité, třeba nové články.

Web s dokumentací k PowerShellu se skládá z několika úložišť, která obsahují jednu nebo více sad dokumentů:

- [Principy PowerShellu a referenční rutiny][psdocs].
- Sada PowerShell SDK se vzorovým kódem – privátní úložiště, které obsahuje ukázky používané v článcích sady SDK.
- [Referenční informace k sadě PowerShell .NET SDK](/dotnet/api/?view=pscore-6.2.0) – obsah privátního úložiště generovaný zdrojovým kódem PowerShellu.

Ke sledování problémů týkajících se veškerého obsahu slouží úložiště [PowerShell-Docs][docsrepo].

## <a name="repository-structure"></a>Struktura úložiště

Úložiště PowerShell-Docs se skládá ze tří sad dokumentů publikovaných na webu [Microsoft Docs][psdocs]. Sady dokumentů jsou v následujících složkách:

- [/reference/][ref] – obsahuje referenční informace k rutinám PowerShellu pro rutiny dodávané v PowerShellu. Referenční informace jsou shromážděné do složek podle verzí (3.0, 4.0, 5.0, 5.1, 6 a 7). Tato sada dokumentů neobsahuje referenční informace o modulech dodávaných ve Windows ani v jiných produktech Microsoftu.
- [/reference/docs-conceptual][conceptual] – obsahuje koncepční dokumentaci k PowerShellu. Obsahuje pokyny k nastavení, ukázkové skripty, návody a další materiály.
- [/developer/][SDK] – obsahuje koncepční dokumentaci sady SDK PowerShellu.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
