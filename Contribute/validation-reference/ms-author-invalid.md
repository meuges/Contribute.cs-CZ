---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236531"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="3515a-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="3515a-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="3515a-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="3515a-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="3515a-105">Řešení</span><span class="sxs-lookup"><span data-stu-id="3515a-105">Resolution</span></span>

<span data-ttu-id="3515a-106">Ověřte, že hodnota `ms.author` je platný alias Microsoftu aktuálního autora.</span><span class="sxs-lookup"><span data-stu-id="3515a-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="3515a-107">Pokud je tento alias distribučním seznamem, musí být také na seznamu povolených.</span><span class="sxs-lookup"><span data-stu-id="3515a-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="3515a-108">Platné hodnoty pro distribuční seznamy se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="3515a-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
