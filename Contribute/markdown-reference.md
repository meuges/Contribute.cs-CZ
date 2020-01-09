---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: 452cbf97db748532ae2b0e09b4bb558c8f757a61
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188269"
---
# <a name="markdown-reference"></a><span data-ttu-id="84a5c-103">Referenční informace k jazyku Markdown</span><span class="sxs-lookup"><span data-stu-id="84a5c-103">Markdown Reference</span></span>

<span data-ttu-id="84a5c-104">Markdown je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="84a5c-105">Platforma Docs podporuje standard CommonMark pro Markdown plus několik vlastních rozšíření navržených kvůli poskytování bohatšího obsahu na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="84a5c-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="84a5c-106">Tento článek obsahuje referenční informace o používání jazyka Markdown pro docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="84a5c-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="84a5c-107">K vytváření Markdownu můžete použít libovolný textový editor.</span><span class="sxs-lookup"><span data-stu-id="84a5c-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="84a5c-108">Jako editor, který umožňuje vkládání standardní syntaxe Markdownu i vlastních rozšíření Docs, doporučujeme [VS Code](https://code.visualstudio.com/) s nainstalovaným [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="84a5c-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="84a5c-109">Web Docs používá modul Markdig Markdown.</span><span class="sxs-lookup"><span data-stu-id="84a5c-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="84a5c-110">Zobrazení Markdownu v Markdigu v porovnání s jinými moduly můžete otestovat na adrese [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="84a5c-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="84a5c-111">Výstrahy – Note (Poznámka), Tip, Important (Důležité), Caution (Pozor), Warning (Upozornění)</span><span class="sxs-lookup"><span data-stu-id="84a5c-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="84a5c-112">Výstrahy jsou rozšíření Docs Markdown určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="84a5c-113">Podporují se následující typy výstrah:</span><span class="sxs-lookup"><span data-stu-id="84a5c-113">The following alert types are supported:</span></span>

```md
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

<span data-ttu-id="84a5c-114">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-114">These alerts look like this on docs.microsoft.com:</span></span>

![Ukazuje, jak výstrahy v předchozím příkladu vypadají na publikované stránce Docs s různými ikonami a barvami.](media/alerts-rendering.png)

## <a name="code-snippets"></a><span data-ttu-id="84a5c-116">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="84a5c-116">Code snippets</span></span>

<span data-ttu-id="84a5c-117">Do souborů Markdown můžete začlenit fragmenty kódu:</span><span class="sxs-lookup"><span data-stu-id="84a5c-117">You can embed code snippets in your Markdown files:</span></span>

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="84a5c-118">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="84a5c-118">Headings</span></span>

<span data-ttu-id="84a5c-119">Web Docs podporuje šest úrovní nadpisů Markdownu:</span><span class="sxs-lookup"><span data-stu-id="84a5c-119">Docs supports six levels of Markdown headings:</span></span>

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="84a5c-120">Mezi posledním symbolem `#` a textem nadpisu musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="84a5c-120">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="84a5c-121">Každý soubor Markdown musí mít právě jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="84a5c-121">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="84a5c-122">Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.</span><span class="sxs-lookup"><span data-stu-id="84a5c-122">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="84a5c-123">Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="84a5c-123">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="84a5c-124">Nadpisy nižších úrovní nikoli, proto nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-124">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="84a5c-125">Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění sestavení.</span><span class="sxs-lookup"><span data-stu-id="84a5c-125">HTML headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="84a5c-126">Odkazy na jednotlivé nadpisy v souboru můžete realizovat přes [záložky](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="84a5c-126">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="84a5c-127">HTML</span><span class="sxs-lookup"><span data-stu-id="84a5c-127">HTML</span></span>

<span data-ttu-id="84a5c-128">Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="84a5c-128">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="84a5c-129">Obrázky</span><span class="sxs-lookup"><span data-stu-id="84a5c-129">Images</span></span>

