---
title: ms-service-and-subservice-invalid
description: Vysvětlení a řešení problému sestavení ms-service-and-subservice-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637292"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`. Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici. Buď je neplatná hodnota `ms.service`, nebo hodnota `ms.subservice` netvoří platnou dvojici s `ms.service`.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná. Pak zvolte platnou hodnotu `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
