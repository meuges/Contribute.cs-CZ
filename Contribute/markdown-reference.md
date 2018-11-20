---
title: Referenční informace k jazyku Markdown pro OPS a docs.microsoft.com
description: Průvodce platformou OPS pro Markdown a rozšíření DFM (DocFX Flavored Markdown)
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 64921bacf48e638221048db4b24e1a941f1d2777
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609538"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="85c36-103">Referenční informace k jazyku Markdown pro OPS</span><span class="sxs-lookup"><span data-stu-id="85c36-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="85c36-104">Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu.</span><span class="sxs-lookup"><span data-stu-id="85c36-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="85c36-105">Platforma Open Publishing Services (OPS) podporuje standard CommonMark jazyka Markdown a k němu několik vlastních rozšíření Markdownu navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="85c36-105">Open Publishing Services (OPS) supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="85c36-106">Tento článek obsahuje referenční informace o používání jazyka Markdown v OPS pro docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="85c36-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="85c36-107">K vytváření Markdownu můžete použít libovolný textový editor.</span><span class="sxs-lookup"><span data-stu-id="85c36-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="85c36-108">Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření OPS, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="85c36-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="85c36-109">Platforma OPS přijala Markdig za standard pro všechna nová úložiště a starší úložiště se na Markdig migrují.</span><span class="sxs-lookup"><span data-stu-id="85c36-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="85c36-110">Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="85c36-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="85c36-111">Výstrahy (Poznámka, Tip, Důležité, Pozor, Upozornění)</span><span class="sxs-lookup"><span data-stu-id="85c36-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="85c36-112">Výstrahy jsou rozšíření Markdownu, které je specifické pro OPS. Umožňují vytvářet citované bloky zobrazované na webu docs.microsoft.com i s barvami a ikonami, které zdůrazňují důležitost obsahu.</span><span class="sxs-lookup"><span data-stu-id="85c36-112">Alerts is an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="85c36-113">Podporují se následující typy výstrah:</span><span class="sxs-lookup"><span data-stu-id="85c36-113">The following alert types are supported:</span></span>

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="85c36-114">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="85c36-115">Informace, kterých by si uživatel měl všimnout i při rychlém čtení</span><span class="sxs-lookup"><span data-stu-id="85c36-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="85c36-116">Informace, které pomáhají uživateli lépe uspět</span><span class="sxs-lookup"><span data-stu-id="85c36-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85c36-117">Důležité informace potřebné k tomu, aby uživatel uspěl</span><span class="sxs-lookup"><span data-stu-id="85c36-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="85c36-118">Negativní potenciální důsledky nějaké akce</span><span class="sxs-lookup"><span data-stu-id="85c36-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="85c36-119">Nebezpečné důsledky nějaké akce</span><span class="sxs-lookup"><span data-stu-id="85c36-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="85c36-120">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="85c36-120">Code snippets</span></span>

<span data-ttu-id="85c36-121">Do souborů Markdown můžete začlenit fragmenty kódu:</span><span class="sxs-lookup"><span data-stu-id="85c36-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="85c36-122">Nadpis</span><span class="sxs-lookup"><span data-stu-id="85c36-122">Headings</span></span>

<span data-ttu-id="85c36-123">OPS podporuje šest úrovní nadpisů Markdownu:</span><span class="sxs-lookup"><span data-stu-id="85c36-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="85c36-124">Mezi posledním symbolem `#` a textem nadpisu musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="85c36-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="85c36-125">Každý soubor Markdown musí mít právě jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="85c36-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="85c36-126">Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.</span><span class="sxs-lookup"><span data-stu-id="85c36-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="85c36-127">Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="85c36-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="85c36-128">Nadpisy nižších úrovní nikoli, proto nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.</span><span class="sxs-lookup"><span data-stu-id="85c36-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="85c36-129">Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="85c36-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="85c36-130">Odkazy na jednotlivé nadpisy v souboru můžete realizovat přes [záložky](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="85c36-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="85c36-131">HTML</span><span class="sxs-lookup"><span data-stu-id="85c36-131">HTML</span></span>

<span data-ttu-id="85c36-132">Ačkoli Markdown podporuje vložený kód HTML, pro publikování přes OPS se HTML nedoporučuje, přičemž až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="85c36-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="85c36-133">Obrázky</span><span class="sxs-lookup"><span data-stu-id="85c36-133">Images</span></span>

