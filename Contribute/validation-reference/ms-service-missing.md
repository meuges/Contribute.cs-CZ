---
title: ms-service-missing
description: Vysvětlení a řešení problému sestavení ms-service-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236497"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>Upozornění

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`, ale pokud zadáte `ms.subservice`, musíte také zadat `ms.service`. Hodnoty `ms.service` a `ms.subservice` musí tvořit platnou dvojici.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je vámi zadaná hodnota `ms.subservice` pro váš článek správná. Potom přidejte příslušnou hodnotu `ms.service`, která je platným nadřazeným objektem pro `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists). Pokud si chcete vyžádat nové hodnoty, postupujte podle [tohoto procesu](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
