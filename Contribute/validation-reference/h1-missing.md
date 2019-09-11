---
title: h1-missing
description: Vysvětlení a řešení problému sestavení h1-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 677127d09349445bb80778dfb501d7d4294ea46b
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848473"
---
# <a name="h1-missing"></a><span data-ttu-id="4d744-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="4d744-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="4d744-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="4d744-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="4d744-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="4d744-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="4d744-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="4d744-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="4d744-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="4d744-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="4d744-108">Řešení</span><span class="sxs-lookup"><span data-stu-id="4d744-108">Resolution</span></span>

<span data-ttu-id="4d744-109">Pro nápravu tohoto problému přidejte do souboru nadpis H1 jako první obsah za blokem metadat YML:</span><span class="sxs-lookup"><span data-stu-id="4d744-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="4d744-110">Toto pravidlo se netýká zahrnutých souborů.</span><span class="sxs-lookup"><span data-stu-id="4d744-110">This rule does not apply to included files.</span></span> <span data-ttu-id="4d744-111">Pokud se upozornění H1 zobrazí u zahrnutých souborů, budete pravděpodobně muset zahrnuté soubory přesunout do složky `includes`.</span><span class="sxs-lookup"><span data-stu-id="4d744-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="4d744-112">Složka `includes` se může v cestě k souboru nacházet na libovolné úrovni.</span><span class="sxs-lookup"><span data-stu-id="4d744-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="4d744-113">Sestavení na webu Docs na základě cesty rozpozná daný soubor jako zahrnutý soubor a ověření H1 se nebudou provádět.</span><span class="sxs-lookup"><span data-stu-id="4d744-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]