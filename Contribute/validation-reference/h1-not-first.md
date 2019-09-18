---
title: h1-not-first
description: Vysvětlení a řešení problému sestavení h1-not-first na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895455"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Návrh

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
