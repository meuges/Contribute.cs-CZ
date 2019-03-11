---
title: multiple-h1
description: Vysvětlení a řešení problému sestavení multiple-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427323"
---
# <a name="multiple-h1"></a><span data-ttu-id="f1072-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="f1072-103">multiple-h1</span></span>

## <a name="warning"></a><span data-ttu-id="f1072-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="f1072-104">Warning</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="f1072-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="f1072-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="f1072-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="f1072-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="f1072-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="f1072-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="f1072-108">V každém souboru může být jenom jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="f1072-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="f1072-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="f1072-109">Resolution</span></span>

<span data-ttu-id="f1072-110">Pro nápravu tohoto problému změňte úroveň dalších nadpisů H1 na H2 (`##`) nebo reorganizujte soubor jiným způsobem.</span><span class="sxs-lookup"><span data-stu-id="f1072-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="f1072-111">Upozorňujeme, že přeskakování úrovní nadpisů (například nadpis H1, za kterým následuje nadpis H3) není povoleno.</span><span class="sxs-lookup"><span data-stu-id="f1072-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]