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
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="76a34-103">Přispívání do dokumentace k PowerShellu</span><span class="sxs-lookup"><span data-stu-id="76a34-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="76a34-104">Děkujeme vám za váš zájem o dokumentaci k PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="76a34-105">Tento dokument vysvětluje postup přispívání do článků a vzorového kódu hostovaného na webu s dokumentací k PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="76a34-106">Příspěvky můžou být jednoduché, třeba oprava překlepu, nebo složité, třeba nové články.</span><span class="sxs-lookup"><span data-stu-id="76a34-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="76a34-107">Web s dokumentací k PowerShellu se skládá z několika úložišť, která obsahují jednu nebo více sad dokumentů:</span><span class="sxs-lookup"><span data-stu-id="76a34-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="76a34-108">[Principy PowerShellu a referenční rutiny][psdocs].</span><span class="sxs-lookup"><span data-stu-id="76a34-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="76a34-109">Sada PowerShell SDK se vzorovým kódem – privátní úložiště, které obsahuje ukázky používané v článcích sady SDK.</span><span class="sxs-lookup"><span data-stu-id="76a34-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="76a34-110">[Referenční informace k sadě PowerShell .NET SDK](/dotnet/api/?view=pscore-6.2.0) – obsah privátního úložiště generovaný zdrojovým kódem PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="76a34-111">Ke sledování problémů týkajících se veškerého obsahu slouží úložiště [PowerShell-Docs][docsrepo].</span><span class="sxs-lookup"><span data-stu-id="76a34-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="76a34-112">Struktura úložiště</span><span class="sxs-lookup"><span data-stu-id="76a34-112">Repository Structure</span></span>

<span data-ttu-id="76a34-113">Úložiště PowerShell-Docs se skládá ze tří sad dokumentů publikovaných na webu [Microsoft Docs][psdocs]. Sady dokumentů jsou v následujících složkách:</span><span class="sxs-lookup"><span data-stu-id="76a34-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="76a34-114">[/reference/][ref] – obsahuje referenční informace k rutinám PowerShellu pro rutiny dodávané v PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="76a34-115">Referenční informace jsou shromážděné do složek podle verzí (3.0, 4.0, 5.0, 5.1, 6 a 7).</span><span class="sxs-lookup"><span data-stu-id="76a34-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="76a34-116">Tato sada dokumentů neobsahuje referenční informace o modulech dodávaných ve Windows ani v jiných produktech Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="76a34-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="76a34-117">[/reference/docs-conceptual][conceptual] – obsahuje koncepční dokumentaci k PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="76a34-118">Obsahuje pokyny k nastavení, ukázkové skripty, návody a další materiály.</span><span class="sxs-lookup"><span data-stu-id="76a34-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="76a34-119">[/developer/][SDK] – obsahuje koncepční dokumentaci sady SDK PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="76a34-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
