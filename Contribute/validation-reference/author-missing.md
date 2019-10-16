---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288519"
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
