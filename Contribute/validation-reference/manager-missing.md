---
title: manager-missing
description: Vysvětlení a řešení problému sestavení manager-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637246"
---
# <a name="manager-missing"></a><span data-ttu-id="e3004-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="e3004-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e3004-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="e3004-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="e3004-105">Některé skupiny obsahu vyžadují, aby autorova vedoucího identifikoval atribut `manager`.</span><span class="sxs-lookup"><span data-stu-id="e3004-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="e3004-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="e3004-106">Resolution</span></span>

<span data-ttu-id="e3004-107">Přidejte platný alias Microsoftu pro atribut `manager`:</span><span class="sxs-lookup"><span data-stu-id="e3004-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
