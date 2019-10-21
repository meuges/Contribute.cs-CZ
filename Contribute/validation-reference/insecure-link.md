---
title: insecure-link
description: Vysvětlení a řešení problému sestavení insecure-link na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379512"
---
# <a name="insecure-link"></a><span data-ttu-id="3205d-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="3205d-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3205d-104">Návrh</span><span class="sxs-lookup"><span data-stu-id="3205d-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="3205d-105">Tato zpráva znamená, že jste v jazyce Markdown použili explicitní odkaz v `http` nebo neupravenou adresu URL, například `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="3205d-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="3205d-106">Neupravené adresy URL se při publikování na webu Docs převádějí na nezabezpečené odkazy, a proto byste je neměli používat.</span><span class="sxs-lookup"><span data-stu-id="3205d-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="3205d-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="3205d-107">Resolution</span></span>

<span data-ttu-id="3205d-108">Změňte všechny adresy URL webů Microsoftu tak, aby místo `http` používaly `https`.</span><span class="sxs-lookup"><span data-stu-id="3205d-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="3205d-109">Pokud odkaz představuje neupravenou adresu URL, změňte ji na explicitní odkaz Markdownu, který začíná na `https`.</span><span class="sxs-lookup"><span data-stu-id="3205d-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="3205d-110">Součástí rozšíření Docs jazyka Markdown pro VS Code je i skript, který vyčistí odkazy na weby Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="3205d-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="3205d-111">Skript zkontroluje v úložišti všechny odkazy na weby Microsoftu, aby ověřil, že začínají na `https` místo na `http`, a neobsahují kódy národního prostředí, například `en-us`.</span><span class="sxs-lookup"><span data-stu-id="3205d-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="3205d-112">Spuštění skriptu:</span><span class="sxs-lookup"><span data-stu-id="3205d-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="3205d-113">Nainstalujte rozšíření [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pro VS Code.</span><span class="sxs-lookup"><span data-stu-id="3205d-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="3205d-114">Klávesovou zkratkou Alt+M otevřete nabídku jazyka Markdown.</span><span class="sxs-lookup"><span data-stu-id="3205d-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="3205d-115">Vyberte **Vyčištění** a pak vyberte **odkazy Microsoftu**.</span><span class="sxs-lookup"><span data-stu-id="3205d-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
