---
title: Roadmapa popisků, projektů a milníků
description: Tento článek vysvětluje, jak se používají popisky, projekty a milníky v úložišti dotnet/docs.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/06/2020
ms.openlocfilehash: b8e9f2a33f9b4a8025aa36a890bff1017cf132c6
ms.sourcegitcommit: abcc67cb3ec1f635a6374d7c47a4831e3eee9050
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559256"
---
# <a name="labels-projects-and-milestones-roadmap"></a>Roadmapa popisků, projektů a milníků

Tým dokumentace k .NET rozsáhle využívá [popisky GitHubu](https://github.com/dotnet/docs/labels) k uspořádání a zpřehlednění naší práce. Díky vyfiltrování kombinace popisků se můžeme na [webu dokumentace k .NET](https://docs.microsoft.com/dotnet) rychle zaměřit na oddíly, které nás zajímají. Například všechny otevřené problémy s prioritou `P1` bychom vyfiltrovali pomocí dotazu [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).

K uspořádání sprintů a dalších procesů (příběhů) zaměřených na cíle používáme [projekty GitHubu](https://github.com/dotnet/docs/projects). Ke sledování práce používáme také [milníky GitHubu](https://github.com/dotnet/docs/milestones). Nejlepší je uvažovat projekty pro plánování (problémy) a milníky pro práci (žádosti o přijetí změn).

Tato roadmapa vysvětluje, jak tyto organizační nástroje používáme, a obsahuje odkazy na užitečné filtry, které používáme k vyhledání požadovaných oblastí.

## <a name="labels"></a>Popisky

Pokud jde o vaši první zkušenost s příspěvky do [dotnet/docs](https://github.com/dotnet/docs), začněte se záležitostmi [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs). Jde o problémy, které mají konkrétnější zaměření. Představují skvělý způsob, jak udělat svůj první příspěvek. V zobrazení pro up-for-grabs můžete dál filtrovat problémy na základě oblastí a priority. Vhodné problémy pro začátečníky jsme označili popiskem [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue), pokud chcete vyzkoušet menší první příspěvek.

Pomocí popisků rozdělujeme problémy mnoha různými způsoby:

- [Příručky .NET](#find-a-single-net-guide) a [oddíly příručky](#search-one-section-of-a-guide)
- [Cílová verze](#releases)
- [Priorita](#priority)

Můžete zkombinovat popisek z každé sady (příručka, verze, priorita), a zúžit tak prostor pro hledání problémů, na kterých chcete pracovat.

### <a name="find-a-single-net-guide"></a>Vyhledání jedné příručky pro rozhraní .NET

Popisky používáme pro každou elektronickou knihu (e-knihu) architektury a pro každou příručku .NET.

![:book: příručka na světle zeleném pozadí](./media/labels-projects/guide.png "Předpona pro popisky příručky architektury")

E-knihy architektury jsou označeny předponou `:book: guide` a mají světlé zelené pozadí. Jsou to rozsáhlejší oblasti, které se týkají doporučené architektury. Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky architektury .NET.

- [Webové aplikace ASP.NET Core](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Nativní cloud](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [Životní cyklus nástroje Docker](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizace s kontejnery Windows](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Aplikace bez serveru](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Tento styl popisku se také používá v [pravidlech návrhu Frameworku](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). Tato oblast má stejný vzhled popisku, ale využívání v komunitě se nedoporučuje. Tento materiál je reprodukován s oprávněním a neměl se upravovat.

![:books: Oblast na tmavě modrém pozadí](./media/labels-projects/area.png "Předpona pro popisky oblastí příručky .NET")

Každá příručka .NET je označena předponou `:books: Area` a má tmavě modré pozadí. Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky .NET.

- [Referenční informace k rozhraním API](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Azure .NET SDK](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Desktop Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) (dá se odebrat)
- [.NET Core Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) (dá se odebrat)
- [Visual Basic Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Hledání v jednom oddílu příručky

![:card_file_box: Oblast na středně tmavém modrém pozadí](./media/labels-projects/technology.png "Předpona pro popisky podoblastí příručky .NET")

Příručky .NET jsou velké, takže tyto popisky vymezují rozsah podle oddílu příručky. Každá podoblast příručky .NET je označena předponou `:card_file_box: Technology` a má středně tmavé modré pozadí. Mnohé z těchto popisků platí pro více příruček, ale některé jsou jenom v jedné. Když po filtrování v oblasti přidáte jeden z těchto popisků, rozsah problémů se zúží.

- AppCompat
- Async Task
- Koncepty C# Advanced
- Kompilátor C#
- Základy C#
- Začínáme s C#
- Referenční dokumentace jazyka C#
- Bezpečnost C# Null
- Novinky v C#
- Rozhraní příkazového řádku
- Přístup k datům
- Docker
- Instalační programy
- LINQ
- NCL
- .NET Standard
- Rozhraní API pro Roslyn
- Zabezpečení
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Verze

![:checkered_flag: Verze: na tmavě žluté](./media/labels-projects/release.png "Předpona pro popisky verzí")

Problémy označené pro konkrétní verzi jsou označeny předponou `:checkered_flag: Release:` a mají tmavě žluté pozadí.

- .NET Core 2.2
- .NET Core 3.0
-  .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Priorita

Popisky priorit `P` jsou všechny následované jednou číslicí. Nižší hodnota znamená vyšší prioritu:

- P0 – označuje problémy nebo žádosti o přijetí změn, které mají kritickou prioritou
- P1 – vysoká priorita
- P2 – střední priorita
- P3 – nízká priorita

### <a name="what-about-the-other-labels"></a>K čemu jsou ostatní popisky

Týmy obsahu používají mnoho dalších popisků, které slouží ke správě různých klasifikací problémů. Pokud nejste v týmu obsahu, můžete tyto další popisky ignorovat.

## <a name="projects"></a>Projekty

Projekty jsou určené pro účely plánování, kdy práce s prioritou je automatizována prostřednictvím panelu Kanbanu. Projekty by měly vždy obsahovat jen problémy GitHubu, _ne_ žádosti o přijetí změn. Projekty se liší od milníků tím, že milníky obsahují jen žádosti o přijetí změn.

Projekty používáme dvěma způsoby:

- Typy projektů `Month YYYY`: Jde o panely Kanbanu pro pracovní plán každého měsíce.
  - Příklady: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) a tak dále.
- Dlouhodobé procesy: Slouží k uspořádání úkolů směrem k cíli, kdy práce bude probíhat několik měsíců.
  - Příklady: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave)](https://github.com/dotnet/docs/projects/106) a tak dále.

## <a name="milestones"></a>Milníky

Milníky se obvykle řídí stejnými zásadami vytváření názvů jako projekty `Month YYYY`, ale od projektů se liší. Milníky používáme ke sledování dokončené práce. Milníky by _ne_měly obsahovat problémy (potenciální práci), ale výhradně jen žádosti o přijetí změn. Aktuální milník se automaticky použije na nové žádosti o přijetí změn.
