---
title: Odeslání žádosti o přijetí změn
description: Tento článek popisuje postup žádosti o přijetí změn a vysvětluje osvědčené postupy, které zajistí slučitelnost vašeho příspěvku.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290074"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="6f688-103">Osvědčené postupy u žádostí o přijetí změn</span><span class="sxs-lookup"><span data-stu-id="6f688-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="6f688-104">Když chcete publikovat změny obsahu, odešlete ze svého forku žádost o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="6f688-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="6f688-105">Každá žádost o přijetí změn se musí před sloučením zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="6f688-105">Every pull request has to be reviewed before it can merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="6f688-106">Volba správné větve</span><span class="sxs-lookup"><span data-stu-id="6f688-106">Target the correct branch</span></span>

<span data-ttu-id="6f688-107">Všechny změny je potřeba provést ve větvi `staging`.</span><span class="sxs-lookup"><span data-stu-id="6f688-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="6f688-108">Změny by se nikdy neměly provádět ve větvi `live`.</span><span class="sxs-lookup"><span data-stu-id="6f688-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="6f688-109">Změny provedené ve větvi `staging` se sloučí do větve `live`, takže všechny změny provedené ve větvi `live` se přepíšou.</span><span class="sxs-lookup"><span data-stu-id="6f688-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="6f688-110">Pokud odesíláte změnu v dokumentaci, která platí jenom pro nevydanou verzi PowerShellu, zkontrolujte, jestli má daná verze svou větev.</span><span class="sxs-lookup"><span data-stu-id="6f688-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="6f688-111">Všechny změny, které se týkají určité budoucí verze, musí být určeny pro větev vydané verze.</span><span class="sxs-lookup"><span data-stu-id="6f688-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="6f688-112">Větve vydaných verzí mají název v následujícím tvaru: `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="6f688-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="6f688-113">Efektivnější fungování fronty žádostí o přijetí změn pro všechny</span><span class="sxs-lookup"><span data-stu-id="6f688-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="6f688-114">Ve frontě žádostí o přijetí změn fungují dvě základní skutečnosti:</span><span class="sxs-lookup"><span data-stu-id="6f688-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="6f688-115">Kontrola žádostí o přijetí změn, které jsou menšího rozsahu a obsahují podobné změny, trvá kratší dobu.</span><span class="sxs-lookup"><span data-stu-id="6f688-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="6f688-116">Naopak kontrola žádostí o přijetí změn, které jsou rozsáhlé nebo obsahují nesouvisející změny, trvá déle.</span><span class="sxs-lookup"><span data-stu-id="6f688-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="6f688-117">Eliminace větví, které aktualizují velký počet souborů</span><span class="sxs-lookup"><span data-stu-id="6f688-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="6f688-118">Oddělte menší aktualizace stávajících článků od nových článků nebo výrazných přepracování.</span><span class="sxs-lookup"><span data-stu-id="6f688-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="6f688-119">Na těchto změnách pracujte v samostatných pracovních větvích.</span><span class="sxs-lookup"><span data-stu-id="6f688-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="6f688-120">Hromadné změny se používají u žádostí o přijetí změn s velkým počtem změněných souborů.</span><span class="sxs-lookup"><span data-stu-id="6f688-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="6f688-121">Omezte své žádosti o přijetí změn na nejvýše 50 změněných souborů.</span><span class="sxs-lookup"><span data-stu-id="6f688-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="6f688-122">Rozsáhlé žádosti o přijetí změn se obtížně kontrolují a je u nich větší pravděpodobnost výskytu chyb.</span><span class="sxs-lookup"><span data-stu-id="6f688-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="6f688-123">Přejmenovávání nebo odstraňování souborů</span><span class="sxs-lookup"><span data-stu-id="6f688-123">Renaming or deleting files</span></span>

