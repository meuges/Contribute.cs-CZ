---
title: hard-coded-locale
description: Vysvětlení a řešení problému sestavení hard-coded-locale na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 0fbc7634e00202fdfdf607b9504744a6d9846792
ms.sourcegitcommit: 836d4d6127fabb5569ffc0809db5fb25e46038b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2019
ms.locfileid: "72590868"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="2f5e4-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="2f5e4-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f5e4-104">Toto pravidlo bylo nejdříve povoleno jako Návrh, aby týmy pro obsah měly čas na posouzení dopadu a na vytvoření plánu, jak úložiště vyčistit.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="2f5e4-105">**20. 12. 2019 bude úroveň zvýšena na Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="2f5e4-106">Návrh</span><span class="sxs-lookup"><span data-stu-id="2f5e4-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="2f5e4-107">Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="2f5e4-108">Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="2f5e4-109">Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="2f5e4-110">Do tohoto ověřování jsou zahrnuty tyto weby:</span><span class="sxs-lookup"><span data-stu-id="2f5e4-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="2f5e4-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2f5e4-111">azure.microsoft.com</span></span>
- <span data-ttu-id="2f5e4-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2f5e4-112">docs.microsoft.com</span></span>
- <span data-ttu-id="2f5e4-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2f5e4-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="2f5e4-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="2f5e4-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="2f5e4-115">Řešení</span><span class="sxs-lookup"><span data-stu-id="2f5e4-115">Resolution</span></span>

<span data-ttu-id="2f5e4-116">Odeberte kódy národního prostředí z odkazů na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="2f5e4-117">Tady je příklad.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-117">The following is an example.</span></span>

<span data-ttu-id="2f5e4-118">Před:</span><span class="sxs-lookup"><span data-stu-id="2f5e4-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="2f5e4-119">Po:</span><span class="sxs-lookup"><span data-stu-id="2f5e4-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="2f5e4-120">Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="2f5e4-121">Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="2f5e4-122">Spuštění skriptu:</span><span class="sxs-lookup"><span data-stu-id="2f5e4-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="2f5e4-123">Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="2f5e4-124">Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="2f5e4-125">Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.</span><span class="sxs-lookup"><span data-stu-id="2f5e4-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
