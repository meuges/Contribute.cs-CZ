---
title: hard-coded-locale
description: Vysvětlení a řešení problému sestavení hard-coded-locale na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166822"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> Toto pravidlo bylo nejdříve povoleno jako Návrh, aby týmy pro obsah měly čas na posouzení dopadu a na vytvoření plánu, jak úložiště vyčistit. **20. 12. 2019 bude úroveň zvýšena na Upozornění**.

## <a name="suggestion"></a>Návrh

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu. Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí. Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.

Do tohoto ověřování jsou zahrnuty tyto weby:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com (kromě webu social.msdn.com, který k propojení se správným fórem potřebuje národní prostředí)
- technet.microsoft.com

## <a name="resolution"></a>Řešení

Odeberte kódy národního prostředí z odkazů na weby Microsoftu. Tady je příklad.

Před:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Po:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu. Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`. Spuštění skriptu:
>
> 1. Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.
> 1. Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.
> 1. Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
