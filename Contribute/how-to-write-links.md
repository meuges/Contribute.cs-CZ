---
title: Používání odkazů v dokumentaci
description: Tento článek obsahuje pokyny k vytváření odkazů na obsah na webu docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "80624758"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="c8278-103">Použití odkazů v dokumentaci</span><span class="sxs-lookup"><span data-stu-id="c8278-103">Use links in documentation</span></span>

<span data-ttu-id="c8278-104">Tento článek popisuje způsob používání hypertextových odkazů ze stránek hostovaných na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c8278-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="c8278-105">Odkazy se snadno přidávají do markdownu pomocí několika různých konvencí.</span><span class="sxs-lookup"><span data-stu-id="c8278-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="c8278-106">Odkazy směrují uživatele na obsah na stejné stránce, na jiné sousední stránky nebo na externí weby a adresy URL.</span><span class="sxs-lookup"><span data-stu-id="c8278-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="c8278-107">Back-end webu docs.microsoft.com používá platformu OPS (Open Publishing Services), která podporuje markdown kompatibilní s verzí [CommonMark][] parsovaný prostřednictvím parsovacího modulu [Markdig][].</span><span class="sxs-lookup"><span data-stu-id="c8278-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="c8278-108">Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)][GFM], protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat.</span><span class="sxs-lookup"><span data-stu-id="c8278-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="c8278-109">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="c8278-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8278-110">Všechny odkazy musí být zabezpečené (`https` versus `http`), když to cíl podporuje (což by měla drtivá většina).</span><span class="sxs-lookup"><span data-stu-id="c8278-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="c8278-111">Text odkazu</span><span class="sxs-lookup"><span data-stu-id="c8278-111">Link text</span></span>

<span data-ttu-id="c8278-112">Slova, která použijete v textu odkazu, by měla být popisná.</span><span class="sxs-lookup"><span data-stu-id="c8278-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="c8278-113">Jinými slovy by mělo jít o normální slova nebo název stránky, na kterou odkazujete.</span><span class="sxs-lookup"><span data-stu-id="c8278-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8278-114">Nepoužívejte „klikněte sem“.</span><span class="sxs-lookup"><span data-stu-id="c8278-114">Do not use "click here."</span></span> <span data-ttu-id="c8278-115">Je to špatné pro optimalizaci vyhledávacího webu a adekvátně to nepopisuje cílovou stránku.</span><span class="sxs-lookup"><span data-stu-id="c8278-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="c8278-116">**Správně:**</span><span class="sxs-lookup"><span data-stu-id="c8278-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="c8278-117">**Nesprávně:**</span><span class="sxs-lookup"><span data-stu-id="c8278-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="c8278-118">Odkazy z jednoho článku na druhý</span><span class="sxs-lookup"><span data-stu-id="c8278-118">Links from one article to another</span></span>

