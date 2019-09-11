---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848585"
---
# <a name="author-missing"></a><span data-ttu-id="36e93-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="36e93-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="36e93-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="36e93-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="36e93-105">Atribut `author` identifikuje autora článku pomocí ID GitHubu.</span><span class="sxs-lookup"><span data-stu-id="36e93-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="36e93-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="36e93-106">Resolution</span></span>

<span data-ttu-id="36e93-107">Jako hlavičku YML zadejte ID GitHubu aktuálního autora:</span><span class="sxs-lookup"><span data-stu-id="36e93-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="36e93-108">Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="36e93-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
