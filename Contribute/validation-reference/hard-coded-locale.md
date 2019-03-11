---
title: hard-coded-locale
description: Vysvětlení a řešení problému sestavení hard-coded-locale na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427272"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="17405-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="17405-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="17405-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="17405-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="17405-105">Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="17405-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="17405-106">Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí.</span><span class="sxs-lookup"><span data-stu-id="17405-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="17405-107">Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.</span><span class="sxs-lookup"><span data-stu-id="17405-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="17405-108">Do tohoto ověřování jsou zahrnuty tyto weby:</span><span class="sxs-lookup"><span data-stu-id="17405-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="17405-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="17405-109">azure.microsoft.com</span></span>
- <span data-ttu-id="17405-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="17405-110">docs.microsoft.com</span></span>
- <span data-ttu-id="17405-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="17405-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="17405-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="17405-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="17405-113">Řešení</span><span class="sxs-lookup"><span data-stu-id="17405-113">Resolution</span></span>

<span data-ttu-id="17405-114">Odeberte kódy národního prostředí z odkazů na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="17405-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="17405-115">Tady je příklad.</span><span class="sxs-lookup"><span data-stu-id="17405-115">The following is an example.</span></span>

<span data-ttu-id="17405-116">Před:</span><span class="sxs-lookup"><span data-stu-id="17405-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="17405-117">Po:</span><span class="sxs-lookup"><span data-stu-id="17405-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]