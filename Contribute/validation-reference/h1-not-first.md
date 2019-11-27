---
title: h1-not-first
description: Vysvětlení a řešení problému sestavení h1-not-first na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528919"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>Upozornění

`Markdown content is not allowed before H1.`

Před záhlavím H1 v souboru Markdown se může nacházet jen hlavička metadat YAML. Pokud chcete například do horní části článku přidat poznámku nebo obrázek, musí následovat po H1. Toto není povoleno:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Místo toho postupujte takto:

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Další běžnou příčinou tohoto problému jsou [značky pořadí bajtů (BOM)](http://www.websina.com/bugzero/kb/unicode-bom.html) před hlavičkou YAML. Někdy se vkládají při problémech s kódováním během potvrzování obsahu do úložišť. Výsledkem je chybné vykreslování na GitHubu a měly by být odebrány.

## <a name="resolution"></a>Řešení

Odeberte veškerý obsah před záhlavím H1 s výjimkou hlavičky metadat YAML.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
