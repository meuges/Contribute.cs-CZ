---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236323"
---
# <a name="author-missing"></a><span data-ttu-id="459a7-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="459a7-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="459a7-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="459a7-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="459a7-105">Atribut `author` identifikuje autora článku pomocí ID GitHubu.</span><span class="sxs-lookup"><span data-stu-id="459a7-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="459a7-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="459a7-106">Resolution</span></span>

<span data-ttu-id="459a7-107">Jako hlavičku YML zadejte ID GitHubu aktuálního autora:</span><span class="sxs-lookup"><span data-stu-id="459a7-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="459a7-108">Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="459a7-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
