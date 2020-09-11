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
# <a name="labels-projects-and-milestones-roadmap"></a><span data-ttu-id="0cde8-103">Roadmapa popisků, projektů a milníků</span><span class="sxs-lookup"><span data-stu-id="0cde8-103">Labels, projects, and milestones roadmap</span></span>

<span data-ttu-id="0cde8-104">Tým dokumentace k .NET rozsáhle využívá [popisky GitHubu](https://github.com/dotnet/docs/labels) k uspořádání a zpřehlednění naší práce.</span><span class="sxs-lookup"><span data-stu-id="0cde8-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="0cde8-105">Díky vyfiltrování kombinace popisků se můžeme na [webu dokumentace k .NET](https://docs.microsoft.com/dotnet) rychle zaměřit na oddíly, které nás zajímají.</span><span class="sxs-lookup"><span data-stu-id="0cde8-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span> <span data-ttu-id="0cde8-106">Například všechny otevřené problémy s prioritou `P1` bychom vyfiltrovali pomocí dotazu [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span><span class="sxs-lookup"><span data-stu-id="0cde8-106">For example, we could filter to all of the open priority one `P1` issues with a query to [is:issue is:open label:":books: Area - .NET Architecture Guide"](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3A%22%3Abooks%3A+Area+-+.NET+Architecture+Guide%22).</span></span>

<span data-ttu-id="0cde8-107">K uspořádání sprintů a dalších procesů (příběhů) zaměřených na cíle používáme [projekty GitHubu](https://github.com/dotnet/docs/projects).</span><span class="sxs-lookup"><span data-stu-id="0cde8-107">We use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span> <span data-ttu-id="0cde8-108">Ke sledování práce používáme také [milníky GitHubu](https://github.com/dotnet/docs/milestones).</span><span class="sxs-lookup"><span data-stu-id="0cde8-108">We also use [GitHub milestones](https://github.com/dotnet/docs/milestones) to track work.</span></span> <span data-ttu-id="0cde8-109">Nejlepší je uvažovat projekty pro plánování (problémy) a milníky pro práci (žádosti o přijetí změn).</span><span class="sxs-lookup"><span data-stu-id="0cde8-109">It is best to think of projects for planning (issues), and milestones for work (pull requests).</span></span>

<span data-ttu-id="0cde8-110">Tato roadmapa vysvětluje, jak tyto organizační nástroje používáme, a obsahuje odkazy na užitečné filtry, které používáme k vyhledání požadovaných oblastí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-110">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="0cde8-111">Popisky</span><span class="sxs-lookup"><span data-stu-id="0cde8-111">Labels</span></span>

<span data-ttu-id="0cde8-112">Pokud jde o vaši první zkušenost s příspěvky do [dotnet/docs](https://github.com/dotnet/docs), začněte se záležitostmi [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs).</span><span class="sxs-lookup"><span data-stu-id="0cde8-112">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="0cde8-113">Jde o problémy, které mají konkrétnější zaměření.</span><span class="sxs-lookup"><span data-stu-id="0cde8-113">These are issues that have a more focused scope.</span></span> <span data-ttu-id="0cde8-114">Představují skvělý způsob, jak udělat svůj první příspěvek.</span><span class="sxs-lookup"><span data-stu-id="0cde8-114">They are a great way to make your first contribution.</span></span> <span data-ttu-id="0cde8-115">V zobrazení pro up-for-grabs můžete dál filtrovat problémy na základě oblastí a priority.</span><span class="sxs-lookup"><span data-stu-id="0cde8-115">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="0cde8-116">Vhodné problémy pro začátečníky jsme označili popiskem [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue), pokud chcete vyzkoušet menší první příspěvek.</span><span class="sxs-lookup"><span data-stu-id="0cde8-116">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="0cde8-117">Pomocí popisků rozdělujeme problémy mnoha různými způsoby:</span><span class="sxs-lookup"><span data-stu-id="0cde8-117">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="0cde8-118">[Příručky .NET](#find-a-single-net-guide) a [oddíly příručky](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="0cde8-118">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="0cde8-119">Cílová verze</span><span class="sxs-lookup"><span data-stu-id="0cde8-119">Target release</span></span>](#releases)
- [<span data-ttu-id="0cde8-120">Priorita</span><span class="sxs-lookup"><span data-stu-id="0cde8-120">Priority</span></span>](#priority)

<span data-ttu-id="0cde8-121">Můžete zkombinovat popisek z každé sady (příručka, verze, priorita), a zúžit tak prostor pro hledání problémů, na kterých chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="0cde8-121">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="0cde8-122">Vyhledání jedné příručky pro rozhraní .NET</span><span class="sxs-lookup"><span data-stu-id="0cde8-122">Find a single .NET guide</span></span>

<span data-ttu-id="0cde8-123">Popisky používáme pro každou elektronickou knihu (e-knihu) architektury a pro každou příručku .NET.</span><span class="sxs-lookup"><span data-stu-id="0cde8-123">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="0cde8-124">![:book: příručka na světle zeleném pozadí](./media/labels-projects/guide.png "Předpona pro popisky příručky architektury")</span><span class="sxs-lookup"><span data-stu-id="0cde8-124">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="0cde8-125">E-knihy architektury jsou označeny předponou `:book: guide` a mají světlé zelené pozadí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-125">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="0cde8-126">Jsou to rozsáhlejší oblasti, které se týkají doporučené architektury.</span><span class="sxs-lookup"><span data-stu-id="0cde8-126">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="0cde8-127">Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky architektury .NET.</span><span class="sxs-lookup"><span data-stu-id="0cde8-127">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="0cde8-128">Webové aplikace ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="0cde8-128">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="0cde8-129">Blazor</span><span class="sxs-lookup"><span data-stu-id="0cde8-129">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="0cde8-130">Nativní cloud</span><span class="sxs-lookup"><span data-stu-id="0cde8-130">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="0cde8-131">Životní cyklus nástroje Docker</span><span class="sxs-lookup"><span data-stu-id="0cde8-131">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="0cde8-132">gRPC</span><span class="sxs-lookup"><span data-stu-id="0cde8-132">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="0cde8-133">Modernizace s kontejnery Windows</span><span class="sxs-lookup"><span data-stu-id="0cde8-133">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="0cde8-134">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="0cde8-134">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="0cde8-135">Aplikace bez serveru</span><span class="sxs-lookup"><span data-stu-id="0cde8-135">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="0cde8-136">Tento styl popisku se také používá v [pravidlech návrhu Frameworku](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="0cde8-136">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="0cde8-137">Tato oblast má stejný vzhled popisku, ale využívání v komunitě se nedoporučuje.</span><span class="sxs-lookup"><span data-stu-id="0cde8-137">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="0cde8-138">Tento materiál je reprodukován s oprávněním a neměl se upravovat.</span><span class="sxs-lookup"><span data-stu-id="0cde8-138">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="0cde8-139">![:books: Oblast na tmavě modrém pozadí](./media/labels-projects/area.png "Předpona pro popisky oblastí příručky .NET")</span><span class="sxs-lookup"><span data-stu-id="0cde8-139">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="0cde8-140">Každá příručka .NET je označena předponou `:books: Area` a má tmavě modré pozadí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-140">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="0cde8-141">Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky .NET.</span><span class="sxs-lookup"><span data-stu-id="0cde8-141">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="0cde8-142">Referenční informace k rozhraním API</span><span class="sxs-lookup"><span data-stu-id="0cde8-142">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="0cde8-143">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="0cde8-143">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="0cde8-144">C# Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-144">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="0cde8-145">Desktop Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-145">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="0cde8-146">F# Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-146">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="0cde8-147">ML.NET Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-147">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="0cde8-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) (dá se odebrat)</span><span class="sxs-lookup"><span data-stu-id="0cde8-148">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="0cde8-149">.NET Core Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-149">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="0cde8-150">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-150">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="0cde8-151">.NET Framework Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-151">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="0cde8-152">.NET Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-152">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="0cde8-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) (dá se odebrat)</span><span class="sxs-lookup"><span data-stu-id="0cde8-153">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="0cde8-154">Visual Basic Guide</span><span class="sxs-lookup"><span data-stu-id="0cde8-154">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="0cde8-155">Hledání v jednom oddílu příručky</span><span class="sxs-lookup"><span data-stu-id="0cde8-155">Search one section of a guide</span></span>

<span data-ttu-id="0cde8-156">![:card_file_box: Oblast na středně tmavém modrém pozadí](./media/labels-projects/technology.png "Předpona pro popisky podoblastí příručky .NET")</span><span class="sxs-lookup"><span data-stu-id="0cde8-156">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="0cde8-157">Příručky .NET jsou velké, takže tyto popisky vymezují rozsah podle oddílu příručky.</span><span class="sxs-lookup"><span data-stu-id="0cde8-157">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="0cde8-158">Každá podoblast příručky .NET je označena předponou `:card_file_box: Technology` a má středně tmavé modré pozadí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-158">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="0cde8-159">Mnohé z těchto popisků platí pro více příruček, ale některé jsou jenom v jedné.</span><span class="sxs-lookup"><span data-stu-id="0cde8-159">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="0cde8-160">Když po filtrování v oblasti přidáte jeden z těchto popisků, rozsah problémů se zúží.</span><span class="sxs-lookup"><span data-stu-id="0cde8-160">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="0cde8-161">AppCompat</span><span class="sxs-lookup"><span data-stu-id="0cde8-161">AppCompat</span></span>
- <span data-ttu-id="0cde8-162">Async Task</span><span class="sxs-lookup"><span data-stu-id="0cde8-162">Async Task</span></span>
- <span data-ttu-id="0cde8-163">Koncepty C# Advanced</span><span class="sxs-lookup"><span data-stu-id="0cde8-163">C# Advanced concepts</span></span>
- <span data-ttu-id="0cde8-164">Kompilátor C#</span><span class="sxs-lookup"><span data-stu-id="0cde8-164">C# compiler</span></span>
- <span data-ttu-id="0cde8-165">Základy C#</span><span class="sxs-lookup"><span data-stu-id="0cde8-165">C# Fundamentals</span></span>
- <span data-ttu-id="0cde8-166">Začínáme s C#</span><span class="sxs-lookup"><span data-stu-id="0cde8-166">C# Get Started</span></span>
- <span data-ttu-id="0cde8-167">Referenční dokumentace jazyka C#</span><span class="sxs-lookup"><span data-stu-id="0cde8-167">C# Language Reference</span></span>
- <span data-ttu-id="0cde8-168">Bezpečnost C# Null</span><span class="sxs-lookup"><span data-stu-id="0cde8-168">C# Null safety</span></span>
- <span data-ttu-id="0cde8-169">Novinky v C#</span><span class="sxs-lookup"><span data-stu-id="0cde8-169">C# What's new</span></span>
- <span data-ttu-id="0cde8-170">Rozhraní příkazového řádku</span><span class="sxs-lookup"><span data-stu-id="0cde8-170">CLI</span></span>
- <span data-ttu-id="0cde8-171">Přístup k datům</span><span class="sxs-lookup"><span data-stu-id="0cde8-171">Data Access</span></span>
- <span data-ttu-id="0cde8-172">Docker</span><span class="sxs-lookup"><span data-stu-id="0cde8-172">Docker</span></span>
- <span data-ttu-id="0cde8-173">Instalační programy</span><span class="sxs-lookup"><span data-stu-id="0cde8-173">Installers</span></span>
- <span data-ttu-id="0cde8-174">LINQ</span><span class="sxs-lookup"><span data-stu-id="0cde8-174">LINQ</span></span>
- <span data-ttu-id="0cde8-175">NCL</span><span class="sxs-lookup"><span data-stu-id="0cde8-175">NCL</span></span>
- <span data-ttu-id="0cde8-176">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="0cde8-176">.NET Standard</span></span>
- <span data-ttu-id="0cde8-177">Rozhraní API pro Roslyn</span><span class="sxs-lookup"><span data-stu-id="0cde8-177">Roslyn APIs</span></span>
- <span data-ttu-id="0cde8-178">Zabezpečení</span><span class="sxs-lookup"><span data-stu-id="0cde8-178">Security</span></span>
- <span data-ttu-id="0cde8-179">WCF</span><span class="sxs-lookup"><span data-stu-id="0cde8-179">WCF</span></span>
- <span data-ttu-id="0cde8-180">WF</span><span class="sxs-lookup"><span data-stu-id="0cde8-180">WF</span></span>
- <span data-ttu-id="0cde8-181">WIF</span><span class="sxs-lookup"><span data-stu-id="0cde8-181">WIF</span></span>
- <span data-ttu-id="0cde8-182">WinForms</span><span class="sxs-lookup"><span data-stu-id="0cde8-182">WinForms</span></span>
- <span data-ttu-id="0cde8-183">WPF</span><span class="sxs-lookup"><span data-stu-id="0cde8-183">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="0cde8-184">Verze</span><span class="sxs-lookup"><span data-stu-id="0cde8-184">Releases</span></span>

<span data-ttu-id="0cde8-185">![:checkered_flag: Verze: na tmavě žluté](./media/labels-projects/release.png "Předpona pro popisky verzí")</span><span class="sxs-lookup"><span data-stu-id="0cde8-185">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="0cde8-186">Problémy označené pro konkrétní verzi jsou označeny předponou `:checkered_flag: Release:` a mají tmavě žluté pozadí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-186">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="0cde8-187">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="0cde8-187">.NET Core 2.2</span></span>
- <span data-ttu-id="0cde8-188">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="0cde8-188">.NET Core 3.0</span></span>
- <span data-ttu-id="0cde8-189"> .NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="0cde8-189">.NET Framework 4.8</span></span>
- <span data-ttu-id="0cde8-190">.NET 5</span><span class="sxs-lookup"><span data-stu-id="0cde8-190">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="0cde8-191">Priorita</span><span class="sxs-lookup"><span data-stu-id="0cde8-191">Priority</span></span>

<span data-ttu-id="0cde8-192">Popisky priorit `P` jsou všechny následované jednou číslicí.</span><span class="sxs-lookup"><span data-stu-id="0cde8-192">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="0cde8-193">Nižší hodnota znamená vyšší prioritu:</span><span class="sxs-lookup"><span data-stu-id="0cde8-193">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="0cde8-194">P0 – označuje problémy nebo žádosti o přijetí změn, které mají kritickou prioritou</span><span class="sxs-lookup"><span data-stu-id="0cde8-194">P0 - Indicates issues or PRs that are critical priority</span></span>
- <span data-ttu-id="0cde8-195">P1 – vysoká priorita</span><span class="sxs-lookup"><span data-stu-id="0cde8-195">P1 - High priority</span></span>
- <span data-ttu-id="0cde8-196">P2 – střední priorita</span><span class="sxs-lookup"><span data-stu-id="0cde8-196">P2 - Medium priority</span></span>
- <span data-ttu-id="0cde8-197">P3 – nízká priorita</span><span class="sxs-lookup"><span data-stu-id="0cde8-197">P3 - Low priority</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="0cde8-198">K čemu jsou ostatní popisky</span><span class="sxs-lookup"><span data-stu-id="0cde8-198">What about the other labels</span></span>

<span data-ttu-id="0cde8-199">Týmy obsahu používají mnoho dalších popisků, které slouží ke správě různých klasifikací problémů.</span><span class="sxs-lookup"><span data-stu-id="0cde8-199">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="0cde8-200">Pokud nejste v týmu obsahu, můžete tyto další popisky ignorovat.</span><span class="sxs-lookup"><span data-stu-id="0cde8-200">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="0cde8-201">Projekty</span><span class="sxs-lookup"><span data-stu-id="0cde8-201">Projects</span></span>

<span data-ttu-id="0cde8-202">Projekty jsou určené pro účely plánování, kdy práce s prioritou je automatizována prostřednictvím panelu Kanbanu.</span><span class="sxs-lookup"><span data-stu-id="0cde8-202">Projects are intended for planning purposes, where prioritized work is automated through a Kanban board.</span></span> <span data-ttu-id="0cde8-203">Projekty by měly vždy obsahovat jen problémy GitHubu, _ne_ žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="0cde8-203">Projects should only ever contain GitHub issues, _not_ pull requests.</span></span> <span data-ttu-id="0cde8-204">Projekty se liší od milníků tím, že milníky obsahují jen žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="0cde8-204">Projects differ from milestones, in that milestones only contain pull requests.</span></span>

<span data-ttu-id="0cde8-205">Projekty používáme dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="0cde8-205">We use projects in two ways:</span></span>

- <span data-ttu-id="0cde8-206">Typy projektů `Month YYYY`: Jde o panely Kanbanu pro pracovní plán každého měsíce.</span><span class="sxs-lookup"><span data-stu-id="0cde8-206">`Month YYYY` project types: These are Kanban boards for each month's working plan.</span></span>
  - <span data-ttu-id="0cde8-207">Příklady: [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117) a tak dále.</span><span class="sxs-lookup"><span data-stu-id="0cde8-207">Examples, [July 2020](https://github.com/dotnet/docs/projects/103), [August 2020](https://github.com/dotnet/docs/projects/117), and so on.</span></span>
- <span data-ttu-id="0cde8-208">Dlouhodobé procesy: Slouží k uspořádání úkolů směrem k cíli, kdy práce bude probíhat několik měsíců.</span><span class="sxs-lookup"><span data-stu-id="0cde8-208">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
  - <span data-ttu-id="0cde8-209">Příklady: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave)](https://github.com/dotnet/docs/projects/106) a tak dále.</span><span class="sxs-lookup"><span data-stu-id="0cde8-209">Examples: [.NET 5 Wave - Reorganization](https://github.com/dotnet/docs/projects/105), [.NET Languages (.NET 5 wave) ](https://github.com/dotnet/docs/projects/106), and so on.</span></span>

## <a name="milestones"></a><span data-ttu-id="0cde8-210">Milníky</span><span class="sxs-lookup"><span data-stu-id="0cde8-210">Milestones</span></span>

<span data-ttu-id="0cde8-211">Milníky se obvykle řídí stejnými zásadami vytváření názvů jako projekty `Month YYYY`, ale od projektů se liší.</span><span class="sxs-lookup"><span data-stu-id="0cde8-211">Milestones typically follow the same naming convention of projects `Month YYYY`, but they're different from projects.</span></span> <span data-ttu-id="0cde8-212">Milníky používáme ke sledování dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="0cde8-212">We use milestones to track completed work.</span></span> <span data-ttu-id="0cde8-213">Milníky by _ne_měly obsahovat problémy (potenciální práci), ale výhradně jen žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="0cde8-213">Milestones should _not_ contain issues (potential work), but rather exclusively contain pull requests.</span></span> <span data-ttu-id="0cde8-214">Aktuální milník se automaticky použije na nové žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="0cde8-214">The current milestone is automatically applied to new pull requests.</span></span>
