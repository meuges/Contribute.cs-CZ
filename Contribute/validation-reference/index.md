---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084468"
---
# <a name="docs-pr-validation-service"></a><span data-ttu-id="5d87a-101">Odkaz na službu ověřování žádostí o přijetí změn Docs</span><span class="sxs-lookup"><span data-stu-id="5d87a-101">Docs PR validation service</span></span>

<span data-ttu-id="5d87a-102">Služba ověřování žádostí o přijetí změn Docs je githubová aplikace, která spouští ověřovací pravidla u souborů v žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="5d87a-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="5d87a-103">Když je služba ověřování povolená u úložiště, setkáte s tímto chováním:</span><span class="sxs-lookup"><span data-stu-id="5d87a-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="5d87a-104">Odešlete žádost o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="5d87a-104">You submit a PR.</span></span>
1. <span data-ttu-id="5d87a-105">V komentáři GitHubu, který označuje stav vaší žádosti o přijetí změn, se zobrazí stav kontrol povolených u úložiště.</span><span class="sxs-lookup"><span data-stu-id="5d87a-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="5d87a-106">Všimněte si, že v tomto příkladu jsou povolené dvě kontroly, Commit Validation a OpenPublishing.Build:</span><span class="sxs-lookup"><span data-stu-id="5d87a-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![Některé kontroly nebyly úspěšné.](media/validation-failed.png)

   <span data-ttu-id="5d87a-108">Sestavení může projít, i když se ověření potvrzení nezdaří.</span><span class="sxs-lookup"><span data-stu-id="5d87a-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="5d87a-109">Další informace se zobrazí po kliknutí na **Details** (Podrobnosti).</span><span class="sxs-lookup"><span data-stu-id="5d87a-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="5d87a-110">Na stránce podrobností uvidíte všechny neúspěšné kontroly ověřování s informacemi o tom, jak problémy opravit:</span><span class="sxs-lookup"><span data-stu-id="5d87a-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![Zpráva ověřování](media/validation-details.png)

<span data-ttu-id="5d87a-112">Seznam ověřování, která služba momentálně obsahuje, najdete v seznamu nalevo.</span><span class="sxs-lookup"><span data-stu-id="5d87a-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>