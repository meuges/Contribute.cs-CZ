---
title: deprecated-attribute
description: Vysvětlení a řešení problému sestavení deprecated-attribute na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987783"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Deprecated attribute: ms.component. Use ms.subservice instead.`

K zadání cloudových služeb používejte `ms.service`. Pokud chcete o `ms.service` zadat podrobnější informace, můžete volitelně zadat `ms.subservice`. Nepoužívejte `ms.component`, pro tento obsah je to zastaralé.

## <a name="resolution"></a>Řešení

Ujistěte se, jestli je hodnota `ms.service` pro váš článek správná. Pak zvolte platnou hodnotu `ms.subservice`.

Platné hodnoty se dají najít na [tomto interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
