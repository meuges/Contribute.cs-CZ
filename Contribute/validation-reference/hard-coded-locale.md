---
title: hard-coded-locale
description: Vysvětlení a řešení problému sestavení hard-coded-locale na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310320"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>Upozornění

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu. Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí. Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.

Do tohoto ověřování jsou zahrnuty tyto weby:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
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