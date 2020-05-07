---
ms.openlocfilehash: b64e8dd4c62ca05b6e04ef404ebf98a618d0171e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "66391383"
---
Automatizace komentářů umožňuje uživatelům na úrovni čtení (uživatelům, kteří v úložišti nemají oprávnění k zápisu) provést akci na úrovni zápisu, a to přiřazením odpovídajícího označení k žádosti o přijetí změn. Pokud pracujete v úložišti s implementovanou automatizací komentářů, pomocí hashtagových komentářů z následující tabulky můžete přiřadit nebo změnit označení nebo zavřít žádost o přijetí změn. Kdykoli budou navrženy změny článků, kterých jste autorem, budou také zaměstnanci Microsoftu prostřednictvím e-mailu upozorněni, aby zkontrolovali a schválili žádosti o přijetí změn ve veřejném úložišti.

| Hashtagový komentář | Co dělá | Dostupnost úložiště |
| --- | --- | --- |
| `#sign-off` |Když autor článku do streamu komentářů napíše `#sign-off`, přiřadí se popisek **ready-to-merge** (připraveno ke sloučení). Toto označení kontrolory v úložišti informuje, že je žádost o přijetí změn připravená ke kontrole/sloučení. <br/><br/> Pokud se žádost o přijetí změn ve veřejném úložišti pomocí komentáře *pokusí schválit přispěvatel, který*není`#sign-off` uvedeným autorem, zapíše se do žádosti o přijetí změn zpráva, že tento popisek může přiřadit jenom autor. |Veřejné a soukromé |
| `#hold-off` |Autoři můžou do komentáře k žádosti o přijetí změn napsat `#hold-off`, aby odebrali popisek **ready-to-merge** (připraveno ke sloučení) v případě, že se rozhodli jinak nebo udělali chybu. V soukromém úložišti se tím přiřadí označení **do-not-merge** (neslučovat). |Veřejné a soukromé |
| `#please-close` |Autoři můžou do streamu komentářů napsat `#please-close`, aby žádost o přijetí změn zavřeli, pokud se rozhodnou, že změny nechtějí sloučit. |Veřejné |
