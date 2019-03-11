---
title: internal-bookmark-not-found
description: Vysvětlení a řešení problému sestavení internal-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427311"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="ef532-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="ef532-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="ef532-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="ef532-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ef532-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="ef532-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="ef532-106">Pokoušíte se vytvořit odkaz na nadpis v aktuálním souboru, který neexistuje.</span><span class="sxs-lookup"><span data-stu-id="ef532-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="ef532-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="ef532-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="ef532-108">Ověřte nadpis, na který chcete vytvořit odkaz, a aktualizujte daný odkaz.</span><span class="sxs-lookup"><span data-stu-id="ef532-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="ef532-109">K vytvoření odkazu na oddíl v aktuálním článku použijte symbol hash a za ním text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="ef532-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="ef532-110">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="ef532-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="ef532-111">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="ef532-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
