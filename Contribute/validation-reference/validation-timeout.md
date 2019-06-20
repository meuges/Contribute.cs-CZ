---
title: validation-timeout
description: Vysvětlení a řešení problému sestavení validation-timeout na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033293"
---
# <a name="validation-timeout"></a><span data-ttu-id="e6dd5-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="e6dd5-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="e6dd5-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="e6dd5-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="e6dd5-105">Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby.</span><span class="sxs-lookup"><span data-stu-id="e6dd5-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="e6dd5-106">Po několika pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.</span><span class="sxs-lookup"><span data-stu-id="e6dd5-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="e6dd5-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="e6dd5-107">Resolution</span></span>

<span data-ttu-id="e6dd5-108">Zkuste žádost o přijetí změn zavřít a znovu otevřít, případně znovu spustit ruční sestavení přes portál Docs (jen správci úložiště).</span><span class="sxs-lookup"><span data-stu-id="e6dd5-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="e6dd5-109">Po prvotním pokusu se problémy se službou často vyřeší samovolně.</span><span class="sxs-lookup"><span data-stu-id="e6dd5-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="e6dd5-110">Pokud potřebujete pomoc od správce nebo pokud se tato zpráva nepřestává zobrazovat, zadejte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu) nebo v žádosti o přijetí změn pomocí zmínky (@) požádejte o pomoc autora článku (pokud jste externím přispěvatelem).</span><span class="sxs-lookup"><span data-stu-id="e6dd5-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
