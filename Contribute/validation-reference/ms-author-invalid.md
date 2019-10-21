---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246293"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="ee11e-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="ee11e-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="ee11e-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="ee11e-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="ee11e-105">Řešení</span><span class="sxs-lookup"><span data-stu-id="ee11e-105">Resolution</span></span>

<span data-ttu-id="ee11e-106">Aktualizujte hodnotu `ms.author` platným aliasem Microsoftu, který patří aktuálnímu autorovi.</span><span class="sxs-lookup"><span data-stu-id="ee11e-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="ee11e-107">Doporučujeme jako autora zvolit zaměstnance na plný úvazek nebo týmový distribuční seznam, nikoli krátkodobého dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ee11e-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="ee11e-108">Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="ee11e-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="ee11e-109">Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="ee11e-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
