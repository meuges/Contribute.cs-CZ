---
title: external-bookmark-not-found
description: Vysvětlení a řešení problému sestavení external-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427299"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Upozornění

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Pokoušíte se vytvořit odkaz na nadpis v jiném souboru, který neexistuje.

## <a name="resolution"></a>Řešení

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Zkontrolujte soubor, na který odkazujete, a aktualizujte odkaz záložky tak, aby směřoval na platný oddíl v daném souboru.

K odkazu na nadpis oddílu v jiném článku použijte odkaz na daný soubor nebo server, za kterým bude následovat symbol hash a text nadpisu. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami. Tady je příklad:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
