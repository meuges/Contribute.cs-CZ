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
# <a name="smart-quote-replacement"></a><span data-ttu-id="6462d-103">Nahrazení inteligentních uvozovek</span><span class="sxs-lookup"><span data-stu-id="6462d-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="6462d-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="6462d-104">Summary</span></span>

<span data-ttu-id="6462d-105">Vývojáři obsahu zodpovídají za vytváření některých z nejpokročilejších funkcí moderní technologie a inteligentních postupů, přesto naše nástroje dnes ještě dávají přednost používání „neinteligentních uvozovek“ v Markdownu.</span><span class="sxs-lookup"><span data-stu-id="6462d-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="6462d-106">Protiklad k tomu jsou samozřejmě „inteligentní uvozovky“.</span><span class="sxs-lookup"><span data-stu-id="6462d-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="6462d-107">Inteligentní uvozovky jsou běžné s ideálními typografiemi, ale neupřednostňují se u Markdownu a vykresleného HTML.</span><span class="sxs-lookup"><span data-stu-id="6462d-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="6462d-108">Při práci na dokumentu v Microsoft Wordu jste si například asi všimli, že když podržíte <kbd>Shift</kbd> a zadáte <kbd>"</kbd>, Microsoft Word znak `"` rychle nahradí ekvivalentním znakem `“` inteligentních uvozovek.</span><span class="sxs-lookup"><span data-stu-id="6462d-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="6462d-109">Description</span><span class="sxs-lookup"><span data-stu-id="6462d-109">Description</span></span>        | <span data-ttu-id="6462d-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="6462d-110">Unicode</span></span>  | <span data-ttu-id="6462d-111">Inteligentní uvozovky</span><span class="sxs-lookup"><span data-stu-id="6462d-111">Smart Quote</span></span> | <span data-ttu-id="6462d-112">Nahrazení</span><span class="sxs-lookup"><span data-stu-id="6462d-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="6462d-113">Dvojité levé uvozovky</span><span class="sxs-lookup"><span data-stu-id="6462d-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="6462d-114">Dvojité pravé uvozovky</span><span class="sxs-lookup"><span data-stu-id="6462d-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="6462d-115">Jednoduchá levá uvozovka</span><span class="sxs-lookup"><span data-stu-id="6462d-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="6462d-116">Jednoduchá pravá uvozovka</span><span class="sxs-lookup"><span data-stu-id="6462d-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="6462d-117">Když v souboru Markdownu ( *\*.md*) vložíte text nebo aktualizujete obsah, tato funkce aktivně vyhodnotí obsah a automaticky nahradí hodnoty odpovídajícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6462d-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="6462d-118">Funkce nahrazení inteligentních uvozovek také nahrazuje jiné znaky, mimo jiné například; (`©, ™, ®, •`, znaky dolního indexu a horního indexu).</span><span class="sxs-lookup"><span data-stu-id="6462d-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="6462d-119">To je užitečné při vkládání textu z dokumentů aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="6462d-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="6462d-120">Předvolby</span><span class="sxs-lookup"><span data-stu-id="6462d-120">Preferences</span></span>

<span data-ttu-id="6462d-121">Tato funkce je volitelná, ale výchozí hodnota je `true`.</span><span class="sxs-lookup"><span data-stu-id="6462d-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="6462d-122">Zapnutí nebo vypnutí této funkce:</span><span class="sxs-lookup"><span data-stu-id="6462d-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="6462d-123">Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="6462d-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="6462d-124">Přepněte nastavení v oddíle **Markdown: Nahrazení inteligentních uvozovek**.</span><span class="sxs-lookup"><span data-stu-id="6462d-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="6462d-125">V praxi</span><span class="sxs-lookup"><span data-stu-id="6462d-125">In action</span></span>

<span data-ttu-id="6462d-126">Tady vidíte krátkou ukázku této funkce.</span><span class="sxs-lookup"><span data-stu-id="6462d-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="6462d-127">[![Ukázka nahrazení inteligentních uvozovek](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6462d-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
