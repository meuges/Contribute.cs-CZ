---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 3142b1aee8cadb69f82bfbcd3f89c701fac5b356
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288305"
---
# <a name="markdown-reference"></a><span data-ttu-id="8b261-103">Referenční informace k jazyku Markdown</span><span class="sxs-lookup"><span data-stu-id="8b261-103">Markdown Reference</span></span>

<span data-ttu-id="8b261-104">Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu.</span><span class="sxs-lookup"><span data-stu-id="8b261-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="8b261-105">Platforma Docs podporuje standard CommonMark pro Markdown plus několik vlastních rozšíření navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8b261-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="8b261-106">Tento článek obsahuje referenční informace o používání jazyka Markdown pro docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8b261-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="8b261-107">K vytváření Markdownu můžete použít libovolný textový editor.</span><span class="sxs-lookup"><span data-stu-id="8b261-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="8b261-108">Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření Docs, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="8b261-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="8b261-109">Web Docs používá modul Markdig Markdown.</span><span class="sxs-lookup"><span data-stu-id="8b261-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="8b261-110">Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="8b261-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="8b261-111">Výstrahy – Note (Poznámka), Tip, Important (Důležité), Caution (Pozor), Warning (Upozornění)</span><span class="sxs-lookup"><span data-stu-id="8b261-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="8b261-112">Výstrahy jsou rozšíření Docs Markdown určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu.</span><span class="sxs-lookup"><span data-stu-id="8b261-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="8b261-113">Podporují se následující typy výstrah:</span><span class="sxs-lookup"><span data-stu-id="8b261-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="8b261-114">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="8b261-115">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="8b261-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="8b261-116">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="8b261-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b261-117">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="8b261-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="8b261-118">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="8b261-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="8b261-119">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="8b261-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="8b261-120">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="8b261-120">Code snippets</span></span>

<span data-ttu-id="8b261-121">Do souborů Markdown můžete začlenit fragmenty kódu:</span><span class="sxs-lookup"><span data-stu-id="8b261-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="8b261-122">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="8b261-122">Headings</span></span>

<span data-ttu-id="8b261-123">Web Docs podporuje šest úrovní nadpisů Markdownu:</span><span class="sxs-lookup"><span data-stu-id="8b261-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="8b261-124">Mezi posledním symbolem `#` a textem nadpisu musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="8b261-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="8b261-125">Každý soubor Markdown musí mít právě jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="8b261-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="8b261-126">Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.</span><span class="sxs-lookup"><span data-stu-id="8b261-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="8b261-127">Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="8b261-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="8b261-128">Nadpisy nižších úrovní nikoli, proto nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.</span><span class="sxs-lookup"><span data-stu-id="8b261-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="8b261-129">Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="8b261-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="8b261-130">Odkazy na jednotlivé nadpisy v souboru můžete realizovat přes [záložky](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="8b261-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="8b261-131">HTML</span><span class="sxs-lookup"><span data-stu-id="8b261-131">HTML</span></span>

<span data-ttu-id="8b261-132">Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="8b261-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="8b261-133">Obrázky</span><span class="sxs-lookup"><span data-stu-id="8b261-133">Images</span></span>

<span data-ttu-id="8b261-134">Syntaxe pro začlenění obrázku:</span><span class="sxs-lookup"><span data-stu-id="8b261-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="8b261-135">`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="8b261-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="8b261-136">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="8b261-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="8b261-137">Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="8b261-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="8b261-138">Obrázky by měly být uložené ve složce `/media` v sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="8b261-139">Pro obrázky se standardně podporují tyto typy souborů:</span><span class="sxs-lookup"><span data-stu-id="8b261-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="8b261-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="8b261-140">.jpg</span></span>
- <span data-ttu-id="8b261-141">.png</span><span class="sxs-lookup"><span data-stu-id="8b261-141">.png</span></span>

<span data-ttu-id="8b261-142">Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json</span><span class="sxs-lookup"><span data-stu-id="8b261-142">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="8b261-143">pro sadu dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-143">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="8b261-144">Odkazy</span><span class="sxs-lookup"><span data-stu-id="8b261-144">Links</span></span>

