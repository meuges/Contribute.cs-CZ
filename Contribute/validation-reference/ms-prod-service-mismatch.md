---
title: ms-prod-service-mismatch
description: Vysvětlení a řešení problému sestavení ms-prod-service-mismatch na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636786"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

K zadání místních produktů používejte `ms.prod`, pro cloudové služby používejte `ms.service`. Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete zadat `ms.subservice`. Nemůžete použít `ms.prod` s `ms.subservice` ani `ms.service` s `ms.technology`.

## <a name="resolution"></a>Řešení

Nejdříve ověřte, jestli jste pro váš článek vybrali správný nadřazený atribut (`ms.prod` nebo `ms.service`). Pak přidejte patřičné podřízené pole s platnou spárovanou hodnotou. Odeberte všechna nadbytečná pole.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
