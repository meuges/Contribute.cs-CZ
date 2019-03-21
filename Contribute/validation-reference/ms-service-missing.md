---
title: ms-service-missing
description: Vysvětlení a řešení problému sestavení ms-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987714"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`, ale pokud zadáte `ms.subservice`, musíte také zadat `ms.service`. Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je vámi zadaná hodnota `ms.subservice` pro váš článek správná. Potom přidejte příslušnou hodnotu `ms.service`, která je platným nadřazeným objektem pro `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
