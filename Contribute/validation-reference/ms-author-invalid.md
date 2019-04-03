---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6d6c77b9b378865913e2055abf2b64ccba8ca482
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636717"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="99e3f-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="99e3f-103">ms-author-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="99e3f-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="99e3f-104">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="99e3f-105">Řešení</span><span class="sxs-lookup"><span data-stu-id="99e3f-105">Resolution</span></span>

<span data-ttu-id="99e3f-106">Ověřte, že hodnota `ms.author` je platný alias Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="99e3f-106">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="99e3f-107">Pokud je tento alias distribučním seznamem, musí být také na seznamu povolených.</span><span class="sxs-lookup"><span data-stu-id="99e3f-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="99e3f-108">Platné hodnoty pro distribuční seznamy se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="99e3f-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
