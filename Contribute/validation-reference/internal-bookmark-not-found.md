---
title: internal-bookmark-not-found
description: Vysvětlení a řešení problému sestavení internal-bookmark-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427311"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Připravujeme**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

`Current file doesn't contain a bookmark named '{bookmark}'.`

Pokoušíte se vytvořit odkaz na nadpis v aktuálním souboru, který neexistuje.

## <a name="resolution"></a>Řešení

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Ověřte nadpis, na který chcete vytvořit odkaz, a aktualizujte daný odkaz.

K vytvoření odkazu na oddíl v aktuálním článku použijte symbol hash a za ním text nadpisu. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami. Tady je příklad:

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
