---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459112"
---
# <a name="h1-missing"></a><span data-ttu-id="59abe-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="59abe-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="59abe-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="59abe-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="59abe-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="59abe-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="59abe-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="59abe-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="59abe-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="59abe-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="59abe-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="59abe-108">Resolution</span></span>

<span data-ttu-id="59abe-109">Pro nápravu tohoto problému přidejte do souboru nadpis H1 jako první obsah za blokem metadat YML:</span><span class="sxs-lookup"><span data-stu-id="59abe-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="59abe-110">Toto pravidlo se netýká zahrnutých souborů.</span><span class="sxs-lookup"><span data-stu-id="59abe-110">This rule does not apply to included files.</span></span> <span data-ttu-id="59abe-111">Pokud se upozornění H1 zobrazí u zahrnutých souborů, budete pravděpodobně muset zahrnuté soubory přesunout do složky `includes`.</span><span class="sxs-lookup"><span data-stu-id="59abe-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="59abe-112">Složka `includes` se může v cestě k souboru nacházet na libovolné úrovni.</span><span class="sxs-lookup"><span data-stu-id="59abe-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="59abe-113">Sestavení na webu Docs na základě cesty rozpozná daný soubor jako zahrnutý soubor a ověření H1 se nebudou provádět.</span><span class="sxs-lookup"><span data-stu-id="59abe-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]