<span data-ttu-id="85c36-134">Syntaxe pro začlenění obrázku:</span><span class="sxs-lookup"><span data-stu-id="85c36-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="85c36-135">`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="85c36-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="85c36-136">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="85c36-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="85c36-137">Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="85c36-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="85c36-138">Obrázky by měly být uložené ve složce `/media` v sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="85c36-139">Pro obrázky se standardně podporují tyto typy souborů:</span><span class="sxs-lookup"><span data-stu-id="85c36-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="85c36-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="85c36-140">.jpg</span></span>
- <span data-ttu-id="85c36-141">.png</span><span class="sxs-lookup"><span data-stu-id="85c36-141">.png</span></span>

<span data-ttu-id="85c36-142">Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json<!--add link to reference when available--> sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="85c36-143">Odkazy</span><span class="sxs-lookup"><span data-stu-id="85c36-143">Links</span></span>

<span data-ttu-id="85c36-144">OPS používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky.</span><span class="sxs-lookup"><span data-stu-id="85c36-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="85c36-145">Typy odkazů jsou popsané v níže uvedených pododdílech.</span><span class="sxs-lookup"><span data-stu-id="85c36-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="85c36-146">Balíček pro vytváření obsahu na webu Docs pro VS Code vám může pomoci vkládat relativní odkazy a záložky bez nudného určování cest.</span><span class="sxs-lookup"><span data-stu-id="85c36-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85c36-147">Do odkazů na weby Microsoftu nezačleňujte kódy národního prostředí, například cs-cz.</span><span class="sxs-lookup"><span data-stu-id="85c36-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="85c36-148">Pevně zakódované kódy národního prostředí zabraňují zobrazení lokalizovaného obsahu, což je pro uživatele v jiných národních prostředích nepříjemná zkušenost, a způsobují významné náklady na lokalizaci.</span><span class="sxs-lookup"><span data-stu-id="85c36-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="85c36-149">Při kopírování adresy URL z prohlížeče se automaticky kopíruje i kód národního prostředí, který při vytváření odkazu musíte ručně odstranit.</span><span class="sxs-lookup"><span data-stu-id="85c36-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="85c36-150">Použijte například tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="85c36-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="85c36-151">Nikoli tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="85c36-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="85c36-152">Relativní odkazy na soubory ve stejné sadě dokumentace</span><span class="sxs-lookup"><span data-stu-id="85c36-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="85c36-153">Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru.</span><span class="sxs-lookup"><span data-stu-id="85c36-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="85c36-154">V OPS můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="85c36-155">Relativní cesta má následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="85c36-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="85c36-156">`../` označuje jednu úroveň výše v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="85c36-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="85c36-157">Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.</span><span class="sxs-lookup"><span data-stu-id="85c36-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="85c36-158">K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="85c36-159">Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="85c36-160">OPS podporuje speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="85c36-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="85c36-161">Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="85c36-162">Během sestavování se ověří a přeloží i tento druh cesty.</span><span class="sxs-lookup"><span data-stu-id="85c36-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85c36-163">Do relativní cesty začleňte příponu souboru.</span><span class="sxs-lookup"><span data-stu-id="85c36-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="85c36-164">Při sestavování se ověřuje existence cílového souboru v této relativní cestě.</span><span class="sxs-lookup"><span data-stu-id="85c36-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="85c36-165">Pokud relativní cesta neobsahuje příponu souboru, při sestavování se pravděpodobně nahlásí upozornění nebo přerušený hypertextový odkaz.</span><span class="sxs-lookup"><span data-stu-id="85c36-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="85c36-166">Použijte například tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="85c36-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="85c36-167">Nikoli tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="85c36-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="85c36-168">Absolutní odkazy na jiné soubory v OPS</span><span class="sxs-lookup"><span data-stu-id="85c36-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="85c36-169">Nezačleňujte příponu souboru (.md).</span><span class="sxs-lookup"><span data-stu-id="85c36-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="85c36-170">Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.</span><span class="sxs-lookup"><span data-stu-id="85c36-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="85c36-171">Odkazy na externí weby</span><span class="sxs-lookup"><span data-stu-id="85c36-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="85c36-172">Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).</span><span class="sxs-lookup"><span data-stu-id="85c36-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="85c36-173">Odkazy na záložky</span><span class="sxs-lookup"><span data-stu-id="85c36-173">Bookmark links</span></span>

