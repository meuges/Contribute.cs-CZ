---
title: validation-timeout
description: Vysvětlení a řešení problému sestavení validation-timeout na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166761"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Upozornění

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby. Po několika pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.

## <a name="resolution"></a>Řešení

Zkuste zavřít a znovu otevřít svoji žádost o přijetí změn nebo vynutit úplné sestavení přes [portál Docs](https://ops.microsoft.com/#/). Po prvotním pokusu se problémy se službou často vyřeší samovolně.

Abyste mohli vynutit úplné sestavení přes portál Docs, musíte být správce úložiště. Pokud nevíte, kdo je váš správce úložiště nebo pokud se tato zpráva bude objevovat i po vynuceném sestavení, zadejte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu) nebo v žádosti o přijetí změn požádejte pomocí zmínky (@) o pomoc autora článku (pokud jste externím přispěvatelem).

Pokud jste správce úložiště, můžete vynutit úplné sestavení následujícím způsobem:

1. Přejděte na [portál Docs](https://ops.microsoft.com/#/) a přihlaste se.
1. Hledáním v levém horním rohu najděte své úložiště a vyberte ho.

   :::image type="content" source="media/find-repo.png" alt-text="Najděte své úložiště prostřednictvím vyhledávacího pole na portálu Docs.":::
1. Na kartě **Historie sestavení** klikněte na **+ Ruční publikování**.
1. Vyberte větev, pro kterou se zobrazuje upozornění, například hlavní větev.
1. Cíl ponechte výchozí – **web Docs**.
1. Zaškrtněte políčko **Vynutit publikování**.
1. Klikněte na **Publikovat**.

   :::image type="content" source="media/force-build.png" alt-text="Postup vynucení úplného sestavení":::

Tím se vynutí úplné sestavení ve větvi.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
