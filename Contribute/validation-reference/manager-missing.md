---
title: manager-missing
description: Vysvětlení a řešení problému sestavení manager-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427310"
---
# <a name="manager-missing"></a><span data-ttu-id="30b20-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="30b20-103">manager-missing</span></span>

<span data-ttu-id="30b20-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="30b20-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="30b20-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="30b20-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="30b20-106">Některé skupiny obsahu vyžadují, aby autorova vedoucího identifikoval atribut `manager`.</span><span class="sxs-lookup"><span data-stu-id="30b20-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="30b20-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="30b20-107">Resolution</span></span>

<span data-ttu-id="30b20-108">Přidejte platný alias Microsoftu pro atribut `manager`:</span><span class="sxs-lookup"><span data-stu-id="30b20-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
