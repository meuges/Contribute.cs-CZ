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
# <a name="sort-redirects"></a><span data-ttu-id="2bb57-103">Řazení přesměrování</span><span class="sxs-lookup"><span data-stu-id="2bb57-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="2bb57-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="2bb57-104">Summary</span></span>

<span data-ttu-id="2bb57-105">S vývojem sady dokumentů docs.microsoft.com dochází k odstraňování některých souborů Markdownu.</span><span class="sxs-lookup"><span data-stu-id="2bb57-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="2bb57-106">Při odstranění souboru je potřeba zadat přesměrování, aby se jakýkoli odkaz na daný článek správně vyřešil.</span><span class="sxs-lookup"><span data-stu-id="2bb57-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="2bb57-107">Přesměrování se zadávají v souboru *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="2bb57-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="2bb57-108">Otevřete paletu příkazů a stiskněte klávesu <kbd>F1</kbd> (nebo <kbd>⇧⌘P</kbd> na macOS).</span><span class="sxs-lookup"><span data-stu-id="2bb57-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="2bb57-109">Zadejte: **Docs: Sort master redirection file**</span><span class="sxs-lookup"><span data-stu-id="2bb57-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="2bb57-110">Vyberte příkaz, který se má spustit.</span><span class="sxs-lookup"><span data-stu-id="2bb57-110">Select the command to execute it</span></span>
1. <span data-ttu-id="2bb57-111">Prohlédněte si změny v souboru *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="2bb57-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="2bb57-112">Důležité informace</span><span class="sxs-lookup"><span data-stu-id="2bb57-112">Considerations</span></span>

<span data-ttu-id="2bb57-113">K původní podobě souboru *.openpublishing.redirection.json* se váže pojem řetězení.</span><span class="sxs-lookup"><span data-stu-id="2bb57-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="2bb57-114">Soubory přidané jako přesměrování po nějaké době zastarávají.</span><span class="sxs-lookup"><span data-stu-id="2bb57-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="2bb57-115">Dochází k tomu tehdy, když se odstraní soubor A a potřebuje přesměrování na soubor B, a následně se soubor B také odstraní a přesměruje na soubor C. Obě položky by ideálně měly vést na C (A se přesměruje na C a B zůstane stejné).</span><span class="sxs-lookup"><span data-stu-id="2bb57-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="2bb57-116">Jedná se o drobné zvýšení výkonu. Na této funkci se stále aktivně pracuje.</span><span class="sxs-lookup"><span data-stu-id="2bb57-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="2bb57-117">V praxi</span><span class="sxs-lookup"><span data-stu-id="2bb57-117">In action</span></span>

<span data-ttu-id="2bb57-118">Tady vidíte krátkou ukázku této funkce:</span><span class="sxs-lookup"><span data-stu-id="2bb57-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="2bb57-119">[![Ukázka řazení přesměrování](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2bb57-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
