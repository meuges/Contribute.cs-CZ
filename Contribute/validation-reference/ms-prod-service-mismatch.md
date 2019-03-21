---
title: ms-prod-service-mismatch
description: Vysvětlení a řešení problému sestavení ms-prod-service-mismatch na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987608"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Připravujeme**

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
