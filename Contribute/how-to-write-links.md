---
title: Používání odkazů v dokumentaci
description: Tento článek obsahuje pokyny k vytváření odkazů na obsah na webu docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 970f80b4e6ce795e0e2f15192d31680d7de6d35b
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188338"
---
# <a name="use-links-in-documentation"></a><span data-ttu-id="78bb0-103">Použití odkazů v dokumentaci</span><span class="sxs-lookup"><span data-stu-id="78bb0-103">Use links in documentation</span></span>

<span data-ttu-id="78bb0-104">Tento článek popisuje způsob používání hypertextových odkazů ze stránek hostovaných na webu docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="78bb0-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="78bb0-105">Odkazy se snadno přidávají do markdownu pomocí několika různých konvencí.</span><span class="sxs-lookup"><span data-stu-id="78bb0-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="78bb0-106">Odkazy směrují uživatele na obsah na stejné stránce, na jiné sousední stránky nebo na externí weby a adresy URL.</span><span class="sxs-lookup"><span data-stu-id="78bb0-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="78bb0-107">Back-end webu docs.microsoft.com používá platformu OPS (Open Publishing Services), která podporuje markdown kompatibilní s verzí [CommonMark](https://commonmark.org/) parsovaný prostřednictvím parsovacího modulu [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="78bb0-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark](https://commonmark.org/)-compliant markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="78bb0-108">Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)](https://help.github.com/categories/writing-on-github/), protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat.</span><span class="sxs-lookup"><span data-stu-id="78bb0-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="78bb0-109">Další funkce se přidávají prostřednictvím rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="78bb0-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78bb0-110">Všechny odkazy musí být zabezpečené (`https` versus `http`), když to cíl podporuje (což by měla drtivá většina).</span><span class="sxs-lookup"><span data-stu-id="78bb0-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="78bb0-111">Text odkazu</span><span class="sxs-lookup"><span data-stu-id="78bb0-111">Link text</span></span>

<span data-ttu-id="78bb0-112">Slova, která použijete v textu odkazu, by měla být popisná.</span><span class="sxs-lookup"><span data-stu-id="78bb0-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="78bb0-113">Jinými slovy by mělo jít o normální slova nebo název stránky, na kterou odkazujete.</span><span class="sxs-lookup"><span data-stu-id="78bb0-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78bb0-114">Nepoužívejte „klikněte sem“.</span><span class="sxs-lookup"><span data-stu-id="78bb0-114">Do not use "click here."</span></span> <span data-ttu-id="78bb0-115">Je to špatné pro optimalizaci vyhledávacího webu a adekvátně to nepopisuje cílovou stránku.</span><span class="sxs-lookup"><span data-stu-id="78bb0-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="78bb0-116">**Správně:**</span><span class="sxs-lookup"><span data-stu-id="78bb0-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="78bb0-117">**Nesprávně:**</span><span class="sxs-lookup"><span data-stu-id="78bb0-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="78bb0-118">Odkazy z jednoho článku na druhý</span><span class="sxs-lookup"><span data-stu-id="78bb0-118">Links from one article to another</span></span>

<span data-ttu-id="78bb0-119">Pokud chcete vytvořit vložený odkaz (hotlink) z technického článku na webu Docs na jiný technický článek webu Docs v rámci stejné sady *docset*, použijte následující syntax pro odkazy:</span><span class="sxs-lookup"><span data-stu-id="78bb0-119">To create an inline link from a Docs technical article to another Docs technical article within the same *docset*, use the following link syntax:</span></span>

- <span data-ttu-id="78bb0-120">Článek odkazuje na jiný článek ve stejném adresáři:</span><span class="sxs-lookup"><span data-stu-id="78bb0-120">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="78bb0-121">Článek odkazuje na článek v nadřazeném adresáři aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="78bb0-121">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="78bb0-122">Článek odkazuje na článek v podadresáři aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="78bb0-122">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="78bb0-123">Článek odkazuje na článek v podadresáři nadřazeného adresáře aktuálního adresáře:</span><span class="sxs-lookup"><span data-stu-id="78bb0-123">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="78bb0-124">V žádném z předchozích příkladů se jako součást odkazu nepoužívá `~/`.</span><span class="sxs-lookup"><span data-stu-id="78bb0-124">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="78bb0-125">Pokud chcete vytvořit odkaz na absolutní cestu, která začíná v kořenovém adresáři úložiště, začněte odkaz znakem `/`.</span><span class="sxs-lookup"><span data-stu-id="78bb0-125">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="78bb0-126">Při zahrnutí řetězce `~/` vznikají neplatné odkazy pro navigaci do zdrojových úložišť na GitHubu.</span><span class="sxs-lookup"><span data-stu-id="78bb0-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="78bb0-127">Problém se vyřeší, když bude cesta začínat znakem `/`.</span><span class="sxs-lookup"><span data-stu-id="78bb0-127">Starting the path with `/` resolves correctly.</span></span>

<span data-ttu-id="78bb0-128">Jestli chcete vytvořit odkaz na článek v jiné sadě docset, i když je soubor ve stejném úložišti, použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="78bb0-128">To link to an article in a different docset, even if the file is in the same repository, use the following syntax:</span></span>

`[link text](/docset-root/directory/article-name)`
   
<span data-ttu-id="78bb0-129">Pokud například článek, jehož kořenová adresa URL je `https://docs.microsoft.com/dotnet`, odkazuje na článek, jehož kořenová adresa URL je `https://docs.microsoft.com/visualstudio`, odkaz by vypadal takto: `[link text](/visualstudio/directory/article-name)`.</span><span class="sxs-lookup"><span data-stu-id="78bb0-129">For example, if an article whose root URL is `https://docs.microsoft.com/dotnet` links to an article whose root URL is `https://docs.microsoft.com/visualstudio`, the link would look like `[link text](/visualstudio/directory/article-name)`.</span></span>

> [!TIP]
> <span data-ttu-id="78bb0-130">Články ve stejné sadě *docset* mají po docs.microsoft.com stejný fragment adresy URL.</span><span class="sxs-lookup"><span data-stu-id="78bb0-130">Articles in the same *docset* have the same URL fragment after "docs.microsoft.com".</span></span> <span data-ttu-id="78bb0-131">Například `https://docs.microsoft.com/dotnet/core/get-started` a `https://docs.microsoft.com/dotnet/framework/install` jsou ve stejné sadě docset a `https://docs.microsoft.com/dotnet/core/get-started` a `https://docs.microsoft.com/visualstudio/whats-new` jsou v různých sadách docset.</span><span class="sxs-lookup"><span data-stu-id="78bb0-131">For example, `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/dotnet/framework/install` are in the same docset, and `https://docs.microsoft.com/dotnet/core/get-started` and `https://docs.microsoft.com/visualstudio/whats-new` are in different docsets.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="78bb0-132">Odkazy na ukotvení</span><span class="sxs-lookup"><span data-stu-id="78bb0-132">Links to anchors</span></span>

<span data-ttu-id="78bb0-133">Ukotvení vytvářet nemusíte.</span><span class="sxs-lookup"><span data-stu-id="78bb0-133">You do not have to create anchors.</span></span> <span data-ttu-id="78bb0-134">Generují se automaticky pro všechny nadpisy H2 při publikování.</span><span class="sxs-lookup"><span data-stu-id="78bb0-134">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="78bb0-135">Jediné, co musíte udělat, je vytvořit odkazy na oddíly H2.</span><span class="sxs-lookup"><span data-stu-id="78bb0-135">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="78bb0-136">Vytvoření odkazu na nadpis ve stejném článku:</span><span class="sxs-lookup"><span data-stu-id="78bb0-136">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="78bb0-137">Vytvoření odkazu na ukotvení v jiném článku:</span><span class="sxs-lookup"><span data-stu-id="78bb0-137">To link to an anchor in another article:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="78bb0-138">Odkazy z vložených souborů</span><span class="sxs-lookup"><span data-stu-id="78bb0-138">Links from includes</span></span>

<span data-ttu-id="78bb0-139">Jelikož jsou vložené soubory umístěné v jiném adresáři, musíte použít delší relativní cesty.</span><span class="sxs-lookup"><span data-stu-id="78bb0-139">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="78bb0-140">Pokud chcete vytvořit odkaz na článek z vloženého souboru, použijte tento formát:</span><span class="sxs-lookup"><span data-stu-id="78bb0-140">To link to an article from an include file, use this format:</span></span>

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a><span data-ttu-id="78bb0-141">Odkazy v selektorech</span><span class="sxs-lookup"><span data-stu-id="78bb0-141">Links in selectors</span></span>

<span data-ttu-id="78bb0-142">Volič je součást navigace, která se v článku dokumentace zobrazuje ve formě rozevíracího seznamu.</span><span class="sxs-lookup"><span data-stu-id="78bb0-142">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="78bb0-143">Když čtenář vybere nějakou hodnotu v tomto rozevíracím seznamu, otevře prohlížeč vybraný článek.</span><span class="sxs-lookup"><span data-stu-id="78bb0-143">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="78bb0-144">Seznam voliče zpravidla obsahuje odkazy na související články, například na stejnou problematiku v několika programovacích jazycích nebo na úzce související sérii článků.</span><span class="sxs-lookup"><span data-stu-id="78bb0-144">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span> 

<span data-ttu-id="78bb0-145">Pokud máte voliče, které jsou začleněné ve vloženém souboru, použijte následující strukturu odkazu:</span><span class="sxs-lookup"><span data-stu-id="78bb0-145">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a><span data-ttu-id="78bb0-146">Odkazy z referencí</span><span class="sxs-lookup"><span data-stu-id="78bb0-146">Reference-style links</span></span>

<span data-ttu-id="78bb0-147">Pokud chcete, aby byl váš zdrojový obsah lépe čitelný, můžete použít odkazy z referencí.</span><span class="sxs-lookup"><span data-stu-id="78bb0-147">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="78bb0-148">Odkazy z referencí nahradí syntax hotlinku jednodušší syntaxí, která vám umožní přesunout dlouhé adresy URL na konec článku.</span><span class="sxs-lookup"><span data-stu-id="78bb0-148">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="78bb0-149">Zde je příklad z webu [Daring Fireball](https://daringfireball.net/projects/markdown/):</span><span class="sxs-lookup"><span data-stu-id="78bb0-149">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="78bb0-150">Vložený text:</span><span class="sxs-lookup"><span data-stu-id="78bb0-150">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="78bb0-151">Odkazy referencí na konci článku:</span><span class="sxs-lookup"><span data-stu-id="78bb0-151">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
<span data-ttu-id="78bb0-152">Nezapomeňte mezi dvojtečkou a odkazem vytvořit mezeru.</span><span class="sxs-lookup"><span data-stu-id="78bb0-152">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="78bb0-153">Pokud odkazujete na ostatní technické články a zapomenete mezeru vytvořit, odkaz nebude v publikovaném článku fungovat.</span><span class="sxs-lookup"><span data-stu-id="78bb0-153">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="78bb0-154">Odkazování na stránky, které nejsou součástí sady technické dokumentace</span><span class="sxs-lookup"><span data-stu-id="78bb0-154">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="78bb0-155">Pokud chcete vytvořit odkaz na jiný web ve vlastnictví Microsoftu (jako je stránka s ceníkem, stránka SLA nebo cokoli jiného, co není článek dokumentace), použijte absolutní adresu URL, ale vynechejte národní prostředí.</span><span class="sxs-lookup"><span data-stu-id="78bb0-155">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="78bb0-156">Cílem je, aby odkazy fungovaly v GitHubu a na zobrazené stránce:</span><span class="sxs-lookup"><span data-stu-id="78bb0-156">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a><span data-ttu-id="78bb0-157">Odkazy na weby třetích stran</span><span class="sxs-lookup"><span data-stu-id="78bb0-157">Links to third-party sites</span></span>

<span data-ttu-id="78bb0-158">Nejlepší uživatelské prostředí minimalizuje odchod uživatelů na jiný web.</span><span class="sxs-lookup"><span data-stu-id="78bb0-158">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="78bb0-159">Odkazy na weby třetích stran, které jsou občas potřeba, proto vytvářejte na základě těchto informací:</span><span class="sxs-lookup"><span data-stu-id="78bb0-159">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="78bb0-160">**Odpovědnost:** Když jde o informace, které má sdílet třetí strana, odkazujte na obsah třetí strany.</span><span class="sxs-lookup"><span data-stu-id="78bb0-160">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="78bb0-161">Úkolem Microsoftu například není říkat lidem, jak používat vývojářské nástroje pro Android – to má udělat Google.</span><span class="sxs-lookup"><span data-stu-id="78bb0-161">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="78bb0-162">Pokud je to potřeba, můžeme vysvětlit, jak vývojářské nástroje pro Android používat *se* službou Azure, ale jak tyto nástroje celkově používat by měl vysvětlit Google.</span><span class="sxs-lookup"><span data-stu-id="78bb0-162">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="78bb0-163">**Schválení od PM:** O schválení obsahu třetí strany požádejte Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78bb0-163">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="78bb0-164">Odkazování na takový obsah znamená, že mu důvěřujeme, a zahrnuje odpovědnost, pokud se lidé těmito pokyny budou řídit.</span><span class="sxs-lookup"><span data-stu-id="78bb0-164">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="78bb0-165">**Kontroly aktuálnosti:** Ověřujte, jestli jsou informace třetí strany stále aktuální, správné a relevantní a jestli se odkaz nezměnil.</span><span class="sxs-lookup"><span data-stu-id="78bb0-165">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="78bb0-166">**Přesměrování ven:** Informujte uživatele, že budou přesměrováni na jiný web.</span><span class="sxs-lookup"><span data-stu-id="78bb0-166">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="78bb0-167">Pokud to není jasné z kontextu, přidejte vysvětlení.</span><span class="sxs-lookup"><span data-stu-id="78bb0-167">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="78bb0-168">Například: „Požadavky zahrnují vývojářské nástroje pro Android, které si můžete stáhnout z webu Android Studio.“</span><span class="sxs-lookup"><span data-stu-id="78bb0-168">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="78bb0-169">**Další kroky:** V sekci Další kroky můžete přidat odkaz například na blog MVP.</span><span class="sxs-lookup"><span data-stu-id="78bb0-169">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="78bb0-170">Jen uživatele znovu nezapomeňte informovat, že budou přesměrováni na jiný web.</span><span class="sxs-lookup"><span data-stu-id="78bb0-170">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="78bb0-171">**Právní náležitosti:** Jsme právně krytí částí **Odkazy na weby třetích stran** v **Podmínkách použití** uvedených v zápatí každé stránky ms.com.</span><span class="sxs-lookup"><span data-stu-id="78bb0-171">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="78bb0-172">Odkazy na referenční obsah Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="78bb0-172">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="78bb0-173">Referenční obsah Azure PowerShell prošel od listopadu 2016 několika změnami.</span><span class="sxs-lookup"><span data-stu-id="78bb0-173">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="78bb0-174">Pro odkazování na tento obsah z jiných článků na webu docs.microsoft.com použijte následující pokyny.</span><span class="sxs-lookup"><span data-stu-id="78bb0-174">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="78bb0-175">Struktura adresy URL:</span><span class="sxs-lookup"><span data-stu-id="78bb0-175">Structure of the URL:</span></span>

* <span data-ttu-id="78bb0-176">Pro rutiny:</span><span class="sxs-lookup"><span data-stu-id="78bb0-176">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="78bb0-177">Pro koncepční témata:</span><span class="sxs-lookup"><span data-stu-id="78bb0-177">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="78bb0-178">Část `<moniker-name>` je volitelná.</span><span class="sxs-lookup"><span data-stu-id="78bb0-178">The `<moniker-name>` portion is optional.</span></span> <span data-ttu-id="78bb0-179">Pokud ji vynecháte, budete přesměrováni na nejnovější verzi obsahu.</span><span class="sxs-lookup"><span data-stu-id="78bb0-179">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="78bb0-180">Část `<service-name>` je jedním z příkladů uvedených v následujících základních adresách URL:</span><span class="sxs-lookup"><span data-stu-id="78bb0-180">The `<service-name>` portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="78bb0-181">Obsah Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span><span class="sxs-lookup"><span data-stu-id="78bb0-181">Azure PowerShell (AzureRM) content: [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)</span></span>
- <span data-ttu-id="78bb0-182">Obsah Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span><span class="sxs-lookup"><span data-stu-id="78bb0-182">Azure PowerShell (ASM) content: [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)</span></span>
- <span data-ttu-id="78bb0-183">Obsah Azure Active Directory (AzureAD) PowerShell: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span><span class="sxs-lookup"><span data-stu-id="78bb0-183">Azure Active Directory (AzureAD) PowerShell content: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)</span></span>
- <span data-ttu-id="78bb0-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span><span class="sxs-lookup"><span data-stu-id="78bb0-184">Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)</span></span>
- <span data-ttu-id="78bb0-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span><span class="sxs-lookup"><span data-stu-id="78bb0-185">Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)</span></span>
- <span data-ttu-id="78bb0-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span><span class="sxs-lookup"><span data-stu-id="78bb0-186">Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)</span></span>

<span data-ttu-id="78bb0-187">Když tyto adresy URL použijete, budete přesměrováni na nejnovější verzi obsahu.</span><span class="sxs-lookup"><span data-stu-id="78bb0-187">When you use these URLs, you'll be redirected to the latest version of the content.</span></span> <span data-ttu-id="78bb0-188">Tímto způsobem nemusíte určovat verzi parametru moniker.</span><span class="sxs-lookup"><span data-stu-id="78bb0-188">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="78bb0-189">Nebudete tak mít odkazy na koncepční obsah, které se musí při změně verze aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="78bb0-189">And, you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="78bb0-190">Pokud chcete vytvořit správný odkaz, najděte ve svém prohlížeči stránku, na kterou chcete odkázat, zkopírujte její adresu URL a pak odeberte kód národního prostředí, například **en-us**.</span><span class="sxs-lookup"><span data-stu-id="78bb0-190">To create the correct link, find the page that you want to link to in your browser, copy the URL, and then remove the locale code, for example, **en-us**.</span></span>

<span data-ttu-id="78bb0-191">Příklad Markdownu:</span><span class="sxs-lookup"><span data-stu-id="78bb0-191">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](https://docs.microsoft.com/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](https://docs.microsoft.com/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-azurerm-ps)
```
