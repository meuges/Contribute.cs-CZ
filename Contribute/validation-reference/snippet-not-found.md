---
title: snippet-not-found
description: Vysvětlení a řešení problému sestavení snippet-not-found na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459089"
---
# <a name="snippet-not-found"></a><span data-ttu-id="b1f32-103">snippet-not-found</span><span class="sxs-lookup"><span data-stu-id="b1f32-103">snippet-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="b1f32-104">Upozornění</span><span class="sxs-lookup"><span data-stu-id="b1f32-104">Warning</span></span>

`Code snippet '{snippet path}' not found.`

<span data-ttu-id="b1f32-105">Odkazy na fragmenty kódu na zadané cestě neexistují nebo cesta není z aktuálního souboru dostupná.</span><span class="sxs-lookup"><span data-stu-id="b1f32-105">The code snippet references doesn't exist at the specified path, or the path isn't available from the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="b1f32-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="b1f32-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="b1f32-107">Ujistěte se, že cesta k fragmentu kódu je správná.</span><span class="sxs-lookup"><span data-stu-id="b1f32-107">Ensure that your snippet path is correct.</span></span> <span data-ttu-id="b1f32-108">Pokud je fragment kódu uložen mimo aktuální úložiště, ujistěte se, že je dané úložiště nakonfigurováno jako závislé úložiště.</span><span class="sxs-lookup"><span data-stu-id="b1f32-108">If the snippet is stored outside the current repo, make sure the repo is configured ase a dependent repo.</span></span> <span data-ttu-id="b1f32-109">Další informace najdete v [interním článku Microsoftu o fragmentech kódu](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).</span><span class="sxs-lookup"><span data-stu-id="b1f32-109">For more information, see the Microsoft-internal [code snippet article](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
