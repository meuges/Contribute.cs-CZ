---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.openlocfilehash: 17bc6d3bf2de5077f490bea2f03cddf23d925b78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2019
ms.locfileid: "55712940"
---
# <a name="markdown-reference"></a><span data-ttu-id="ea1ff-103">Referenční informace k jazyku Markdown</span><span class="sxs-lookup"><span data-stu-id="ea1ff-103">Markdown Reference</span></span>

<span data-ttu-id="ea1ff-104">Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="ea1ff-105">Platforma Docs podporuje standard CommonMark pro Markdown plus několik vlastních rozšíření navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="ea1ff-106">Tento článek obsahuje referenční informace o používání jazyka Markdown pro docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="ea1ff-107">K vytváření Markdownu můžete použít libovolný textový editor.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="ea1ff-108">Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření Docs, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="ea1ff-109">Web Docs používá modul Markdig Markdown.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="ea1ff-110">Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="ea1ff-111">Výstrahy (Poznámka, Tip, Důležité, Pozor, Upozornění)</span><span class="sxs-lookup"><span data-stu-id="ea1ff-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="ea1ff-112">Výstrahy jsou rozšíření Docs Markdown určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="ea1ff-113">Podporují se následující typy výstrah:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="ea1ff-114">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="ea1ff-115">Informace, kterých by si uživatel měl všimnout i při rychlém čtení</span><span class="sxs-lookup"><span data-stu-id="ea1ff-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="ea1ff-116">Informace, které pomáhají uživateli lépe uspět</span><span class="sxs-lookup"><span data-stu-id="ea1ff-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea1ff-117">Důležité informace potřebné k tomu, aby uživatel uspěl</span><span class="sxs-lookup"><span data-stu-id="ea1ff-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="ea1ff-118">Negativní potenciální důsledky nějaké akce</span><span class="sxs-lookup"><span data-stu-id="ea1ff-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="ea1ff-119">Nebezpečné důsledky nějaké akce</span><span class="sxs-lookup"><span data-stu-id="ea1ff-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="ea1ff-120">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="ea1ff-120">Code snippets</span></span>

<span data-ttu-id="ea1ff-121">Do souborů Markdown můžete začlenit fragmenty kódu:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="ea1ff-122">Nadpis</span><span class="sxs-lookup"><span data-stu-id="ea1ff-122">Headings</span></span>

