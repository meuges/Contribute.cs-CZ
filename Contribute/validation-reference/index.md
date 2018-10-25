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
# <a name="docs-pr-validation-service"></a>Odkaz na službu ověřování žádostí o přijetí změn Docs

Služba ověřování žádostí o přijetí změn Docs je githubová aplikace, která spouští ověřovací pravidla u souborů v žádosti o přijetí změn.

Když je služba ověřování povolená u úložiště, setkáte s tímto chováním:

1. Odešlete žádost o přijetí změn.
1. V komentáři GitHubu, který označuje stav vaší žádosti o přijetí změn, se zobrazí stav kontrol povolených u úložiště. Všimněte si, že v tomto příkladu jsou povolené dvě kontroly, Commit Validation a OpenPublishing.Build:

   ![Některé kontroly nebyly úspěšné.](media/validation-failed.png)

   Sestavení může projít, i když se ověření potvrzení nezdaří.

1. Další informace se zobrazí po kliknutí na **Details** (Podrobnosti).
1. Na stránce podrobností uvidíte všechny neúspěšné kontroly ověřování s informacemi o tom, jak problémy opravit:

   ![Zpráva ověřování](media/validation-details.png)

Seznam ověřování, která služba momentálně obsahuje, najdete v seznamu nalevo.