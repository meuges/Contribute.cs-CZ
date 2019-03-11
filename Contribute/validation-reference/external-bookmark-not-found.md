---
title: external-bookmark-not-found
description: Vysvětlení a řešení problému sestavení external-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427299"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="59815-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="59815-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="59815-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="59815-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="59815-105">Pokoušíte se vytvořit odkaz na nadpis v jiném souboru, který neexistuje.</span><span class="sxs-lookup"><span data-stu-id="59815-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="59815-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="59815-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="59815-107">Zkontrolujte soubor, na který odkazujete, a aktualizujte odkaz záložky tak, aby směřoval na platný oddíl v daném souboru.</span><span class="sxs-lookup"><span data-stu-id="59815-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="59815-108">K odkazu na nadpis oddílu v jiném článku použijte odkaz na daný soubor nebo server, za kterým bude následovat symbol hash a text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="59815-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="59815-109">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="59815-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="59815-110">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="59815-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
