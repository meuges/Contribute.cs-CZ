---
title: yaml-header-invalid
description: Vysvětlení a řešení problému sestavení yaml-header-invalid na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459020"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="76dca-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="76dca-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="76dca-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="76dca-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="76dca-105">Obvykle to znamená, že hodnota metadat bez uvozovek v hlavičce YAML obsahuje dvojtečku nebo jiný speciální znak.</span><span class="sxs-lookup"><span data-stu-id="76dca-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="76dca-106">Může to také znamenat, že v páru klíč-hodnota za dvojtečkou chybí mezera.</span><span class="sxs-lookup"><span data-stu-id="76dca-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="76dca-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="76dca-107">Resolution</span></span>

<span data-ttu-id="76dca-108">Zkontrolujte hlavičku YAML.</span><span class="sxs-lookup"><span data-stu-id="76dca-108">Review your YAML header.</span></span> <span data-ttu-id="76dca-109">Hledejte následující chyby.</span><span class="sxs-lookup"><span data-stu-id="76dca-109">Look for the following mistakes.</span></span>

<span data-ttu-id="76dca-110">Dvojtečka v hodnotě bez uvozovek:</span><span class="sxs-lookup"><span data-stu-id="76dca-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="76dca-111">Změňte na:</span><span class="sxs-lookup"><span data-stu-id="76dca-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="76dca-112">V páru klíč-hodnota za dvojtečkou chybí mezera:</span><span class="sxs-lookup"><span data-stu-id="76dca-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="76dca-113">Změňte na:</span><span class="sxs-lookup"><span data-stu-id="76dca-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
