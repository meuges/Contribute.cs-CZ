---
title: multiple-h1
description: Vysvětlení a řešení problému sestavení multiple-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848604"
---
# <a name="multiple-h1"></a><span data-ttu-id="8f38f-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="8f38f-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8f38f-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="8f38f-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="8f38f-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="8f38f-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="8f38f-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="8f38f-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="8f38f-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="8f38f-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="8f38f-108">V každém souboru může být jenom jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="8f38f-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="8f38f-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="8f38f-109">Resolution</span></span>

<span data-ttu-id="8f38f-110">Pro nápravu tohoto problému změňte úroveň dalších nadpisů H1 na H2 (`##`) nebo reorganizujte soubor jiným způsobem.</span><span class="sxs-lookup"><span data-stu-id="8f38f-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="8f38f-111">Upozorňujeme, že přeskakování úrovní nadpisů (například nadpis H1, za kterým následuje nadpis H3) není povoleno.</span><span class="sxs-lookup"><span data-stu-id="8f38f-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

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