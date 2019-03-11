---
title: circular-reference
description: Vysvětlení a řešení problému sestavení circular-reference na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459204"
---
# <a name="circular-reference"></a><span data-ttu-id="5059c-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="5059c-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="5059c-104">Chyba</span><span class="sxs-lookup"><span data-stu-id="5059c-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="5059c-105">Může se jednat například o zahrnutý soubor, který odkazuje na aktuální soubor, nebo o odkaz na soubor, který byl přesměrován na aktuální soubor.</span><span class="sxs-lookup"><span data-stu-id="5059c-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="5059c-106">Řešení</span><span class="sxs-lookup"><span data-stu-id="5059c-106">Resolution</span></span>

<span data-ttu-id="5059c-107">Zkontrolujte odkazy v souborech a proveďte potřebné úpravy, aby žádný soubor neodkazoval sám na sebe ani nezahrnoval sám sebe.</span><span class="sxs-lookup"><span data-stu-id="5059c-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
