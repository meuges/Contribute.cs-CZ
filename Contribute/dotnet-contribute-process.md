---
title: Postup psaní příspěvků do úložišť dokumentace k .NET
description: V tomto článku najdete stručný úvod k psaní příspěvků do úložišť dokumentace k .NET. Dozvíte se, jaká se používají úložiště, jaký je postup při uspořádání obsahu a jaké zásady platí pro správu vzorového kódu a dalších prostředků.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 161f831bf3f31428f78d3a828b12b4c9ecaffb0e
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331753"
---
# <a name="process-for-contributing-to-net-docs"></a>Postup psaní příspěvků do dokumentace k .NET

Vážíme si příspěvků, kterými komunita přispívá do dokumentace. V následujícím seznamu najdete několik pravidel, kterými byste se při psaní příspěvků do dokumentace k .NET měli řídit:

- **NEPŘEKVAPUJTE NÁS** rozsáhlými žádostmi o přijetí změn. Než budete něčemu věnovat hodně času, zadejte problém a zahajte diskusi, abychom se mohli předem dohodnout na postupu.
- **DODRŽUJTE** tyto pokyny a pokyny týkající se [způsobu vyjadřování](dotnet-voice-tone.md).
- **POUŽÍVEJTE** jako výchozí bod své práce soubor se [šablonou](dotnet-style-guide.md).
- **VYTVOŘTE** ve svém forku samostatnou větev dřív, než začnete pracovat na článcích.
- **DODRŽUJTE**[pracovní postup v toku GitHubu](https://guides.github.com/introduction/flow/).
- **BLOGUJTE A TWEETUJTE** (nebo jinak komunikujte) o svých příspěvcích co nejčastěji.

Dodržením těchto pokynů usnadníte práci sobě i nám.

## <a name="make-a-contribution-to-net-docs"></a>Vytvoření příspěvku do dokumentace k .NET

**1. krok:** U malých změn můžete tento krok přeskočit. Pokud se zajímáte o psaní nového obsahu nebo o úplné přepracování stávajícího obsahu, otevřete [problém](https://github.com/dotnet/docs/issues) a popište v něm, co chcete dělat.

Obsah ve složce **docs** je uspořádaný do oddílů, které odpovídají tabulce s obsahem. Určete, kde se má téma v obsahu nacházet. Získejte ke svému návrhu zpětnou vazbu.

-nebo-

Vyberte některý ze stávajících problémů, ke kterým jsou vítané komunitní příspěvky. V [projektech pro přispěvatele z komunity .NET](https://github.com/dotnet/docs/projects/35) je řada problémů, ke kterým můžou přispěvatelé z komunity psát příspěvky. Podle svých zájmů a rozsahu své účasti si můžou vybrat z problémů uspořádaných do následujících kategorií:

- **Údržba:** Tato kategorie obsahuje relativně jednoduché příspěvky, třeba opravu nefunkčních nebo nesprávných odkazů, přidání chybějících ukázek kódu nebo řešení menších problémů týkajících se obsahu. V některých případech se tyto problémy můžou týkat velkého počtu souborů. V takovém případě nám dejte předem vědět, na čem byste chtěli začít pracovat. Přidejte k problému komentář, ze kterého poznáme, že na něm pracujete.

- **Aktualizace obsahu:** Vzhledem k obrovskému rozsahu dokumentace se může snadno stát, že je obsah zastaralý a vyžaduje revizi. Navíc z různých důvodů může být obsah duplicitní nebo i triplicitní. Při aktualizaci obsahu je potřeba ověřit, jestli jsou jednotlivá témata aktuální, případně revidovat obsah funkční oblasti tak, aby se vyloučily duplicity. Je také potřeba zajistit, aby byl veškerý jedinečný obsah uchováván v menší sadě dokumentace.

- **Tvorba nového obsahu:** Pokud se zajímáte o tvorbu vlastních nových témat, najdete v těchto problémech seznam témat o kterých víme, že bychom je chtěli přidat do naší sady dokumentace. Přesto nám dejte předem vědět, než na tématu začnete pracovat. Pokud máte zájem o napsání tématu, které zde není, otevřete nový problém.

Můžete si také prohlédnout seznam [otevřených problémů](https://github.com/dotnet/docs/issues) a dobrovolně pracovat na těch, které vás zajímají. K označení problémů, ke kterým můžou psát příspěvky členové komunity, používáme značku [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs). U těchto příspěvků se většinou vyžaduje minimální kontext, a jsou proto vhodné jako první problémy. Zveme zkušené přispěvatele v naší komunitě, aby se podívali na problémy, které by je mohly zajímat. Když nějaký najdete, přidejte komentář s dotazem, jestli je otevřený.

Jakmile jste vybrali úkol, na kterém chcete pracovat, postupujte podle [úvodních](get-started-setup-github.md) pokynů, podle kterých si vytvoříte účet GitHub a nastavíte prostředí.

**2. krok:** Vytvořte fork potřebných úložišť `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` nebo `dotnet/ml-api-docs` a vytvořte větev pro změny.

U malých změn si prohlédněte pokyny k úpravě GitHubu, které jsou na [domovské stránce](index.md#quick-edits-to-existing-documents) příručky pro přispěvatele.

**3. krok:** Proveďte změny v této nové větvi.

Pokud je téma nové, použijte jako výchozí bod tento [soubor se šablonou](dotnet-style-guide.md). Obsahuje pokyny k psaní a vysvětluje metadata, která jsou ke každému článku potřeba, například informace o autorovi.

Přejděte do složky, která odpovídá místu v obsahu, které jste pro svůj článek vybrali v prvním kroku. V této složce jsou soubory v jazyce Markdown všech článků v tomto oddílu. Pokud je to potřeba, vytvořte novou složku, do které umístíte soubory se svým obsahem. Hlavní článek v tomto oddílu se jmenuje *index.md*. Pro obrázky a další statické prostředky vytvořte podsložku nazvanou **media** (pokud ještě neexistuje) a dejte ji do složky se svým článkem. Ve složce **media** vytvořte podsložku s názvem článku (kromě souboru indexu). Vzorový kód musí být v úložišti `dotnet/samples`. Popis najdete v části o [ukázkách](#contributing-to-samples).

Dodržujte správnou syntaxi jazyka Markdown. Nejčastější příklady použití najdete ve [stručné nápovědě k šablonám a jazyku Markdown](dotnet-style-guide.md).

## <a name="example-structure"></a>Příklad struktury

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**4. krok:** Odešlete žádost o přijetí změn (PR) ze své větve do hlavní větve.

> [!IMPORTANT]
> V této chvíli není v úložištích dokumentace k .NET dostupná funkce [automatických komentářů](how-to-write-workflows-major.md#review-and-sign-off). Vaši žádost o přijetí změn zkontrolují členové týmu pro dokumentaci k .NET a sloučí ji.

Každá žádost o přijetí změn by měla vždy řešit jenom jeden problém. Žádost o přijetí změn se může týkat změny jednoho nebo několika souborů. Pokud řešíte více oprav, které se týkají různých souborů, použijte raději samostatné žádosti o přijetí změn. Pokud kromě tvorby ukázek také aktualizujete Markdown, musíte pro ukázky vytvořit samostatné žádosti o přijetí změn.

Pokud vaše žádost o přijetí změn řeší stávající problém, přidejte do zprávy o potvrzení nebo do žádosti o přijetí změn klíčové slovo `Fixes #Issue_Number`. Když ho přidáte, problém se po sloučení žádosti o přijetí změn automaticky uzavře. Další informace najdete v tématu o [zavírání problémů prostřednictvím zpráv o potvrzení](https://help.github.com/articles/closing-issues-via-commit-messages/).

Tým .NET zkontroluje vaši žádost o přijetí změn a bude vás informovat, jestli jsou před schválením potřeba další aktualizace nebo změny.

**5. krok:** Proveďte ve větvi potřebné aktualizace, které jste projednali s týmem.

Jakmile jsou připomínky zapracované a změny schválené, sloučí správci vaši žádost o přijetí změn s hlavní větví.

Všechny potvrzené změny v hlavní větvi pravidelně sdílíme do živé větve. Teprve potom uvidíte svůj příspěvek živě na adrese https://docs.microsoft.com/dotnet/. Během pracovního týdne změny většinou publikujeme každý den. Provádění údržby může publikování o několik dní zdržet.

## <a name="contributing-to-samples"></a>Příspěvky do ukázek kódu

Veškerý vzorový kód, který je součástí témat v dokumentaci k .NET, je v úložišti [dotnet/samples](https://github.com/dotnet/samples). Některé projekty jsou uspořádané do podsložek. Tyto podsložky jsou uspořádané podobně jako dokumentace k .NET.

Kód, který je v úložišti, rozdělujeme do dvou skupin:

- Ukázky: Čtenáři si je můžou stáhnout a spustit. Všechny ukázky musí představovat celé aplikace nebo knihovny. Pokud ukázka vytvoří knihovnu, musí obsahovat testy jednotek nebo aplikaci, která uživatelům umožní kód spustit. Ukázky často používají více technologií, funkcí nebo sad nástrojů. Soubor readme.md, který je u každé ukázky, odkazuje na článek, kde si můžete přečíst další informace o probírané látce.
- Fragmenty kódu: Ilustrují menší prvek nebo úlohu. Jsou kompilovatelné, ale nejde o kompletní aplikace. Měly by běžet správně, i když nejde o ukázkovou aplikaci pro typický scénář. Jsou navržené tak, aby byly co nejmenší a ilustrovaly jednu určitou problematiku nebo funkci. Neměly by být delší než jedna obrazovka kódu.

Veškerý kód je v úložišti [dotnet/samples](https://github.com/dotnet/samples). Pracujeme na modelu, ve kterém bude struktura složek s ukázkami odpovídat struktuře složek dokumentace. Dodržujeme tato pravidla:

- Nejvyšší složka *snippets* obsahuje fragmenty kódu, které představují malé, jednoúčelové ukázky.
- Ukázky referenčního rozhraní API se ukládají do složek podle tohoto vzoru: *fragmenty kódu/\<jazyk>/api/\<obor názvů>/\<název rozhraní api>* .
- Další složky nejvyšší úrovně odpovídají nejvyšším složkám v úložišti *docs*. Například v úložišti docs je složka *machine-learning/tutorials* a ukázky ke kurzům věnovaným strojovému učení jsou ve složce *samples/machine-learning/tutorials*.

Navíc všechny ukázky ve složkách *core* a *standard* se musí dát vytvořit a spustit na všech platformách, které podporuje .NET Core. To zajistí náš systém sestavení CI. Nejvyšší složka *framework* obsahuje ukázky, které jsou vytvořené a ověřené jen ve Windows.

Ukázkové projekty se mají dát vytvořit a spustit na co nejvíce platformách. V praxi to znamená, že pokud je to možné, je potřeba vytvářet konzolové aplikace založené na .NET Core. Pokud se ukázky týkají určité webové nebo uživatelské platformy, měli byste podle potřeby přidat i tyto nástroje. Příkladem jsou webové aplikace, mobilní aplikace, aplikace WPF nebo WinForms apod.

Pracujeme na tom, abychom pro všechen kód mohli používat systém CI. Při aktualizaci ukázek dbejte na to, aby každá aktualizace byla součástí sestavitelného projektu. Ideálně přidejte k ukázkám také testy správnosti.

Každá hotová ukázka, kterou vytvoříte, má obsahovat soubor *readme.md*. V tomto souboru by měl být krátký popis ukázky (jeden nebo dva odstavce). Ze souboru *readme.md* by se čtenáři měli dozvědět, co se naučí, když si tuto ukázku vyzkouší. V souboru *readme.md* má být také odkaz na živý dokument na [webu s dokumentací k .NET](https://docs.microsoft.com/dotnet/welcome). Pokud chcete zjistit mapování daného souboru v úložišti na tento web, nahraďte `/docs` v cestě k úložišti adresou `https://docs.microsoft.com/dotnet`.

Odkaz na ukázku bude i ve vašem tématu. Vytvořte odkaz přímo na složku s ukázkou na GitHubu.

### <a name="writing-a-new-snippet-or-sample"></a>Psaní nového fragmentu nebo ukázky kódu

1. Vaše ukázka **musí být součástí sestavitelného projektu**. Pokud je to možné, měly by být projekty sestavitelné na všech platformách, které podporuje .NET Core. Výjimkou jsou ukázky, které předvádějí funkce určité platformy, nebo nástroj, který se používá jenom pro určitou platformu.

2. Kvůli zachování konzistence by měla ukázka odpovídat [stylu programování CoreFX](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md).

    - V ukázkách, ve kterých se nevyžaduje vytvoření instance nového objektu, také raději používáme metody `static` místo instancí metod.

3. Vaše ukázka by měla mít **náležitě ošetřeny výjimky**. V ukázce by měly být ošetřeny všechny výjimky, které se v této souvislosti můžou vyskytnout. Například v ukázce, ve které se načítá uživatelský vstup voláním metody [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline), musí být náležitě ošetřena výjimka, kdy se vstupní řetězec předá metodě jako argument. Podobně platí, že pokud se v ukázce předpokládá, že volání metody způsobí chybu, musíte výslednou výjimku ošetřit. Vždy ošetřete konkrétní výjimky způsobené metodou místo výjimek základních tříd, jako je [Exception](https://docs.microsoft.com/dotnet/api/system.exception) nebo [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. Pokud ukázka vytvoří samostatný balíček, musíte kromě modulů runtime použitých v ukázce zahrnout také moduly runtime použité naším systémem sestavení CI:
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

V blízké době zavedeme systém CI, který bude sloužit ke kompilaci těchto projektů.

Postup vytvoření ukázky:

1. Zadejte [problém](https://github.com/dotnet/docs/issues) nebo přidejte komentář ke stávajícímu problému a uveďte, že na něm pracujete.
2. Napište téma a vysvětlete v něm, co v ukázce předvádíte (příklad: `docs/standard/linq/where-clause.md`).
3. Napište ukázku (příklad: `WhereClause-Sample1.cs`).
4. Vytvořte soubor Program.cs s hlavním vstupním bodem, který volá vaše ukázky. Pokud soubor existuje, přidejte do něj volání své ukázky:

    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```

K vytvoření fragmentu nebo ukázky kódu pro .NET Core použijete nástroje .NET Core CLI, které si můžete nainstalovat se sadou [.NET Core SDK](https://www.microsoft.com/net/download). Postup vytvoření a spuštění ukázky:

1. Přejděte do ukázkové složky a zkontrolujte chyby tím, že program zkompilujete:

    ```console
    dotnet build
    ```
2. Spusťte ukázku:

    ```console
    dotnet run
    ```

3. Do kořenové složky ukázky přidejte soubor readme.md.

   Soubor by měl obsahovat stručný popis kódu a měl by uživatele odkázat na článek, který se ukázky týká.

Pokud není uvedeno jinak, jsou všechny ukázky vytvořené z příkazového řádku pro libovolnou platformu, kterou podporuje .NET Core. Některé ukázky jsou určené konkrétně pro Visual Studio, a proto vyžadují Visual Studio 2017 nebo novější verzi. Jiné ukázky předvádějí funkce určité platformy, a proto vyžadují určitou platformu. Další ukázky a fragmenty kódu vyžadují rozhraní .NET Framework. Půjdou spustit na platformě Windows, ale budou potřebovat sadu Developer Pack pro verzi cílové architektury.

## <a name="the-c-interactive-experience"></a>Interaktivní prostředí jazyka C#

U všech ukázek v článku je [značka jazyka](code-in-docs.md), která označuje zdrojový jazyk. Krátké ukázky kódu v jazyce C# používají jazykovou značku `csharp-interactive`, která znamená, že ukázku v jazyce C# můžete spustit v prohlížeči (ukázky vloženého kódu používají značku `csharp-interactive`, pro fragmenty kódu zahrnuté ze zdroje se používá značka `code-csharp-interactive`). Tyto ukázky kódu jsou v článku zobrazené v okně kódu a ve výstupním okně. V okně výstupu se zobrazuje výstup spuštěného interaktivního kódu po spuštění ukázky uživatelem.

Prostředí kompilačního nástroje C# Interactive mění způsob práce s ukázkami. Návštěvníci můžou ukázku spustit a podívat se na výsledky. To, jestli mají být v ukázce nebo v příslušném textu i informace o výstupu, záleží na řadě okolností.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Kdy zobrazit očekávaný výstup bez spuštění ukázky

- Výstup by měly obsahovat články, které jsou určené začátečníkům, aby čtenáři mohli porovnat svůj výstup s očekávanou odpovědí.
- Výstup by také měl být v ukázkách, ve kterých je nedílnou součástí tématu. Například v článcích o formátovaném textu by se měl zobrazovat formát textu bez spouštění ukázky.
- Zobrazení výstupu byste měli zvážit i v případě, že ukázka i očekávaný výsledek jsou krátké. Trochu to šetří čas.
- Očekávaný výsledek by také měl být popsaný v článcích, které vysvětlují vliv aktuální jazykové verze nebo invariantní jazykové verze na výstup. Interaktivní prostředí REPL (Read Evaluate Print Loop) běží na linuxovém hostiteli. Výchozí jazyková verze a invariantní jazyková verze vytvářejí v různých operačních systémech a na různých počítačích odlišné výstupy. V článku by měl být popsaný výstup v systémech Windows, Linux a Mac.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Kdy z ukázky očekávaný výstup vyloučit

- Pokud je v článcích ukázka, která generuje větší výstup, neměl by být v komentáři. Kód je po spuštění ukázky nepřehledný.
- Pokud článek předvádí nějaké téma, ale výstup není k jeho pochopení nezbytně nutný. Pokud třeba kód spustí dotaz LINQ kvůli vysvětlení syntaxe dotazu a pak zobrazí každou položku výstupní kolekce.

> [!NOTE]
> Možná jste si všimli, že v současnosti některá témata nedodržují všechny uvedené pokyny. Pracujeme na tom, aby měl web konzistentní podobu. Můžete se podívat na seznam [otevřených problémů](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22), které k tomuto cíli v současnosti evidujeme.

## <a name="contributor-license-agreement"></a>Licenční smlouva s přispěvatelem

Před sloučením žádosti o přijetí změn musíte podepsat [licenční smlouvu s přispěvatelem (CLA) pro .NET Foundation](https://cla.dotnetfoundation.org). Jde o jednorázový požadavek u projektů pro .NET Foundation. Další informace o [licenční smlouvě s přispěvatelem (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) najdete na wikipedii.

Smlouva: [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

Smlouvu nemusíte podepisovat předem. Žádosti o přijetí změn můžete obvyklým způsobem klonovat, odeslat nebo můžete vytvořit fork. Vytvořenou žádost o přijetí změn klasifikuje robot CLA. Pokud se jedná o malou změnu (třeba o opravu překlepu), bude žádost označena `cla-not-required`. V ostatních případech bude zařazena jako `cla-required`. Po podpisu smlouvy CLA budou všechny současné i budoucí žádosti o přijetí změn označeny `cla-signed`.