<span data-ttu-id="8b261-145">Web Docs používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky.</span><span class="sxs-lookup"><span data-stu-id="8b261-145">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="8b261-146">Typy odkazů jsou popsané v níže uvedených pododdílech.</span><span class="sxs-lookup"><span data-stu-id="8b261-146">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="8b261-147">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span><span class="sxs-lookup"><span data-stu-id="8b261-147">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b261-148">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span><span class="sxs-lookup"><span data-stu-id="8b261-148">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="8b261-149">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span><span class="sxs-lookup"><span data-stu-id="8b261-149">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="8b261-150">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span><span class="sxs-lookup"><span data-stu-id="8b261-150">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="8b261-151">For example, use:</span><span class="sxs-lookup"><span data-stu-id="8b261-151">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="8b261-152">Not:</span><span class="sxs-lookup"><span data-stu-id="8b261-152">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="8b261-153">Relativní odkazy na soubory ve stejné sadě dokumentace</span><span class="sxs-lookup"><span data-stu-id="8b261-153">Relative links to files in the same doc set</span></span>

<span data-ttu-id="8b261-154">Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru.</span><span class="sxs-lookup"><span data-stu-id="8b261-154">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="8b261-155">Na webu Docs můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-155">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="8b261-156">Relativní cesta má následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="8b261-156">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="8b261-157">`../` označuje jednu úroveň výše v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="8b261-157">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="8b261-158">Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.</span><span class="sxs-lookup"><span data-stu-id="8b261-158">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="8b261-159">K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-159">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="8b261-160">Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-160">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="8b261-161">Web Docs podporuje také speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="8b261-161">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="8b261-162">Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-162">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="8b261-163">Během sestavování se ověří a přeloží i tento druh cesty.</span><span class="sxs-lookup"><span data-stu-id="8b261-163">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b261-164">Include the file extension in the relative path.</span><span class="sxs-lookup"><span data-stu-id="8b261-164">Include the file extension in the relative path.</span></span> <span data-ttu-id="8b261-165">Build validates the existence of the target file of that relative path.</span><span class="sxs-lookup"><span data-stu-id="8b261-165">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="8b261-166">If relative path does not include file extension, it is likely build will report a warning of broken link.</span><span class="sxs-lookup"><span data-stu-id="8b261-166">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="8b261-167">For example, use:</span><span class="sxs-lookup"><span data-stu-id="8b261-167">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="8b261-168">Not:</span><span class="sxs-lookup"><span data-stu-id="8b261-168">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="8b261-169">Relativní odkazy na jiné soubory na webu Docs</span><span class="sxs-lookup"><span data-stu-id="8b261-169">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="8b261-170">Nezačleňujte příponu souboru (.md).</span><span class="sxs-lookup"><span data-stu-id="8b261-170">Do not include the file extension (.md).</span></span> <span data-ttu-id="8b261-171">Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.</span><span class="sxs-lookup"><span data-stu-id="8b261-171">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="8b261-172">Odkazy na externí weby</span><span class="sxs-lookup"><span data-stu-id="8b261-172">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="8b261-173">Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).</span><span class="sxs-lookup"><span data-stu-id="8b261-173">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="8b261-174">Odkazy na záložky</span><span class="sxs-lookup"><span data-stu-id="8b261-174">Bookmark links</span></span>

<span data-ttu-id="8b261-175">Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti.</span><span class="sxs-lookup"><span data-stu-id="8b261-175">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="8b261-176">Například:</span><span class="sxs-lookup"><span data-stu-id="8b261-176">For example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="8b261-177">Odkaz na záložku u nadpisu v aktuálním souboru:</span><span class="sxs-lookup"><span data-stu-id="8b261-177">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="8b261-178">Použijte znak hash (`#`) a za ním slova nadpisu.</span><span class="sxs-lookup"><span data-stu-id="8b261-178">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="8b261-179">Pokud chcete změnit text nadpisu na text odkazu:</span><span class="sxs-lookup"><span data-stu-id="8b261-179">To change the heading text into link text:</span></span>
- <span data-ttu-id="8b261-180">Použijte jenom malá písmena.</span><span class="sxs-lookup"><span data-stu-id="8b261-180">Use all lowercase characters</span></span>
- <span data-ttu-id="8b261-181">Odeberte interpunkci.</span><span class="sxs-lookup"><span data-stu-id="8b261-181">Remove punctuation</span></span>
- <span data-ttu-id="8b261-182">Nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="8b261-182">Replace spaces with dashes</span></span>