<span data-ttu-id="85c36-174">Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti:</span><span class="sxs-lookup"><span data-stu-id="85c36-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="85c36-175">Odkaz na záložku u nadpisu v aktuálním souboru:</span><span class="sxs-lookup"><span data-stu-id="85c36-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="85c36-176">Použijte mřížku následovanou textem nadpisu s odebranou interpunkcí a mezerami nahrazenými pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="85c36-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="85c36-177">Explicitní odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="85c36-177">Explicit anchor links</span></span>

<span data-ttu-id="85c36-178">Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek.</span><span class="sxs-lookup"><span data-stu-id="85c36-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="85c36-179">V obecných souborech Markdown použijte výše popsané záložky.</span><span class="sxs-lookup"><span data-stu-id="85c36-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="85c36-180">Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="85c36-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="85c36-181">`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="85c36-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="85c36-182">Pro odkaz na explicitní ukotvení použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="85c36-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="85c36-183">Křížové odkazy XREF</span><span class="sxs-lookup"><span data-stu-id="85c36-183">XREF (cross reference) links</span></span>

<span data-ttu-id="85c36-184">K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).</span><span class="sxs-lookup"><span data-stu-id="85c36-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="85c36-185">Pokud chcete vytvářet odkazy na stránky s referenčními informacemi k rozhraní API v jiných sadách dokumentace, potřebujete do souboru `docfx.json` přidat konfiguraci `xrefService`.</span><span class="sxs-lookup"><span data-stu-id="85c36-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="85c36-186">Identifikátor odpovídá plně kvalifikované třídě a názvu člena.</span><span class="sxs-lookup"><span data-stu-id="85c36-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="85c36-187">Pokud za UID přidáte \*, představuje tento odkaz stránku přetížení, nikoli konkrétní rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="85c36-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="85c36-188">`List<T>.BinarySearch*` použijte například k odkazu na stránku metody BinarySearch místo odkazu na konkrétní přetížení, jako je `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="85c36-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="85c36-189">Můžete použít jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="85c36-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="85c36-190">Automatický odkaz: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="85c36-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="85c36-191">Nepovinný parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu.</span><span class="sxs-lookup"><span data-stu-id="85c36-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="85c36-192">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="85c36-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="85c36-193">Odkaz Markdownu: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="85c36-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="85c36-194">Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="85c36-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="85c36-195">Příklady:</span><span class="sxs-lookup"><span data-stu-id="85c36-195">Examples:</span></span>

- <span data-ttu-id="85c36-196">`<xref:System.String>` se zobrazí jako „String“.</span><span class="sxs-lookup"><span data-stu-id="85c36-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="85c36-197">`<xref:System.String?displayProperty=nameWithType>` se zobrazí jako „System.String“.</span><span class="sxs-lookup"><span data-stu-id="85c36-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="85c36-198">`[String class](xref:System.String)` se zobrazí jako „třída String“.</span><span class="sxs-lookup"><span data-stu-id="85c36-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="85c36-199">V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID.</span><span class="sxs-lookup"><span data-stu-id="85c36-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="85c36-200"><!-- ? -->Nejlepším způsobem, jak najít UID pro rozhraní API, je zobrazit zdrojový kód stránky API, na kterou chcete odkázat, a najít hodnotu ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="85c36-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="85c36-201">Hodnoty jednotlivých přetížení se ve zdroji nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="85c36-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="85c36-202">Pracujeme na tom, abychom v budoucnu měli lepší systém.</span><span class="sxs-lookup"><span data-stu-id="85c36-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="85c36-203">Pokud UID obsahuje speciální znaky \`, \# nebo \*, musí být hodnota UID uvedena ve formátu HTML `%60`, `%23` a `%2A` v uvedeném pořadí.</span><span class="sxs-lookup"><span data-stu-id="85c36-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="85c36-204">Někdy v tomto formátu uvidíte i závorky, není to ale povinné.</span><span class="sxs-lookup"><span data-stu-id="85c36-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="85c36-205">Příklady:</span><span class="sxs-lookup"><span data-stu-id="85c36-205">Examples:</span></span>

- <span data-ttu-id="85c36-206">System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.</span><span class="sxs-lookup"><span data-stu-id="85c36-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="85c36-207">System.Exception.\#ctor se změní na `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="85c36-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="85c36-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="85c36-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="85c36-209">Seznamy (číslované, odrážkové, kontrolní)</span><span class="sxs-lookup"><span data-stu-id="85c36-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="85c36-210">Číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="85c36-210">Numbered list</span></span>

