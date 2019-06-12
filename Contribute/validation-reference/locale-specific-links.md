---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Odkazy specifické pro národní prostředí
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841261"
---
# <a name="locale-specific-links"></a><span data-ttu-id="ba722-102">Odkazy specifické pro národní prostředí</span><span class="sxs-lookup"><span data-stu-id="ba722-102">Locale-specific links</span></span>

<span data-ttu-id="ba722-103">Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="ba722-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="ba722-104">Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí.</span><span class="sxs-lookup"><span data-stu-id="ba722-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="ba722-105">Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.</span><span class="sxs-lookup"><span data-stu-id="ba722-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="ba722-106">Odeberte kódy národního prostředí z odkazů na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="ba722-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="ba722-107">Tady je příklad.</span><span class="sxs-lookup"><span data-stu-id="ba722-107">The following is an example.</span></span>

<span data-ttu-id="ba722-108">Před:</span><span class="sxs-lookup"><span data-stu-id="ba722-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="ba722-109">Po:</span><span class="sxs-lookup"><span data-stu-id="ba722-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="ba722-110">Do tohoto ověřování jsou zahrnuty tyto weby:</span><span class="sxs-lookup"><span data-stu-id="ba722-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="ba722-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ba722-111">azure.microsoft.com</span></span>
- <span data-ttu-id="ba722-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ba722-112">docs.microsoft.com</span></span>
- <span data-ttu-id="ba722-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ba722-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="ba722-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ba722-114">technet.microsoft.com</span></span>