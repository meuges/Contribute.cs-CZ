---
title: Řazení přesměrování – Balíček pro vytváření obsahu na webu Docs
description: Přečtěte si, jak řadit přesměrování v balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336674"
---
# <a name="sort-redirects"></a>Řazení přesměrování

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

S vývojem sady dokumentů docs.microsoft.com dochází k odstraňování některých souborů Markdownu. Při odstranění souboru je potřeba zadat přesměrování, aby se jakýkoli odkaz na daný článek správně vyřešil. Přesměrování se zadávají v souboru *.openpublishing.redirection.json*.

1. Otevřete paletu příkazů a stiskněte klávesu <kbd>F1</kbd> (nebo <kbd>⇧⌘P</kbd> na macOS).
1. Zadejte: **Docs: Sort master redirection file**
1. Vyberte příkaz, který se má spustit.
1. Prohlédněte si změny v souboru *.openpublishing.redirection.json*.

## <a name="considerations"></a>Důležité informace

K původní podobě souboru *.openpublishing.redirection.json* se váže pojem řetězení. Soubory přidané jako přesměrování po nějaké době zastarávají. Dochází k tomu tehdy, když se odstraní soubor A a potřebuje přesměrování na soubor B, a následně se soubor B také odstraní a přesměruje na soubor C. Obě položky by ideálně měly vést na C (A se přesměruje na C a B zůstane stejné). Jedná se o drobné zvýšení výkonu. Na této funkci se stále aktivně pracuje.

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce:

[![Ukázka řazení přesměrování](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
