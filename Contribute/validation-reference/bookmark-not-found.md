---
title: internal-bookmark-not-found
description: Vysvětlení a řešení problému sestavení internal-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856213"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="c9b61-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c9b61-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="c9b61-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c9b61-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="c9b61-105">Pokoušíte se vytvořit odkaz na nadpis v aktuálním souboru nebo jiném souboru, který neexistuje.</span><span class="sxs-lookup"><span data-stu-id="c9b61-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c9b61-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="c9b61-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c9b61-107">Ověřte nadpis, na který chcete vytvořit odkaz, a aktualizujte daný odkaz.</span><span class="sxs-lookup"><span data-stu-id="c9b61-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="c9b61-108">K vytvoření odkazu na oddíl v aktuálním článku použijte symbol hash a za ním text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="c9b61-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c9b61-109">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="c9b61-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c9b61-110">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="c9b61-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="c9b61-111">Pokud chcete vytvořit odkaz na nadpis v jiném souboru, použijte relativní odkaz na tento soubor následovaný symbolem hash a textem nadpisu.</span><span class="sxs-lookup"><span data-stu-id="c9b61-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="c9b61-112">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="c9b61-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c9b61-113">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="c9b61-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