<span data-ttu-id="8b261-183">Pokud máte například nadpis „2.2 Otázky zabezpečení“, pak text odkazu na záložku bude „#22-otázky-zabezpečení“.</span><span class="sxs-lookup"><span data-stu-id="8b261-183">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="8b261-184">Explicitní odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="8b261-184">Explicit anchor links</span></span>

<span data-ttu-id="8b261-185">Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek.</span><span class="sxs-lookup"><span data-stu-id="8b261-185">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="8b261-186">V obecných souborech Markdown použijte výše popsané záložky.</span><span class="sxs-lookup"><span data-stu-id="8b261-186">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="8b261-187">Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="8b261-187">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="8b261-188">`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="8b261-188">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="8b261-189">Pro odkaz na explicitní ukotvení použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="8b261-189">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="8b261-190">Křížové odkazy XREF</span><span class="sxs-lookup"><span data-stu-id="8b261-190">XREF (cross reference) links</span></span>

<span data-ttu-id="8b261-191">K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).</span><span class="sxs-lookup"><span data-stu-id="8b261-191">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="8b261-192">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span><span class="sxs-lookup"><span data-stu-id="8b261-192">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="8b261-193">Identifikátor odpovídá plně kvalifikované třídě a názvu člena.</span><span class="sxs-lookup"><span data-stu-id="8b261-193">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="8b261-194">Pokud za UID přidáte \*, představuje tento odkaz stránku přetížení, nikoli konkrétní rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="8b261-194">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="8b261-195">`List<T>.BinarySearch*` použijte například k odkazu na stránku metody BinarySearch místo odkazu na konkrétní přetížení, jako je `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="8b261-195">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="8b261-196">Můžete použít jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="8b261-196">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="8b261-197">Automatický odkaz: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="8b261-197">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="8b261-198">Nepovinný parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu.</span><span class="sxs-lookup"><span data-stu-id="8b261-198">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="8b261-199">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="8b261-199">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="8b261-200">Odkaz Markdownu: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="8b261-200">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="8b261-201">Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="8b261-201">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="8b261-202">Příklady:</span><span class="sxs-lookup"><span data-stu-id="8b261-202">Examples:</span></span>

- <span data-ttu-id="8b261-203">`<xref:System.String>` se zobrazí jako „String“.</span><span class="sxs-lookup"><span data-stu-id="8b261-203">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="8b261-204">`<xref:System.String?displayProperty=nameWithType>` se zobrazí jako „System.String“.</span><span class="sxs-lookup"><span data-stu-id="8b261-204">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="8b261-205">`[String class](xref:System.String)` se zobrazí jako „třída String“.</span><span class="sxs-lookup"><span data-stu-id="8b261-205">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="8b261-206">V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID.</span><span class="sxs-lookup"><span data-stu-id="8b261-206">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="8b261-207">Nejlepším způsobem, jak najít identifikátor UID pro rozhraní API, je zobrazit zdroj stránky API, kterou chcete propojit, a najít hodnotu ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="8b261-207">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="8b261-208">Hodnoty jednotlivých přetížení se ve zdroji nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="8b261-208">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="8b261-209">Pracujeme na tom, abychom v budoucnu měli lepší systém.</span><span class="sxs-lookup"><span data-stu-id="8b261-209">We're working on having a better system in the future.</span></span>

<span data-ttu-id="8b261-210">Pokud UID obsahuje speciální znaky \`, \# nebo \*, musí být hodnota UID uvedena ve formátu HTML `%60`, `%23` a `%2A` v uvedeném pořadí.</span><span class="sxs-lookup"><span data-stu-id="8b261-210">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="8b261-211">Někdy v tomto formátu uvidíte i závorky, není to ale povinné.</span><span class="sxs-lookup"><span data-stu-id="8b261-211">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="8b261-212">Příklady:</span><span class="sxs-lookup"><span data-stu-id="8b261-212">Examples:</span></span>

- <span data-ttu-id="8b261-213">System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.</span><span class="sxs-lookup"><span data-stu-id="8b261-213">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="8b261-214">System.Exception.\#ctor se změní na `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="8b261-214">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="8b261-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="8b261-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="8b261-216">Seznamy (číslované, odrážkové, kontrolní)</span><span class="sxs-lookup"><span data-stu-id="8b261-216">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="8b261-217">Číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="8b261-217">Numbered list</span></span>

