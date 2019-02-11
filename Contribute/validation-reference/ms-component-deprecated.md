---
title: ms-component-deprecated
description: Vysvětlení a řešení problému sestavení ms-component-deprecated na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713147"
---
# <a name="ms-component-deprecated"></a>ms-component-deprecated

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Deprecated attribute: ms.component. Use ms.subservice instead.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`. Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná. Pak zvolte platnou hodnotu `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