<span data-ttu-id="85c36-211">Při vytváření číslovaného seznamu můžete všude použít jedničky (1), které se při publikování zobrazí jako sekvenční seznam.</span><span class="sxs-lookup"><span data-stu-id="85c36-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="85c36-212">Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat.</span><span class="sxs-lookup"><span data-stu-id="85c36-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="85c36-213">Nepoužívejte v seznamech ani vnořených seznamech písmena.</span><span class="sxs-lookup"><span data-stu-id="85c36-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="85c36-214">Při publikování přes OPS se nezobrazí správně.</span><span class="sxs-lookup"><span data-stu-id="85c36-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="85c36-215">Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena.</span><span class="sxs-lookup"><span data-stu-id="85c36-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="85c36-216">Například:</span><span class="sxs-lookup"><span data-stu-id="85c36-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="85c36-217">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-217">This renders as follows:</span></span>

1. <span data-ttu-id="85c36-218">Toto je</span><span class="sxs-lookup"><span data-stu-id="85c36-218">This is</span></span>
1. <span data-ttu-id="85c36-219">nadřazený číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="85c36-219">a parent numbered list</span></span>
   1. <span data-ttu-id="85c36-220">a toto je</span><span class="sxs-lookup"><span data-stu-id="85c36-220">and this is</span></span>
   1. <span data-ttu-id="85c36-221">vnořený číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="85c36-221">a nested numbered list</span></span>
1. <span data-ttu-id="85c36-222">(konec)</span><span class="sxs-lookup"><span data-stu-id="85c36-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="85c36-223">Seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="85c36-223">Bulleted list</span></span>

<span data-ttu-id="85c36-224">Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:</span><span class="sxs-lookup"><span data-stu-id="85c36-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="85c36-225">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-225">This renders as follows:</span></span>

- <span data-ttu-id="85c36-226">Toto je</span><span class="sxs-lookup"><span data-stu-id="85c36-226">This is</span></span>
- <span data-ttu-id="85c36-227">nadřazený seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="85c36-227">a parent bulleted list</span></span>
  - <span data-ttu-id="85c36-228">a toto je</span><span class="sxs-lookup"><span data-stu-id="85c36-228">and this is</span></span>
  - <span data-ttu-id="85c36-229">vnořený seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="85c36-229">a nested bulleted list</span></span>
- <span data-ttu-id="85c36-230">Hotovo!</span><span class="sxs-lookup"><span data-stu-id="85c36-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="85c36-231">Kontrolní seznam</span><span class="sxs-lookup"><span data-stu-id="85c36-231">Checklist</span></span>

<span data-ttu-id="85c36-232">Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:</span><span class="sxs-lookup"><span data-stu-id="85c36-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="85c36-233">Tento příklad se na webu docs.microsoft.com zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="85c36-234">List item 1</span><span class="sxs-lookup"><span data-stu-id="85c36-234">List item 1</span></span>
> * <span data-ttu-id="85c36-235">List item 2</span><span class="sxs-lookup"><span data-stu-id="85c36-235">List item 2</span></span>
> * <span data-ttu-id="85c36-236">List item 3</span><span class="sxs-lookup"><span data-stu-id="85c36-236">List item 3</span></span>

<span data-ttu-id="85c36-237">Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku.</span><span class="sxs-lookup"><span data-stu-id="85c36-237">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="85c36-238">Nepřidávejte do svých článků náhodné kontrolní seznamy.</span><span class="sxs-lookup"><span data-stu-id="85c36-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="85c36-239">Akce dalšího kroku</span><span class="sxs-lookup"><span data-stu-id="85c36-239">Next step action</span></span>