<span data-ttu-id="ea1ff-123">Web Docs podporuje šest úrovní nadpisů Markdownu:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="ea1ff-124">Mezi posledním symbolem `#` a textem nadpisu musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="ea1ff-125">Každý soubor Markdown musí mít právě jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="ea1ff-126">Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="ea1ff-127">Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="ea1ff-128">Nadpisy nižších úrovní nikoli, proto nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="ea1ff-129">Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="ea1ff-130">Odkazy na jednotlivé nadpisy v souboru můžete realizovat přes [záložky](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="ea1ff-131">HTML</span><span class="sxs-lookup"><span data-stu-id="ea1ff-131">HTML</span></span>

<span data-ttu-id="ea1ff-132">Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="ea1ff-133">Obrázky</span><span class="sxs-lookup"><span data-stu-id="ea1ff-133">Images</span></span>

<span data-ttu-id="ea1ff-134">Syntaxe pro začlenění obrázku:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="ea1ff-135">`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="ea1ff-136">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="ea1ff-137">Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="ea1ff-138">Obrázky by měly být uložené ve složce `/media` v sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="ea1ff-139">Pro obrázky se standardně podporují tyto typy souborů:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="ea1ff-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="ea1ff-140">.jpg</span></span>
- <span data-ttu-id="ea1ff-141">.png</span><span class="sxs-lookup"><span data-stu-id="ea1ff-141">.png</span></span>

<span data-ttu-id="ea1ff-142">Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json<!--add link to reference when available--> sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="ea1ff-143">Odkazy</span><span class="sxs-lookup"><span data-stu-id="ea1ff-143">Links</span></span>

<span data-ttu-id="ea1ff-144">Web Docs používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="ea1ff-145">Typy odkazů jsou popsané v níže uvedených pododdílech.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="ea1ff-146">Balíček pro vytváření obsahu na webu Docs pro VS Code vám může pomoci vkládat relativní odkazy a záložky bez nudného určování cest.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea1ff-147">Do odkazů na weby Microsoftu nezačleňujte kódy národního prostředí, například cs-cz.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="ea1ff-148">Pevně zakódované kódy národního prostředí zabraňují zobrazení lokalizovaného obsahu, což je pro uživatele v jiných národních prostředích nepříjemná zkušenost, a způsobují významné náklady na lokalizaci.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="ea1ff-149">Při kopírování adresy URL z prohlížeče se automaticky kopíruje i kód národního prostředí, který při vytváření odkazu musíte ručně odstranit.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="ea1ff-150">Použijte například tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="ea1ff-151">Nikoli tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="ea1ff-152">Relativní odkazy na soubory ve stejné sadě dokumentace</span><span class="sxs-lookup"><span data-stu-id="ea1ff-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="ea1ff-153">Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="ea1ff-154">Na webu Docs můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="ea1ff-155">Relativní cesta má následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="ea1ff-156">`../` označuje jednu úroveň výše v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="ea1ff-157">Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="ea1ff-158">K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="ea1ff-159">Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="ea1ff-160">Web Docs podporuje také speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="ea1ff-161">Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="ea1ff-162">Během sestavování se ověří a přeloží i tento druh cesty.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea1ff-163">Do relativní cesty začleňte příponu souboru.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="ea1ff-164">Při sestavování se ověřuje existence cílového souboru v této relativní cestě.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="ea1ff-165">Pokud relativní cesta neobsahuje příponu souboru, při sestavování se pravděpodobně nahlásí upozornění nebo přerušený hypertextový odkaz.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="ea1ff-166">Použijte například tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="ea1ff-167">Nikoli tento odkaz:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="ea1ff-168">Relativní odkazy na jiné soubory na webu Docs</span><span class="sxs-lookup"><span data-stu-id="ea1ff-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="ea1ff-169">Nezačleňujte příponu souboru (.md).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="ea1ff-170">Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="ea1ff-171">Odkazy na externí weby</span><span class="sxs-lookup"><span data-stu-id="ea1ff-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="ea1ff-172">Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="ea1ff-173">Odkazy na záložky</span><span class="sxs-lookup"><span data-stu-id="ea1ff-173">Bookmark links</span></span>

<span data-ttu-id="ea1ff-174">Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="ea1ff-175">Odkaz na záložku u nadpisu v aktuálním souboru:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="ea1ff-176">Použijte mřížku následovanou textem nadpisu s odebranou interpunkcí a mezerami nahrazenými pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="ea1ff-177">Explicitní odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="ea1ff-177">Explicit anchor links</span></span>

<span data-ttu-id="ea1ff-178">Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="ea1ff-179">V obecných souborech Markdown použijte výše popsané záložky.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="ea1ff-180">Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="ea1ff-181">`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="ea1ff-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="ea1ff-182">Pro odkaz na explicitní ukotvení použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="ea1ff-183">Křížové odkazy XREF</span><span class="sxs-lookup"><span data-stu-id="ea1ff-183">XREF (cross reference) links</span></span>

<span data-ttu-id="ea1ff-184">K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="ea1ff-185">Pokud chcete vytvářet odkazy na stránky s referenčními informacemi k rozhraní API v jiných sadách dokumentace, potřebujete do souboru `docfx.json` přidat konfiguraci `xrefService`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="ea1ff-186">Identifikátor odpovídá plně kvalifikované třídě a názvu člena.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="ea1ff-187">Pokud za UID přidáte \*, představuje tento odkaz stránku přetížení, nikoli konkrétní rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="ea1ff-188">`List<T>.BinarySearch*` použijte například k odkazu na stránku metody BinarySearch místo odkazu na konkrétní přetížení, jako je `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="ea1ff-189">Můžete použít jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="ea1ff-190">Automatický odkaz: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="ea1ff-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="ea1ff-191">Nepovinný parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="ea1ff-192">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="ea1ff-193">Odkaz Markdownu: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="ea1ff-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="ea1ff-194">Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="ea1ff-195">Příklady:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-195">Examples:</span></span>

- <span data-ttu-id="ea1ff-196">`<xref:System.String>` se zobrazí jako „String“.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="ea1ff-197">`<xref:System.String?displayProperty=nameWithType>` se zobrazí jako „System.String“.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="ea1ff-198">`[String class](xref:System.String)` se zobrazí jako „třída String“.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="ea1ff-199">V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="ea1ff-200"><!-- ? -->Nejlepším způsobem, jak najít UID pro rozhraní API, je zobrazit zdrojový kód stránky API, na kterou chcete odkázat, a najít hodnotu ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="ea1ff-201">Hodnoty jednotlivých přetížení se ve zdroji nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="ea1ff-202">Pracujeme na tom, abychom v budoucnu měli lepší systém.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="ea1ff-203">Pokud UID obsahuje speciální znaky \`, \# nebo \*, musí být hodnota UID uvedena ve formátu HTML `%60`, `%23` a `%2A` v uvedeném pořadí.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="ea1ff-204">Někdy v tomto formátu uvidíte i závorky, není to ale povinné.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="ea1ff-205">Příklady:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-205">Examples:</span></span>

- <span data-ttu-id="ea1ff-206">System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="ea1ff-207">System.Exception.\#ctor se změní na `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="ea1ff-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="ea1ff-209">Seznamy (číslované, odrážkové, kontrolní)</span><span class="sxs-lookup"><span data-stu-id="ea1ff-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="ea1ff-210">Číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="ea1ff-210">Numbered list</span></span>

<span data-ttu-id="ea1ff-211">Při vytváření číslovaného seznamu můžete všude použít jedničky (1), které se při publikování zobrazí jako sekvenční seznam.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="ea1ff-212">Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="ea1ff-213">Nepoužívejte v seznamech ani vnořených seznamech písmena.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="ea1ff-214">Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="ea1ff-215">Například:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="ea1ff-216">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-216">This renders as follows:</span></span>

1. <span data-ttu-id="ea1ff-217">Toto je</span><span class="sxs-lookup"><span data-stu-id="ea1ff-217">This is</span></span>
1. <span data-ttu-id="ea1ff-218">nadřazený číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="ea1ff-218">a parent numbered list</span></span>
   1. <span data-ttu-id="ea1ff-219">a toto je</span><span class="sxs-lookup"><span data-stu-id="ea1ff-219">and this is</span></span>
   1. <span data-ttu-id="ea1ff-220">vnořený číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="ea1ff-220">a nested numbered list</span></span>
1. <span data-ttu-id="ea1ff-221">(konec)</span><span class="sxs-lookup"><span data-stu-id="ea1ff-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="ea1ff-222">Seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="ea1ff-222">Bulleted list</span></span>

<span data-ttu-id="ea1ff-223">Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="ea1ff-224">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-224">This renders as follows:</span></span>

- <span data-ttu-id="ea1ff-225">Toto je</span><span class="sxs-lookup"><span data-stu-id="ea1ff-225">This is</span></span>
- <span data-ttu-id="ea1ff-226">nadřazený seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="ea1ff-226">a parent bulleted list</span></span>
  - <span data-ttu-id="ea1ff-227">a toto je</span><span class="sxs-lookup"><span data-stu-id="ea1ff-227">and this is</span></span>
  - <span data-ttu-id="ea1ff-228">vnořený seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="ea1ff-228">a nested bulleted list</span></span>
- <span data-ttu-id="ea1ff-229">Hotovo!</span><span class="sxs-lookup"><span data-stu-id="ea1ff-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="ea1ff-230">Kontrolní seznam</span><span class="sxs-lookup"><span data-stu-id="ea1ff-230">Checklist</span></span>

<span data-ttu-id="ea1ff-231">Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="ea1ff-232">Tento příklad se na webu docs.microsoft.com zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="ea1ff-233">List item 1</span><span class="sxs-lookup"><span data-stu-id="ea1ff-233">List item 1</span></span>
> * <span data-ttu-id="ea1ff-234">List item 2</span><span class="sxs-lookup"><span data-stu-id="ea1ff-234">List item 2</span></span>
> * <span data-ttu-id="ea1ff-235">List item 3</span><span class="sxs-lookup"><span data-stu-id="ea1ff-235">List item 3</span></span>

<span data-ttu-id="ea1ff-236">Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="ea1ff-237">Nepřidávejte do svých článků náhodné kontrolní seznamy.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="ea1ff-238">Akce dalšího kroku</span><span class="sxs-lookup"><span data-stu-id="ea1ff-238">Next step action</span></span>

<span data-ttu-id="ea1ff-239">K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="ea1ff-240">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="ea1ff-241">Například:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="ea1ff-242">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ea1ff-243">Informace o základním stylu</span><span class="sxs-lookup"><span data-stu-id="ea1ff-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="ea1ff-244">V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="ea1ff-245">Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="ea1ff-246">Definice oddílu</span><span class="sxs-lookup"><span data-stu-id="ea1ff-246">Section definition</span></span>

<span data-ttu-id="ea1ff-247"><!-- more info about this would be helpful! --> Je možné, že budete potřebovat nadefinovat oddíl.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="ea1ff-248">Tato syntaxe se nejčastěji používá pro tabulky kódu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="ea1ff-249">Prohlédněte si následující příklad:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="ea1ff-250">Předchozí text Markdownu blokové citace se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="ea1ff-251">Voliče</span><span class="sxs-lookup"><span data-stu-id="ea1ff-251">Selectors</span></span>

<span data-ttu-id="ea1ff-252"><!-- could be more clear! --> Selektor můžete použít, když chcete propojit různé stránky stejného článku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="ea1ff-253">Čtenáři pak můžou přepínat mezi těmito stránkami.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="ea1ff-254">Toto rozšíření funguje mezi weby docs.microsoft.com a MSDN různě.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="ea1ff-255">Jeden selektor</span><span class="sxs-lookup"><span data-stu-id="ea1ff-255">Single selector</span></span>

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

<span data-ttu-id="ea1ff-256">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="ea1ff-265">Vícenásobný selektor</span><span class="sxs-lookup"><span data-stu-id="ea1ff-265">Multi-selector</span></span>

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

<span data-ttu-id="ea1ff-266">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-266">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="ea1ff-277">Tables</span><span class="sxs-lookup"><span data-stu-id="ea1ff-277">Tables</span></span>

<span data-ttu-id="ea1ff-278">Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="ea1ff-279">Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="ea1ff-280">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-280">This renders as follows:</span></span>

|<span data-ttu-id="ea1ff-281">Toto je</span><span class="sxs-lookup"><span data-stu-id="ea1ff-281">This is</span></span>   |<span data-ttu-id="ea1ff-282">jednoduché</span><span class="sxs-lookup"><span data-stu-id="ea1ff-282">a simple</span></span>   |<span data-ttu-id="ea1ff-283">záhlaví tabulky</span><span class="sxs-lookup"><span data-stu-id="ea1ff-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="ea1ff-284">data</span><span class="sxs-lookup"><span data-stu-id="ea1ff-284">table</span></span>     |<span data-ttu-id="ea1ff-285">tabulky</span><span class="sxs-lookup"><span data-stu-id="ea1ff-285">data</span></span>       |<span data-ttu-id="ea1ff-286">zde</span><span class="sxs-lookup"><span data-stu-id="ea1ff-286">here</span></span>        |
|<span data-ttu-id="ea1ff-287">ani nemusí</span><span class="sxs-lookup"><span data-stu-id="ea1ff-287">it doesn't</span></span>|<span data-ttu-id="ea1ff-288">být pěkně</span><span class="sxs-lookup"><span data-stu-id="ea1ff-288">actually</span></span>   |<span data-ttu-id="ea1ff-289">zarovnaná!</span><span class="sxs-lookup"><span data-stu-id="ea1ff-289">have to line up nicely!</span></span>||

<span data-ttu-id="ea1ff-290">Můžete také vytvořit tabulku bez záhlaví.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-290">You can also create a table without a header.</span></span> <span data-ttu-id="ea1ff-291">Příklad vytvoření seznamu s více sloupci:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="ea1ff-292">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="ea1ff-293">Tato</span><span class="sxs-lookup"><span data-stu-id="ea1ff-293">This</span></span> | <span data-ttu-id="ea1ff-294">tabulka</span><span class="sxs-lookup"><span data-stu-id="ea1ff-294">table</span></span> |
| <span data-ttu-id="ea1ff-295">nemá žádné</span><span class="sxs-lookup"><span data-stu-id="ea1ff-295">has no</span></span> | <span data-ttu-id="ea1ff-296">záhlaví</span><span class="sxs-lookup"><span data-stu-id="ea1ff-296">header</span></span> |

<span data-ttu-id="ea1ff-297">Sloupce můžete zarovnat pomocí dvojtečky:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="ea1ff-298">Se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="ea1ff-299">zarovnání vpravo:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-299">right aligned:</span></span>|
|<span data-ttu-id="ea1ff-300">:zarovnání vlevo</span><span class="sxs-lookup"><span data-stu-id="ea1ff-300">:left aligned</span></span>     |
|<span data-ttu-id="ea1ff-301">:na střed        :</span><span class="sxs-lookup"><span data-stu-id="ea1ff-301">:centered        :</span></span>|

> [!TIP]
> Rozšíření pro vytváření obsahu na webu Docs pro VS Code usnadňuje přidávání základních tabulek Markdownu.
>
> Můžete také použít [online generátor tabulek](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="ea1ff-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="ea1ff-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Toto funguje jen na webu docs.microsoft.com.

<span data-ttu-id="ea1ff-306">Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="ea1ff-307">Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="ea1ff-308">Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="ea1ff-309">Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="ea1ff-310">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="ea1ff-311">Název</span><span class="sxs-lookup"><span data-stu-id="ea1ff-311">Name</span></span>|<span data-ttu-id="ea1ff-312">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea1ff-312">Syntax</span></span>|<span data-ttu-id="ea1ff-313">Povinné pro tichou instalaci?</span><span class="sxs-lookup"><span data-stu-id="ea1ff-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="ea1ff-314">Popis</span><span class="sxs-lookup"><span data-stu-id="ea1ff-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="ea1ff-315">Tichá instalace</span><span class="sxs-lookup"><span data-stu-id="ea1ff-315">Quiet</span></span>|<span data-ttu-id="ea1ff-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="ea1ff-316">/quiet</span></span>|<span data-ttu-id="ea1ff-317">Ano</span><span class="sxs-lookup"><span data-stu-id="ea1ff-317">Yes</span></span>|<span data-ttu-id="ea1ff-318">Spustí instalační program bez zobrazení uživatelského rozhraní a výzev.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="ea1ff-319">Bez restartování</span><span class="sxs-lookup"><span data-stu-id="ea1ff-319">NoRestart</span></span>|<span data-ttu-id="ea1ff-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="ea1ff-320">/norestart</span></span>|<span data-ttu-id="ea1ff-321">Ne</span><span class="sxs-lookup"><span data-stu-id="ea1ff-321">No</span></span>|<span data-ttu-id="ea1ff-322">Potlačí všechny pokusy o restartování.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="ea1ff-323">Ve výchozím nastavení zobrazí uživatelské rozhraní před restartováním výzvu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="ea1ff-324">Nápověda</span><span class="sxs-lookup"><span data-stu-id="ea1ff-324">Help</span></span>|<span data-ttu-id="ea1ff-325">/help</span><span class="sxs-lookup"><span data-stu-id="ea1ff-325">/help</span></span>|<span data-ttu-id="ea1ff-326">Ne</span><span class="sxs-lookup"><span data-stu-id="ea1ff-326">No</span></span>|<span data-ttu-id="ea1ff-327">Poskytuje nápovědu a stručné referenční informace.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-327">Provides help and quick reference.</span></span> <span data-ttu-id="ea1ff-328">Zobrazí správné použití příkazu instalace včetně seznamu všech možností a chování.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="ea1ff-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="ea1ff-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea1ff-330">Toto funguje jen na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="ea1ff-331">Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="ea1ff-332">Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="ea1ff-333">Tabulky HTML</span><span class="sxs-lookup"><span data-stu-id="ea1ff-333">HTML Tables</span></span>

<span data-ttu-id="ea1ff-334">Tabulky HTML se na webu docs.microsoft.com nedoporučují.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="ea1ff-335">Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="ea1ff-336">Videa</span><span class="sxs-lookup"><span data-stu-id="ea1ff-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="ea1ff-337">Vkládání videí na stránku Markdownu</span><span class="sxs-lookup"><span data-stu-id="ea1ff-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="ea1ff-338">Platforma Docs v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="ea1ff-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="ea1ff-339">YouTube</span></span>
- <span data-ttu-id="ea1ff-340">Channel9</span><span class="sxs-lookup"><span data-stu-id="ea1ff-340">Channel 9</span></span>
- <span data-ttu-id="ea1ff-341">Vlastní systém Microsoftu „One Player“</span><span class="sxs-lookup"><span data-stu-id="ea1ff-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="ea1ff-342">Můžete vložit video s následující syntaxí a Docs ho zobrazí.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="ea1ff-343">Příklad:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="ea1ff-344">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="ea1ff-345">A na publikovaných stránkách se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="ea1ff-346">Adresa URL videa CH9 by měla začínat řetězcem `https` a končit řetězcem `/player`.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="ea1ff-347">V opačném případě totiž místo samotného videa vloží celou stránku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="ea1ff-348">Nahrání nových videí</span><span class="sxs-lookup"><span data-stu-id="ea1ff-348">Uploading new videos</span></span>

<span data-ttu-id="ea1ff-349">Všechna nová videa by měla být nahrána následujícím postupem:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="ea1ff-350">Připojte se ke skupině **docs_video_users** na IDWEB.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="ea1ff-351">Přejděte na adresu https://aka.ms/VideoUploadRequest a vyplňte podrobnosti o videu.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="ea1ff-352">Budete potřebovat zadat tyto údaje (žádné z nich nebudou veřejně viditelné):</span><span class="sxs-lookup"><span data-stu-id="ea1ff-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="ea1ff-353">Název videa</span><span class="sxs-lookup"><span data-stu-id="ea1ff-353">A title for your video.</span></span>
    1. <span data-ttu-id="ea1ff-354">Seznam produktů/služeb, kterých se video týká</span><span class="sxs-lookup"><span data-stu-id="ea1ff-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="ea1ff-355">Cílová stránka nebo (pokud tuto stránku ještě nemáte) sada dokumentace, kde bude video hostované</span><span class="sxs-lookup"><span data-stu-id="ea1ff-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="ea1ff-356">Odkaz na soubor MP4 s videem (pokud ještě nevíte, kde bude soubor umístěný, můžete sem dočasně zadat: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="ea1ff-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="ea1ff-357">Soubory MP4 by měly mít rozlišení 720p nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="ea1ff-358">Popis videa</span><span class="sxs-lookup"><span data-stu-id="ea1ff-358">A description of the video.</span></span>
1. <span data-ttu-id="ea1ff-359">Odešlete (uložte) tuto položku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="ea1ff-360">Video se nahraje během dvou pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="ea1ff-361">Odkaz potřebný k vložení bude umístěn do pracovní položky, která vám bude *přeložena zpět*.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="ea1ff-362">Jakmile získáte odkaz na video, zavřete tuto pracovní položku.</span><span class="sxs-lookup"><span data-stu-id="ea1ff-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="ea1ff-363">Odkaz na video pak můžete přidat do příspěvku pomocí této syntaxe:</span><span class="sxs-lookup"><span data-stu-id="ea1ff-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
