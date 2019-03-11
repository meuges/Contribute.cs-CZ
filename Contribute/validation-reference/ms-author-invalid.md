---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427315"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="955b7-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="955b7-103">ms-author-invalid</span></span>

<span data-ttu-id="955b7-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="955b7-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="955b7-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="955b7-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="955b7-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="955b7-106">Resolution</span></span>

<span data-ttu-id="955b7-107">Ověřte, že hodnota `ms.author` je platný alias Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="955b7-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="955b7-108">Pokud je tento alias distribučním seznamem, musí být také na seznamu povolených.</span><span class="sxs-lookup"><span data-stu-id="955b7-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="955b7-109">Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="955b7-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