<span data-ttu-id="85c36-240">K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.</span><span class="sxs-lookup"><span data-stu-id="85c36-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="85c36-241">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="85c36-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="85c36-242">Například:</span><span class="sxs-lookup"><span data-stu-id="85c36-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="85c36-243">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="85c36-244">Informace o základním stylu</span><span class="sxs-lookup"><span data-stu-id="85c36-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="85c36-245">V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku.</span><span class="sxs-lookup"><span data-stu-id="85c36-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="85c36-246">Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="85c36-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="85c36-247">Definice oddílu</span><span class="sxs-lookup"><span data-stu-id="85c36-247">Section definition</span></span>

<span data-ttu-id="85c36-248"><!-- more info about this would be helpful! --> Je možné, že budete potřebovat nadefinovat oddíl.</span><span class="sxs-lookup"><span data-stu-id="85c36-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="85c36-249">Tato syntaxe se nejčastěji používá pro tabulky kódu.</span><span class="sxs-lookup"><span data-stu-id="85c36-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="85c36-250">Prohlédněte si následující příklad:</span><span class="sxs-lookup"><span data-stu-id="85c36-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="85c36-251">Předchozí text Markdownu blokové citace se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="85c36-252">Voliče</span><span class="sxs-lookup"><span data-stu-id="85c36-252">Selectors</span></span>

<span data-ttu-id="85c36-253"><!-- could be more clear! --> Selektor můžete použít, když chcete propojit různé stránky stejného článku.</span><span class="sxs-lookup"><span data-stu-id="85c36-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="85c36-254">Čtenáři pak můžou přepínat mezi těmito stránkami.</span><span class="sxs-lookup"><span data-stu-id="85c36-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="85c36-255">Toto rozšíření funguje mezi weby docs.microsoft.com a MSDN různě.</span><span class="sxs-lookup"><span data-stu-id="85c36-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="85c36-256">Jeden selektor</span><span class="sxs-lookup"><span data-stu-id="85c36-256">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="85c36-257">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="85c36-266">Vícenásobný selektor</span><span class="sxs-lookup"><span data-stu-id="85c36-266">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="85c36-267">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-267">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows Universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="85c36-278">Tables</span><span class="sxs-lookup"><span data-stu-id="85c36-278">Tables</span></span>

<span data-ttu-id="85c36-279">Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky.</span><span class="sxs-lookup"><span data-stu-id="85c36-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="85c36-280">Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:</span><span class="sxs-lookup"><span data-stu-id="85c36-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="85c36-281">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-281">This renders as follows:</span></span>

|<span data-ttu-id="85c36-282">Toto je</span><span class="sxs-lookup"><span data-stu-id="85c36-282">This is</span></span>   |<span data-ttu-id="85c36-283">jednoduché</span><span class="sxs-lookup"><span data-stu-id="85c36-283">a simple</span></span>   |<span data-ttu-id="85c36-284">záhlaví tabulky</span><span class="sxs-lookup"><span data-stu-id="85c36-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="85c36-285">data</span><span class="sxs-lookup"><span data-stu-id="85c36-285">table</span></span>     |<span data-ttu-id="85c36-286">tabulky</span><span class="sxs-lookup"><span data-stu-id="85c36-286">data</span></span>       |<span data-ttu-id="85c36-287">zde</span><span class="sxs-lookup"><span data-stu-id="85c36-287">here</span></span>        |
|<span data-ttu-id="85c36-288">ani nemusí</span><span class="sxs-lookup"><span data-stu-id="85c36-288">it doesn't</span></span>|<span data-ttu-id="85c36-289">být pěkně</span><span class="sxs-lookup"><span data-stu-id="85c36-289">actually</span></span>   |<span data-ttu-id="85c36-290">zarovnaná!</span><span class="sxs-lookup"><span data-stu-id="85c36-290">have to line up nicely!</span></span>||

<span data-ttu-id="85c36-291">Můžete také vytvořit tabulku bez záhlaví.</span><span class="sxs-lookup"><span data-stu-id="85c36-291">You can also create a table without a header.</span></span> <span data-ttu-id="85c36-292">Příklad vytvoření seznamu s více sloupci:</span><span class="sxs-lookup"><span data-stu-id="85c36-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="85c36-293">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="85c36-294">Tato</span><span class="sxs-lookup"><span data-stu-id="85c36-294">This</span></span> | <span data-ttu-id="85c36-295">tabulka</span><span class="sxs-lookup"><span data-stu-id="85c36-295">table</span></span> |
| <span data-ttu-id="85c36-296">nemá žádné</span><span class="sxs-lookup"><span data-stu-id="85c36-296">has no</span></span> | <span data-ttu-id="85c36-297">záhlaví</span><span class="sxs-lookup"><span data-stu-id="85c36-297">header</span></span> |

