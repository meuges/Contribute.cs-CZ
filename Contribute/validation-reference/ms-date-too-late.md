---
title: ms-date-too-late
description: Vysvětlení a řešení problému sestavení ms-date-too-late na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713101"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="9d3a2-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="9d3a2-103">ms-date-too-late</span></span>

<span data-ttu-id="9d3a2-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="9d3a2-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="9d3a2-105">Upozornění</span><span class="sxs-lookup"><span data-stu-id="9d3a2-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="9d3a2-106">Atribut `ms.date` se používá k indikaci „aktuálnosti“ – to znamená, kdy byl článek naposledy zkontrolován z hlediska relevance, přesnosti, správných snímků obrazovek a funkčních odkazů.</span><span class="sxs-lookup"><span data-stu-id="9d3a2-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="9d3a2-107">Proto nemůže být v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="9d3a2-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="9d3a2-108">S pěti dny můžete počítat na dobu vydání – například když je obsah zmrazený kvůli kontrole kvality při přípravě na nějakou důležitou událost.</span><span class="sxs-lookup"><span data-stu-id="9d3a2-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="9d3a2-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="9d3a2-109">Resolution</span></span>

<span data-ttu-id="9d3a2-110">Zadejte `ms.date` ve formátu MM/DD/RRRR. Datum nesmí být od dnešního dne vzdálenější než pět dnů.</span><span class="sxs-lookup"><span data-stu-id="9d3a2-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
