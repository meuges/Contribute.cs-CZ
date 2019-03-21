---
title: ms-prod-and-technology-invalid
description: Vysvětlení a řešení problému sestavení ms-prod-and-technology-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987576"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Připravujeme**

## <a name="warning"></a>Upozornění

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

K zadání místních produktů používejte `ms.prod`. Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`. Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici. Buď je neplatná hodnota `ms.prod`, nebo hodnota `ms.technology` netvoří platnou dvojici s `ms.prod`.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.prod` pro váš článek správná. Pak zvolte platnou hodnotu `ms.technology`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
