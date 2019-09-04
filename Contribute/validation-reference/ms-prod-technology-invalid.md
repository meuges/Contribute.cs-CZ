---
title: ms-prod-and-technology-invalid
description: Vysvětlení a řešení problému sestavení ms-prod-and-technology-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236329"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

## <a name="warning"></a>Upozornění

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

K zadání místních produktů používejte `ms.prod`. Pokud chcete o `ms.prod` zadat podrobnější informace, můžete volitelně zadat `ms.technology`. Hodnoty `ms.prod` a `ms.technology` musí tvořit platnou dvojici. Buď je neplatná hodnota `ms.prod`, nebo hodnota `ms.technology` netvoří platnou dvojici s `ms.prod`.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.prod` pro váš článek správná. Pak zvolte platnou hodnotu `ms.technology`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists). Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
