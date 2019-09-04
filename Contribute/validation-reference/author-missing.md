---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236323"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Upozornění

`Missing attribute: author. Add the current author's GitHub ID.`

Atribut `author` identifikuje autora článku pomocí ID GitHubu. 

## <a name="resolution"></a>Řešení

Jako hlavičku YML zadejte ID GitHubu aktuálního autora:

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Toto by měl být *aktuální* vlastník článku, nikoli původní autor, pokud došlo ke změně vlastnictví.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