<span data-ttu-id="6f688-124">Když přejmenováváte nebo odstraňujete soubory, snažte se nemíchat tyto změny s přidáváním nebo aktualizací obsahu.</span><span class="sxs-lookup"><span data-stu-id="6f688-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="6f688-125">Tyto změny zpracujte do samostatných žádostí o přijetí změn, které se sloučí až po žádostech o přijetí změn týkajících se souvisejících aktualizací.</span><span class="sxs-lookup"><span data-stu-id="6f688-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="6f688-126">Například před odstraněním článku aktualizujte soubor přesměrování a ověřte, zda přesměrování funguje.</span><span class="sxs-lookup"><span data-stu-id="6f688-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="6f688-127">Musíte aktualizovat všechny soubory, které odkazují na přejmenovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="6f688-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="6f688-128">Patří k nim i všechny soubory s obsahem.</span><span class="sxs-lookup"><span data-stu-id="6f688-128">This includes any TOC files.</span></span> <span data-ttu-id="6f688-129">Dále musíte do hlavního směrovacího souboru (`.openpublishing.redirection.json`), který je v kořenovém adresáři úložiště, přidat záznamy o přesměrování.</span><span class="sxs-lookup"><span data-stu-id="6f688-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="6f688-130">Odkaz na službu ověřování žádostí o přijetí změn Docs</span><span class="sxs-lookup"><span data-stu-id="6f688-130">Docs PR validation service</span></span>

<span data-ttu-id="6f688-131">Služba ověřování žádostí o přijetí změn Docs je githubová aplikace, která spouští ověřovací pravidla u souborů v žádosti o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="6f688-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="6f688-132">Uvidíte následující chování:</span><span class="sxs-lookup"><span data-stu-id="6f688-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="6f688-133">Odešlete žádost o přijetí změn.</span><span class="sxs-lookup"><span data-stu-id="6f688-133">You submit a PR.</span></span>
1. <span data-ttu-id="6f688-134">V komentáři GitHubu, který označuje stav vaší žádosti o přijetí změn, se zobrazí stav kontrol povolených u úložiště.</span><span class="sxs-lookup"><span data-stu-id="6f688-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="6f688-135">Všimněte si, že v tomto příkladu jsou povolené dvě kontroly, Commit Validation a OpenPublishing.Build:</span><span class="sxs-lookup"><span data-stu-id="6f688-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![Některé kontroly nebyly úspěšné.](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="6f688-137">Sestavení může projít, i když se ověření potvrzení nezdaří.</span><span class="sxs-lookup"><span data-stu-id="6f688-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="6f688-138">Další informace se zobrazí po kliknutí na **Details** (Podrobnosti).</span><span class="sxs-lookup"><span data-stu-id="6f688-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="6f688-139">Na stránce podrobností se zobrazí všechny neúspěšné validační kontroly, včetně informací o možném řešení problémů.</span><span class="sxs-lookup"><span data-stu-id="6f688-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="6f688-140">Pokud je ověření úspěšné, přidá se do žádosti o přijetí změn následující komentář:</span><span class="sxs-lookup"><span data-stu-id="6f688-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![Ověření sestavení](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="6f688-142">Pokud jste externím přispěvatelem (nepatříte k Microsoftu), nemáte přístup k podrobným sestavám o sestavení ani k odkazům na verzi Preview.</span><span class="sxs-lookup"><span data-stu-id="6f688-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="6f688-143">Upozornění sestavení</span><span class="sxs-lookup"><span data-stu-id="6f688-143">Build warnings</span></span>

<span data-ttu-id="6f688-144">Normálně byste měli opravit všechny chyby, upozornění a doporučení, které se týkají sestavení.</span><span class="sxs-lookup"><span data-stu-id="6f688-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="6f688-145">Některá upozornění ale můžete ignorovat.</span><span class="sxs-lookup"><span data-stu-id="6f688-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="6f688-146">Následující upozornění můžete ignorovat:</span><span class="sxs-lookup"><span data-stu-id="6f688-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="6f688-147">Can't find service name for `<version>/<modulepath>/About/About.md` (Nelze najít název služby pro...)</span><span class="sxs-lookup"><span data-stu-id="6f688-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="6f688-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`. (Metadata s následujícím názvem nebo názvy nejdou nastavit v nadpisech Yaml, nejdou nastavit jako metadata na úrovni souboru docfx.json, ani jako globální metadata v souboru docfx.json...)</span><span class="sxs-lookup"><span data-stu-id="6f688-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="6f688-149">Tato upozornění generuje platforma Docs, takže se k hodnotám nastaveným na těchto třech místech nebude přihlížet.</span><span class="sxs-lookup"><span data-stu-id="6f688-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="6f688-150">Pokud chcete upozornění vyřešit, odeberte je ze všech tří míst.</span><span class="sxs-lookup"><span data-stu-id="6f688-150">Please remove them from all 3 places to resolve the warning.</span></span>
