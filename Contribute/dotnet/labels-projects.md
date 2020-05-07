---
title: Průvodce popisky a projekty
description: Tento článek vysvětluje, jak se používají popisky a projekty v úložišti dotnet/docs.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "80760369"
---
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="6e2e7-103">Průvodce popisky a projekty</span><span class="sxs-lookup"><span data-stu-id="6e2e7-103">Labels and projects roadmap</span></span>

<span data-ttu-id="6e2e7-104">Tým dokumentace k .NET rozsáhle využívá [popisky GitHubu](https://github.com/dotnet/docs/labels) k uspořádání a zpřehlednění naší práce.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="6e2e7-105">Díky vyfiltrování kombinace popisků se můžeme na [webu dokumentace k .NET](https://docs.microsoft.com/dotnet) rychle zaměřit na oddíly, které nás zajímají.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="6e2e7-106">K uspořádání sprintů a dalších procesů (příběhů) zaměřených na cíle používáme také [projekty GitHubu](https://github.com/dotnet/docs/projects).</span><span class="sxs-lookup"><span data-stu-id="6e2e7-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="6e2e7-107">Tento plán vysvětluje, jak tyto organizační nástroje používáme, a obsahuje odkazy na užitečné filtry, které používáme k vyhledání požadovaných oblastí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="6e2e7-108">Popisky</span><span class="sxs-lookup"><span data-stu-id="6e2e7-108">Labels</span></span>

<span data-ttu-id="6e2e7-109">Pokud jde o vaši první zkušenost s příspěvky do [dotnet/docs](https://github.com/dotnet/docs), začněte se záležitostmi [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs).</span><span class="sxs-lookup"><span data-stu-id="6e2e7-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="6e2e7-110">Jde o problémy, které mají konkrétnější zaměření.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="6e2e7-111">Představují skvělý způsob, jak udělat svůj první příspěvek.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="6e2e7-112">V zobrazení pro up-for-grabs můžete dál filtrovat problémy na základě oblastí a priority.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="6e2e7-113">Vhodné problémy pro začátečníky jsme označili popiskem [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue), pokud chcete vyzkoušet menší první příspěvek.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="6e2e7-114">Pomocí popisků rozdělujeme problémy mnoha různými způsoby:</span><span class="sxs-lookup"><span data-stu-id="6e2e7-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="6e2e7-115">[Příručky .NET](#find-a-single-net-guide) a [oddíly příručky](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="6e2e7-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="6e2e7-116">Cílová verze</span><span class="sxs-lookup"><span data-stu-id="6e2e7-116">Target release</span></span>](#releases)
- [<span data-ttu-id="6e2e7-117">Priorita</span><span class="sxs-lookup"><span data-stu-id="6e2e7-117">Priority</span></span>](#priority)

<span data-ttu-id="6e2e7-118">Můžete zkombinovat popisek z každé sady (příručka, verze, priorita), a zúžit tak prostor pro hledání problémů, na kterých chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="6e2e7-119">Vyhledání jedné příručky pro rozhraní .NET</span><span class="sxs-lookup"><span data-stu-id="6e2e7-119">Find a single .NET guide</span></span>

<span data-ttu-id="6e2e7-120">Popisky používáme pro každou elektronickou knihu (e-knihu) architektury a pro každou příručku .NET.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="6e2e7-121">![:book: příručka na světle zeleném pozadí](./media/labels-projects/guide.png "Předpona pro popisky příručky architektury")</span><span class="sxs-lookup"><span data-stu-id="6e2e7-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="6e2e7-122">E-knihy architektury jsou označeny předponou `:book: guide` a mají světlé zelené pozadí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="6e2e7-123">Jsou to rozsáhlejší oblasti, které se týkají doporučené architektury.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="6e2e7-124">Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky architektury .NET.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- [<span data-ttu-id="6e2e7-125">Webové aplikace ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6e2e7-125">ASP.NET Core web apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)
- [<span data-ttu-id="6e2e7-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="6e2e7-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [<span data-ttu-id="6e2e7-127">Nativní cloud</span><span class="sxs-lookup"><span data-stu-id="6e2e7-127">Cloud Native</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)
- [<span data-ttu-id="6e2e7-128">Životní cyklus nástroje Docker</span><span class="sxs-lookup"><span data-stu-id="6e2e7-128">Docker lifecycle</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)
- [<span data-ttu-id="6e2e7-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="6e2e7-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="6e2e7-130">Modernizace s kontejnery Windows</span><span class="sxs-lookup"><span data-stu-id="6e2e7-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="6e2e7-131">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="6e2e7-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="6e2e7-132">Bezserverové aplikace</span><span class="sxs-lookup"><span data-stu-id="6e2e7-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="6e2e7-133">Tento styl popisku se také používá v [pravidlech návrhu Frameworku](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="6e2e7-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="6e2e7-134">Tato oblast má stejný vzhled popisku, ale využívání v komunitě se nedoporučuje.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="6e2e7-135">Tento materiál je reprodukován s oprávněním a neměl se upravovat.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="6e2e7-136">![:books: Oblast na tmavě modrém pozadí](./media/labels-projects/area.png "Předpona pro popisky oblastí příručky .NET")</span><span class="sxs-lookup"><span data-stu-id="6e2e7-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="6e2e7-137">Každá příručka .NET je označena předponou `:books: Area` a má tmavě modré pozadí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="6e2e7-138">Tady jsou aktuální problémy vyfiltrované pro jednotlivé příručky .NET.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="6e2e7-139">Reference rozhraní API</span><span class="sxs-lookup"><span data-stu-id="6e2e7-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="6e2e7-140">Azure .NET SDK</span><span class="sxs-lookup"><span data-stu-id="6e2e7-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="6e2e7-141">C# Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="6e2e7-142">Desktop Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="6e2e7-143">F# Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="6e2e7-144">ML.NET Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="6e2e7-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) (dá se odebrat)</span><span class="sxs-lookup"><span data-stu-id="6e2e7-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="6e2e7-146">.NET Core Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="6e2e7-147">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="6e2e7-148">.NET Framework Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="6e2e7-149">.NET Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="6e2e7-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) (dá se odebrat)</span><span class="sxs-lookup"><span data-stu-id="6e2e7-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="6e2e7-151">Visual Basic Guide</span><span class="sxs-lookup"><span data-stu-id="6e2e7-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="6e2e7-152">Hledání v jednom oddílu příručky</span><span class="sxs-lookup"><span data-stu-id="6e2e7-152">Search one section of a guide</span></span>

<span data-ttu-id="6e2e7-153">![:card_file_box: Oblast na středně tmavém modrém pozadí](./media/labels-projects/technology.png "Předpona pro popisky podoblastí příručky .NET")</span><span class="sxs-lookup"><span data-stu-id="6e2e7-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="6e2e7-154">Příručky .NET jsou velké, takže tyto popisky vymezují rozsah podle oddílu příručky.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="6e2e7-155">Každá podoblast příručky .NET je označena předponou `:card_file_box: Technology` a má středně tmavé modré pozadí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="6e2e7-156">Mnohé z těchto popisků platí pro více příruček, ale některé jsou jenom v jedné.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="6e2e7-157">Když po filtrování v oblasti přidáte jeden z těchto popisků, rozsah problémů se zúží.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="6e2e7-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="6e2e7-158">AppCompat</span></span>
- <span data-ttu-id="6e2e7-159">Async Task</span><span class="sxs-lookup"><span data-stu-id="6e2e7-159">Async Task</span></span>
- <span data-ttu-id="6e2e7-160">Koncepty C# Advanced</span><span class="sxs-lookup"><span data-stu-id="6e2e7-160">C# Advanced concepts</span></span>
- <span data-ttu-id="6e2e7-161">Kompilátor C#</span><span class="sxs-lookup"><span data-stu-id="6e2e7-161">C# compiler</span></span>
- <span data-ttu-id="6e2e7-162">Základy C#</span><span class="sxs-lookup"><span data-stu-id="6e2e7-162">C# Fundamentals</span></span>
- <span data-ttu-id="6e2e7-163">Začínáme s C#</span><span class="sxs-lookup"><span data-stu-id="6e2e7-163">C# Get Started</span></span>
- <span data-ttu-id="6e2e7-164">Referenční informace k jazyku C#</span><span class="sxs-lookup"><span data-stu-id="6e2e7-164">C# Language Reference</span></span>
- <span data-ttu-id="6e2e7-165">Bezpečnost C# Null</span><span class="sxs-lookup"><span data-stu-id="6e2e7-165">C# Null safety</span></span>
- <span data-ttu-id="6e2e7-166">Novinky v C#</span><span class="sxs-lookup"><span data-stu-id="6e2e7-166">C# What's new</span></span>
- <span data-ttu-id="6e2e7-167">CLI</span><span class="sxs-lookup"><span data-stu-id="6e2e7-167">CLI</span></span>
- <span data-ttu-id="6e2e7-168">Přístup k datům</span><span class="sxs-lookup"><span data-stu-id="6e2e7-168">Data Access</span></span>
- <span data-ttu-id="6e2e7-169">Docker</span><span class="sxs-lookup"><span data-stu-id="6e2e7-169">Docker</span></span>
- <span data-ttu-id="6e2e7-170">Instalační programy</span><span class="sxs-lookup"><span data-stu-id="6e2e7-170">Installers</span></span>
- <span data-ttu-id="6e2e7-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="6e2e7-171">LINQ</span></span>
- <span data-ttu-id="6e2e7-172">NCL</span><span class="sxs-lookup"><span data-stu-id="6e2e7-172">NCL</span></span>
- <span data-ttu-id="6e2e7-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="6e2e7-173">.NET Standard</span></span>
- <span data-ttu-id="6e2e7-174">Rozhraní API pro Roslyn</span><span class="sxs-lookup"><span data-stu-id="6e2e7-174">Roslyn APIs</span></span>
- <span data-ttu-id="6e2e7-175">Zabezpečení</span><span class="sxs-lookup"><span data-stu-id="6e2e7-175">Security</span></span>
- <span data-ttu-id="6e2e7-176">WCF</span><span class="sxs-lookup"><span data-stu-id="6e2e7-176">WCF</span></span>
- <span data-ttu-id="6e2e7-177">WF</span><span class="sxs-lookup"><span data-stu-id="6e2e7-177">WF</span></span>
- <span data-ttu-id="6e2e7-178">WIF</span><span class="sxs-lookup"><span data-stu-id="6e2e7-178">WIF</span></span>
- <span data-ttu-id="6e2e7-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="6e2e7-179">WinForms</span></span>
- <span data-ttu-id="6e2e7-180">WPF</span><span class="sxs-lookup"><span data-stu-id="6e2e7-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="6e2e7-181">Verze</span><span class="sxs-lookup"><span data-stu-id="6e2e7-181">Releases</span></span>

<span data-ttu-id="6e2e7-182">![:checkered_flag: Verze: na tmavě žluté](./media/labels-projects/release.png "Předpona pro popisky verzí")</span><span class="sxs-lookup"><span data-stu-id="6e2e7-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="6e2e7-183">Problémy označené pro konkrétní verzi jsou označeny předponou `:checkered_flag: Release:` a mají tmavě žluté pozadí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="6e2e7-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="6e2e7-184">.NET Core 2.2</span></span>
- <span data-ttu-id="6e2e7-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="6e2e7-185">.NET Core 3.0</span></span>
- <span data-ttu-id="6e2e7-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="6e2e7-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="6e2e7-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="6e2e7-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="6e2e7-188">Priorita</span><span class="sxs-lookup"><span data-stu-id="6e2e7-188">Priority</span></span>

<span data-ttu-id="6e2e7-189">Popisky priorit `P` jsou všechny následované jednou číslicí.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="6e2e7-190">Nižší hodnota znamená vyšší prioritu:</span><span class="sxs-lookup"><span data-stu-id="6e2e7-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="6e2e7-191">P0</span><span class="sxs-lookup"><span data-stu-id="6e2e7-191">P0</span></span>
- <span data-ttu-id="6e2e7-192">P1</span><span class="sxs-lookup"><span data-stu-id="6e2e7-192">P1</span></span>
- <span data-ttu-id="6e2e7-193">P2</span><span class="sxs-lookup"><span data-stu-id="6e2e7-193">P2</span></span>
- <span data-ttu-id="6e2e7-194">P3</span><span class="sxs-lookup"><span data-stu-id="6e2e7-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="6e2e7-195">K čemu jsou ostatní popisky?</span><span class="sxs-lookup"><span data-stu-id="6e2e7-195">What about the other labels?</span></span>

<span data-ttu-id="6e2e7-196">Týmy obsahu používají mnoho dalších popisků, které slouží ke správě různých klasifikací problémů.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="6e2e7-197">Pokud nejste v týmu obsahu, můžete tyto další popisky ignorovat.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="6e2e7-198">Projekty</span><span class="sxs-lookup"><span data-stu-id="6e2e7-198">Projects</span></span>

<span data-ttu-id="6e2e7-199">Projekty používáme dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="6e2e7-199">We use projects in two ways:</span></span>

- <span data-ttu-id="6e2e7-200">Typy projektů Měsíc RRRR: Jde o panely úkolů pro pracovní plán každého měsíce.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="6e2e7-201">Dlouhodobé procesy: Slouží k uspořádání úkolů směrem k cíli, kdy práce bude probíhat několik měsíců.</span><span class="sxs-lookup"><span data-stu-id="6e2e7-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
