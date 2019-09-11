---
title: block-section-invalid
description: Vysvětlení a řešení problému sestavení block-section-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 500527c7371dd9d4966460b3eafe0a44874fc4eb
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848532"
---
# <a name="block-section-invalid"></a><span data-ttu-id="47660-103">block-section-invalid</span><span class="sxs-lookup"><span data-stu-id="47660-103">block-section-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="47660-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="47660-104">Warning</span></span>

`Invalid syntax for alert, div, or video. The text will be rendered as a block quote.`

<span data-ttu-id="47660-105">Několik rozšíření Markdownu na webu Docs začíná řetězcem `> [!`.</span><span class="sxs-lookup"><span data-stu-id="47660-105">Several Docs Markdown extensions begin with the string `> [!`.</span></span> <span data-ttu-id="47660-106">Mezi `>` a `[` musí být mezera a musí se použít uzavírací závorka `]`.</span><span class="sxs-lookup"><span data-stu-id="47660-106">A space is required between `>` and `[`, and there must be a closing `]`.</span></span> <span data-ttu-id="47660-107">Pokud je syntaxe nesprávná, zobrazí se text jako bloková citace.</span><span class="sxs-lookup"><span data-stu-id="47660-107">If the syntax is incorrect, the text will be rendered as a block quote.</span></span>

## <a name="resolution"></a><span data-ttu-id="47660-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="47660-108">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="47660-109">Ověřte správnost syntaxe pro rozšíření, které používáte:</span><span class="sxs-lookup"><span data-stu-id="47660-109">Ensure the syntax is correct for the extension you're using:</span></span>

```markdown

Alerts:

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

Videos:

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

Sections (div):

> [!div class="class"]

```


<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