<span data-ttu-id="c8278-119">Systém publikování podporuje dva typy hypertextových odkazů: **adresy URL** a **odkazy na soubory**.</span><span class="sxs-lookup"><span data-stu-id="c8278-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="c8278-120">Odkaz URL může být cesta URL relativní ke kořenu webu docs.microsoft.com nebo absolutní adresa URL, která obsahuje úplnou syntaxi adresy URL (například `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span><span class="sxs-lookup"><span data-stu-id="c8278-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="c8278-121">Použijte odkazy URL při odkazování na obsah mimo aktuální sadu dokumentace (_docset_) nebo mezi automaticky generovanými referenčními a koncepčními články v rámci sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="c8278-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="c8278-122">Nejjednodušší způsob, jak vytvořit relativní odkaz, je zkopírovat adresu URL z prohlížeče a pak z hodnoty, kterou vložíte do markdownu, odebrat `https://docs.microsoft.com/en-us`.</span><span class="sxs-lookup"><span data-stu-id="c8278-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="c8278-123">Nedávejte do adres URL národní prostředí pro vlastnosti Microsoftu (z adresy URL odeberte například „/en-US“).</span><span class="sxs-lookup"><span data-stu-id="c8278-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="c8278-124">Odkaz na soubor se používá k propojení mezi jedním článkem a jiným v rámci sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="c8278-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="c8278-125">Všechny cesty k souborům používají znaky lomítka (`/`) místo znaků zpětného lomítka.</span><span class="sxs-lookup"><span data-stu-id="c8278-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="c8278-126">Článek odkazuje na jiný článek ve stejném adresáři:</span><span class="sxs-lookup"><span data-stu-id="c8278-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="c8278-127">Článek odkazuje na článek v nadřazeném adresáři aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="c8278-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="c8278-128">Článek odkazuje na článek v podadresáři aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="c8278-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="c8278-129">Článek odkazuje na článek v podadresáři nadřazeného adresáře aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="c8278-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="c8278-130">V žádném z předchozích příkladů se jako součást odkazu nepoužívá `~/`.</span><span class="sxs-lookup"><span data-stu-id="c8278-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="c8278-131">Pokud chcete vytvořit odkaz na absolutní cestu, která začíná v kořenovém adresáři úložiště, začněte odkaz znakem `/`.</span><span class="sxs-lookup"><span data-stu-id="c8278-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="c8278-132">Při zahrnutí řetězce `~/` vznikají neplatné odkazy pro navigaci do zdrojových úložišť na GitHubu.</span><span class="sxs-lookup"><span data-stu-id="c8278-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="c8278-133">Problém se vyřeší, když bude cesta začínat znakem `/`.</span><span class="sxs-lookup"><span data-stu-id="c8278-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="c8278-134">Struktura odkazů na docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c8278-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="c8278-135">Obsah publikovaný na docs.microsoft.com má následující strukturu adresy URL:</span><span class="sxs-lookup"><span data-stu-id="c8278-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="c8278-136">Příklady:</span><span class="sxs-lookup"><span data-stu-id="c8278-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="c8278-137">`<locale>` – Identifikuje jazyk článku (příklad: en-us nebo cs-cz).</span><span class="sxs-lookup"><span data-stu-id="c8278-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="c8278-138">`<product-service>` – Název produktu nebo služby (příklad: powershell, dotnet nebo azure).</span><span class="sxs-lookup"><span data-stu-id="c8278-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="c8278-139">`[<feature-service>]` – (nepovinné) Název funkce nebo dílčí služby produktu (například: csharp nebo load-balancer).</span><span class="sxs-lookup"><span data-stu-id="c8278-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="c8278-140">`[<subfolder>]` – (nepovinné) Název podsložky v rámci funkce.</span><span class="sxs-lookup"><span data-stu-id="c8278-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="c8278-141">`<topic>` – Název souboru článku pro téma (například: prehled-nastroje-pro-vyrovnavani-zatizeni nebo prehled).</span><span class="sxs-lookup"><span data-stu-id="c8278-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="c8278-142">`[?view=\<view-name>]` – (nepovinné) Název zobrazení používaný selektorem verzí pro obsah, který má více dostupných verzí (například: azps-3.5.0).</span><span class="sxs-lookup"><span data-stu-id="c8278-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="c8278-143">Ve většině případů mají články ve stejné sadě _docset_ stejný fragment adresy URL `<product-service>`.</span><span class="sxs-lookup"><span data-stu-id="c8278-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="c8278-144">Například:</span><span class="sxs-lookup"><span data-stu-id="c8278-144">For example:</span></span>
> - <span data-ttu-id="c8278-145">Stejná sada docset</span><span class="sxs-lookup"><span data-stu-id="c8278-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="c8278-146">Různé sady docset</span><span class="sxs-lookup"><span data-stu-id="c8278-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="c8278-147">Odkazy na záložky</span><span class="sxs-lookup"><span data-stu-id="c8278-147">Bookmark links</span></span>

