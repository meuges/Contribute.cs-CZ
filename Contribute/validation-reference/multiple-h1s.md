---
title: multiple-h1
description: Vysvětlení a řešení problému sestavení multiple-h1 na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: c97ae237cd2ce657bd02132af5169cb6544ae306
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246274"
---
# <a name="multiple-h1"></a><span data-ttu-id="9e8e3-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="9e8e3-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9e8e3-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="9e8e3-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="9e8e3-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="9e8e3-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="9e8e3-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="9e8e3-108">V každém souboru může být jenom jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="9e8e3-109">Tato zpráva se také může zobrazit, pokud článek obsahuje řádek stejných znaků, které tvoří dvojité podtržení, například: `=======`.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="9e8e3-110">Jde o alternativní syntaxi jazyka Markdown pro nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="9e8e3-111">Často se s ní můžeme setkat u konfliktů při sloučení:</span><span class="sxs-lookup"><span data-stu-id="9e8e3-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="9e8e3-112">Řešení</span><span class="sxs-lookup"><span data-stu-id="9e8e3-112">Resolution</span></span>

<span data-ttu-id="9e8e3-113">Pro nápravu tohoto problému změňte úroveň dalších nadpisů H1 na H2 (`##`) nebo reorganizujte soubor jiným způsobem.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="9e8e3-114">Upozorňujeme, že přeskakování úrovní nadpisů (třeba H3 po H1) je zakázané.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="9e8e3-115">Pokud další nadpis H1 ve skutečnosti představuje dvojité podtržení (`=======`), podle potřeby ho buď odeberte, nebo ho nahraďte nadpisem hashtag, jako je například `##`.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="9e8e3-116">Pokud je dvojité podtržení součástí konfliktu při sloučení, nezapomeňte odebrat také počáteční a koncové značky konfliktu při sloučení a zastaralý text.</span><span class="sxs-lookup"><span data-stu-id="9e8e3-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
