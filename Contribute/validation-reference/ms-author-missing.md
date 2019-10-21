---
title: ms-author-missing
description: Vysvětlení a řešení problému sestavení ms-author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246255"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>Upozornění

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>Řešení

Pro hodnotu `ms.author` zadejte alias Microsoftu aktuálního autora. Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví. Doporučujeme jako autora zvolit zaměstnance na plný úvazek nebo týmový distribuční seznam, nikoli krátkodobého dodavatele. 

Pokud tento alias představuje distribuční seznam, musí být také na seznamu povolených pro `ms.author`.

Platné hodnoty pro distribuční seznamy `ms.author` se dají najít na tomto [interním webu Microsoftu](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
