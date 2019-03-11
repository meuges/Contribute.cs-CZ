---
title: no-space-in-h1
description: Vysvětlení a řešení problému sestavení no-space-in-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427314"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="6fbe4-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="6fbe4-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="6fbe4-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="6fbe4-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="6fbe4-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="6fbe4-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="6fbe4-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="6fbe4-108">Pokud za znakem hash není mezera, web Docs nerozpozná nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="6fbe4-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="6fbe4-109">Resolution</span></span>

<span data-ttu-id="6fbe4-110">Tuto chybu opravíte tak, že v nadpisu H1 za znak hash přidáte mezeru.</span><span class="sxs-lookup"><span data-stu-id="6fbe4-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]