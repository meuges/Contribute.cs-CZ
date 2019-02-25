---
title: multiple-values
description: Vysvětlení a řešení problému sestavení multiple-values na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465109"
---
# <a name="multiple-values"></a><span data-ttu-id="d49b4-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="d49b4-103">multiple-values</span></span>

<span data-ttu-id="d49b4-104">**Připravujeme**</span><span class="sxs-lookup"><span data-stu-id="d49b4-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="d49b4-105">Návrh</span><span class="sxs-lookup"><span data-stu-id="d49b4-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="d49b4-106">Zadali jste více hodnot atributu, u kterého je povolena jen jedna hodnota.</span><span class="sxs-lookup"><span data-stu-id="d49b4-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="d49b4-107">Atributy, které nemůžou mít více hodnot, je potřeba zadávat ve formátu YML s jednou (tj. skalární) hodnotou.</span><span class="sxs-lookup"><span data-stu-id="d49b4-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="d49b4-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="d49b4-108">Resolution</span></span>

<span data-ttu-id="d49b4-109">Tento návrh se vám zobrazí vždy, když pro atribut s jednou hodnotou použijete pole více hodnot, ať už toto pole obsahuje více hodnot, nebo jen jedinou.</span><span class="sxs-lookup"><span data-stu-id="d49b4-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="d49b4-110">U atributů s více hodnotami, jako je `ms.custom`, podporuje jazyk YML následující formáty polí:</span><span class="sxs-lookup"><span data-stu-id="d49b4-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="d49b4-111">Tyto formáty nejsou platné pro atributy s jednou hodnotou, jako je `author`.</span><span class="sxs-lookup"><span data-stu-id="d49b4-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="d49b4-112">Pokud jste zadali více hodnot, zkontrolujte je a určete, která je správná.</span><span class="sxs-lookup"><span data-stu-id="d49b4-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="d49b4-113">Odeberte ostatní hodnoty a správnou hodnotu zadejte bez závorek na stejný řádek jako atribut, takto:</span><span class="sxs-lookup"><span data-stu-id="d49b4-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="d49b4-114">Pokud jste použili pole s jednou hodnotou, změňte ho na skalární formát popsaný výše.</span><span class="sxs-lookup"><span data-stu-id="d49b4-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