<span data-ttu-id="85c36-298">Sloupce můžete zarovnat pomocí dvojtečky:</span><span class="sxs-lookup"><span data-stu-id="85c36-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="85c36-299">Se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="85c36-300">zarovnání vpravo:</span><span class="sxs-lookup"><span data-stu-id="85c36-300">right aligned:</span></span>|
|<span data-ttu-id="85c36-301">:zarovnání vlevo</span><span class="sxs-lookup"><span data-stu-id="85c36-301">:left aligned</span></span>     |
|<span data-ttu-id="85c36-302">:na střed        :</span><span class="sxs-lookup"><span data-stu-id="85c36-302">:centered        :</span></span>|

> [!TIP]
> Rozšíření pro vytváření obsahu na webu Docs pro VS Code usnadňuje přidávání základních tabulek Markdownu.
>
> Můžete také použít [online generátor tabulek](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="85c36-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="85c36-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Toto funguje jen na webu docs.microsoft.com.

<span data-ttu-id="85c36-307">Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou.</span><span class="sxs-lookup"><span data-stu-id="85c36-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="85c36-308">Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit.</span><span class="sxs-lookup"><span data-stu-id="85c36-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="85c36-309">Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="85c36-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="85c36-310">Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="85c36-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="85c36-311">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="85c36-312">Název</span><span class="sxs-lookup"><span data-stu-id="85c36-312">Name</span></span>|<span data-ttu-id="85c36-313">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85c36-313">Syntax</span></span>|<span data-ttu-id="85c36-314">Povinné pro tichou instalaci?</span><span class="sxs-lookup"><span data-stu-id="85c36-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="85c36-315">Popis</span><span class="sxs-lookup"><span data-stu-id="85c36-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="85c36-316">Tichá instalace</span><span class="sxs-lookup"><span data-stu-id="85c36-316">Quiet</span></span>|<span data-ttu-id="85c36-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="85c36-317">/quiet</span></span>|<span data-ttu-id="85c36-318">Ano</span><span class="sxs-lookup"><span data-stu-id="85c36-318">Yes</span></span>|<span data-ttu-id="85c36-319">Spustí instalační program bez zobrazení uživatelského rozhraní a výzev.</span><span class="sxs-lookup"><span data-stu-id="85c36-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="85c36-320">Bez restartování</span><span class="sxs-lookup"><span data-stu-id="85c36-320">NoRestart</span></span>|<span data-ttu-id="85c36-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="85c36-321">/norestart</span></span>|<span data-ttu-id="85c36-322">Ne</span><span class="sxs-lookup"><span data-stu-id="85c36-322">No</span></span>|<span data-ttu-id="85c36-323">Potlačí všechny pokusy o restartování.</span><span class="sxs-lookup"><span data-stu-id="85c36-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="85c36-324">Ve výchozím nastavení zobrazí uživatelské rozhraní před restartováním výzvu.</span><span class="sxs-lookup"><span data-stu-id="85c36-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="85c36-325">Nápověda</span><span class="sxs-lookup"><span data-stu-id="85c36-325">Help</span></span>|<span data-ttu-id="85c36-326">/help</span><span class="sxs-lookup"><span data-stu-id="85c36-326">/help</span></span>|<span data-ttu-id="85c36-327">Ne</span><span class="sxs-lookup"><span data-stu-id="85c36-327">No</span></span>|<span data-ttu-id="85c36-328">Poskytuje nápovědu a stručné referenční informace.</span><span class="sxs-lookup"><span data-stu-id="85c36-328">Provides help and quick reference.</span></span> <span data-ttu-id="85c36-329">Zobrazí správné použití příkazu instalace včetně seznamu všech možností a chování.</span><span class="sxs-lookup"><span data-stu-id="85c36-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="85c36-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="85c36-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85c36-331">Toto funguje jen na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="85c36-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="85c36-332">Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova.</span><span class="sxs-lookup"><span data-stu-id="85c36-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="85c36-333">Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.</span><span class="sxs-lookup"><span data-stu-id="85c36-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="85c36-334">Tabulky HTML</span><span class="sxs-lookup"><span data-stu-id="85c36-334">HTML Tables</span></span>

<span data-ttu-id="85c36-335">Tabulky HTML se na webu docs.microsoft.com nedoporučují.</span><span class="sxs-lookup"><span data-stu-id="85c36-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="85c36-336">Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.</span><span class="sxs-lookup"><span data-stu-id="85c36-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="85c36-337">Videa</span><span class="sxs-lookup"><span data-stu-id="85c36-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="85c36-338">Vkládání videí na stránku Markdownu</span><span class="sxs-lookup"><span data-stu-id="85c36-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="85c36-339">OPS v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:</span><span class="sxs-lookup"><span data-stu-id="85c36-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="85c36-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="85c36-340">YouTube</span></span>
- <span data-ttu-id="85c36-341">Channel9</span><span class="sxs-lookup"><span data-stu-id="85c36-341">Channel 9</span></span>
- <span data-ttu-id="85c36-342">Vlastní systém Microsoftu „One Player“</span><span class="sxs-lookup"><span data-stu-id="85c36-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="85c36-343">Můžete vložit video s následující syntaxí a OPS ho zobrazí.</span><span class="sxs-lookup"><span data-stu-id="85c36-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="85c36-344">Příklad:</span><span class="sxs-lookup"><span data-stu-id="85c36-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="85c36-345">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="85c36-346">A na publikovaných stránkách se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="85c36-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="85c36-347">Adresa URL videa CH9 by měla začínat řetězcem `https` a končit řetězcem `/player`.</span><span class="sxs-lookup"><span data-stu-id="85c36-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="85c36-348">V opačném případě totiž místo samotného videa vloží celou stránku.</span><span class="sxs-lookup"><span data-stu-id="85c36-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="85c36-349">Nahrání nových videí</span><span class="sxs-lookup"><span data-stu-id="85c36-349">Uploading new videos</span></span>

<span data-ttu-id="85c36-350">Všechna nová videa by měla být nahrána následujícím postupem:</span><span class="sxs-lookup"><span data-stu-id="85c36-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="85c36-351">Připojte se ke skupině **docs_video_users** na IDWEB.</span><span class="sxs-lookup"><span data-stu-id="85c36-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="85c36-352">Přejděte na adresu https://aka.ms/VideoUploadRequest a vyplňte podrobnosti o videu.</span><span class="sxs-lookup"><span data-stu-id="85c36-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="85c36-353">Budete potřebovat zadat tyto údaje (žádné z nich nebudou veřejně viditelné):</span><span class="sxs-lookup"><span data-stu-id="85c36-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="85c36-354">Název videa</span><span class="sxs-lookup"><span data-stu-id="85c36-354">A title for your video.</span></span>
    1. <span data-ttu-id="85c36-355">Seznam produktů/služeb, kterých se video týká</span><span class="sxs-lookup"><span data-stu-id="85c36-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="85c36-356">Cílová stránka nebo (pokud tuto stránku ještě nemáte) sada dokumentace, kde bude video hostované</span><span class="sxs-lookup"><span data-stu-id="85c36-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="85c36-357">Odkaz na soubor MP4 s videem (pokud ještě nevíte, kde bude soubor umístěný, můžete sem dočasně zadat: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="85c36-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="85c36-358">Soubory MP4 by měly mít rozlišení 720p nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="85c36-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="85c36-359">Popis videa</span><span class="sxs-lookup"><span data-stu-id="85c36-359">A description of the video.</span></span>
1. <span data-ttu-id="85c36-360">Odešlete (uložte) tuto položku.</span><span class="sxs-lookup"><span data-stu-id="85c36-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="85c36-361">Video se nahraje během dvou pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="85c36-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="85c36-362">Odkaz potřebný k vložení bude umístěn do pracovní položky, která vám bude *přeložena zpět*.</span><span class="sxs-lookup"><span data-stu-id="85c36-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="85c36-363">Jakmile získáte odkaz na video, zavřete tuto pracovní položku.</span><span class="sxs-lookup"><span data-stu-id="85c36-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="85c36-364">Odkaz na video pak můžete přidat do příspěvku pomocí této syntaxe:</span><span class="sxs-lookup"><span data-stu-id="85c36-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
