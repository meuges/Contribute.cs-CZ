---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: cba9788c113101fc93bffa674702b2bed95afbcb
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713032"
---
# <a name="author-missing"></a><span data-ttu-id="71fcb-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="71fcb-103">author-missing</span></span>

<span data-ttu-id="71fcb-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="71fcb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="71fcb-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="71fcb-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="71fcb-106">Atribut `author` identifikuje autora článku pomocí ID GitHubu.</span><span class="sxs-lookup"><span data-stu-id="71fcb-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="71fcb-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="71fcb-107">Resolution</span></span>

<span data-ttu-id="71fcb-108">Přidejte ID GitHubu autora do hlavičky YML:</span><span class="sxs-lookup"><span data-stu-id="71fcb-108">Add the author's GitHub ID to the YML header:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]