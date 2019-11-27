---
title: h1-empty
description: Vysvětlení a řešení problému sestavení h1-empty na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528790"
---
# <a name="h1-empty"></a><span data-ttu-id="1583a-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="1583a-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="1583a-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="1583a-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="1583a-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="1583a-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="1583a-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="1583a-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="1583a-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="1583a-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="1583a-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="1583a-108">Resolution</span></span>

<span data-ttu-id="1583a-109">Pro nápravu tohoto problému zajistěte, aby nadpis H1 obsahoval text, ne pouze znak hash.</span><span class="sxs-lookup"><span data-stu-id="1583a-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="1583a-110">Chybně:</span><span class="sxs-lookup"><span data-stu-id="1583a-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="1583a-111">Správně:</span><span class="sxs-lookup"><span data-stu-id="1583a-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
