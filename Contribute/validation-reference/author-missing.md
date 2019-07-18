---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791520"
---
# <a name="author-missing"></a><span data-ttu-id="c32a4-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="c32a4-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="c32a4-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="c32a4-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="c32a4-105">Atribut `author` identifikuje autora článku pomocí ID GitHubu.</span><span class="sxs-lookup"><span data-stu-id="c32a4-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="c32a4-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="c32a4-106">Resolution</span></span>

<span data-ttu-id="c32a4-107">Jako hlavičku YML zadejte ID GitHubu aktuálního autora:</span><span class="sxs-lookup"><span data-stu-id="c32a4-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="c32a4-108">Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="c32a4-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
