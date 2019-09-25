---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247424"
---
# <a name="h1-missing"></a><span data-ttu-id="3c024-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="3c024-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3c024-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="3c024-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="3c024-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="3c024-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="3c024-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="3c024-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="3c024-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="3c024-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c024-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="3c024-108">Resolution</span></span>

<span data-ttu-id="3c024-109">Pro nápravu tohoto problému přidejte do souboru nadpis H1 jako první obsah za blokem metadat YML:</span><span class="sxs-lookup"><span data-stu-id="3c024-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="3c024-110">Toto pravidlo se netýká zahrnutých souborů.</span><span class="sxs-lookup"><span data-stu-id="3c024-110">This rule does not apply to included files.</span></span> <span data-ttu-id="3c024-111">Pokud se v zahrnutých souborech zobrazí výsledky představující nadpisy H1, budete pravděpodobně muset zahrnuté soubory přesunout do složky `includes`.</span><span class="sxs-lookup"><span data-stu-id="3c024-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="3c024-112">Složka `includes` se může v cestě k souboru nacházet na libovolné úrovni.</span><span class="sxs-lookup"><span data-stu-id="3c024-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="3c024-113">Sestavení na webu Docs na základě cesty rozpozná daný soubor jako zahrnutý soubor a ověření H1 se nebudou provádět.</span><span class="sxs-lookup"><span data-stu-id="3c024-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="3c024-114">Běžnou příčinou chybějících nadpisů H1 v nadřazených souborech je chybné použití zahrnutých souborů: H1 je v zahrnutém souboru, ne v nadřazeném souboru.</span><span class="sxs-lookup"><span data-stu-id="3c024-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="3c024-115">To není povoleno, protože použití nadpisu H1 v zahrnutém souboru znamená, že v nadřazených souborech budou duplicitní nadpisy H1 nebo bude zahrnutý soubor použitý jen jednou.</span><span class="sxs-lookup"><span data-stu-id="3c024-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="3c024-116">Nadpisy H1 by měly být v rámci sady obsahu jedinečné a zahrnuté soubory by se měly používat jen ke sdílení obsahu mezi více soubory.</span><span class="sxs-lookup"><span data-stu-id="3c024-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="3c024-117">Pokud se zobrazí výsledky `h1-missing`, protože se nadpis H1 nachází v zahrnutém souboru, dá se to vyřešit přesunutím nadpisu – a veškerého zahrnutého obsahu, pokud je zahrnutý soubor použitý jen jednou – do nadřazeného souboru.</span><span class="sxs-lookup"><span data-stu-id="3c024-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="3c024-118">Další informace o zahrnutých souborech v dokumentaci najdete v interním článku Microsoftu o [zahrnování opakovaně použitelného obsahu do článků](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span><span class="sxs-lookup"><span data-stu-id="3c024-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
