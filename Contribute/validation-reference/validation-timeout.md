---
title: validation-timeout
description: Vysvětlení a řešení problému sestavení validation-timeout na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024203"
---
# <a name="validation-timeout"></a><span data-ttu-id="9fbb5-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="9fbb5-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="9fbb5-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="9fbb5-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="9fbb5-105">Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby.</span><span class="sxs-lookup"><span data-stu-id="9fbb5-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="9fbb5-106">Po třech pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.</span><span class="sxs-lookup"><span data-stu-id="9fbb5-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="9fbb5-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="9fbb5-107">Resolution</span></span>

<span data-ttu-id="9fbb5-108">Zkuste žádost o přijetí změn zavřít a znovu otevřít, nebo znovu spustit ruční sestavení (jen správci úložiště).</span><span class="sxs-lookup"><span data-stu-id="9fbb5-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="9fbb5-109">Po prvotním pokusu se problémy se službou často vyřeší samovolně.</span><span class="sxs-lookup"><span data-stu-id="9fbb5-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="9fbb5-110">Pokud se tato zpráva pořád zobrazuje, založte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu), nebo v žádosti o přijetí změn požádejte pomocí @ zmínky autora článku o pomoc (pokud jste externím přispěvatelem).</span><span class="sxs-lookup"><span data-stu-id="9fbb5-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
