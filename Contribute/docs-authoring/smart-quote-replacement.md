---
title: Automatická nahrazení inteligentních uvozovek – Balíček pro vytváření obsahu na webu Docs
description: Tady se dozvíte, jak automaticky nahrazovat inteligentní uvozovky s Balíčkem pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336697"
---
# <a name="smart-quote-replacement"></a>Nahrazení inteligentních uvozovek

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

Vývojáři obsahu zodpovídají za vytváření některých z nejpokročilejších funkcí moderní technologie a inteligentních postupů, přesto naše nástroje dnes ještě dávají přednost používání „neinteligentních uvozovek“ v Markdownu. Protiklad k tomu jsou samozřejmě „inteligentní uvozovky“. Inteligentní uvozovky jsou běžné s ideálními typografiemi, ale neupřednostňují se u Markdownu a vykresleného HTML.

Při práci na dokumentu v Microsoft Wordu jste si například asi všimli, že když podržíte <kbd>Shift</kbd> a zadáte <kbd>"</kbd>, Microsoft Word znak `"` rychle nahradí ekvivalentním znakem `“` inteligentních uvozovek.

| Description        | Unicode  | Inteligentní uvozovky | Nahrazení |
|--------------------|----------|-------------|-------------|
| Dvojité levé uvozovky  | `\u201c` | `“`         | `"`         |
| Dvojité pravé uvozovky | `\u201d` | `”`         | `"`         |
| Jednoduchá levá uvozovka  | `\u2018` | `‘`         | `'`         |
| Jednoduchá pravá uvozovka | `\u2019` | `’`         | `'`         |

Když v souboru Markdownu ( *\*.md*) vložíte text nebo aktualizujete obsah, tato funkce aktivně vyhodnotí obsah a automaticky nahradí hodnoty odpovídajícím způsobem.

> [!NOTE]
> Funkce nahrazení inteligentních uvozovek také nahrazuje jiné znaky, mimo jiné například; (`©, ™, ®, •`, znaky dolního indexu a horního indexu). To je užitečné při vkládání textu z dokumentů aplikace Word.

## <a name="preferences"></a>Předvolby

Tato funkce je volitelná, ale výchozí hodnota je `true`. Zapnutí nebo vypnutí této funkce:

1. Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.
1. Přepněte nastavení v oddíle **Markdown: Nahrazení inteligentních uvozovek**.

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce.

[![Ukázka nahrazení inteligentních uvozovek](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
