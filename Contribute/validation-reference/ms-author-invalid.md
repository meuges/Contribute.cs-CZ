---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246293"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Upozornění

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Řešení

Aktualizujte hodnotu `ms.author` platným aliasem Microsoftu, který patří aktuálnímu autorovi. Doporučujeme jako autora zvolit zaměstnance na plný úvazek nebo týmový distribuční seznam, nikoli krátkodobého dodavatele. Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.

Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
