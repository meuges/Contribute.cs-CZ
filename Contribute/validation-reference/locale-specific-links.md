---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Odkazy specifické pro národní prostředí
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841261"
---
# <a name="locale-specific-links"></a>Odkazy specifické pro národní prostředí

Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu. Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí. Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.

Odeberte kódy národního prostředí z odkazů na weby Microsoftu. Tady je příklad.

Před:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Po:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

Do tohoto ověřování jsou zahrnuty tyto weby:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com