<span data-ttu-id="8b261-218">Při vytváření číslovaného seznamu můžete všude použít jedničky (1), které se při publikování zobrazí jako sekvenční seznam.</span><span class="sxs-lookup"><span data-stu-id="8b261-218">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="8b261-219">Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat.</span><span class="sxs-lookup"><span data-stu-id="8b261-219">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="8b261-220">Nepoužívejte v seznamech ani vnořených seznamech písmena.</span><span class="sxs-lookup"><span data-stu-id="8b261-220">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="8b261-221">Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena.</span><span class="sxs-lookup"><span data-stu-id="8b261-221">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="8b261-222">Například:</span><span class="sxs-lookup"><span data-stu-id="8b261-222">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="8b261-223">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-223">This renders as follows:</span></span>

1. <span data-ttu-id="8b261-224">This is</span><span class="sxs-lookup"><span data-stu-id="8b261-224">This is</span></span>
1. <span data-ttu-id="8b261-225">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="8b261-225">a parent numbered list</span></span>
   1. <span data-ttu-id="8b261-226">and this is</span><span class="sxs-lookup"><span data-stu-id="8b261-226">and this is</span></span>
   1. <span data-ttu-id="8b261-227">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="8b261-227">a nested numbered list</span></span>
1. <span data-ttu-id="8b261-228">(fin)</span><span class="sxs-lookup"><span data-stu-id="8b261-228">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="8b261-229">Seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="8b261-229">Bulleted list</span></span>

<span data-ttu-id="8b261-230">Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:</span><span class="sxs-lookup"><span data-stu-id="8b261-230">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="8b261-231">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-231">This renders as follows:</span></span>

- <span data-ttu-id="8b261-232">This is</span><span class="sxs-lookup"><span data-stu-id="8b261-232">This is</span></span>
- <span data-ttu-id="8b261-233">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="8b261-233">a parent bulleted list</span></span>
  - <span data-ttu-id="8b261-234">and this is</span><span class="sxs-lookup"><span data-stu-id="8b261-234">and this is</span></span>
  - <span data-ttu-id="8b261-235">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="8b261-235">a nested bulleted list</span></span>
- <span data-ttu-id="8b261-236">All done!</span><span class="sxs-lookup"><span data-stu-id="8b261-236">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="8b261-237">Kontrolní seznam</span><span class="sxs-lookup"><span data-stu-id="8b261-237">Checklist</span></span>

<span data-ttu-id="8b261-238">Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:</span><span class="sxs-lookup"><span data-stu-id="8b261-238">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="8b261-239">Tento příklad se na webu docs.microsoft.com zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-239">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="8b261-240">List item 1</span><span class="sxs-lookup"><span data-stu-id="8b261-240">List item 1</span></span>
> * <span data-ttu-id="8b261-241">List item 2</span><span class="sxs-lookup"><span data-stu-id="8b261-241">List item 2</span></span>
> * <span data-ttu-id="8b261-242">List item 3</span><span class="sxs-lookup"><span data-stu-id="8b261-242">List item 3</span></span>

<span data-ttu-id="8b261-243">Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku.</span><span class="sxs-lookup"><span data-stu-id="8b261-243">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="8b261-244">Nepřidávejte do svých článků náhodné kontrolní seznamy.</span><span class="sxs-lookup"><span data-stu-id="8b261-244">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="8b261-245">Akce dalšího kroku</span><span class="sxs-lookup"><span data-stu-id="8b261-245">Next step action</span></span>