<span data-ttu-id="84a5c-130">Syntaxe pro začlenění obrázku:</span><span class="sxs-lookup"><span data-stu-id="84a5c-130">The syntax to include an image is:</span></span>

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="84a5c-131">`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-131">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="84a5c-132">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-132">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="84a5c-133">Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="84a5c-133">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="84a5c-134">Obrázky by měly být uložené ve složce `/media` v sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-134">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="84a5c-135">Pro obrázky se standardně podporují tyto typy souborů:</span><span class="sxs-lookup"><span data-stu-id="84a5c-135">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="84a5c-136">.jpg</span><span class="sxs-lookup"><span data-stu-id="84a5c-136">.jpg</span></span>
- <span data-ttu-id="84a5c-137">.png</span><span class="sxs-lookup"><span data-stu-id="84a5c-137">.png</span></span>

<span data-ttu-id="84a5c-138">Podporu jiných typů obrázků doplníte tak, že je přidáte jako prostředky do souboru docfx.json</span><span class="sxs-lookup"><span data-stu-id="84a5c-138">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="84a5c-139">pro sadu dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-139">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="84a5c-140">Odkazy</span><span class="sxs-lookup"><span data-stu-id="84a5c-140">Links</span></span>

<span data-ttu-id="84a5c-141">Web Docs používá ve většině případů standardní odkazy Markdownu na jiné soubory a stránky.</span><span class="sxs-lookup"><span data-stu-id="84a5c-141">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="84a5c-142">Typy odkazů jsou popsané v níže uvedených pododdílech.</span><span class="sxs-lookup"><span data-stu-id="84a5c-142">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="84a5c-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span><span class="sxs-lookup"><span data-stu-id="84a5c-143">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84a5c-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span><span class="sxs-lookup"><span data-stu-id="84a5c-144">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="84a5c-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span><span class="sxs-lookup"><span data-stu-id="84a5c-145">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="84a5c-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span><span class="sxs-lookup"><span data-stu-id="84a5c-146">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="84a5c-147">For example, use:</span><span class="sxs-lookup"><span data-stu-id="84a5c-147">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="84a5c-148">Not:</span><span class="sxs-lookup"><span data-stu-id="84a5c-148">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="84a5c-149">Relativní odkazy na soubory ve stejné sadě dokumentace</span><span class="sxs-lookup"><span data-stu-id="84a5c-149">Relative links to files in the same doc set</span></span>

<span data-ttu-id="84a5c-150">Relativní cesta je cesta k cílovému souboru relativní vzhledem k aktuálnímu souboru.</span><span class="sxs-lookup"><span data-stu-id="84a5c-150">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="84a5c-151">Na webu Docs můžete použít relativní cestu k odkazu na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-151">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="84a5c-152">Relativní cesta má následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="84a5c-152">The syntax for a relative path is as follows:</span></span>

```md
[link text](../../folder/filename.md)
```

<span data-ttu-id="84a5c-153">`../` označuje jednu úroveň výše v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="84a5c-153">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="84a5c-154">Relativní cesta se přeloží během sestavování včetně odebrání přípony .md.</span><span class="sxs-lookup"><span data-stu-id="84a5c-154">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="84a5c-155">K odkazování na soubor v nadřazené složce můžete použít ../, tento soubor ale musí být ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-155">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="84a5c-156">Řetězec ../ nemůžete použít k odkazování na soubor v jiné složce se sadou dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-156">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="84a5c-157">Web Docs podporuje také speciální formu relativní cesty začínající na ~ (například ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="84a5c-157">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="84a5c-158">Tato syntaxe označuje soubor relativní vzhledem ke kořenové složce sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-158">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="84a5c-159">Během sestavování se ověří a přeloží i tento druh cesty.</span><span class="sxs-lookup"><span data-stu-id="84a5c-159">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84a5c-160">Include the file extension in the relative path.</span><span class="sxs-lookup"><span data-stu-id="84a5c-160">Include the file extension in the relative path.</span></span> <span data-ttu-id="84a5c-161">Build validates the existence of the target file of that relative path.</span><span class="sxs-lookup"><span data-stu-id="84a5c-161">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="84a5c-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span><span class="sxs-lookup"><span data-stu-id="84a5c-162">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="84a5c-163">For example, use:</span><span class="sxs-lookup"><span data-stu-id="84a5c-163">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="84a5c-164">Not:</span><span class="sxs-lookup"><span data-stu-id="84a5c-164">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="84a5c-165">Relativní odkazy na jiné soubory na webu Docs</span><span class="sxs-lookup"><span data-stu-id="84a5c-165">Site relative links to other files on Docs</span></span>

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="84a5c-166">Nezačleňujte příponu souboru (.md).</span><span class="sxs-lookup"><span data-stu-id="84a5c-166">Do not include the file extension (.md).</span></span> <span data-ttu-id="84a5c-167">Odkazuje na přehledový soubor Linuxu vně sady dokumentace s články Azure.</span><span class="sxs-lookup"><span data-stu-id="84a5c-167">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="84a5c-168">Odkazy na externí weby</span><span class="sxs-lookup"><span data-stu-id="84a5c-168">Links to external sites</span></span>

```md
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="84a5c-169">Odkaz na jinou webovou stránku založený na adrese URL (musí obsahovat https://).</span><span class="sxs-lookup"><span data-stu-id="84a5c-169">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="84a5c-170">Odkazy na záložky</span><span class="sxs-lookup"><span data-stu-id="84a5c-170">Bookmark links</span></span>

<span data-ttu-id="84a5c-171">Odkaz na záložku u nadpisu v jiném souboru ve stejném úložišti.</span><span class="sxs-lookup"><span data-stu-id="84a5c-171">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="84a5c-172">Například:</span><span class="sxs-lookup"><span data-stu-id="84a5c-172">For example:</span></span>

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="84a5c-173">Odkaz na záložku u nadpisu v aktuálním souboru:</span><span class="sxs-lookup"><span data-stu-id="84a5c-173">Bookmark link to a heading in the current file:</span></span>

```md
[Managed Disks](#managed-disks)
```

<span data-ttu-id="84a5c-174">Použijte znak hash (`#`) a za ním slova nadpisu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-174">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="84a5c-175">Pokud chcete změnit text nadpisu na text odkazu:</span><span class="sxs-lookup"><span data-stu-id="84a5c-175">To change the heading text into link text:</span></span>
- <span data-ttu-id="84a5c-176">Použijte jenom malá písmena.</span><span class="sxs-lookup"><span data-stu-id="84a5c-176">Use all lowercase characters</span></span>
- <span data-ttu-id="84a5c-177">Odeberte interpunkci.</span><span class="sxs-lookup"><span data-stu-id="84a5c-177">Remove punctuation</span></span>
- <span data-ttu-id="84a5c-178">Nahraďte mezery pomlčkami.</span><span class="sxs-lookup"><span data-stu-id="84a5c-178">Replace spaces with dashes</span></span>

<span data-ttu-id="84a5c-179">Pokud máte například nadpis „2.2 Otázky zabezpečení“, pak text odkazu na záložku bude „#22-otázky-zabezpečení“.</span><span class="sxs-lookup"><span data-stu-id="84a5c-179">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="84a5c-180">Explicitní odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="84a5c-180">Explicit anchor links</span></span>

<span data-ttu-id="84a5c-181">Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML **nejsou povinné ani doporučené** s výjimkou centra a cílových stránek.</span><span class="sxs-lookup"><span data-stu-id="84a5c-181">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="84a5c-182">V obecných souborech Markdown použijte výše popsané záložky.</span><span class="sxs-lookup"><span data-stu-id="84a5c-182">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="84a5c-183">Pro centrum a cílové stránky použijte ukotvení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="84a5c-183">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="84a5c-184">`## <a id="AnchorText"> </a>Header text` nebo `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="84a5c-184">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="84a5c-185">Pro odkaz na explicitní ukotvení použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="84a5c-185">To link to explicit anchors, use the following syntax:</span></span>

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="84a5c-186">Křížové odkazy XREF</span><span class="sxs-lookup"><span data-stu-id="84a5c-186">XREF (cross reference) links</span></span>

<span data-ttu-id="84a5c-187">K odkazování na automaticky generované stránky s referencemi rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XREF s jedinečným ID (UID).</span><span class="sxs-lookup"><span data-stu-id="84a5c-187">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="84a5c-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span><span class="sxs-lookup"><span data-stu-id="84a5c-188">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="84a5c-189">Identifikátor odpovídá plně kvalifikované třídě a názvu člena.</span><span class="sxs-lookup"><span data-stu-id="84a5c-189">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="84a5c-190">Pokud za UID přidáte \*, představuje tento odkaz stránku přetížení, nikoli konkrétní rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="84a5c-190">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="84a5c-191">`List<T>.BinarySearch*` použijte například k odkazu na stránku metody BinarySearch místo odkazu na konkrétní přetížení, jako je `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-191">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="84a5c-192">Můžete použít jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="84a5c-192">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="84a5c-193">Automatický odkaz: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="84a5c-193">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="84a5c-194">Nepovinný parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-194">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="84a5c-195">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-195">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="84a5c-196">Odkaz Markdownu: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="84a5c-196">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="84a5c-197">Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-197">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="84a5c-198">Příklady:</span><span class="sxs-lookup"><span data-stu-id="84a5c-198">Examples:</span></span>

- <span data-ttu-id="84a5c-199">`<xref:System.String>` se zobrazí jako „String“.</span><span class="sxs-lookup"><span data-stu-id="84a5c-199">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="84a5c-200">`<xref:System.String?displayProperty=nameWithType>` se zobrazí jako „System.String“.</span><span class="sxs-lookup"><span data-stu-id="84a5c-200">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="84a5c-201">`[String class](xref:System.String)` se zobrazí jako „třída String“.</span><span class="sxs-lookup"><span data-stu-id="84a5c-201">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="84a5c-202">V současné době neexistuje jednoduchý způsob, jak najít identifikátory UID.</span><span class="sxs-lookup"><span data-stu-id="84a5c-202">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="84a5c-203">Nejlepším způsobem, jak najít identifikátor UID pro rozhraní API, je zobrazit zdroj stránky API, kterou chcete propojit, a najít hodnotu ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="84a5c-203">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="84a5c-204">Hodnoty jednotlivých přetížení se ve zdroji nezobrazují.</span><span class="sxs-lookup"><span data-stu-id="84a5c-204">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="84a5c-205">Pracujeme na tom, abychom v budoucnu měli lepší systém.</span><span class="sxs-lookup"><span data-stu-id="84a5c-205">We're working on having a better system in the future.</span></span>

<span data-ttu-id="84a5c-206">Pokud UID obsahuje speciální znaky \`, \# nebo \*, musí být hodnota UID uvedena ve formátu HTML `%60`, `%23` a `%2A` v uvedeném pořadí.</span><span class="sxs-lookup"><span data-stu-id="84a5c-206">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="84a5c-207">Někdy v tomto formátu uvidíte i závorky, není to ale povinné.</span><span class="sxs-lookup"><span data-stu-id="84a5c-207">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="84a5c-208">Příklady:</span><span class="sxs-lookup"><span data-stu-id="84a5c-208">Examples:</span></span>

- <span data-ttu-id="84a5c-209">System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-209">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="84a5c-210">System.Exception.\#ctor se změní na `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-210">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="84a5c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-211">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="84a5c-212">Seznamy (číslované, odrážkové, kontrolní)</span><span class="sxs-lookup"><span data-stu-id="84a5c-212">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="84a5c-213">Číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="84a5c-213">Numbered list</span></span>

<span data-ttu-id="84a5c-214">Při vytváření číslovaného seznamu můžete všude použít jedničky (1), které se při publikování zobrazí jako sekvenční seznam.</span><span class="sxs-lookup"><span data-stu-id="84a5c-214">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="84a5c-215">Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat.</span><span class="sxs-lookup"><span data-stu-id="84a5c-215">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="84a5c-216">Nepoužívejte v seznamech ani vnořených seznamech písmena.</span><span class="sxs-lookup"><span data-stu-id="84a5c-216">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="84a5c-217">Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena.</span><span class="sxs-lookup"><span data-stu-id="84a5c-217">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="84a5c-218">Například:</span><span class="sxs-lookup"><span data-stu-id="84a5c-218">For example:</span></span>

```md
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="84a5c-219">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-219">This renders as follows:</span></span>

1. <span data-ttu-id="84a5c-220">This is</span><span class="sxs-lookup"><span data-stu-id="84a5c-220">This is</span></span>
1. <span data-ttu-id="84a5c-221">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="84a5c-221">a parent numbered list</span></span>
   1. <span data-ttu-id="84a5c-222">and this is</span><span class="sxs-lookup"><span data-stu-id="84a5c-222">and this is</span></span>
   1. <span data-ttu-id="84a5c-223">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="84a5c-223">a nested numbered list</span></span>
1. <span data-ttu-id="84a5c-224">(fin)</span><span class="sxs-lookup"><span data-stu-id="84a5c-224">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="84a5c-225">Seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="84a5c-225">Bulleted list</span></span>

<span data-ttu-id="84a5c-226">Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` následovaný mezerou:</span><span class="sxs-lookup"><span data-stu-id="84a5c-226">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```md
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="84a5c-227">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-227">This renders as follows:</span></span>

- <span data-ttu-id="84a5c-228">This is</span><span class="sxs-lookup"><span data-stu-id="84a5c-228">This is</span></span>
- <span data-ttu-id="84a5c-229">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="84a5c-229">a parent bulleted list</span></span>
  - <span data-ttu-id="84a5c-230">and this is</span><span class="sxs-lookup"><span data-stu-id="84a5c-230">and this is</span></span>
  - <span data-ttu-id="84a5c-231">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="84a5c-231">a nested bulleted list</span></span>
- <span data-ttu-id="84a5c-232">All done!</span><span class="sxs-lookup"><span data-stu-id="84a5c-232">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="84a5c-233">Kontrolní seznam</span><span class="sxs-lookup"><span data-stu-id="84a5c-233">Checklist</span></span>

<span data-ttu-id="84a5c-234">Kontrolní seznamy jsou webu docs.microsoft.com dostupné jen při použití vlastního rozšíření Markdownu:</span><span class="sxs-lookup"><span data-stu-id="84a5c-234">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="84a5c-235">Tento příklad se na webu docs.microsoft.com zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-235">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="84a5c-236">List item 1</span><span class="sxs-lookup"><span data-stu-id="84a5c-236">List item 1</span></span>
> * <span data-ttu-id="84a5c-237">List item 2</span><span class="sxs-lookup"><span data-stu-id="84a5c-237">List item 2</span></span>
> * <span data-ttu-id="84a5c-238">List item 3</span><span class="sxs-lookup"><span data-stu-id="84a5c-238">List item 3</span></span>

<span data-ttu-id="84a5c-239">Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-239">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="84a5c-240">Nepřidávejte do svých článků náhodné kontrolní seznamy.</span><span class="sxs-lookup"><span data-stu-id="84a5c-240">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="84a5c-241">Akce dalšího kroku</span><span class="sxs-lookup"><span data-stu-id="84a5c-241">Next step action</span></span>

<span data-ttu-id="84a5c-242">K přidání tlačítka akce dalšího kroku na stránky docs.microsoft.com můžete použít jen vlastní rozšíření.</span><span class="sxs-lookup"><span data-stu-id="84a5c-242">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="84a5c-243">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="84a5c-243">The syntax is as follows:</span></span>

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="84a5c-244">Například:</span><span class="sxs-lookup"><span data-stu-id="84a5c-244">For example:</span></span>

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="84a5c-245">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-245">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="84a5c-246">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="84a5c-246">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="84a5c-247">V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-247">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="84a5c-248">Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="84a5c-248">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="84a5c-249">Definice oddílu</span><span class="sxs-lookup"><span data-stu-id="84a5c-249">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="84a5c-250">Je možné, že budete potřebovat nadefinovat oddíl.</span><span class="sxs-lookup"><span data-stu-id="84a5c-250">You might need to define a section.</span></span> <span data-ttu-id="84a5c-251">Tato syntaxe se nejčastěji používá pro tabulky kódu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-251">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="84a5c-252">Prohlédněte si následující příklad:</span><span class="sxs-lookup"><span data-stu-id="84a5c-252">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="84a5c-253">Předchozí text Markdownu blokové citace se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-253">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="84a5c-254">Voliče</span><span class="sxs-lookup"><span data-stu-id="84a5c-254">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="84a5c-255">Volič neboli selektor můžete použít, když chcete připojit různé stránky pro stejný článek.</span><span class="sxs-lookup"><span data-stu-id="84a5c-255">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="84a5c-256">Čtenáři pak můžou přepínat mezi těmito stránkami.</span><span class="sxs-lookup"><span data-stu-id="84a5c-256">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="84a5c-257">This extension works differently between docs.microsoft.com and MSDN.</span><span class="sxs-lookup"><span data-stu-id="84a5c-257">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="84a5c-258">Jeden selektor</span><span class="sxs-lookup"><span data-stu-id="84a5c-258">Single selector</span></span>

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

<span data-ttu-id="84a5c-259">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-259">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="84a5c-268">Vícenásobný selektor</span><span class="sxs-lookup"><span data-stu-id="84a5c-268">Multi-selector</span></span>

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

<span data-ttu-id="84a5c-269">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-269">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="84a5c-282">Tabulky</span><span class="sxs-lookup"><span data-stu-id="84a5c-282">Tables</span></span>

<span data-ttu-id="84a5c-283">Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky.</span><span class="sxs-lookup"><span data-stu-id="84a5c-283">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="84a5c-284">Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:</span><span class="sxs-lookup"><span data-stu-id="84a5c-284">To create a standard table with a header, follow the first line with dashed line:</span></span>

```md
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="84a5c-285">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-285">This renders as follows:</span></span>

|<span data-ttu-id="84a5c-286">This is</span><span class="sxs-lookup"><span data-stu-id="84a5c-286">This is</span></span>   |<span data-ttu-id="84a5c-287">a simple</span><span class="sxs-lookup"><span data-stu-id="84a5c-287">a simple</span></span>   |<span data-ttu-id="84a5c-288">table header</span><span class="sxs-lookup"><span data-stu-id="84a5c-288">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="84a5c-289">table</span><span class="sxs-lookup"><span data-stu-id="84a5c-289">table</span></span>     |<span data-ttu-id="84a5c-290">data</span><span class="sxs-lookup"><span data-stu-id="84a5c-290">data</span></span>       |<span data-ttu-id="84a5c-291">here</span><span class="sxs-lookup"><span data-stu-id="84a5c-291">here</span></span>        |
|<span data-ttu-id="84a5c-292">it doesn't</span><span class="sxs-lookup"><span data-stu-id="84a5c-292">it doesn't</span></span>|<span data-ttu-id="84a5c-293">actually</span><span class="sxs-lookup"><span data-stu-id="84a5c-293">actually</span></span>   |<span data-ttu-id="84a5c-294">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="84a5c-294">have to line up nicely!</span></span>||

<span data-ttu-id="84a5c-295">Můžete také vytvořit tabulku bez záhlaví.</span><span class="sxs-lookup"><span data-stu-id="84a5c-295">You can also create a table without a header.</span></span> <span data-ttu-id="84a5c-296">Příklad vytvoření seznamu s více sloupci:</span><span class="sxs-lookup"><span data-stu-id="84a5c-296">For example, to create a multiple-column list:</span></span>

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="84a5c-297">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-297">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="84a5c-298">This</span><span class="sxs-lookup"><span data-stu-id="84a5c-298">This</span></span> | <span data-ttu-id="84a5c-299">table</span><span class="sxs-lookup"><span data-stu-id="84a5c-299">table</span></span> |
| <span data-ttu-id="84a5c-300">has no</span><span class="sxs-lookup"><span data-stu-id="84a5c-300">has no</span></span> | <span data-ttu-id="84a5c-301">header</span><span class="sxs-lookup"><span data-stu-id="84a5c-301">header</span></span> |

<span data-ttu-id="84a5c-302">Sloupce můžete zarovnat pomocí dvojtečky:</span><span class="sxs-lookup"><span data-stu-id="84a5c-302">You can align the columns by using colons:</span></span>

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="84a5c-303">Se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-303">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="84a5c-304">right aligned:</span><span class="sxs-lookup"><span data-stu-id="84a5c-304">right aligned:</span></span>|
|<span data-ttu-id="84a5c-305">:left aligned</span><span class="sxs-lookup"><span data-stu-id="84a5c-305">:left aligned</span></span>     |
|<span data-ttu-id="84a5c-306">:centered        :</span><span class="sxs-lookup"><span data-stu-id="84a5c-306">:centered        :</span></span>|

> [!TIP]
> <span data-ttu-id="84a5c-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span><span class="sxs-lookup"><span data-stu-id="84a5c-307">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="84a5c-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="84a5c-308">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="mx-tdbreakall"></a><span data-ttu-id="84a5c-309">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="84a5c-309">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84a5c-310">This only works on the docs.microsoft.com site.</span><span class="sxs-lookup"><span data-stu-id="84a5c-310">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="84a5c-311">Když vytvoříte tabulku v Markdownu, často se stane, že tabulka zasahuje do navigace napravo a stává se nečitelnou.</span><span class="sxs-lookup"><span data-stu-id="84a5c-311">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="84a5c-312">Tento problém můžete vyřešit tak, že při zobrazování na webu Docs umožníte tabulku v případě potřeby rozdělit.</span><span class="sxs-lookup"><span data-stu-id="84a5c-312">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="84a5c-313">Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-313">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="84a5c-314">Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-314">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```md
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="84a5c-315">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-315">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="84a5c-316">Name</span><span class="sxs-lookup"><span data-stu-id="84a5c-316">Name</span></span>|<span data-ttu-id="84a5c-317">Syntax</span><span class="sxs-lookup"><span data-stu-id="84a5c-317">Syntax</span></span>|<span data-ttu-id="84a5c-318">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="84a5c-318">Mandatory for silent installation?</span></span>|<span data-ttu-id="84a5c-319">Description</span><span class="sxs-lookup"><span data-stu-id="84a5c-319">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="84a5c-320">Quiet</span><span class="sxs-lookup"><span data-stu-id="84a5c-320">Quiet</span></span>|<span data-ttu-id="84a5c-321">/quiet</span><span class="sxs-lookup"><span data-stu-id="84a5c-321">/quiet</span></span>|<span data-ttu-id="84a5c-322">Yes</span><span class="sxs-lookup"><span data-stu-id="84a5c-322">Yes</span></span>|<span data-ttu-id="84a5c-323">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="84a5c-323">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="84a5c-324">NoRestart</span><span class="sxs-lookup"><span data-stu-id="84a5c-324">NoRestart</span></span>|<span data-ttu-id="84a5c-325">/norestart</span><span class="sxs-lookup"><span data-stu-id="84a5c-325">/norestart</span></span>|<span data-ttu-id="84a5c-326">No</span><span class="sxs-lookup"><span data-stu-id="84a5c-326">No</span></span>|<span data-ttu-id="84a5c-327">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="84a5c-327">Suppresses any attempts to restart.</span></span> <span data-ttu-id="84a5c-328">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="84a5c-328">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="84a5c-329">Help</span><span class="sxs-lookup"><span data-stu-id="84a5c-329">Help</span></span>|<span data-ttu-id="84a5c-330">/help</span><span class="sxs-lookup"><span data-stu-id="84a5c-330">/help</span></span>|<span data-ttu-id="84a5c-331">No</span><span class="sxs-lookup"><span data-stu-id="84a5c-331">No</span></span>|<span data-ttu-id="84a5c-332">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="84a5c-332">Provides help and quick reference.</span></span> <span data-ttu-id="84a5c-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="84a5c-333">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="84a5c-334">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="84a5c-334">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84a5c-335">This only works on the docs.microsoft.com site.</span><span class="sxs-lookup"><span data-stu-id="84a5c-335">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="84a5c-336">Někdy se může stát, že druhý sloupec v tabulce obsahuje velmi dlouhá slova.</span><span class="sxs-lookup"><span data-stu-id="84a5c-336">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="84a5c-337">Pokud chcete zajistit jejich správné rozdělení, můžete použít třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.</span><span class="sxs-lookup"><span data-stu-id="84a5c-337">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="84a5c-338">Tabulky HTML</span><span class="sxs-lookup"><span data-stu-id="84a5c-338">HTML Tables</span></span>

<span data-ttu-id="84a5c-339">Tabulky HTML se na webu docs.microsoft.com nedoporučují.</span><span class="sxs-lookup"><span data-stu-id="84a5c-339">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="84a5c-340">Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-340">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="84a5c-341">Videa</span><span class="sxs-lookup"><span data-stu-id="84a5c-341">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="84a5c-342">Vkládání videí na stránku Markdownu</span><span class="sxs-lookup"><span data-stu-id="84a5c-342">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="84a5c-343">Platforma Docs v současnosti podporuje videa publikovaná v jednom z těchto tří umístění:</span><span class="sxs-lookup"><span data-stu-id="84a5c-343">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="84a5c-344">YouTube</span><span class="sxs-lookup"><span data-stu-id="84a5c-344">YouTube</span></span>
- <span data-ttu-id="84a5c-345">Channel9</span><span class="sxs-lookup"><span data-stu-id="84a5c-345">Channel 9</span></span>
- <span data-ttu-id="84a5c-346">Vlastní systém Microsoftu „One Player“</span><span class="sxs-lookup"><span data-stu-id="84a5c-346">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="84a5c-347">Můžete vložit video s následující syntaxí a Docs ho zobrazí.</span><span class="sxs-lookup"><span data-stu-id="84a5c-347">You can embed a video with the following syntax, and Docs will render it.</span></span>

```md
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="84a5c-348">Příklad:</span><span class="sxs-lookup"><span data-stu-id="84a5c-348">Example:</span></span>

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="84a5c-349">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-349">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="84a5c-350">A na publikovaných stránkách se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="84a5c-350">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="84a5c-351">The CH9 video URL should start with `https` and end with `/player`.</span><span class="sxs-lookup"><span data-stu-id="84a5c-351">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="84a5c-352">Otherwise, it will embed the whole page instead of the video only.</span><span class="sxs-lookup"><span data-stu-id="84a5c-352">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="84a5c-353">Nahrání nových videí</span><span class="sxs-lookup"><span data-stu-id="84a5c-353">Uploading new videos</span></span>

<span data-ttu-id="84a5c-354">Všechna nová videa by měla být nahrána následujícím postupem:</span><span class="sxs-lookup"><span data-stu-id="84a5c-354">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="84a5c-355">Připojte se ke skupině **docs_video_users** na IDWEB.</span><span class="sxs-lookup"><span data-stu-id="84a5c-355">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="84a5c-356">Přejděte na adresu https://aka.ms/VideoUploadRequest a vyplňte podrobnosti o videu.</span><span class="sxs-lookup"><span data-stu-id="84a5c-356">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="84a5c-357">Budete potřebovat zadat tyto údaje (žádné z nich nebudou veřejně viditelné):</span><span class="sxs-lookup"><span data-stu-id="84a5c-357">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="84a5c-358">Název videa</span><span class="sxs-lookup"><span data-stu-id="84a5c-358">A title for your video.</span></span>
    1. <span data-ttu-id="84a5c-359">Seznam produktů/služeb, kterých se video týká</span><span class="sxs-lookup"><span data-stu-id="84a5c-359">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="84a5c-360">Cílová stránka nebo (pokud tuto stránku ještě nemáte) sada dokumentace, kde bude video hostované</span><span class="sxs-lookup"><span data-stu-id="84a5c-360">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="84a5c-361">Odkaz na soubor MP4 s videem (pokud ještě nevíte, kde bude soubor umístěný, můžete sem dočasně zadat: `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="84a5c-361">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="84a5c-362">Soubory MP4 by měly mít rozlišení 720p nebo vyšší.</span><span class="sxs-lookup"><span data-stu-id="84a5c-362">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="84a5c-363">Popis videa</span><span class="sxs-lookup"><span data-stu-id="84a5c-363">A description of the video.</span></span>
1. <span data-ttu-id="84a5c-364">Odešlete (uložte) tuto položku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-364">Submit (save) that item.</span></span>
1. <span data-ttu-id="84a5c-365">Video se nahraje během dvou pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="84a5c-365">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="84a5c-366">Odkaz potřebný k vložení bude umístěn do pracovní položky, která vám bude *přeložena zpět*.</span><span class="sxs-lookup"><span data-stu-id="84a5c-366">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="84a5c-367">Jakmile získáte odkaz na video, zavřete tuto pracovní položku.</span><span class="sxs-lookup"><span data-stu-id="84a5c-367">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="84a5c-368">Odkaz na video pak můžete přidat do příspěvku pomocí této syntaxe:</span><span class="sxs-lookup"><span data-stu-id="84a5c-368">The video link can then be added to your post, using this syntax:</span></span>

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
