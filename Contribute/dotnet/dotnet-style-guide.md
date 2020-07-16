---
title: Šablona a stručná nápověda k článkům o .NET
description: V tomto článku najdete praktickou šablonu, kterou můžete použít k vytvoření nových článků pro úložiště dokumentace k .NET.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 926516895798757bde0861a345e0b5d0f95218a4
ms.sourcegitcommit: 5f5fc0fc2ff64610cc19a4b40cb3313adbc152cd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/13/2020
ms.locfileid: "86290904"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="262da-103">Metadata a šablona v Markdownu pro dokumentaci k .NET</span><span class="sxs-lookup"><span data-stu-id="262da-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="262da-104">Tato šablona pro dotnet/dokumentaci obsahuje příklady syntaxe jazyka Markdown a pokyny k nastavení metadat.</span><span class="sxs-lookup"><span data-stu-id="262da-104">This dotnet/docs template contains examples of Markdown syntax and guidance on setting the metadata.</span></span>

<span data-ttu-id="262da-105">Při vytváření souboru Markdown zkopírujte přiloženou šablonu do nového souboru, vyplňte metadata podle návodu níže a nastavte nadpis H1 výše na název článku.</span><span class="sxs-lookup"><span data-stu-id="262da-105">When creating a Markdown file, copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="262da-106">Metadata</span><span class="sxs-lookup"><span data-stu-id="262da-106">Metadata</span></span>

<span data-ttu-id="262da-107">Požadovaný blok metadat je v následujícím ukázkovém bloku metadat:</span><span class="sxs-lookup"><span data-stu-id="262da-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="262da-108">Mezi dvojtečkou (:) a hodnotou prvku metadat **musí** být mezera.</span><span class="sxs-lookup"><span data-stu-id="262da-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="262da-109">Dvojtečky v hodnotě (třeba v nadpisu) způsobí chybu analyzátoru metadat.</span><span class="sxs-lookup"><span data-stu-id="262da-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="262da-110">V takovém případě dejte nadpis do dvojitých uvozovek (příklad: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="262da-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="262da-111">**title** (název): Zobrazí se ve výsledcích vyhledávačů.</span><span class="sxs-lookup"><span data-stu-id="262da-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="262da-112">Nadpis nemusí být stejný jako nadpis v záhlaví H1 a nesmí být delší než 60 znaků.</span><span class="sxs-lookup"><span data-stu-id="262da-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="262da-113">**description** (popis): Shrnuje obsah článku.</span><span class="sxs-lookup"><span data-stu-id="262da-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="262da-114">Většinou se zobrazuje na stránce s výsledky hledání, ale nepoužívá se k řazení výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="262da-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="262da-115">Měl by mít 115–145 znaků (včetně mezer).</span><span class="sxs-lookup"><span data-stu-id="262da-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="262da-116">**author** (autor): Pole autora musí obsahovat **uživatelské jméno autora na GitHubu**.</span><span class="sxs-lookup"><span data-stu-id="262da-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="262da-117">**ms.date**: Datum poslední významné aktualizace.</span><span class="sxs-lookup"><span data-stu-id="262da-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="262da-118">U stávajících článků datum aktualizujte, pokud zkontrolujete a aktualizujete celý článek.</span><span class="sxs-lookup"><span data-stu-id="262da-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="262da-119">U malých oprav, jako jsou opravy překlepů apod., nejde o aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="262da-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="262da-120">Ke každému článku jsou připojená další metadata, ale většinu hodnot metadat obvykle používáme na úrovni složky zadané v souboru **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="262da-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="262da-121">Základy jazyka Markdown (GFM) a speciální znaky</span><span class="sxs-lookup"><span data-stu-id="262da-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="262da-122">Základní informace o jazyce Markdown, variantě GitHub Flavored Markdown (GFM) a rozšířeních specifických pro OPS najdete v článku [Referenční informace k jazyku Markdown](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="262da-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS-specific extensions in the [Markdown reference](../markdown-reference.md) article.</span></span>

