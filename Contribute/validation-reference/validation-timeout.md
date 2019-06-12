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
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Upozornění

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby. Po třech pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.

## <a name="resolution"></a>Řešení

Zkuste žádost o přijetí změn zavřít a znovu otevřít, nebo znovu spustit ruční sestavení (jen správci úložiště). Po prvotním pokusu se problémy se službou často vyřeší samovolně. Pokud se tato zpráva pořád zobrazuje, založte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu), nebo v žádosti o přijetí změn požádejte pomocí @ zmínky autora článku o pomoc (pokud jste externím přispěvatelem).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
