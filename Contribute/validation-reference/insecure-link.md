---
title: insecure-link
description: Vysvětlení a řešení problému sestavení insecure-link na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587684"
---
# <a name="insecure-link"></a><span data-ttu-id="16b73-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="16b73-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16b73-104">Toto pravidlo bylo nejdříve povoleno jako Návrh, aby týmy pro obsah měly čas na posouzení dopadu a na vytvoření plánu, jak úložiště vyčistit.</span><span class="sxs-lookup"><span data-stu-id="16b73-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="16b73-105">**20. 12. 2019 bude úroveň zvýšena na Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="16b73-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="16b73-106">Návrh</span><span class="sxs-lookup"><span data-stu-id="16b73-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="16b73-107">Tato zpráva znamená, že jste v jazyce Markdown použili explicitní odkaz v `http` nebo neupravenou adresu URL, například `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="16b73-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="16b73-108">Neupravené adresy URL se při publikování na webu Docs převádějí na nezabezpečené odkazy, a proto byste je neměli používat.</span><span class="sxs-lookup"><span data-stu-id="16b73-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="16b73-109">Řešení</span><span class="sxs-lookup"><span data-stu-id="16b73-109">Resolution</span></span>

<span data-ttu-id="16b73-110">Změňte všechny adresy URL webů Microsoftu tak, aby místo `http` používaly `https`.</span><span class="sxs-lookup"><span data-stu-id="16b73-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="16b73-111">Pokud odkaz představuje neupravenou adresu URL, změňte ji na explicitní odkaz Markdownu, který začíná na `https`.</span><span class="sxs-lookup"><span data-stu-id="16b73-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="16b73-112">Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="16b73-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="16b73-113">Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`.</span><span class="sxs-lookup"><span data-stu-id="16b73-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="16b73-114">Spuštění skriptu:</span><span class="sxs-lookup"><span data-stu-id="16b73-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="16b73-115">Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.</span><span class="sxs-lookup"><span data-stu-id="16b73-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="16b73-116">Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="16b73-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="16b73-117">Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.</span><span class="sxs-lookup"><span data-stu-id="16b73-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