<span data-ttu-id="262da-123">Markdown používá k formátování zvláštní znaky, například \*, \` a \#.</span><span class="sxs-lookup"><span data-stu-id="262da-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="262da-124">Pokud chcete některý z těchto znaků přidat do obsahu, máte na výběr dvě možnosti:</span><span class="sxs-lookup"><span data-stu-id="262da-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="262da-125">Dejte před speciální znak zpětné lomítko jako „řídicí znak“ (například `\*` pro \*).</span><span class="sxs-lookup"><span data-stu-id="262da-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*).</span></span>
- <span data-ttu-id="262da-126">Použijte pro znak [kód entity HTML](http://www.ascii.cl/htmlcodes.htm) (třeba `&#42;` pro &#42;).</span><span class="sxs-lookup"><span data-stu-id="262da-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="262da-127">Názvy souborů</span><span class="sxs-lookup"><span data-stu-id="262da-127">File names</span></span>

<span data-ttu-id="262da-128">Pro názvy souborů platí následující pravidla:</span><span class="sxs-lookup"><span data-stu-id="262da-128">File names use the following rules:</span></span>

* <span data-ttu-id="262da-129">Smí obsahovat jenom malá písmena, číslice a pomlčky.</span><span class="sxs-lookup"><span data-stu-id="262da-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="262da-130">Nesmí obsahovat mezery ani interpunkční znaménka.</span><span class="sxs-lookup"><span data-stu-id="262da-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="262da-131">K oddělení slov a čísel v názvu souboru používejte pomlčky.</span><span class="sxs-lookup"><span data-stu-id="262da-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="262da-132">Používejte slovesa, která vyjadřují určitou činnost, třeba develop (vyvíjet), buy (koupit), build (sestavit) nebo troubleshoot (řešit potíže).</span><span class="sxs-lookup"><span data-stu-id="262da-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="262da-133">Nepoužívejte slova s koncovkou -ing.</span><span class="sxs-lookup"><span data-stu-id="262da-133">No -ing words.</span></span>
* <span data-ttu-id="262da-134">Nepoužívejte krátká slova (nepoužívejte členy a spojky a, and, the, in, or atd.).</span><span class="sxs-lookup"><span data-stu-id="262da-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="262da-135">Musí být ve formátu Markdown a mít příponu souboru .md.</span><span class="sxs-lookup"><span data-stu-id="262da-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="262da-136">Názvy souborů musí být krátké,</span><span class="sxs-lookup"><span data-stu-id="262da-136">Keep file names reasonably short.</span></span> <span data-ttu-id="262da-137">protože tvoří část adresy URL vašich článků.</span><span class="sxs-lookup"><span data-stu-id="262da-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="262da-138">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="262da-138">Headings</span></span>

<span data-ttu-id="262da-139">Používejte velká písmena jako při psaní věty.</span><span class="sxs-lookup"><span data-stu-id="262da-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="262da-140">První slovo v nadpisu musí začínat velkým písmenem.</span><span class="sxs-lookup"><span data-stu-id="262da-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="262da-141">Styl textu</span><span class="sxs-lookup"><span data-stu-id="262da-141">Text styling</span></span>

<span data-ttu-id="262da-142">*Kurzíva*</span><span class="sxs-lookup"><span data-stu-id="262da-142">*Italics*</span></span>\
<span data-ttu-id="262da-143">Použijte pro soubory, složky, cesty (dlouhé položky dejte na samostatný řádek) a nové výrazy.</span><span class="sxs-lookup"><span data-stu-id="262da-143">Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="262da-144">**Tučné**</span><span class="sxs-lookup"><span data-stu-id="262da-144">**Bold**</span></span>\
<span data-ttu-id="262da-145">Použijte pro prvky uživatelského rozhraní.</span><span class="sxs-lookup"><span data-stu-id="262da-145">Use for UI elements.</span></span>

`Code`\
<span data-ttu-id="262da-146">Použijte pro vložený kód, klíčová slova jazyka, názvy balíčků NuGet, příkazy příkazového řádku, názvy databázových tabulek a sloupců a pro adresy URL, které nemají fungovat jako odkaz, na který se dá kliknout.</span><span class="sxs-lookup"><span data-stu-id="262da-146">Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="262da-147">Odkazy</span><span class="sxs-lookup"><span data-stu-id="262da-147">Links</span></span>