<span data-ttu-id="8b261-246">K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.</span><span class="sxs-lookup"><span data-stu-id="8b261-246">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="8b261-247">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="8b261-247">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="8b261-248">Například:</span><span class="sxs-lookup"><span data-stu-id="8b261-248">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="8b261-249">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-249">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8b261-250">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="8b261-250">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="8b261-251">V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku.</span><span class="sxs-lookup"><span data-stu-id="8b261-251">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="8b261-252">Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="8b261-252">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="8b261-253">Definice oddílu</span><span class="sxs-lookup"><span data-stu-id="8b261-253">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="8b261-254">Je možné, že budete potřebovat nadefinovat oddíl.</span><span class="sxs-lookup"><span data-stu-id="8b261-254">You might need to define a section.</span></span> <span data-ttu-id="8b261-255">Tato syntaxe se nejčastěji používá pro tabulky kódu.</span><span class="sxs-lookup"><span data-stu-id="8b261-255">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="8b261-256">Prohlédněte si následující příklad:</span><span class="sxs-lookup"><span data-stu-id="8b261-256">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="8b261-257">Předchozí text Markdownu blokové citace se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-257">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="8b261-258">Voliče</span><span class="sxs-lookup"><span data-stu-id="8b261-258">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="8b261-259">Volič neboli selektor můžete použít, když chcete připojit různé stránky pro stejný článek.</span><span class="sxs-lookup"><span data-stu-id="8b261-259">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="8b261-260">Čtenáři pak můžou přepínat mezi těmito stránkami.</span><span class="sxs-lookup"><span data-stu-id="8b261-260">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="8b261-261">This extension works differently between docs.microsoft.com and MSDN.</span><span class="sxs-lookup"><span data-stu-id="8b261-261">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="8b261-262">Jeden selektor</span><span class="sxs-lookup"><span data-stu-id="8b261-262">Single selector</span></span>

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

<span data-ttu-id="8b261-263">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-263">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="8b261-272">Vícenásobný selektor</span><span class="sxs-lookup"><span data-stu-id="8b261-272">Multi-selector</span></span>

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

<span data-ttu-id="8b261-273">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-273">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platforma" title2="Back-end"]
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

## <a name="tables"></a><span data-ttu-id="8b261-286">Tabulky</span><span class="sxs-lookup"><span data-stu-id="8b261-286">Tables</span></span>

<span data-ttu-id="8b261-287">Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky.</span><span class="sxs-lookup"><span data-stu-id="8b261-287">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="8b261-288">Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:</span><span class="sxs-lookup"><span data-stu-id="8b261-288">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="8b261-289">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-289">This renders as follows:</span></span>

|<span data-ttu-id="8b261-290">This is</span><span class="sxs-lookup"><span data-stu-id="8b261-290">This is</span></span>   |<span data-ttu-id="8b261-291">a simple</span><span class="sxs-lookup"><span data-stu-id="8b261-291">a simple</span></span>   |<span data-ttu-id="8b261-292">table header</span><span class="sxs-lookup"><span data-stu-id="8b261-292">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="8b261-293">table</span><span class="sxs-lookup"><span data-stu-id="8b261-293">table</span></span>     |<span data-ttu-id="8b261-294">data</span><span class="sxs-lookup"><span data-stu-id="8b261-294">data</span></span>       |<span data-ttu-id="8b261-295">here</span><span class="sxs-lookup"><span data-stu-id="8b261-295">here</span></span>        |
|<span data-ttu-id="8b261-296">it doesn't</span><span class="sxs-lookup"><span data-stu-id="8b261-296">it doesn't</span></span>|<span data-ttu-id="8b261-297">actually</span><span class="sxs-lookup"><span data-stu-id="8b261-297">actually</span></span>   |<span data-ttu-id="8b261-298">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="8b261-298">have to line up nicely!</span></span>||

<span data-ttu-id="8b261-299">Můžete také vytvořit tabulku bez záhlaví.</span><span class="sxs-lookup"><span data-stu-id="8b261-299">You can also create a table without a header.</span></span> <span data-ttu-id="8b261-300">Příklad vytvoření seznamu s více sloupci:</span><span class="sxs-lookup"><span data-stu-id="8b261-300">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="8b261-301">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-301">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="8b261-302">This</span><span class="sxs-lookup"><span data-stu-id="8b261-302">This</span></span> | <span data-ttu-id="8b261-303">table</span><span class="sxs-lookup"><span data-stu-id="8b261-303">table</span></span> |
| <span data-ttu-id="8b261-304">has no</span><span class="sxs-lookup"><span data-stu-id="8b261-304">has no</span></span> | <span data-ttu-id="8b261-305">header</span><span class="sxs-lookup"><span data-stu-id="8b261-305">header</span></span> |

