---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653544"
---
# <a name="locale-specific-links"></a><span data-ttu-id="c7e9e-101">Odkazy specifické pro národní prostředí</span><span class="sxs-lookup"><span data-stu-id="c7e9e-101">Locale-specific links</span></span>

<span data-ttu-id="c7e9e-102">Kódy národního prostředí, například `en-us`, byste neměli uvádět v odkazech vedoucích na určité weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="c7e9e-103">Pokud totiž kód národního prostředí uvedete v odkazu na anglický obsah, tento kód se zahrne také do lokalizovaných odkazů, které pak vedou na nesprávné lokalizované prostředí.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="c7e9e-104">Pokud například odkaz v českém lokalizovaném obsahu zahrnuje `en-us`, čeští zákazníci budou přesměrovaní na anglický článek, i když je k dispozici jeho česká verze.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="c7e9e-105">Odeberte kódy národního prostředí z odkazů na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="c7e9e-106">Tady je příklad.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-106">The following is an example.</span></span>

<span data-ttu-id="c7e9e-107">Před:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="c7e9e-108">Po:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="c7e9e-109">Do tohoto ověřování jsou zahrnuty tyto weby:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="c7e9e-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c7e9e-110">azure.microsoft.com</span></span>
- <span data-ttu-id="c7e9e-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c7e9e-111">docs.microsoft.com</span></span>
- <span data-ttu-id="c7e9e-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c7e9e-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="c7e9e-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c7e9e-113">technet.microsoft.com</span></span>