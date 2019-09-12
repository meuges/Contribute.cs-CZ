---
title: internal-bookmark-not-found
description: Vysvětlení a řešení problému sestavení internal-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856213"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Upozornění

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

Pokoušíte se vytvořit odkaz na nadpis v aktuálním souboru nebo jiném souboru, který neexistuje.

## <a name="resolution"></a>Řešení

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Ověřte nadpis, na který chcete vytvořit odkaz, a aktualizujte daný odkaz.

K vytvoření odkazu na oddíl v aktuálním článku použijte symbol hash a za ním text nadpisu. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami. Tady je příklad:

```markdown
[Managed Disks](#managed-disks)
```

Pokud chcete vytvořit odkaz na nadpis v jiném souboru, použijte relativní odkaz na tento soubor následovaný symbolem hash a textem nadpisu. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami. Tady je příklad:

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
