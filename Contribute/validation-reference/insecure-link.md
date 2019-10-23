---
title: insecure-link
description: Vysvětlení a řešení problému sestavení insecure-link na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587684"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Toto pravidlo bylo nejdříve povoleno jako Návrh, aby týmy pro obsah měly čas na posouzení dopadu a na vytvoření plánu, jak úložiště vyčistit. **20. 12. 2019 bude úroveň zvýšena na Upozornění**.

## <a name="suggestion"></a>Návrh

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Tato zpráva znamená, že jste v jazyce Markdown použili explicitní odkaz v `http` nebo neupravenou adresu URL, například `www.microsoft.com`. Neupravené adresy URL se při publikování na webu Docs převádějí na nezabezpečené odkazy, a proto byste je neměli používat.

## <a name="resolution"></a>Řešení

Změňte všechny adresy URL webů Microsoftu tak, aby místo `http` používaly `https`.

Pokud odkaz představuje neupravenou adresu URL, změňte ji na explicitní odkaz Markdownu, který začíná na `https`.

> [!TIP]
> Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu. Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`. Spuštění skriptu:
>
> 1. Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.
> 1. Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.
> 1. Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
