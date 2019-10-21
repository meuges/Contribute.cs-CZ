---
title: ms-author-missing
description: Vysvětlení a řešení problému sestavení ms-author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246255"
---
# <a name="ms-author-missing"></a><span data-ttu-id="49da4-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="49da4-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="49da4-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="49da4-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="49da4-105">Řešení</span><span class="sxs-lookup"><span data-stu-id="49da4-105">Resolution</span></span>

<span data-ttu-id="49da4-106">Pro hodnotu `ms.author` zadejte alias Microsoftu aktuálního autora.</span><span class="sxs-lookup"><span data-stu-id="49da4-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="49da4-107">Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví.</span><span class="sxs-lookup"><span data-stu-id="49da4-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="49da4-108">Doporučujeme jako autora zvolit zaměstnance na plný úvazek nebo týmový distribuční seznam, nikoli krátkodobého dodavatele.</span><span class="sxs-lookup"><span data-stu-id="49da4-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="49da4-109">Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="49da4-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="49da4-110">Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="49da4-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
