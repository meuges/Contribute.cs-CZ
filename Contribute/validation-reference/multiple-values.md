---
title: multiple-values
description: Vysvětlení a řešení problému sestavení multiple-values na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 515a8cd76cbd3d9bd117b1d0d59492f4a77bea4c
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236467"
---
# <a name="multiple-values"></a><span data-ttu-id="b168e-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="b168e-103">multiple-values</span></span>

## <a name="warning"></a><span data-ttu-id="b168e-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="b168e-104">Warning</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="b168e-105">Zadali jste více hodnot atributu, u kterého je povolena jen jedna hodnota.</span><span class="sxs-lookup"><span data-stu-id="b168e-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="b168e-106">Atributy, které nemůžou mít více hodnot, je potřeba zadávat ve formátu YML s jednou (tj. skalární) hodnotou.</span><span class="sxs-lookup"><span data-stu-id="b168e-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="b168e-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="b168e-107">Resolution</span></span>

<span data-ttu-id="b168e-108">Tento návrh se vám zobrazí vždy, když pro atribut s jednou hodnotou použijete pole více hodnot, ať už toto pole obsahuje více hodnot, nebo jen jedinou.</span><span class="sxs-lookup"><span data-stu-id="b168e-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="b168e-109">U atributů s více hodnotami, jako je `ms.custom`, podporuje jazyk YML následující formáty polí:</span><span class="sxs-lookup"><span data-stu-id="b168e-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="b168e-110">Tyto formáty nejsou platné pro atributy s jednou hodnotou, jako je `author`.</span><span class="sxs-lookup"><span data-stu-id="b168e-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="b168e-111">Pokud jste zadali více hodnot, zkontrolujte je a určete, která je správná.</span><span class="sxs-lookup"><span data-stu-id="b168e-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="b168e-112">Odeberte ostatní hodnoty a správnou hodnotu zadejte bez závorek na stejný řádek jako atribut, takto:</span><span class="sxs-lookup"><span data-stu-id="b168e-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="b168e-113">Pokud jste použili pole s jednou hodnotou, změňte ho na skalární formát popsaný výše.</span><span class="sxs-lookup"><span data-stu-id="b168e-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="b168e-114">Kterých atributů se to týká</span><span class="sxs-lookup"><span data-stu-id="b168e-114">Attributes in scope</span></span>

<span data-ttu-id="b168e-115">Následující atributy musí mít jenom jednu hodnotu:</span><span class="sxs-lookup"><span data-stu-id="b168e-115">The following attributes are required to be single-valued:</span></span>

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