<span data-ttu-id="c8278-148">Pro odkaz na záložku na nadpis v *aktuálním* souboru použijte symbol hash následovaný slovy nadpisu malými písmeny.</span><span class="sxs-lookup"><span data-stu-id="c8278-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="c8278-149">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami:</span><span class="sxs-lookup"><span data-stu-id="c8278-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="c8278-150">K odkazu na nadpis záložky v jiném článku použijte odkaz na daný soubor nebo web, za kterým bude následovat symbol hash a text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="c8278-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c8278-151">Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami:</span><span class="sxs-lookup"><span data-stu-id="c8278-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="c8278-152">Odkaz na záložku můžete také zkopírovat z adresy URL.</span><span class="sxs-lookup"><span data-stu-id="c8278-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="c8278-153">Pokud chcete najít adresu URL, najeďte myší na řádek nadpisu na docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c8278-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="c8278-154">Měla by se zobrazit ikona odkazu:</span><span class="sxs-lookup"><span data-stu-id="c8278-154">You should see a link icon appear:</span></span>

![Ikona odkazu v nadpisu článku](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="c8278-156">Klikněte na ikonu odkazu a pak zkopírujte text ukotvení záložky z adresy URL (tj. část za znakem hash).</span><span class="sxs-lookup"><span data-stu-id="c8278-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="c8278-157">Rozšíření Docs obsahuje také nástroje, které vám pomůžou s vytvářením odkazů.</span><span class="sxs-lookup"><span data-stu-id="c8278-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="c8278-158">Explicitní odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="c8278-158">Explicit anchor links</span></span>

<span data-ttu-id="c8278-159">Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML není nutné přidávat a ani se to nedoporučuje, s výjimkou centra a cílových stránek.</span><span class="sxs-lookup"><span data-stu-id="c8278-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="c8278-160">Místo toho použijte automaticky generované záložky, jak je popsáno v části [odkazy na záložky](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="c8278-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="c8278-161">Pro centrum a cílové stránky deklarujte ukotvení následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c8278-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="c8278-162">nebo</span><span class="sxs-lookup"><span data-stu-id="c8278-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="c8278-163">A následující text k propojení na ukotvení:</span><span class="sxs-lookup"><span data-stu-id="c8278-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="c8278-164">Text ukotvení musí být vždycky malými písmeny a nesmí obsahovat mezery.</span><span class="sxs-lookup"><span data-stu-id="c8278-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="c8278-165">Křížové odkazy (XRef)</span><span class="sxs-lookup"><span data-stu-id="c8278-165">XRef (cross reference) links</span></span>

<span data-ttu-id="c8278-166">Odkazy XRef jsou doporučeným způsobem, jak odkazovat na rozhraní API, protože jsou ověřovány při sestavení.</span><span class="sxs-lookup"><span data-stu-id="c8278-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="c8278-167">K odkazování na automaticky generované referenční stránky rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XRef s jedinečným ID ([UID](#determine-the-uid)) typu nebo člena.</span><span class="sxs-lookup"><span data-stu-id="c8278-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="c8278-168">K vložení odkazů XRref pro .NET, které jsou umístěny v [Prohlížeč rozhraní .NET API][], můžete použít [rozšíření Docs Markdown pro VS Code][docsextension] (součást balíčku pro vytváření obsahu na webu Docs).</span><span class="sxs-lookup"><span data-stu-id="c8278-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="c8278-169">Ověřte, jestli rozhraní API, ke kterému chcete vytvořit odkaz, je na webu [docs.microsoft.com][docs], zadáním jeho celého názvu nebo části názvu do vyhledávacího pole [Prohlížeč rozhraní .NET API][] nebo [Windows UPW][].</span><span class="sxs-lookup"><span data-stu-id="c8278-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="c8278-170">Pokud se nezobrazí žádné výsledky, typ ještě není na docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c8278-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="c8278-171">Můžete použít jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="c8278-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="c8278-172">Automatické odkazy:</span><span class="sxs-lookup"><span data-stu-id="c8278-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="c8278-173">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="c8278-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="c8278-174">Volitelný parametr dotazu `displayProperty=nameWithType` vytvoří plně kvalifikovaný text odkazu, tj. **namespace.type**, pro typy a **type.member** pro členy typu, včetně členů výčtového typu.</span><span class="sxs-lookup"><span data-stu-id="c8278-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="c8278-175">Odkazy ve stylu Markdownu:</span><span class="sxs-lookup"><span data-stu-id="c8278-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="c8278-176">Použijte odkazy ve stylu Markdownu pro odkazy XRef, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="c8278-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="c8278-177">Příklady:</span><span class="sxs-lookup"><span data-stu-id="c8278-177">Examples:</span></span>

- <span data-ttu-id="c8278-178">**\<xref:System.String>** se zobrazí jako <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="c8278-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="c8278-179">**\<xref:System.String?displayProperty=nameWithType>** se zobrazí jako <xref:System.String?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c8278-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="c8278-180">**\[String class](xref:System.String)** se zobrazí jako [String class](xref:System.String).</span><span class="sxs-lookup"><span data-stu-id="c8278-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="c8278-181">Parametr dotazu `displayProperty=fullName` funguje stejným způsobem jako `displayProperty=nameWithType` pro třídy.</span><span class="sxs-lookup"><span data-stu-id="c8278-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="c8278-182">To znamená, že text odkazu se změní na **namespace.classname**.</span><span class="sxs-lookup"><span data-stu-id="c8278-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="c8278-183">Členům se ale text odkazu zobrazuje jako **namespace.classname.membername**, což může být nežádoucí.</span><span class="sxs-lookup"><span data-stu-id="c8278-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="c8278-184">U identifikátorů UID se rozlišuje velikost písmen.</span><span class="sxs-lookup"><span data-stu-id="c8278-184">UIDs are case sensitive.</span></span> <span data-ttu-id="c8278-185">Například `<xref:System.Object>` se přeloží správně, ale `<xref:system.object>` ne.</span><span class="sxs-lookup"><span data-stu-id="c8278-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="c8278-186">Upozornění sestavení odkazu XRef a přírůstková sestavení</span><span class="sxs-lookup"><span data-stu-id="c8278-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="c8278-187">Přírůstkové sestavení (build) sestaví pouze soubory, které byly změněny nebo ovlivněny změnou.</span><span class="sxs-lookup"><span data-stu-id="c8278-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="c8278-188">Pokud se zobrazí upozornění sestavení týkající se neplatného odkazu XRef, ale odkaz je ve skutečnosti platný, může to být proto, že sestavení bylo přírůstkové.</span><span class="sxs-lookup"><span data-stu-id="c8278-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="c8278-189">Soubor, který způsobil upozornění, se nezměnil, takže nebyl sestaven a byla znovu přehrána minulá upozornění.</span><span class="sxs-lookup"><span data-stu-id="c8278-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="c8278-190">Když se soubor změní nebo když spustíte úplné sestavení (úplné sestavení můžete spustit na ops.microsoft.com), upozornění zmizí.</span><span class="sxs-lookup"><span data-stu-id="c8278-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="c8278-191">To je nevýhoda přírůstkových sestavení, protože DocFX neumí zjistit aktualizaci dat uvnitř služby XREF.</span><span class="sxs-lookup"><span data-stu-id="c8278-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="c8278-192">Určení UID</span><span class="sxs-lookup"><span data-stu-id="c8278-192">Determine the UID</span></span>

<span data-ttu-id="c8278-193">Identifikátor UID je obvykle plně kvalifikovaná třída nebo název člena.</span><span class="sxs-lookup"><span data-stu-id="c8278-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="c8278-194">Existují alespoň dva způsoby, jak určit UID:</span><span class="sxs-lookup"><span data-stu-id="c8278-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="c8278-195">Klikněte pravým tlačítkem myši na stránku [Docs][docs] pro typ nebo člena, vyberte **Zobrazit zdroj** a potom zkopírujte hodnotu **content** pro **ms.assetid**:</span><span class="sxs-lookup"><span data-stu-id="c8278-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid ve zdroji pro webovou stránku](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="c8278-197">Použijte [web automatického dokončování][] připojením části názvu typu nebo celého názvu typu k adrese URL.</span><span class="sxs-lookup"><span data-stu-id="c8278-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="c8278-198">Například zadáním `https://xref.docs.microsoft.com/autocomplete?text=Writeline` do panelu Adresa v prohlížeči se zobrazí všechny typy a metody, které v názvu obsahují **Writeline**, spolu s jejich UID.</span><span class="sxs-lookup"><span data-stu-id="c8278-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="c8278-199">Ověření UID</span><span class="sxs-lookup"><span data-stu-id="c8278-199">Verify the UID</span></span>

<span data-ttu-id="c8278-200">Pokud chcete otestovat, jestli máte správné UID, nahraďte **System.String** v následující adrese URL vaším UID a pak ho vložte do panelu Adresa v prohlížeči:</span><span class="sxs-lookup"><span data-stu-id="c8278-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="c8278-201">V UID v adrese URL se rozlišují velká a malá písmena, a pokud kontrolujete UID přetížení metody, nepoužívejte mezi typy parametrů mezery.</span><span class="sxs-lookup"><span data-stu-id="c8278-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="c8278-202">Pokud se zobrazí něco podobného, máte správné UID:</span><span class="sxs-lookup"><span data-stu-id="c8278-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="c8278-203">Pokud se na stránce zobrazuje jenom `[]`, máte nesprávné UID.</span><span class="sxs-lookup"><span data-stu-id="c8278-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="c8278-204">Procentové kódování adres URL</span><span class="sxs-lookup"><span data-stu-id="c8278-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="c8278-205">Speciální znaky v UID musí být kódovány ve formátu HTML následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c8278-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="c8278-206">Znak</span><span class="sxs-lookup"><span data-stu-id="c8278-206">Character</span></span> | <span data-ttu-id="c8278-207">Kódování HTML</span><span class="sxs-lookup"><span data-stu-id="c8278-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="c8278-208">%60</span><span class="sxs-lookup"><span data-stu-id="c8278-208">%60</span></span>           |
| `#`       | <span data-ttu-id="c8278-209">%23</span><span class="sxs-lookup"><span data-stu-id="c8278-209">%23</span></span>           |
| `*`       | <span data-ttu-id="c8278-210">%2A</span><span class="sxs-lookup"><span data-stu-id="c8278-210">%2A</span></span>           |

<span data-ttu-id="c8278-211">Tady najdete úplný seznam [procentových kódů](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="c8278-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="c8278-212">Příklady kódování:</span><span class="sxs-lookup"><span data-stu-id="c8278-212">Encoding examples:</span></span>

- <span data-ttu-id="c8278-213">`System.Threading.Tasks.Task``1` se kóduje jako `System.Threading.Tasks.Task%601` (viz [oddíl o obecných typech](#generic-types)).</span><span class="sxs-lookup"><span data-stu-id="c8278-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="c8278-214">`System.Exception.#ctor` se kóduje jako `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="c8278-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="c8278-215">`System.Object.Equals*` se kóduje jako `System.Object.Equals%2A`.</span><span class="sxs-lookup"><span data-stu-id="c8278-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="c8278-216">Obecné typy</span><span class="sxs-lookup"><span data-stu-id="c8278-216">Generic types</span></span>

<span data-ttu-id="c8278-217">Obecné typy jsou tyto typy jako například `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="c8278-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="c8278-218">Pokud přejdete na tento typ v [prohlížeči .NET API](https://docs.microsoft.com/dotnet/api/) a podíváte se na jeho adresu URL, uvidíte, že `<T>` je v adrese URL napsáno jako `-1`, což ve skutečnosti představuje **\`1**:</span><span class="sxs-lookup"><span data-stu-id="c8278-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="c8278-219">Pokud chcete vytvořit odkaz na obecný typ, jako je **List\<T>** , zakódujte znak pro zpětný apostrof **\`** jako **%60**, jak je znázorněno v následujícím příkladu:</span><span class="sxs-lookup"><span data-stu-id="c8278-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="c8278-220">Metody</span><span class="sxs-lookup"><span data-stu-id="c8278-220">Methods</span></span>

<span data-ttu-id="c8278-221">Pokud chcete vytvořit odkaz na metodu, můžete buď vytvořit odkaz na obecnou stránku metody přidáním hvězdičky (`*`) za název metody, nebo na konkrétní přetížení.</span><span class="sxs-lookup"><span data-stu-id="c8278-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="c8278-222">Obecnou stránku například použijte, když chcete vytvořit odkaz na metodu `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` bez specifických typů parametrů.</span><span class="sxs-lookup"><span data-stu-id="c8278-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="c8278-223">Znak hvězdičky je kódován jako `%2A`.</span><span class="sxs-lookup"><span data-stu-id="c8278-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="c8278-224">Například:</span><span class="sxs-lookup"><span data-stu-id="c8278-224">For example:</span></span>

<span data-ttu-id="c8278-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` je odkaz na <xref:System.Object.Equals%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c8278-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="c8278-226">Jestliže chcete vytvořit odkaz na konkrétní přetížení, přidejte za název metody závorky a doplňte úplný název typu každého parametru.</span><span class="sxs-lookup"><span data-stu-id="c8278-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="c8278-227">Nedávejte mezeru mezi názvy typů, jinak odkaz nebude fungovat.</span><span class="sxs-lookup"><span data-stu-id="c8278-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="c8278-228">Například:</span><span class="sxs-lookup"><span data-stu-id="c8278-228">For example:</span></span>

<span data-ttu-id="c8278-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` je odkaz na <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c8278-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="c8278-230">Odkazy z vložených souborů</span><span class="sxs-lookup"><span data-stu-id="c8278-230">Links from includes</span></span>

<span data-ttu-id="c8278-231">Jelikož jsou vložené soubory umístěné v jiném adresáři, musíte použít delší relativní cesty.</span><span class="sxs-lookup"><span data-stu-id="c8278-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="c8278-232">Pokud chcete vytvořit odkaz na článek z vloženého souboru, použijte tento formát:</span><span class="sxs-lookup"><span data-stu-id="c8278-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="c8278-233">Rozšíření [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) pro Visual Studio Code vám pomůže správně vkládat relativní odkazy a záložky bez únavného řešení cest.</span><span class="sxs-lookup"><span data-stu-id="c8278-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="c8278-234">Odkazy v selektorech</span><span class="sxs-lookup"><span data-stu-id="c8278-234">Links in selectors</span></span>

<span data-ttu-id="c8278-235">Volič je součást navigace, která se v článku dokumentace zobrazuje ve formě rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="c8278-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="c8278-236">Když čtenář vybere nějakou hodnotu v tomto rozevíracím seznamu, otevře prohlížeč vybraný článek.</span><span class="sxs-lookup"><span data-stu-id="c8278-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="c8278-237">Seznam voliče zpravidla obsahuje odkazy na související články, například na stejnou problematiku v několika programovacích jazycích nebo na úzce související sérii článků.</span><span class="sxs-lookup"><span data-stu-id="c8278-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="c8278-238">Pokud máte voliče, které jsou začleněné ve vloženém souboru, použijte následující strukturu odkazu:</span><span class="sxs-lookup"><span data-stu-id="c8278-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="c8278-239">Odkazy z referencí</span><span class="sxs-lookup"><span data-stu-id="c8278-239">Reference-style links</span></span>

<span data-ttu-id="c8278-240">Pokud chcete, aby byl váš zdrojový obsah lépe čitelný, můžete použít odkazy z referencí.</span><span class="sxs-lookup"><span data-stu-id="c8278-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="c8278-241">Odkazy z referencí nahradí syntax hotlinku jednodušší syntaxí, která vám umožní přesunout dlouhé adresy URL na konec článku.</span><span class="sxs-lookup"><span data-stu-id="c8278-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="c8278-242">Zde je příklad z webu [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="c8278-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="c8278-243">Vložený text:</span><span class="sxs-lookup"><span data-stu-id="c8278-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="c8278-244">Odkazy referencí na konci článku:</span><span class="sxs-lookup"><span data-stu-id="c8278-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="c8278-245">Nezapomeňte mezi dvojtečkou a odkazem vytvořit mezeru.</span><span class="sxs-lookup"><span data-stu-id="c8278-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="c8278-246">Pokud odkazujete na ostatní technické články a zapomenete mezeru vytvořit, odkaz nebude v publikovaném článku fungovat.</span><span class="sxs-lookup"><span data-stu-id="c8278-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="c8278-247">Odkazování na stránky, které nejsou součástí sady technické dokumentace</span><span class="sxs-lookup"><span data-stu-id="c8278-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="c8278-248">Pokud chcete vytvořit odkaz na jiný web ve vlastnictví Microsoftu (jako je stránka s ceníkem, stránka SLA nebo cokoli jiného, co není článek dokumentace), použijte absolutní adresu URL, ale vynechejte národní prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8278-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="c8278-249">Cílem je, aby odkazy fungovaly v GitHubu a na zobrazené stránce:</span><span class="sxs-lookup"><span data-stu-id="c8278-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="c8278-250">Odkazy na weby třetích stran</span><span class="sxs-lookup"><span data-stu-id="c8278-250">Links to third-party sites</span></span>

<span data-ttu-id="c8278-251">Nejlepší uživatelské prostředí minimalizuje odchod uživatelů na jiný web.</span><span class="sxs-lookup"><span data-stu-id="c8278-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="c8278-252">Odkazy na weby třetích stran, které jsou občas potřeba, proto vytvářejte na základě těchto informací:</span><span class="sxs-lookup"><span data-stu-id="c8278-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="c8278-253">**Odpovědnost:** Když jde o informace, které má sdílet třetí strana, odkazujte na obsah třetí strany.</span><span class="sxs-lookup"><span data-stu-id="c8278-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="c8278-254">Úkolem Microsoftu například není říkat lidem, jak používat vývojářské nástroje pro Android – to má udělat Google.</span><span class="sxs-lookup"><span data-stu-id="c8278-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="c8278-255">Pokud je to potřeba, můžeme vysvětlit, jak vývojářské nástroje pro Android používat *se* službou Azure, ale jak tyto nástroje celkově používat by měl vysvětlit Google.</span><span class="sxs-lookup"><span data-stu-id="c8278-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="c8278-256">**Schválení od PM:** O schválení obsahu třetí strany požádejte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c8278-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="c8278-257">Odkazování na takový obsah znamená, že mu důvěřujeme, a zahrnuje odpovědnost, pokud se lidé těmito pokyny budou řídit.</span><span class="sxs-lookup"><span data-stu-id="c8278-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="c8278-258">**Kontroly aktuálnosti:** Ověřujte, jestli jsou informace třetí strany stále aktuální, správné a relevantní a jestli se odkaz nezměnil.</span><span class="sxs-lookup"><span data-stu-id="c8278-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="c8278-259">**Přesměrování ven:** Informujte uživatele, že budou přesměrováni na jiný web.</span><span class="sxs-lookup"><span data-stu-id="c8278-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="c8278-260">Pokud to není jasné z kontextu, přidejte vysvětlení.</span><span class="sxs-lookup"><span data-stu-id="c8278-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="c8278-261">Například: „Požadavky zahrnují vývojářské nástroje pro Android, které si můžete stáhnout z webu Android Studio.“</span><span class="sxs-lookup"><span data-stu-id="c8278-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="c8278-262">**Další kroky:** V oddíle Další kroky můžete přidat odkaz například na blog MVP.</span><span class="sxs-lookup"><span data-stu-id="c8278-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="c8278-263">Jen uživatele znovu nezapomeňte informovat, že budou přesměrováni na jiný web.</span><span class="sxs-lookup"><span data-stu-id="c8278-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="c8278-264">**Právní náležitosti:** Jsme právně krytí částí **Odkazy na weby třetích stran** v **Podmínkách použití** uvedených v zápatí každé stránky microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c8278-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Prohlížeč rozhraní .NET API]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UPW]: https://docs.microsoft.com/uwp/api
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[web automatického dokončování]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