<span data-ttu-id="262da-148">Informace o ukotveních, interních odkazech, odkazech na jiné dokumenty, zahrnutém kódu a externích odkazech najdete v obecném článku o [odkazech](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="262da-148">See the general article on [Links](../how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="262da-149">Tým pro dokumentaci k .NET používá následující konvence:</span><span class="sxs-lookup"><span data-stu-id="262da-149">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="262da-150">Ve většině případů používáme relativní odkazy. V odkazech nedoporučujeme používat znak `~/`, protože relativní odkazy se překládají ve zdroji na GitHubu.</span><span class="sxs-lookup"><span data-stu-id="262da-150">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="262da-151">Pokud ale odkazujeme na soubor v závislém úložišti, použijeme v cestě znak `~/`.</span><span class="sxs-lookup"><span data-stu-id="262da-151">However, whenever we link to a file in a dependent repo, we use the `~/` character to provide the path.</span></span> <span data-ttu-id="262da-152">Soubory v závislém úložišti jsou v GitHubu umístěné jinde, a proto se tyto odkazy nepřeloží správně s relativními odkazy bez ohledu na způsob jejich zápisu.</span><span class="sxs-lookup"><span data-stu-id="262da-152">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="262da-153">Specifikace jazyka C# a specifikace jazyka Visual Basic zahrnete do dokumentace k .NET tak, že uvedete zdroj z jazykových úložišť.</span><span class="sxs-lookup"><span data-stu-id="262da-153">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="262da-154">Zdroje v Markdownu jsou spravované v úložištích [csharplang](https://github.com/dotnet/csharplang) a [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="262da-154">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="262da-155">Odkazy na specifikaci musí mířit na zdrojové adresáře s touto specifikací.</span><span class="sxs-lookup"><span data-stu-id="262da-155">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="262da-156">Pro C# je to **~/_csharplang/spec** a pro VB je to **~/_vblang/spec**, jak vidíte v následujícím příkladu:</span><span class="sxs-lookup"><span data-stu-id="262da-156">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="262da-157">Odkazy na rozhraní API</span><span class="sxs-lookup"><span data-stu-id="262da-157">Links to APIs</span></span>

<span data-ttu-id="262da-158">Kompilační systém má několik přípon, které umožňují vytvořit odkaz na rozhraní .NET API bez použití externích odkazů.</span><span class="sxs-lookup"><span data-stu-id="262da-158">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="262da-159">Použijte jednu z následujících syntaxí:</span><span class="sxs-lookup"><span data-stu-id="262da-159">You use one of the following syntax:</span></span>

1. <span data-ttu-id="262da-160">Automatické propojení: `<xref:UID>` nebo `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="262da-160">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="262da-161">Parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu.</span><span class="sxs-lookup"><span data-stu-id="262da-161">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="262da-162">Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.</span><span class="sxs-lookup"><span data-stu-id="262da-162">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="262da-163">Odkaz Markdownu: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="262da-163">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="262da-164">Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.</span><span class="sxs-lookup"><span data-stu-id="262da-164">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="262da-165">Příklady:</span><span class="sxs-lookup"><span data-stu-id="262da-165">Examples:</span></span>

- <span data-ttu-id="262da-166">`<xref:System.String>` se zobrazí jako [String](https://docs.microsoft.com/dotnet/api/system.string).</span><span class="sxs-lookup"><span data-stu-id="262da-166">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="262da-167">`<xref:System.String?displayProperty=nameWithType>` se zobrazí jako [System.String](https://docs.microsoft.com/dotnet/api/system.string).</span><span class="sxs-lookup"><span data-stu-id="262da-167">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="262da-168">`[String class](xref:System.String)` se zobrazí jako [třída String](https://docs.microsoft.com/dotnet/api/system.string).</span><span class="sxs-lookup"><span data-stu-id="262da-168">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="262da-169">Další informace o použití tohoto zápisu najdete v části [Použití křížového odkazu](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span><span class="sxs-lookup"><span data-stu-id="262da-169">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="262da-170">Některé identifikátory uživatele (UID) obsahují speciální znaky \`, \# nebo \*. Hodnota UID pak musí být zakódovaná do HTML jako `%60`, `%23` nebo `%2A`.</span><span class="sxs-lookup"><span data-stu-id="262da-170">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="262da-171">Někdy v tomto formátu uvidíte i závorky, není to ale povinné.</span><span class="sxs-lookup"><span data-stu-id="262da-171">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="262da-172">Příklady:</span><span class="sxs-lookup"><span data-stu-id="262da-172">Examples:</span></span>

- <span data-ttu-id="262da-173">System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.</span><span class="sxs-lookup"><span data-stu-id="262da-173">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="262da-174">System.Exception.\#ctor se změní na `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="262da-174">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="262da-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.</span><span class="sxs-lookup"><span data-stu-id="262da-175">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="262da-176">Identifikátory UID typů, seznam přetížení členů nebo určitého přetíženého člena najdete na adrese `https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="262da-176">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="262da-177">Řetězec dotazu `?text=*\<type-member-name>*` identifikuje typ nebo člena, jehož identifikátory UID chcete vidět.</span><span class="sxs-lookup"><span data-stu-id="262da-177">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="262da-178">Třeba `https://xref.docs.microsoft.com/autocomplete?text=string.format` načte přetížení [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format).</span><span class="sxs-lookup"><span data-stu-id="262da-178">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="262da-179">Nástroj vyhledá zadaný parametr dotazu `text` v libovolné části identifikátoru UID.</span><span class="sxs-lookup"><span data-stu-id="262da-179">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="262da-180">Můžete třeba hledat jméno člena (ToString), část jména člena (ToStri), typ a jméno člena (Double.ToString) atd.</span><span class="sxs-lookup"><span data-stu-id="262da-180">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="262da-181">Pokud za UID přidáte \* (nebo `%2A`), představuje tento odkaz stránku přetížení, nikoli určité rozhraní API.</span><span class="sxs-lookup"><span data-stu-id="262da-181">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="262da-182">Můžete to například použít, pokud chcete odkazovat na stránku [metody List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) obecným způsobem namísto konkrétního přetížení, jako je [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="262da-182">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="262da-183">Znaky \* také můžete použít k odkazu na stránku člena, pokud není přetížený, abyste v identifikátoru UID nemuseli uvádět seznam parametrů.</span><span class="sxs-lookup"><span data-stu-id="262da-183">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="262da-184">Pokud chcete vytvořit odkaz na určité přetížení metody, musíte do všech parametrů metody zahrnout úplně určený název typu.</span><span class="sxs-lookup"><span data-stu-id="262da-184">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="262da-185">Například \<xref:System.DateTime.ToString> odkazuje na metodu [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) bez parametrů, zatímco \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> odkazuje na metodu [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="262da-185">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="262da-186">Pokud chcete vytvořit odkaz na obecný typ, třeba na [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), použijte znak \` (`%60`) a za něj uveďte počet parametrů obecného typu.</span><span class="sxs-lookup"><span data-stu-id="262da-186">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="262da-187">Například `<xref:System.Nullable%601>` odkazuje na typ [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), zatímco `<xref:System.Func%602>` odkazuje na delegáta [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="262da-187">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="262da-188">Kód</span><span class="sxs-lookup"><span data-stu-id="262da-188">Code</span></span>

<span data-ttu-id="262da-189">Nejlepší způsob, jak zahrnout kód, je použít fragmenty kódu z funkční ukázky.</span><span class="sxs-lookup"><span data-stu-id="262da-189">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="262da-190">Vytvořte ukázku podle pokynů v článku o [příspěvcích pro .NET](dotnet-contribute.md#contribute-to-samples).</span><span class="sxs-lookup"><span data-stu-id="262da-190">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute.md#contribute-to-samples) article.</span></span> <span data-ttu-id="262da-191">Základní pravidla, která platí pro zahrnutí kódu, najdete v obecných pokynech ke [kódu](../code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="262da-191">The basic rules for including code are located in the general guidance on [code](../code-in-docs.md).</span></span>

<span data-ttu-id="262da-192">K zahrnutí kódu použijte následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="262da-192">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="262da-193">`-<language>` (*volitelné*, ale *doporučené*)</span><span class="sxs-lookup"><span data-stu-id="262da-193">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="262da-194">Jazyk fragmentu kódu, na který vytváříte odkaz.</span><span class="sxs-lookup"><span data-stu-id="262da-194">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="262da-195">`<name>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="262da-195">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="262da-196">Název fragmentu kódu</span><span class="sxs-lookup"><span data-stu-id="262da-196">Name for the code snippet.</span></span> <span data-ttu-id="262da-197">Nemá žádný vliv na výstupní HTML, ale můžete ho použít ke zlepšení čitelnosti zdroje Markdownu.</span><span class="sxs-lookup"><span data-stu-id="262da-197">It doesn't have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="262da-198">`<pathToFile>` (*povinné*)</span><span class="sxs-lookup"><span data-stu-id="262da-198">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="262da-199">Relativní cesta v systému souborů označující soubor fragmentu kódu, na který se má odkazovat</span><span class="sxs-lookup"><span data-stu-id="262da-199">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="262da-200">Může být složitá kvůli různým úložištím, která tvoří sadu dokumentace k .NET.</span><span class="sxs-lookup"><span data-stu-id="262da-200">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="262da-201">Ukázky k .NET jsou v úložišti dotnet/samples.</span><span class="sxs-lookup"><span data-stu-id="262da-201">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="262da-202">Všechny cesty k fragmentům kódu začínají na `~/samples`. Zbytek cesty představuje cestu ke zdroji z kořenového adresáře daného úložiště.</span><span class="sxs-lookup"><span data-stu-id="262da-202">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="262da-203">`<queryoption>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="262da-203">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="262da-204">Používá se k upřesnění způsobu načtení kódu ze souboru:</span><span class="sxs-lookup"><span data-stu-id="262da-204">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="262da-205">`#`:  `#{tagname}` (název značky) *nebo* `#L{startlinenumber}-L{endlinenumber}` (rozsah řádků).</span><span class="sxs-lookup"><span data-stu-id="262da-205">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="262da-206">Nedoporučujeme používat čísla řádků kvůli jejich snadnému porušení.</span><span class="sxs-lookup"><span data-stu-id="262da-206">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="262da-207">Jako odkaz na fragmenty kódu doporučujeme používat název značky.</span><span class="sxs-lookup"><span data-stu-id="262da-207">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="262da-208">Názvy značek by měly být srozumitelné.</span><span class="sxs-lookup"><span data-stu-id="262da-208">Use meaningful tag names.</span></span> <span data-ttu-id="262da-209">(Mnoho fragmentů kódu bylo migrováno z předchozí platformy. Jsou v nich značky s názvy třeba `Snippet1`, `Snippet2` atd. V praxi je dodržení tohoto pravidla velice náročné.)</span><span class="sxs-lookup"><span data-stu-id="262da-209">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="262da-210">`range`: `?range=1,3-5` Rozsah řádků.</span><span class="sxs-lookup"><span data-stu-id="262da-210">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="262da-211">Tento příklad zahrnuje řádky 1, 3, 4 a 5.</span><span class="sxs-lookup"><span data-stu-id="262da-211">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="262da-212">Všude, kde je to možné, doporučujeme používat názvy značek.</span><span class="sxs-lookup"><span data-stu-id="262da-212">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="262da-213">Název značky je vlastně název oblasti nebo komentáře kódu ve formátu `Snippettagname`, který je ve zdrojovém kódu.</span><span class="sxs-lookup"><span data-stu-id="262da-213">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="262da-214">V následujícím příkladu je vidět, jak odkazovat na název značky `BasicThrow`:</span><span class="sxs-lookup"><span data-stu-id="262da-214">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="262da-215">Relativní cesta ke zdroji v úložišti **dotnet/samples** je `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="262da-215">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="262da-216">Strukturu značek fragmentů kódu si můžete prohlédnout v [tomto zdrojovém souboru](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span><span class="sxs-lookup"><span data-stu-id="262da-216">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="262da-217">Podrobnosti o reprezentaci názvů značek ve zdrojových souborech fragmentu kódu v jednotlivých jazycích najdete v [pokynech pro DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="262da-217">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="262da-218">V následujícím příkladu je kód ve všech třech jazycích .NET:</span><span class="sxs-lookup"><span data-stu-id="262da-218">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

<span data-ttu-id="262da-219">Tím, že zahrnete fragmenty kódu z celých programů, zajistíte spustitelnost veškerého kódu v našem systému kontinuální integrace (CI).</span><span class="sxs-lookup"><span data-stu-id="262da-219">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="262da-220">Pokud ale chcete předvést něco, co způsobuje chyby při kompilaci nebo spuštění, můžete použít vložené bloky kódu.</span><span class="sxs-lookup"><span data-stu-id="262da-220">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="262da-221">Obrázky</span><span class="sxs-lookup"><span data-stu-id="262da-221">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="262da-222">Statický obrázek nebo animovaný GIF</span><span class="sxs-lookup"><span data-stu-id="262da-222">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="262da-223">Propojený obrázek</span><span class="sxs-lookup"><span data-stu-id="262da-223">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="262da-224">Videa</span><span class="sxs-lookup"><span data-stu-id="262da-224">Videos</span></span>

<span data-ttu-id="262da-225">V současnosti můžete ke vkládání videí služeb Channel 9 a YouTube použít následující syntaxi:</span><span class="sxs-lookup"><span data-stu-id="262da-225">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="262da-226">Channel9</span><span class="sxs-lookup"><span data-stu-id="262da-226">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="262da-227">Pokud chcete získat správnou adresu URL videa, vyberte kartu **Vložit** pod snímkem videa a zkopírujte adresu URL z prvku `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="262da-227">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="262da-228">Například:</span><span class="sxs-lookup"><span data-stu-id="262da-228">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="262da-229">YouTube</span><span class="sxs-lookup"><span data-stu-id="262da-229">YouTube</span></span>

<span data-ttu-id="262da-230">Pokud chcete získat správnou adresu URL videa, klikněte na něj pravým tlačítkem, vyberte **Kopírovat kód pro vložení** a zkopírujte adresu URL z prvku `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="262da-230">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="262da-231">Například:</span><span class="sxs-lookup"><span data-stu-id="262da-231">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="262da-232">docs.microsoft extensions</span><span class="sxs-lookup"><span data-stu-id="262da-232">docs.microsoft extensions</span></span>

<span data-ttu-id="262da-233">Další rozšíření dialektu GitHub Flavored Markdown najdete v dokumentaci na webu docs.microsoft.</span><span class="sxs-lookup"><span data-stu-id="262da-233">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="262da-234">Seznamy se zaškrtávacími políčky</span><span class="sxs-lookup"><span data-stu-id="262da-234">Checked lists</span></span>

<span data-ttu-id="262da-235">Pro seznamy je k dispozici vlastní styl.</span><span class="sxs-lookup"><span data-stu-id="262da-235">A custom style is available for lists.</span></span> <span data-ttu-id="262da-236">Můžete zobrazit seznamy se zelenými zaškrtnutími.</span><span class="sxs-lookup"><span data-stu-id="262da-236">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="262da-237">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="262da-237">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="262da-238">Vytvoření aplikace v .NET Core</span><span class="sxs-lookup"><span data-stu-id="262da-238">How to create a .NET Core app</span></span>
> * <span data-ttu-id="262da-239">Přidání odkazu do balíčku Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="262da-239">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="262da-240">Úprava souboru MyApp.csproj a přidání závislostí</span><span class="sxs-lookup"><span data-stu-id="262da-240">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="262da-241">Přidání třídy a objektu XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="262da-241">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="262da-242">Sestavení a spuštění aplikace</span><span class="sxs-lookup"><span data-stu-id="262da-242">How to build and run the application</span></span>

<span data-ttu-id="262da-243">Příklad použití seznamů se zaškrtávacími políčky najdete v [dokumentaci k .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="262da-243">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="262da-244">Tlačítka</span><span class="sxs-lookup"><span data-stu-id="262da-244">Buttons</span></span>

<span data-ttu-id="262da-245">Odkazy na tlačítka:</span><span class="sxs-lookup"><span data-stu-id="262da-245">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="262da-246">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="262da-246">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="262da-247">odkazy na tlačítka</span><span class="sxs-lookup"><span data-stu-id="262da-247">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="262da-248">Příklad použití tlačítek najdete v [dokumentaci k sadě Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="262da-248">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="262da-249">Postupy</span><span class="sxs-lookup"><span data-stu-id="262da-249">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="262da-250">Příklad použití postupů najdete v [příručce k jazyku C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="262da-250">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