<span data-ttu-id="8b261-306">Sloupce můžete zarovnat pomocí dvojtečky:</span><span class="sxs-lookup"><span data-stu-id="8b261-306">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="8b261-307">Se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-307">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="8b261-308">right aligned:</span><span class="sxs-lookup"><span data-stu-id="8b261-308">right aligned:</span></span>|
|<span data-ttu-id="8b261-309">:left aligned</span><span class="sxs-lookup"><span data-stu-id="8b261-309">:left aligned</span></span>     |
|<span data-ttu-id="8b261-310">:centered        :</span><span class="sxs-lookup"><span data-stu-id="8b261-310">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="8b261-311">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span><span class="sxs-lookup"><span data-stu-id="8b261-311">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="8b261-312">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="8b261-312">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="8b261-313">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="8b261-313">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b261-314">This only works on the docs.microsoft.com site.</span><span class="sxs-lookup"><span data-stu-id="8b261-314">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="8b261-315">Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou.</span><span class="sxs-lookup"><span data-stu-id="8b261-315">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="8b261-316">Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit.</span><span class="sxs-lookup"><span data-stu-id="8b261-316">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="8b261-317">Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="8b261-317">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="8b261-318">Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="8b261-318">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="8b261-319">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-319">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="8b261-320">Name</span><span class="sxs-lookup"><span data-stu-id="8b261-320">Name</span></span>|<span data-ttu-id="8b261-321">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b261-321">Syntax</span></span>|<span data-ttu-id="8b261-322">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="8b261-322">Mandatory for silent installation?</span></span>|<span data-ttu-id="8b261-323">Description</span><span class="sxs-lookup"><span data-stu-id="8b261-323">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="8b261-324">Quiet</span><span class="sxs-lookup"><span data-stu-id="8b261-324">Quiet</span></span>|<span data-ttu-id="8b261-325">/quiet</span><span class="sxs-lookup"><span data-stu-id="8b261-325">/quiet</span></span>|<span data-ttu-id="8b261-326">Yes</span><span class="sxs-lookup"><span data-stu-id="8b261-326">Yes</span></span>|<span data-ttu-id="8b261-327">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="8b261-327">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="8b261-328">NoRestart</span><span class="sxs-lookup"><span data-stu-id="8b261-328">NoRestart</span></span>|<span data-ttu-id="8b261-329">/norestart</span><span class="sxs-lookup"><span data-stu-id="8b261-329">/norestart</span></span>|<span data-ttu-id="8b261-330">No</span><span class="sxs-lookup"><span data-stu-id="8b261-330">No</span></span>|<span data-ttu-id="8b261-331">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="8b261-331">Suppresses any attempts to restart.</span></span> <span data-ttu-id="8b261-332">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="8b261-332">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="8b261-333">Help</span><span class="sxs-lookup"><span data-stu-id="8b261-333">Help</span></span>|<span data-ttu-id="8b261-334">/help</span><span class="sxs-lookup"><span data-stu-id="8b261-334">/help</span></span>|<span data-ttu-id="8b261-335">No</span><span class="sxs-lookup"><span data-stu-id="8b261-335">No</span></span>|<span data-ttu-id="8b261-336">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="8b261-336">Provides help and quick reference.</span></span> <span data-ttu-id="8b261-337">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="8b261-337">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="8b261-338">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="8b261-338">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b261-339">This only works on the docs.microsoft.com site.</span><span class="sxs-lookup"><span data-stu-id="8b261-339">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="8b261-340">Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova.</span><span class="sxs-lookup"><span data-stu-id="8b261-340">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="8b261-341">Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.</span><span class="sxs-lookup"><span data-stu-id="8b261-341">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="8b261-342">Tabulky HTML</span><span class="sxs-lookup"><span data-stu-id="8b261-342">HTML Tables</span></span>

