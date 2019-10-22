---
title: Šablona a stručná nápověda k článkům o PowerShellu
description: V tomto článku najdete praktickou šablonu, kterou můžete použít k vytvoření nových článků tvořících dokumentaci k PowerShellu.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290350"
---
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="88d93-103">Průvodce správným stylem jazyka Markdown pro dokumentaci k PowerShellu</span><span class="sxs-lookup"><span data-stu-id="88d93-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="88d93-104">Tento článek obsahuje konkrétní pokyny týkající se stylu obsahu dokumentace k PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="88d93-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="88d93-105">Další pokyny, které se týkají stylu psaní, najdete v [průvodci správným stylem od Microsoftu](https://docs.microsoft.com/style-guide/welcome/).</span><span class="sxs-lookup"><span data-stu-id="88d93-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="88d93-106">Metadata</span><span class="sxs-lookup"><span data-stu-id="88d93-106">Metadata</span></span>

<span data-ttu-id="88d93-107">Tato šablona obsahuje příklady syntaxe jazyka Markdown a pokyny k nastavení metadat.</span><span class="sxs-lookup"><span data-stu-id="88d93-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="88d93-108">Při vytváření souboru Markdown byste měli přiloženou šablonu zkopírovat do nového souboru, vyplnit metadata podle tohoto návodu a nastavit záhlaví H1 jako nadpis článku.</span><span class="sxs-lookup"><span data-stu-id="88d93-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="88d93-109">Požadovaný blok metadat je v následujícím ukázkovém bloku metadat:</span><span class="sxs-lookup"><span data-stu-id="88d93-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="88d93-110">Mezi dvojtečkou (:) a hodnotou prvku metadat **musí** být mezera.</span><span class="sxs-lookup"><span data-stu-id="88d93-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="88d93-111">Dvojtečky v hodnotě (třeba v nadpisu) způsobí chybu analyzátoru metadat.</span><span class="sxs-lookup"><span data-stu-id="88d93-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="88d93-112">V takovém případě dejte nadpis do dvojitých uvozovek (příklad: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="88d93-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="88d93-113">**author** (autor): Pole autora musí obsahovat **uživatelské jméno autora na GitHubu**.</span><span class="sxs-lookup"><span data-stu-id="88d93-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="88d93-114">**description** (popis): Shrnuje obsah článku.</span><span class="sxs-lookup"><span data-stu-id="88d93-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="88d93-115">Většinou se zobrazuje na stránce s výsledky hledání, ale nepoužívá se k řazení výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="88d93-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="88d93-116">Měl by mít 115–145 znaků (včetně mezer).</span><span class="sxs-lookup"><span data-stu-id="88d93-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="88d93-117">**ms.date**: Datum poslední významné aktualizace.</span><span class="sxs-lookup"><span data-stu-id="88d93-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="88d93-118">U stávajících článků datum aktualizujte, pokud zkontrolujete a aktualizujete celý článek.</span><span class="sxs-lookup"><span data-stu-id="88d93-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="88d93-119">U malých oprav, jako jsou opravy překlepů apod., nejde o aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="88d93-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="88d93-120">**title** (název): Zobrazí se ve výsledcích vyhledávačů.</span><span class="sxs-lookup"><span data-stu-id="88d93-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="88d93-121">Nadpis nemusí přesně odpovídat názvu v nadpisu H1, ale měl by mít maximálně 60 znaků.</span><span class="sxs-lookup"><span data-stu-id="88d93-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="88d93-122">Ke každému článku jsou připojená další metadata, ale většinu hodnot metadat obvykle používáme na úrovni složky zadané v souboru **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="88d93-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="88d93-123">Terminologie produktu</span><span class="sxs-lookup"><span data-stu-id="88d93-123">Product Terminology</span></span>

<span data-ttu-id="88d93-124">Existují různé varianty PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="88d93-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="88d93-125">V této tabulce jsou definované různé výrazy používané k vysvětlení PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="88d93-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="88d93-126">**PowerShell** – výchozí produkt.</span><span class="sxs-lookup"><span data-stu-id="88d93-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="88d93-127">PowerShell je produkt, který dodáváme.</span><span class="sxs-lookup"><span data-stu-id="88d93-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="88d93-128">Výraz PowerShell může popisovat libovolnou edici produktu.</span><span class="sxs-lookup"><span data-stu-id="88d93-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="88d93-129">**PowerShell Core** – PowerShell vytvořený v modulu .NET Core Common Language Runtime (CoreCLR) pro některou z podporovaných platforem.</span><span class="sxs-lookup"><span data-stu-id="88d93-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="88d93-130">**Windows PowerShell** – PowerShell vytvořený v modulu .NET Framework Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="88d93-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="88d93-131">Windows PowerShell se dodává jenom ve Windows a vyžaduje celý modul .Net Framework CLR.</span><span class="sxs-lookup"><span data-stu-id="88d93-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="88d93-132">Obecně platí, že odkazy na „Windows PowerShell“ můžete v dokumentaci změnit na „PowerShell“.</span><span class="sxs-lookup"><span data-stu-id="88d93-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="88d93-133">„Windows PowerShell“ byste ale **neměli** měnit, pokud mluvíte o určité technologii Windows.</span><span class="sxs-lookup"><span data-stu-id="88d93-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="88d93-134">Základy jazyka Markdown (GFM) a speciální znaky</span><span class="sxs-lookup"><span data-stu-id="88d93-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="88d93-135">Základy jazyka Markdown také označované jako GitHub Flavored Markdown (GFM) a určité přípony OPS jsou v obecných článcích o [Markdownu](../how-to-write-use-markdown.md) a v [referenčních materiálech k Markdownu](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="88d93-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](../how-to-write-use-markdown.md) and [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="88d93-136">Markdown používá k formátování zvláštní znaky, například \*, \` a \#.</span><span class="sxs-lookup"><span data-stu-id="88d93-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="88d93-137">Pokud chcete některý z těchto znaků přidat do obsahu, máte na výběr dvě možnosti:</span><span class="sxs-lookup"><span data-stu-id="88d93-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="88d93-138">Dejte před speciální znak zpětné lomítko, abyste znak vyloučili (třeba `\*` pro \*).</span><span class="sxs-lookup"><span data-stu-id="88d93-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="88d93-139">Použijte pro znak [kód entity HTML](http://www.ascii.cl/htmlcodes.htm) (třeba `&#42;` pro &#42;).</span><span class="sxs-lookup"><span data-stu-id="88d93-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="88d93-140">Soubory Markdown by měly používat prostý text v kódování ASCII nebo UTF-8.</span><span class="sxs-lookup"><span data-stu-id="88d93-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="88d93-141">Vyhýbejte se ale vícebajtovým znakům v kódování UTF-8.</span><span class="sxs-lookup"><span data-stu-id="88d93-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="88d93-142">Raději použijte prvek HTML.</span><span class="sxs-lookup"><span data-stu-id="88d93-142">Instead use an HTML entity.</span></span> <span data-ttu-id="88d93-143">Například pro symbol autorských práv použijte `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="88d93-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="88d93-144">Vykreslí se jako &copy;.</span><span class="sxs-lookup"><span data-stu-id="88d93-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="88d93-145">Hypertextové odkazy</span><span class="sxs-lookup"><span data-stu-id="88d93-145">Hyperlinks</span></span>

- <span data-ttu-id="88d93-146">Vyhýbejte se používání neupravených adres URL.</span><span class="sxs-lookup"><span data-stu-id="88d93-146">Avoid using bare URLs.</span></span> <span data-ttu-id="88d93-147">Odkazy by měly mít syntaxi jazyka Markdown: `[friendlyname](url-or-path)`.</span><span class="sxs-lookup"><span data-stu-id="88d93-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="88d93-148">Odkazy musí mít popisný název. Většinou je to nadpis propojeného tématu.</span><span class="sxs-lookup"><span data-stu-id="88d93-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="88d93-149">Všechny položky v závěrečném oddílu Související odkazy musí být hypertextové odkazy.</span><span class="sxs-lookup"><span data-stu-id="88d93-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="88d93-150">Při vytváření odkazů na jiný obsah, který je hostovaný na webu **docs.microsoft.com**, použijte relativní odkazy.</span><span class="sxs-lookup"><span data-stu-id="88d93-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="88d93-151">V závorkách hypertextového odkazu nepoužívejte zpětné apostrofy, tučné písmo ani jiné značky.</span><span class="sxs-lookup"><span data-stu-id="88d93-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="88d93-152">Podrobnější informace o vytváření odkazů najdete v tématu [Používání odkazů v dokumentaci](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="88d93-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="88d93-153">Názvy souborů</span><span class="sxs-lookup"><span data-stu-id="88d93-153">Filenames</span></span>

<span data-ttu-id="88d93-154">Názvy souborů se řídí následujícími pravidly:</span><span class="sxs-lookup"><span data-stu-id="88d93-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="88d93-155">Obsahují jenom písmena, číslice a pomlčky.</span><span class="sxs-lookup"><span data-stu-id="88d93-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="88d93-156">Nesmí obsahovat mezery ani interpunkční znaménka.</span><span class="sxs-lookup"><span data-stu-id="88d93-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="88d93-157">K oddělení slov a čísel v názvu souboru používejte pomlčky.</span><span class="sxs-lookup"><span data-stu-id="88d93-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="88d93-158">Používejte slovesa, která vyjadřují určitou činnost, třeba develop (vyvíjet), buy (koupit), build (sestavit) nebo troubleshoot (řešit potíže).</span><span class="sxs-lookup"><span data-stu-id="88d93-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="88d93-159">Nepoužívejte slova s koncovkou -ing.</span><span class="sxs-lookup"><span data-stu-id="88d93-159">No -ing words.</span></span>
- <span data-ttu-id="88d93-160">Nepoužívejte krátká slova (nepoužívejte členy a spojky a, and, the, in, or atd.).</span><span class="sxs-lookup"><span data-stu-id="88d93-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="88d93-161">Musí být ve formátu Markdown a mít příponu souboru .md.</span><span class="sxs-lookup"><span data-stu-id="88d93-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="88d93-162">Názvy souborů musí být krátké,</span><span class="sxs-lookup"><span data-stu-id="88d93-162">Keep file names reasonably short.</span></span> <span data-ttu-id="88d93-163">protože tvoří část adresy URL vašich článků.</span><span class="sxs-lookup"><span data-stu-id="88d93-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="88d93-164">Prázdné řádky, mezery a tabulátory</span><span class="sxs-lookup"><span data-stu-id="88d93-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="88d93-165">Odeberte duplicitní prázdné řádky.</span><span class="sxs-lookup"><span data-stu-id="88d93-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="88d93-166">Více prázdných řádků se v HTML vykreslí jako jeden prázdný řádek, takže není potřeba používat více prázdných řádků.</span><span class="sxs-lookup"><span data-stu-id="88d93-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="88d93-167">Prázdné řádky v jazyce Markdown také signalizují konec bloku.</span><span class="sxs-lookup"><span data-stu-id="88d93-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="88d93-168">Mezi různými typy bloků jazyka Markdown (například mezi odstavcem a seznamem nebo nadpisem) by měl být jeden prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="88d93-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="88d93-169">Mezery jsou v jazyce Markdown důležité.</span><span class="sxs-lookup"><span data-stu-id="88d93-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="88d93-170">Vždy používejte mezery, nikoli pevné tabulátory.</span><span class="sxs-lookup"><span data-stu-id="88d93-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="88d93-171">Odeberte nadbytečné mezery na konci řádků.</span><span class="sxs-lookup"><span data-stu-id="88d93-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="88d93-172">Nadpisy a záhlaví</span><span class="sxs-lookup"><span data-stu-id="88d93-172">Titles and headings</span></span>

<span data-ttu-id="88d93-173">Používejte jenom [nadpisy ATX][atx] (hlavičky ve tvaru # místo tvaru `=` nebo `-`).</span><span class="sxs-lookup"><span data-stu-id="88d93-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="88d93-174">Používejte velká písmena jako ve větě. Velkým písmenem by měla začínat jenom vlastní jména a první písmeno nadpisu nebo záhlaví.</span><span class="sxs-lookup"><span data-stu-id="88d93-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="88d93-175">Mezi znakem `#` a prvním písmenem nadpisu musí být jedna mezera.</span><span class="sxs-lookup"><span data-stu-id="88d93-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="88d93-176">Nadpisy musí být obklopeny jedním prázdným řádkem.</span><span class="sxs-lookup"><span data-stu-id="88d93-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="88d93-177">Dokument má jenom jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="88d93-177">Only one H1 per document</span></span>
- <span data-ttu-id="88d93-178">Úrovně nadpisů by se měly zvyšovat vždy o jednu úroveň. Nepřeskakujte úrovně.</span><span class="sxs-lookup"><span data-stu-id="88d93-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="88d93-179">Nepoužívejte v nadpisech zpětné apostrofy, tučné písmo ani jiné značky.</span><span class="sxs-lookup"><span data-stu-id="88d93-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="88d93-180">Schéma odkazů na referenční rutiny v modulu [PlatyPS][platyPS] vyžaduje zvláštní nadpisy H2 a H3.</span><span class="sxs-lookup"><span data-stu-id="88d93-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="88d93-181">Přidání nebo odebrání nadpisů může poškodit sestavení.</span><span class="sxs-lookup"><span data-stu-id="88d93-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="88d93-182">Další informace najdete v [referenčním průvodci správným stylem rutin](powershell-style-reference.md).</span><span class="sxs-lookup"><span data-stu-id="88d93-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="88d93-183">Omezení délky řádku na 100 znaků</span><span class="sxs-lookup"><span data-stu-id="88d93-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="88d93-184">Zjednoduší se tím výstup příkazového řádku v podobě rozdílů a historie.</span><span class="sxs-lookup"><span data-stu-id="88d93-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="88d93-185">Toto pravidlo neplatilo u většiny stávajícího obsahu v dokumentaci k PowerShellu, ale postupně pracujeme na jeho zavedení.</span><span class="sxs-lookup"><span data-stu-id="88d93-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="88d93-186">Budeme rádi, když nám pomůžete. K jednoduchému přeformátování odstavců na tuto délku můžete v editoru Visual Studio Code (VSCode) použít [rozšíření reflow][reflow].</span><span class="sxs-lookup"><span data-stu-id="88d93-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="88d93-187">Seznamy</span><span class="sxs-lookup"><span data-stu-id="88d93-187">Lists</span></span>

<span data-ttu-id="88d93-188">Pokud seznam obsahuje několik vět nebo odstavců, raději místo seznamu použijte podnadpis nižší úrovně.</span><span class="sxs-lookup"><span data-stu-id="88d93-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="88d93-189">Kolem seznamu musí být jeden prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="88d93-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="88d93-190">Neuspořádané seznamy</span><span class="sxs-lookup"><span data-stu-id="88d93-190">Unordered lists</span></span>

<span data-ttu-id="88d93-191">Nezakončujte položky seznamu tečkou, pokud neobsahují více vět.</span><span class="sxs-lookup"><span data-stu-id="88d93-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="88d93-192">Jako odrážky u položek seznamu používejte znak spojovníku (`-`).</span><span class="sxs-lookup"><span data-stu-id="88d93-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="88d93-193">Vyhnete se tím záměně se značkou tučného písma nebo kurzívy, kterou je hvězdička [`*`].</span><span class="sxs-lookup"><span data-stu-id="88d93-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="88d93-194">Pokud chcete do položky s odrážkou zahrnout odstavec nebo jiné prvky, vložte konec řádku a zarovnejte odsazení podle prvního znaku za odrážkou.</span><span class="sxs-lookup"><span data-stu-id="88d93-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="88d93-195">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="88d93-196">Tento seznam obsahuje pod odrážkou dílčí prvky.</span><span class="sxs-lookup"><span data-stu-id="88d93-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="88d93-197">Odrážka první položky</span><span class="sxs-lookup"><span data-stu-id="88d93-197">First bullet item</span></span>

  <span data-ttu-id="88d93-198">Věta, která vysvětluje první odrážku.</span><span class="sxs-lookup"><span data-stu-id="88d93-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="88d93-199">Dílčí odrážka s položkou</span><span class="sxs-lookup"><span data-stu-id="88d93-199">Sub-bullet item</span></span>

    <span data-ttu-id="88d93-200">Věta, která vysvětluje dílčí odrážku.</span><span class="sxs-lookup"><span data-stu-id="88d93-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="88d93-201">Odrážka druhé položky</span><span class="sxs-lookup"><span data-stu-id="88d93-201">Second bullet item</span></span>
- <span data-ttu-id="88d93-202">Odrážka třetí položky</span><span class="sxs-lookup"><span data-stu-id="88d93-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="88d93-203">Uspořádané seznamy</span><span class="sxs-lookup"><span data-stu-id="88d93-203">Ordered lists</span></span>

<span data-ttu-id="88d93-204">Pokud položka číslovaného seznamu obsahuje odstavec nebo jiné prvky, zarovnejte odsazení s prvním znakem za číslem položky.</span><span class="sxs-lookup"><span data-stu-id="88d93-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

<span data-ttu-id="88d93-205">Jak to udělat:</span><span class="sxs-lookup"><span data-stu-id="88d93-205">to get this output:</span></span>

> 1. <span data-ttu-id="88d93-206">U prvního prvku vložte za číslo 1 jednu mezeru.</span><span class="sxs-lookup"><span data-stu-id="88d93-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="88d93-207">Dlouhá souvětí musí být zalomena na další řádek a musí být zarovnaná s prvním znakem za značkou číslovaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="88d93-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="88d93-208">Pokud chcete přidat druhý prvek (viz tento příklad), vložte za první prvek zalomení řádku a zarovnejte odsazení.</span><span class="sxs-lookup"><span data-stu-id="88d93-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="88d93-209">Odsazení druhého prvku musí být zarovnané s prvním znakem, který je za značkou číslovaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="88d93-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="88d93-210">U jednociferných položek, jako je například tato, odsadíte text do 4. sloupce.</span><span class="sxs-lookup"><span data-stu-id="88d93-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="88d93-211">U dvouciferných položek, jako je například položka číslo 10, odsadíte text do 5. sloupce.</span><span class="sxs-lookup"><span data-stu-id="88d93-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="88d93-212">Tady začíná další číslovaná položka.</span><span class="sxs-lookup"><span data-stu-id="88d93-212">The next numbered item starts here.</span></span>

<span data-ttu-id="88d93-213">Všechny položky číslovaného seznamu musí mít číslo `1.` místo zvyšujícího se čísla u každé položky.</span><span class="sxs-lookup"><span data-stu-id="88d93-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="88d93-214">Markdown při vykreslení hodnotu automaticky zvýší.</span><span class="sxs-lookup"><span data-stu-id="88d93-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="88d93-215">Tím se zjednoduší změna pořadí položek a standardizuje se odsazení podřízeného obsahu.</span><span class="sxs-lookup"><span data-stu-id="88d93-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="88d93-216">Syntaktické prvky formátování příkazů</span><span class="sxs-lookup"><span data-stu-id="88d93-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="88d93-217">Názvy rutin PowerShellu používají [psaní velkých a malých písmen podle jazyka Pascal][pascal-case].</span><span class="sxs-lookup"><span data-stu-id="88d93-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="88d93-218">Slovesa jsou od podstatných jmen oddělena pomlčkou.</span><span class="sxs-lookup"><span data-stu-id="88d93-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="88d93-219">U rutin a parametrů vždy používejte jejich plný název s velkými a malými písmeny jako v jazyce Pascal.</span><span class="sxs-lookup"><span data-stu-id="88d93-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="88d93-220">Raději nepoužívejte aliasy, pokud o nich výslovně nehovoříte.</span><span class="sxs-lookup"><span data-stu-id="88d93-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="88d93-221">V odstavci ohraničte klíčová slova jazyka, názvy rutin a odkazy na proměnné znaky zpětného apostrofu (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="88d93-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="88d93-222">Názvy vlastností, parametrů a tříd mají být **tučně**.</span><span class="sxs-lookup"><span data-stu-id="88d93-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="88d93-223">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="88d93-224">Když odkazujete na parametr jeho názvem, měl by být tento název **tučným písmem**.</span><span class="sxs-lookup"><span data-stu-id="88d93-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="88d93-225">Když popisujete použití parametru s předponou ve tvaru spojovníku, dejte parametr do zpětných apostrofů.</span><span class="sxs-lookup"><span data-stu-id="88d93-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="88d93-226">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="88d93-227">V odkazech na externí příkazy (soubory EXE, skripty apod.) by měl být název příkazu tučným písmem, všechna písmena malá (nebo s velkým počátečním písmenem, pokud jde o začátek věty) a měl by být včetně příslušné přípony souboru.</span><span class="sxs-lookup"><span data-stu-id="88d93-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="88d93-228">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="88d93-229">Pokud předvádíte příklad použití externího příkazu, měli byste ho dát do zpětných apostrofů.</span><span class="sxs-lookup"><span data-stu-id="88d93-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="88d93-230">Pokud název koliduje s aliasem, musíte v ukázkovém příkladu uvést i příponu souboru.</span><span class="sxs-lookup"><span data-stu-id="88d93-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="88d93-231">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="88d93-232">Při psaní koncepčního článku (na rozdíl od referenčního obsahu), musí první instance názvu rutiny představovat hypertextový odkaz na dokumentaci k dané rutině.</span><span class="sxs-lookup"><span data-stu-id="88d93-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="88d93-233">V závorkách hypertextového odkazu nepoužívejte zpětné apostrofy, tučné písmo ani jiné značky.</span><span class="sxs-lookup"><span data-stu-id="88d93-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="88d93-234">Například:</span><span class="sxs-lookup"><span data-stu-id="88d93-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="88d93-235">Další informace najdete v části [Hypertextové odkazy](#hyperlinks) v průvodci správným stylem.</span><span class="sxs-lookup"><span data-stu-id="88d93-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="88d93-236">Obrázky</span><span class="sxs-lookup"><span data-stu-id="88d93-236">Images</span></span>

<span data-ttu-id="88d93-237">Syntaxe pro začlenění obrázku:</span><span class="sxs-lookup"><span data-stu-id="88d93-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="88d93-238">Příklad:</span><span class="sxs-lookup"><span data-stu-id="88d93-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="88d93-239">`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="88d93-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="88d93-240">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="88d93-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="88d93-241">Tento text je také užitečný v případě chyby na webu, kdy obrázek nejde vykreslit.</span><span class="sxs-lookup"><span data-stu-id="88d93-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="88d93-242">Obrázky by se měly ukládat do složky `media/<article-name>`, která je ve složce obsahující váš článek.</span><span class="sxs-lookup"><span data-stu-id="88d93-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="88d93-243">Obrázky by se neměly mezi články sdílet.</span><span class="sxs-lookup"><span data-stu-id="88d93-243">Images should not be shared between articles.</span></span> <span data-ttu-id="88d93-244">Ve složce `media` vytvořte složku, která odpovídá názvu souboru vašeho článku.</span><span class="sxs-lookup"><span data-stu-id="88d93-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="88d93-245">Obrázky k danému článku zkopírujte do této nové složky.</span><span class="sxs-lookup"><span data-stu-id="88d93-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="88d93-246">Pokud se obrázek používá ve více článcích, musí být v každé složce obrázků také kopie daného obrázkového souboru.</span><span class="sxs-lookup"><span data-stu-id="88d93-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="88d93-247">Takový postup brání tomu, aby změna obrázku v jednom článku měli vliv na jiný článek.</span><span class="sxs-lookup"><span data-stu-id="88d93-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="88d93-248">V některých případech chcete sdílet obrázky, třeba loga a ikony, ve více článcích.</span><span class="sxs-lookup"><span data-stu-id="88d93-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="88d93-249">Takové obrázky se ukládají do složky `/media/shared` v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="88d93-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="88d93-250">Podporované jsou následující typy obrázkových souborů: \*.png, \*.gif, \*.jpeg, \*.jpg a \*.svg.</span><span class="sxs-lookup"><span data-stu-id="88d93-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
