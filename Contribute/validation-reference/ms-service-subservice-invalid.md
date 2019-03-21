---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987631"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Připravujeme**

## <a name="warning"></a>Upozornění

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`. Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici. Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná. Pak zvolte platnou hodnotu `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
