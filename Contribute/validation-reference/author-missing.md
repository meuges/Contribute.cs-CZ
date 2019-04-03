---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6c7306cf674a345b25d3e05c4e00662623c44469
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637430"
---
# <a name="author-missing"></a><span data-ttu-id="8950c-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="8950c-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="8950c-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="8950c-104">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="8950c-105">Atribut `author` identifikuje autora článku pomocí ID GitHubu.</span><span class="sxs-lookup"><span data-stu-id="8950c-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="8950c-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="8950c-106">Resolution</span></span>

<span data-ttu-id="8950c-107">Přidejte ID GitHubu autora do hlavičky YML:</span><span class="sxs-lookup"><span data-stu-id="8950c-107">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]