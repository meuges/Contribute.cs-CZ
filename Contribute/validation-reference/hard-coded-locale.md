---
title: hard-coded-locale
description: Vysvětlení a řešení problému sestavení hard-coded-locale na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310320"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="b7d65-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="b7d65-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="b7d65-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="b7d65-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="b7d65-105">Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="b7d65-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="b7d65-106">Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí.</span><span class="sxs-lookup"><span data-stu-id="b7d65-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="b7d65-107">Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.</span><span class="sxs-lookup"><span data-stu-id="b7d65-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="b7d65-108">Do tohoto ověřování jsou zahrnuty tyto weby:</span><span class="sxs-lookup"><span data-stu-id="b7d65-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="b7d65-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b7d65-109">azure.microsoft.com</span></span>
- <span data-ttu-id="b7d65-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b7d65-110">docs.microsoft.com</span></span>
- <span data-ttu-id="b7d65-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b7d65-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="b7d65-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b7d65-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="b7d65-113">Řešení</span><span class="sxs-lookup"><span data-stu-id="b7d65-113">Resolution</span></span>

<span data-ttu-id="b7d65-114">Odeberte kódy národního prostředí z odkazů na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="b7d65-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="b7d65-115">Tady je příklad.</span><span class="sxs-lookup"><span data-stu-id="b7d65-115">The following is an example.</span></span>

<span data-ttu-id="b7d65-116">Před:</span><span class="sxs-lookup"><span data-stu-id="b7d65-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="b7d65-117">Po:</span><span class="sxs-lookup"><span data-stu-id="b7d65-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="b7d65-118">Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="b7d65-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="b7d65-119">Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`.</span><span class="sxs-lookup"><span data-stu-id="b7d65-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="b7d65-120">Spuštění skriptu:</span><span class="sxs-lookup"><span data-stu-id="b7d65-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="b7d65-121">Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.</span><span class="sxs-lookup"><span data-stu-id="b7d65-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="b7d65-122">Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="b7d65-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="b7d65-123">Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.</span><span class="sxs-lookup"><span data-stu-id="b7d65-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]