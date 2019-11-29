---
title: insecure-link
description: Vysvětlení a řešení problému sestavení insecure-link na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528848"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Toto pravidlo bylo nejdříve povoleno jako Návrh, aby týmy pro obsah měly čas na posouzení dopadu a na vytvoření plánu, jak úložiště vyčistit. **20. 12. 2019 bude úroveň zvýšena na Upozornění**.

## <a name="suggestion"></a>Návrh

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Tato zpráva znamená, že jste v jazyce Markdown použili explicitní odkaz v `http` nebo neupravenou adresu URL, například `www.microsoft.com`. Neupravené adresy URL se při publikování na webu Docs převádějí na nezabezpečené odkazy, a proto byste je neměli používat.

## <a name="resolution"></a>Řešení

Změňte všechny adresy URL webů Microsoftu tak, aby místo `http` používaly `https`.

Pokud odkaz představuje neupravenou adresu URL, změňte ji na explicitní odkaz Markdownu, který začíná na `https`, například:

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu. Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`. Spuštění skriptu:
>
> 1. Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.
> 1. Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.
> 1. Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.

V některých případech může být nutné zadokumentovat webové adresy, například plně kvalifikované názvy domén, které nemají mít podobu prokliknutelných odkazů. Ty by měly být ve stylu vloženého kódu, například:

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
