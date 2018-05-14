Automatizace komentářů umožňuje uživatelům na úrovni čtení (uživatelům, kteří v úložišti nemají oprávnění k zápisu) provést akci na úrovni zápisu, a to přiřazením odpovídajícího označení k žádosti o přijetí změn. Pokud pracujete v úložišti s implementovanou automatizací komentářů, pomocí hashtagových komentářů z následující tabulky můžete přiřadit nebo změnit označení nebo zavřít žádost o přijetí změn. Kdykoli budou navrženy změny článků, kterých jste autorem, budou také zaměstnanci Microsoftu prostřednictvím e-mailu upozorněni, aby zkontrolovali a schválili žádosti o přijetí změn ve veřejném úložišti.


| Hashtagový komentář | Co dělá | Dostupnost úložiště |
| --- | --- | --- |
| #sign-off |Když autor článku do streamu komentářů napíše **#sign-off**, přiřadí se označení **ready-to-merge** (připraveno ke sloučení). Toto označení kontrolory v úložišti informuje, že je žádost o přijetí změn připravená ke kontrole/sloučení. |Veřejné a soukromé |
| #sign-off |Pokud se veřejnou žádost o přijetí změn pomocí komentáře **#sign-off** pokusí schválit přispěvatel, který *není* uvedeným autorem, zapíše se do žádosti o přijetí změn zpráva, že toto označení může přiřadit jenom autor. |Veřejné |
| #hold-off |Autoři můžou do komentáře k žádosti o přijetí změn napsat **#hold-off**, aby odebrali označení **ready-to-merge** (připraveno ke sloučení) v případě, že se rozhodli jinak nebo udělali chybu. V soukromém úložišti se tím přiřadí označení **do-not-merge** (neslučovat). |Veřejné a soukromé |
| #please-close |Autoři můžou do streamu komentářů napsat **#please-close**, aby žádost o přijetí změn zavřeli, pokud se rozhodnou, že změny nechtějí sloučit. |Veřejné |
