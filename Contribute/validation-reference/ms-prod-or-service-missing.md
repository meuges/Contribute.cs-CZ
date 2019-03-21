---
title: ms-prod-or-service-missing
description: Vysvětlení a řešení problému sestavení ms-prod-or-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987553"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Řešení

Vyžaduje se buď `ms.prod`, nebo `ms.service`, ale ne obojí: `ms.prod` se používá pro místní produkty, `ms.service` se používá pro cloudové služby. Zjistěte, které z obou polí je pro váš článek to patřičné, ověřte správnost hodnoty a odeberte zbývající pole.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]