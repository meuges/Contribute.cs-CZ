---
title: yaml-header-invalid
description: Vysvětlení a řešení problému sestavení yaml-header-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459020"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Upozornění

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Obvykle to znamená, že hodnota metadat bez uvozovek v hlavičce YAML obsahuje dvojtečku nebo jiný speciální znak. Může to také znamenat, že v páru klíč-hodnota za dvojtečkou chybí mezera.

## <a name="resolution"></a>Řešení

Zkontrolujte hlavičku YAML. Hledejte následující chyby.

Dvojtečka v hodnotě bez uvozovek:

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Změňte na:

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

V páru klíč-hodnota za dvojtečkou chybí mezera:

```yml
---
title:I omitted a space.
---
```

Změňte na:

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
