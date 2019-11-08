---
title: validation-timeout
description: Vysvětlení a řešení problému sestavení validation-timeout na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: f75f005ce9ab0cf332667d5c8b7778ba4ef35a0a
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592543"
---
# <a name="validation-timeout"></a><span data-ttu-id="a9b8c-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="a9b8c-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="a9b8c-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="a9b8c-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="a9b8c-105">Přechodné problémy ověřovací služby, jako je špatný stav serveru, někdy brání sestavení na webu Docs v úspěšném volání služby.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="a9b8c-106">Po několika pokusech časový limit tohoto volání vyprší a ověřování se zruší, aby se zabránilo kumulaci prodlev a zahlcení kanálu buildu.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="a9b8c-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="a9b8c-107">Resolution</span></span>

<span data-ttu-id="a9b8c-108">Zkuste zavřít a znovu otevřít svoji žádost o přijetí změn nebo vynutit úplné sestavení přes [portál Docs](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="a9b8c-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="a9b8c-109">Po prvotním pokusu se problémy se službou často vyřeší samovolně.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="a9b8c-110">Abyste mohli vynutit úplné sestavení přes portál Docs, musíte být správce úložiště.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="a9b8c-111">Pokud nevíte, kdo je váš správce úložiště nebo pokud se tato zpráva bude objevovat i po vynuceném sestavení, zadejte problém přes [https://SiteHelp](https://SiteHelp) (pokud jste zaměstnancem Microsoftu) nebo v žádosti o přijetí změn požádejte pomocí zmínky (@) o pomoc autora článku (pokud jste externím přispěvatelem).</span><span class="sxs-lookup"><span data-stu-id="a9b8c-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="a9b8c-112">Pokud jste správce úložiště, můžete vynutit úplné sestavení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="a9b8c-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="a9b8c-113">Přejděte na [portál Docs](https://ops.microsoft.com/#/) a přihlaste se.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="a9b8c-114">Hledáním v levém horním rohu najděte své úložiště a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="a9b8c-115">:::image type="content" source="media/find-repo.png" alt-text="Najděte své úložiště prostřednictvím vyhledávacího pole na portálu Docs.":::</span><span class="sxs-lookup"><span data-stu-id="a9b8c-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="a9b8c-116">Na kartě **Historie sestavení** klikněte na **+ Ruční publikování**.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="a9b8c-117">Vyberte větev, pro kterou se zobrazuje upozornění, například hlavní větev.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-117">Select the branch that's getting the Warning, such as master.</span></span>
1. <span data-ttu-id="a9b8c-118">Cíl ponechte výchozí – **web Docs**.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-118">For target, keep the default, **Docs Site**.</span></span>
1. <span data-ttu-id="a9b8c-119">Zaškrtněte políčko **Vynutit publikování**.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="a9b8c-120">Klikněte na **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-120">Click **Publish**.</span></span>

   <span data-ttu-id="a9b8c-121">:::image type="content" source="media/force-build.png" alt-text="Postup vynucení úplného sestavení":::</span><span class="sxs-lookup"><span data-stu-id="a9b8c-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="a9b8c-122">Tím se vynutí úplné sestavení ve větvi.</span><span class="sxs-lookup"><span data-stu-id="a9b8c-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
