---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481697"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="9669b-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="9669b-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="9669b-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="9669b-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="9669b-105">Řešení</span><span class="sxs-lookup"><span data-stu-id="9669b-105">Resolution</span></span>

<span data-ttu-id="9669b-106">Ověřte, že hodnota `ms.author` je platný alias Microsoftu aktuálního autora.</span><span class="sxs-lookup"><span data-stu-id="9669b-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="9669b-107">Doporučujeme, aby byl jako autor určen zaměstnanec na plný úvazek nebo distribuční seznam představující tým, ne externí dodavatel s krátkodobým kontraktem.</span><span class="sxs-lookup"><span data-stu-id="9669b-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="9669b-108">Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="9669b-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="9669b-109">Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="9669b-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
