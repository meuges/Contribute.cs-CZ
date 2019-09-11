---
title: author-missing
description: Vysvětlení a řešení problému sestavení author-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848585"
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
