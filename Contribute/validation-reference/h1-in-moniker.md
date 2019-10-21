---
title: h1-in-moniker
description: Vysvětlení a řešení problému sestavení h1-in-moniker na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246353"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="a3c18-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="a3c18-103">h1-in-moniker</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a3c18-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="a3c18-104">Suggestion</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="a3c18-105">H1 se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="a3c18-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a3c18-106">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="a3c18-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="a3c18-107">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (#) a mezerou, za kterou následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="a3c18-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="a3c18-108">V každém souboru může být jenom jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="a3c18-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="a3c18-109">V oddílech monikerů nejsou nadpisy H1 povolené, protože můžou snadno vést k duplicitám nebo chybějícím nadpisům H1 podle toho, jak je nakonfigurovaná správa verzí.</span><span class="sxs-lookup"><span data-stu-id="a3c18-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="a3c18-110">Tato zpráva se také může zobrazit, pokud oddíl monikeru obsahuje řádek stejných znaků, které tvoří dvojité podtržení. Příklad: `=======`.</span><span class="sxs-lookup"><span data-stu-id="a3c18-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="a3c18-111">Jde o alternativní syntaxi jazyka Markdown pro nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="a3c18-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="a3c18-112">Často se s ní můžeme setkat u konfliktů při sloučení:</span><span class="sxs-lookup"><span data-stu-id="a3c18-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="a3c18-113">Řešení</span><span class="sxs-lookup"><span data-stu-id="a3c18-113">Resolution</span></span>

<span data-ttu-id="a3c18-114">Tento problém opravíte tak, že nadpisy H1 odeberete ze všech oddílů a zajistíte, aby nadpis H1 na začátku článku odpovídal všem oddílům monikerů.</span><span class="sxs-lookup"><span data-stu-id="a3c18-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="a3c18-115">Upozorňujeme, že přeskakování úrovní nadpisů (třeba H3 po H1) je zakázané.</span><span class="sxs-lookup"><span data-stu-id="a3c18-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="a3c18-116">Pokud nadpis H1 v oddílu monikeru znamená ve skutečnosti dvojité podtržení (`=======`), podle potřeby ho buď odeberte,nebo ho nahraďte nadpisem hashtag, například `##`.</span><span class="sxs-lookup"><span data-stu-id="a3c18-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="a3c18-117">Pokud je dvojité podtržení součástí konfliktu při sloučení, nezapomeňte odebrat také počáteční a koncové značky konfliktu při sloučení a zastaralý text.</span><span class="sxs-lookup"><span data-stu-id="a3c18-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
