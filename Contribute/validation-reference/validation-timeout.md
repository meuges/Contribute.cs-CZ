---
title: validation-timeout
description: Vysvětlení a řešení problému sestavení validation-timeout na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817410"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Upozornění

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby. Po několika pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.

## <a name="resolution"></a>Řešení

Zkuste žádost o přijetí změn zavřít a znovu otevřít, případně znovu spustit ruční sestavení přes portál Docs (jen správci úložiště). Po prvotním pokusu se problémy se službou často vyřeší samovolně. Pokud potřebujete pomoc od správce nebo pokud se tato zpráva nepřestává zobrazovat, zadejte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu) nebo v žádosti o přijetí změn pomocí zmínky (@) požádejte o pomoc autora článku (pokud jste externím přispěvatelem).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
