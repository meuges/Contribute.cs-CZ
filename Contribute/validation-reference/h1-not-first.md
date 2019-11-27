---
title: h1-not-first
description: Vysvětlení a řešení problému sestavení h1-not-first na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528919"
---
# <a name="h1-not-first"></a><span data-ttu-id="5ed09-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="5ed09-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="5ed09-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="5ed09-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="5ed09-105">Před záhlavím H1 v souboru Markdown se může nacházet jen hlavička metadat YAML.</span><span class="sxs-lookup"><span data-stu-id="5ed09-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="5ed09-106">Pokud chcete například do horní části článku přidat poznámku nebo obrázek, musí následovat po H1.</span><span class="sxs-lookup"><span data-stu-id="5ed09-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="5ed09-107">Toto není povoleno:</span><span class="sxs-lookup"><span data-stu-id="5ed09-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="5ed09-108">Místo toho postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="5ed09-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="5ed09-109">Další běžnou příčinou tohoto problému jsou [značky pořadí bajtů (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) před hlavičkou YAML.</span><span class="sxs-lookup"><span data-stu-id="5ed09-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="5ed09-110">Někdy se vkládají při problémech s kódováním během potvrzování obsahu do úložišť.</span><span class="sxs-lookup"><span data-stu-id="5ed09-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="5ed09-111">Výsledkem je chybné vykreslování na GitHubu a měly by být odebrány.</span><span class="sxs-lookup"><span data-stu-id="5ed09-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="5ed09-112">Řešení</span><span class="sxs-lookup"><span data-stu-id="5ed09-112">Resolution</span></span>

<span data-ttu-id="5ed09-113">Odeberte veškerý obsah před záhlavím H1 s výjimkou hlavičky metadat YAML.</span><span class="sxs-lookup"><span data-stu-id="5ed09-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
