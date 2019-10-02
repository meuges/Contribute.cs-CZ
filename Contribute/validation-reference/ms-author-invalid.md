---
title: ms-author-invalid
description: Vysvětlení a řešení problému sestavení ms-author-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481697"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Upozornění

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Řešení

Ověřte, že hodnota `ms.author` je platný alias Microsoftu aktuálního autora. Doporučujeme, aby byl jako autor určen zaměstnanec na plný úvazek nebo distribuční seznam představující tým, ne externí dodavatel s krátkodobým kontraktem. Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.

Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