<span data-ttu-id="8b261-343">Tabulky HTML se na webu docs.microsoft.com nedoporučují.</span><span class="sxs-lookup"><span data-stu-id="8b261-343">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="8b261-344">Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.</span><span class="sxs-lookup"><span data-stu-id="8b261-344">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="8b261-345">Videa</span><span class="sxs-lookup"><span data-stu-id="8b261-345">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="8b261-346">Vkládání videí na stránku Markdownu</span><span class="sxs-lookup"><span data-stu-id="8b261-346">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="8b261-347">Platforma Docs v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:</span><span class="sxs-lookup"><span data-stu-id="8b261-347">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="8b261-348">YouTube</span><span class="sxs-lookup"><span data-stu-id="8b261-348">YouTube</span></span>
- <span data-ttu-id="8b261-349">Channel9</span><span class="sxs-lookup"><span data-stu-id="8b261-349">Channel 9</span></span>
- <span data-ttu-id="8b261-350">Vlastní systém Microsoftu „One Player“</span><span class="sxs-lookup"><span data-stu-id="8b261-350">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="8b261-351">Můžete vložit video s následující syntaxí a Docs ho zobrazí.</span><span class="sxs-lookup"><span data-stu-id="8b261-351">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="8b261-352">Příklad:</span><span class="sxs-lookup"><span data-stu-id="8b261-352">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="8b261-353">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-353">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="8b261-354">A na publikovaných stránkách se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="8b261-354">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="8b261-355">The CH9 video URL should start with `https` and end with `/player`.</span><span class="sxs-lookup"><span data-stu-id="8b261-355">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="8b261-356">Otherwise, it will embed the whole page instead of the video only.</span><span class="sxs-lookup"><span data-stu-id="8b261-356">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="8b261-357">Nahrání nových videí</span><span class="sxs-lookup"><span data-stu-id="8b261-357">Uploading new videos</span></span>

<span data-ttu-id="8b261-358">Všechna nová videa by měla být nahrána následujícím postupem:</span><span class="sxs-lookup"><span data-stu-id="8b261-358">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="8b261-359">Připojte se ke skupině **docs_video_users** na IDWEB.</span><span class="sxs-lookup"><span data-stu-id="8b261-359">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="8b261-360">Přejděte na adresu https://aka.ms/VideoUploadRequest a vyplňte podrobnosti o videu.</span><span class="sxs-lookup"><span data-stu-id="8b261-360">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="8b261-361">Budete potřebovat zadat tyto údaje (žádné z nich nebudou veřejně viditelné):</span><span class="sxs-lookup"><span data-stu-id="8b261-361">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="8b261-362">Název videa</span><span class="sxs-lookup"><span data-stu-id="8b261-362">A title for your video.</span></span>
    1. <span data-ttu-id="8b261-363">Seznam produktů/služeb, kterých se video týká</span><span class="sxs-lookup"><span data-stu-id="8b261-363">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="8b261-364">Cílová stránka nebo (pokud tuto stránku ještě nemáte) sada dokumentace, kde bude video hostované</span><span class="sxs-lookup"><span data-stu-id="8b261-364">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="8b261-365">Odkaz na soubor MP4 s videem (pokud ještě nevíte, kde bude soubor umístěný, můžete sem dočasně zadat: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="8b261-365">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="8b261-366">Soubory MP4 by měly mít rozlišení 720p nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="8b261-366">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="8b261-367">Popis videa</span><span class="sxs-lookup"><span data-stu-id="8b261-367">A description of the video.</span></span>
1. <span data-ttu-id="8b261-368">Odešlete (uložte) tuto položku.</span><span class="sxs-lookup"><span data-stu-id="8b261-368">Submit (save) that item.</span></span>
1. <span data-ttu-id="8b261-369">Video se nahraje během dvou pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="8b261-369">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="8b261-370">Odkaz potřebný k vložení bude umístěn do pracovní položky, která vám bude *přeložena zpět*.</span><span class="sxs-lookup"><span data-stu-id="8b261-370">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="8b261-371">Jakmile získáte odkaz na video, zavřete tuto pracovní položku.</span><span class="sxs-lookup"><span data-stu-id="8b261-371">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="8b261-372">Odkaz na video pak můžete přidat do příspěvku pomocí této syntaxe:</span><span class="sxs-lookup"><span data-stu-id="8b261-372">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
