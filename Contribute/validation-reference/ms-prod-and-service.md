---
title: ms-prod-and-service
description: Vysvětlení a řešení problému sestavení ms-prod-and-service na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236353"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

## <a name="warning"></a>Upozornění
https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Řešení

Vyžaduje se buď `ms.prod`, nebo `ms.service`, ale ne obojí: `ms.prod` se používá pro místní produkty, `ms.service` se používá pro cloudové služby. Zjistěte, které z obou polí je pro váš článek to patřičné, ověřte správnost hodnoty a odeberte zbývající pole.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists). Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
