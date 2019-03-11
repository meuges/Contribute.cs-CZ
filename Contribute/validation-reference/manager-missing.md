---
title: manager-missing
description: Vysvětlení a řešení problému sestavení manager-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427310"
---
# <a name="manager-missing"></a>manager-missing

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Některé skupiny obsahu vyžadují, aby autorova vedoucího identifikoval atribut `manager`.

## <a name="resolution"></a>Řešení

Přidejte platný alias Microsoftu pro atribut `manager`:

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
