---
title: Jak do dokumentů vkládat kód
description: Přečtěte si, jak zahrnout elementy a fragmenty kódu do článků, které se mají publikovat na docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4e57af6a1fe9a9d3799f09cb04f3bd3f0b9b712d
ms.sourcegitcommit: 59e77d2fb9c38cccbacde9d2a7df61ae58c38fa4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "84421038"
---
# <a name="how-to-include-code-in-docs"></a><span data-ttu-id="53624-103">Jak do dokumentů vkládat kód</span><span class="sxs-lookup"><span data-stu-id="53624-103">How to include code in docs</span></span>

<span data-ttu-id="53624-104">Kód se dá do článku, který se má publikovat na docs.microsoft.com, přidat několika způsoby:</span><span class="sxs-lookup"><span data-stu-id="53624-104">There are several ways to include code in an article published on docs.microsoft.com:</span></span>

* <span data-ttu-id="53624-105">Jednotlivé elementy (slova) v rámci řádku.</span><span class="sxs-lookup"><span data-stu-id="53624-105">Individual elements (words) within a line.</span></span>

  <span data-ttu-id="53624-106">Tady je příklad stylu kódu: `code`.</span><span class="sxs-lookup"><span data-stu-id="53624-106">Here's an example of `code` style.</span></span>

  <span data-ttu-id="53624-107">Použijte formát kódu při odkazování na pojmenované parametry a proměnné v okolním bloku kódu v textu.</span><span class="sxs-lookup"><span data-stu-id="53624-107">Use code format when referring to named parameters and variables in a nearby code block in your text.</span></span> <span data-ttu-id="53624-108">Formát kódu jde také použít pro vlastnosti, metody, třídy a klíčová slova jazyka.</span><span class="sxs-lookup"><span data-stu-id="53624-108">Code format may also be used for properties, methods, classes, and language keywords.</span></span> <span data-ttu-id="53624-109">Další informace najdete v tématu [Elementy kódu](#code-elements) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-109">For more information, see [Code elements](#code-elements) later in this article..</span></span>

* <span data-ttu-id="53624-110">Bloky kódu v souboru Markdown článku.</span><span class="sxs-lookup"><span data-stu-id="53624-110">Code blocks in the article Markdown file.</span></span>

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  <span data-ttu-id="53624-111">Používejte vložené bloky kódu, pokud je nepraktické zobrazit kód pomocí odkazu na soubor kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-111">Use inline code blocks when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="53624-112">Další informace najdete v tématu [Bloky kódu](#inline-code-blocks) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-112">For more information, see [Code blocks](#inline-code-blocks) later in this article.</span></span>

* <span data-ttu-id="53624-113">Bloky kódu pomocí odkazu na soubor kódu v místním úložišti.</span><span class="sxs-lookup"><span data-stu-id="53624-113">Code blocks by reference to a code file in the local repository.</span></span>

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  <span data-ttu-id="53624-114">Další informace najdete v tématu [Odkazy na fragmenty v úložišti](#in-repo-snippet-references) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-114">For more information, see [In-repo snippet references](#in-repo-snippet-references) later in this article.</span></span>

* <span data-ttu-id="53624-115">Bloky kódu pomocí odkazu na soubor kódu v jiném úložišti.</span><span class="sxs-lookup"><span data-stu-id="53624-115">Code blocks by reference to a code file in another repository.</span></span>

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  <span data-ttu-id="53624-116">Další informace najdete v tématu [Odkazy na fragmenty mimo úložiště](#out-of-repo-snippet-references) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-116">For more information, see [Out-of-repo snippet references](#out-of-repo-snippet-references) later in this article.</span></span>
  
* <span data-ttu-id="53624-117">Bloky kódu, které umožní uživateli spustit kód v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="53624-117">Code blocks that let the user execute code in the browser.</span></span>

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  <span data-ttu-id="53624-118">Další informace najdete v tématu [Interaktivní fragmenty kódu](#interactive-code-snippets) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-118">For more information, see [Interactive code snippets](#interactive-code-snippets) later in this article.</span></span>

<span data-ttu-id="53624-119">Mimo vysvětlení k souboru Markdown pro každý z těchto způsobů, jak přidat kód, článek obsahuje některé [obecné pokyny pro všechny bloky kódu](#code-blocks).</span><span class="sxs-lookup"><span data-stu-id="53624-119">Besides explaining the Markdown for each of these ways to include code, the article provides some [general guidance for all code blocks](#code-blocks).</span></span>

## <a name="code-elements"></a><span data-ttu-id="53624-120">Elementy kódu</span><span class="sxs-lookup"><span data-stu-id="53624-120">Code elements</span></span>

<span data-ttu-id="53624-121">Element kódu je klíčové slovo programovacího jazyka, název třídy, název vlastnosti a tak dále.</span><span class="sxs-lookup"><span data-stu-id="53624-121">A "code element" is a programming language keyword, class name, property name, and so forth.</span></span> <span data-ttu-id="53624-122">Není vždy zřejmé, co se považuje za kód.</span><span class="sxs-lookup"><span data-stu-id="53624-122">It's not always obvious what qualifies as code.</span></span> <span data-ttu-id="53624-123">Například názvy balíčků NuGet by se měly považovat za kód.</span><span class="sxs-lookup"><span data-stu-id="53624-123">For example, NuGet package names should be treated as code.</span></span> <span data-ttu-id="53624-124">Pokud máte pochybnosti, podívejte se do článku [Pokyny k formátování textu](text-formatting-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="53624-124">When in doubt, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>

### <a name="inline-code-style"></a><span data-ttu-id="53624-125">Styl vloženého kódu</span><span class="sxs-lookup"><span data-stu-id="53624-125">Inline code style</span></span>

<span data-ttu-id="53624-126">Pokud chcete zahrnout element kódu do textu článku, dejte ho do zpětných apostrofů (\`), kterými označíte styl kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-126">To include a code element in article text, surround it with backticks (\`) to indicate code style.</span></span>
<span data-ttu-id="53624-127">Styl vloženého kódu by neměl používat formát s trojnásobným zpětným apostrofem.</span><span class="sxs-lookup"><span data-stu-id="53624-127">Inline code style shouldn't use the triple-backtick format.</span></span>

|<span data-ttu-id="53624-128">Markdown</span><span class="sxs-lookup"><span data-stu-id="53624-128">Markdown</span></span> |<span data-ttu-id="53624-129">Vykreslení</span><span class="sxs-lookup"><span data-stu-id="53624-129">Rendered</span></span> |
|---------|---------|
|<span data-ttu-id="53624-130">Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem \`Id\` nebo \`ClassnameID\` jako primární klíč.</span><span class="sxs-lookup"><span data-stu-id="53624-130">By default, the Entity Framework interprets a property that's named \`Id\` or \`ClassnameID\` as the primary key.</span></span>|<span data-ttu-id="53624-131">Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem `Id` nebo `ClassnameID` jako primární klíč.</span><span class="sxs-lookup"><span data-stu-id="53624-131">By default, the Entity Framework interprets a property that's named `Id` or `ClassnameID` as the primary key.</span></span>|

<span data-ttu-id="53624-132">Když se článek lokalizuje (přeloží do jiných jazyků), text ve stylu kódu zůstane nepřeložený.</span><span class="sxs-lookup"><span data-stu-id="53624-132">When an article is localized (translated into other languages), text styled as code is left untranslated.</span></span> <span data-ttu-id="53624-133">Pokud chcete zabránit lokalizaci bez použití stylu kódu, najdete informace v části [Nelokalizované řetězce](markdown-reference.md#non-localized-strings).</span><span class="sxs-lookup"><span data-stu-id="53624-133">If you want to prevent localization without using code style, see [Non-localized strings](markdown-reference.md#non-localized-strings).</span></span>

### <a name="bold-style"></a><span data-ttu-id="53624-134">Tučný styl</span><span class="sxs-lookup"><span data-stu-id="53624-134">Bold style</span></span>

<span data-ttu-id="53624-135">Některé starší návody určují tučný styl za vložený kód.</span><span class="sxs-lookup"><span data-stu-id="53624-135">Some older style guides specify bold for inline code.</span></span> <span data-ttu-id="53624-136">Tučné písmo se dá použít, pokud je styl kódu tak vlezlý, že je to na úkor čitelnosti.</span><span class="sxs-lookup"><span data-stu-id="53624-136">Bold is an option when code style is so obtrusive as to compromise readability.</span></span> <span data-ttu-id="53624-137">Pokud například máte tabulku Markdown s převážně kódovými elementy, může být vinou všudypřítomného stylu kódu dost nepřehledná.</span><span class="sxs-lookup"><span data-stu-id="53624-137">For example, a Markdown table with mostly code elements might look too busy with code styling everywhere.</span></span> <span data-ttu-id="53624-138">Pokud se rozhodnete použít tučný styl, použijte [syntaxi nelokalizovaných řetězců](markdown-reference.md#non-localized-strings), abyste zajistili, že kód není lokalizovaný.</span><span class="sxs-lookup"><span data-stu-id="53624-138">If you choose to use bold style, use [non-localized strings syntax](markdown-reference.md#non-localized-strings) to make sure that code is not localized.</span></span>

### <a name="links"></a><span data-ttu-id="53624-139">Odkazy</span><span class="sxs-lookup"><span data-stu-id="53624-139">Links</span></span>

<span data-ttu-id="53624-140">Odkaz na referenční dokumentaci může být v některých kontextech užitečnější než formát kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-140">A link to reference documentation may be more helpful than code format in some contexts.</span></span> <span data-ttu-id="53624-141">Jestliže použijete odkaz, nepoužívejte pro text odkazu formát kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-141">If you use a link, don't apply code format to the link text.</span></span> <span data-ttu-id="53624-142">Pokud se u odkazu nastaví styl kódu, může to zakrýt skutečnost, že text je odkaz.</span><span class="sxs-lookup"><span data-stu-id="53624-142">Styling a link as code can obscure the fact that the text is a link.</span></span>

<span data-ttu-id="53624-143">Když použijete odkaz a později ve stejném kontextu budete na stejný element odkazovat, udělejte následující instance ve formátu kódu místo odkazů.</span><span class="sxs-lookup"><span data-stu-id="53624-143">If you use a link and refer to the same element later in the same context, make the subsequent instances code format rather than links.</span></span>

### <a name="placeholders"></a><span data-ttu-id="53624-144">Zástupné symboly</span><span class="sxs-lookup"><span data-stu-id="53624-144">Placeholders</span></span>

<span data-ttu-id="53624-145">Pokud chcete, aby uživatel nahradil oddíl zobrazeného kódu vlastními hodnotami, použijte zástupný text vyznačený lomenými závorkami nebo složenými závorkami.</span><span class="sxs-lookup"><span data-stu-id="53624-145">If you want the user to replace a section of displayed code with their own values, use placeholder text marked off by angle brackets or curly braces.</span></span> <span data-ttu-id="53624-146">Například: `az group delete -n <ResourceGroupName>`.</span><span class="sxs-lookup"><span data-stu-id="53624-146">For example: `az group delete -n <ResourceGroupName>`.</span></span> <span data-ttu-id="53624-147">Vysvětlete, že při nahrazování skutečnými hodnotami se musí závorky odebrat.</span><span class="sxs-lookup"><span data-stu-id="53624-147">Explain that the brackets or braces must be removed when substituting real values.</span></span>

## <a name="code-blocks"></a><span data-ttu-id="53624-148">Bloky kódu</span><span class="sxs-lookup"><span data-stu-id="53624-148">Code blocks</span></span>

<span data-ttu-id="53624-149">Syntaxe pro zahrnutí kódu v dokumentu závisí na tom, kde se nachází kód:</span><span class="sxs-lookup"><span data-stu-id="53624-149">The syntax for including code in a doc depends on where the code is located:</span></span>

* [<span data-ttu-id="53624-150">V souboru Markdown článku</span><span class="sxs-lookup"><span data-stu-id="53624-150">In the article Markdown file</span></span>](#inline-code-blocks)
* [<span data-ttu-id="53624-151">V souboru kódu ve stejném úložišti</span><span class="sxs-lookup"><span data-stu-id="53624-151">In a code file in the same repository</span></span>](#in-repo-snippet-references)
* [<span data-ttu-id="53624-152">V souboru kódu v jiném úložišti</span><span class="sxs-lookup"><span data-stu-id="53624-152">In a code file in a different repository</span></span>](#out-of-repo-snippet-references)

<span data-ttu-id="53624-153">Pokyny, které platí pro všechny tři typy bloků kódu, jsou následující:</span><span class="sxs-lookup"><span data-stu-id="53624-153">Following are guidelines that apply to all three types of code blocks:</span></span>

* [<span data-ttu-id="53624-154">Automatizujte ověření kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-154">Automate code validation.</span></span>](#code-validation)
* [<span data-ttu-id="53624-155">Zvýrazněte klíčové řádky kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-155">Highlight key lines of code.</span></span>](#highlighting)
* [<span data-ttu-id="53624-156">Vyhněte se vodorovným posuvníkům.</span><span class="sxs-lookup"><span data-stu-id="53624-156">Avoid horizontal scroll bars.</span></span>](#horizontal-scroll-bars)

### <a name="screenshots"></a><span data-ttu-id="53624-157">Snímky obrazovky</span><span class="sxs-lookup"><span data-stu-id="53624-157">Screenshots</span></span>

<span data-ttu-id="53624-158">Všechny metody uvedené v předchozí části mají za následek použitelné bloky kódu:</span><span class="sxs-lookup"><span data-stu-id="53624-158">All of the methods listed in the preceding section result in usable code blocks:</span></span>

* <span data-ttu-id="53624-159">Můžete z nich kopírovat a vkládat.</span><span class="sxs-lookup"><span data-stu-id="53624-159">You can copy and paste from them.</span></span>
* <span data-ttu-id="53624-160">Jsou indexovány vyhledávacími weby.</span><span class="sxs-lookup"><span data-stu-id="53624-160">They're indexed by search engines.</span></span>
* <span data-ttu-id="53624-161">Jsou přístupné pro čtečky obrazovky.</span><span class="sxs-lookup"><span data-stu-id="53624-161">They're accessible to screen readers.</span></span>

<span data-ttu-id="53624-162">To je jen několik důvodů z mnoha, proč se snímky obrazovky integrovaného vývojového prostředí (IDE) nedoporučují jako metoda zahrnutí kódu do článku.</span><span class="sxs-lookup"><span data-stu-id="53624-162">These are just a few of the reasons why IDE screenshots aren't recommended as a method of including code in an article.</span></span> <span data-ttu-id="53624-163">Snímky obrazovky IDE použijte pro kód pouze v případě, že ukazujete něco o samotném IDE, například IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="53624-163">Use IDE screenshots for code only if you're showing something about the IDE itself, like IntelliSense.</span></span> <span data-ttu-id="53624-164">Nepoužívejte snímky obrazovky pouze k zobrazení barev a zvýraznění.</span><span class="sxs-lookup"><span data-stu-id="53624-164">Don't use screenshots just to show colorization and highlighting.</span></span>

### <a name="code-validation"></a><span data-ttu-id="53624-165">Ověření kódu</span><span class="sxs-lookup"><span data-stu-id="53624-165">Code validation</span></span>

<span data-ttu-id="53624-166">Některá úložiště mají implementované procesy, které automaticky zkompilují celý vzorový kód a zkontrolují, jestli neobsahuje chyby.</span><span class="sxs-lookup"><span data-stu-id="53624-166">Some repositories have implemented processes that automatically compile all sample code to check for errors.</span></span> <span data-ttu-id="53624-167">Toto dělá úložiště .NET.</span><span class="sxs-lookup"><span data-stu-id="53624-167">The .NET repository does this.</span></span> <span data-ttu-id="53624-168">Další informace najdete v článku [Příspěvky](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) v úložišti .NET.</span><span class="sxs-lookup"><span data-stu-id="53624-168">For more information, see [Contributing](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) in the .NET repository.</span></span>

<span data-ttu-id="53624-169">Pokud zahrnujete bloky kódu z jiného úložiště, spolupracujte s vlastníky na strategii údržby pro kód tak, aby se váš zahrnutý kód nepokazil nebo nezastaral, když se pak budou vydávat nové verze knihoven, které kód používá.</span><span class="sxs-lookup"><span data-stu-id="53624-169">If you are including code blocks from another repository, work with the owners on a maintenance strategy for the code so that your included code does not break or go out of date as new versions of the libraries the code uses are shipped.</span></span>

### <a name="highlighting"></a><span data-ttu-id="53624-170">Zvýrazňování</span><span class="sxs-lookup"><span data-stu-id="53624-170">Highlighting</span></span>

<span data-ttu-id="53624-171">Fragmenty obvykle obsahují více kódu, než je nezbytné pro získání kontextu.</span><span class="sxs-lookup"><span data-stu-id="53624-171">Snippets typically include more code than necessary in order to provide context.</span></span> <span data-ttu-id="53624-172">Budou se líp číst, když ve fragmentu zvýrazníte klíčové řádky, jako v následujícím příkladu:</span><span class="sxs-lookup"><span data-stu-id="53624-172">It helps readability when you highlight the key lines that you're focusing on in the snippet, as in this example:</span></span>

![Příklad zobrazující zvýrazněný kód](media/code-in-docs/highlighted-code.png)

<span data-ttu-id="53624-174">Kód nemůžete zvýraznit, když ho zahrnete do souboru Markdown článku.</span><span class="sxs-lookup"><span data-stu-id="53624-174">You can't highlight code when you include it in the article Markdown file.</span></span> <span data-ttu-id="53624-175">Funguje to jenom u fragmentů kódu, které jsou zahrnuté odkazem na soubor kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-175">It works only for code snippets included by reference to a code file.</span></span>

### <a name="horizontal-scroll-bars"></a><span data-ttu-id="53624-176">Vodorovné posuvníky</span><span class="sxs-lookup"><span data-stu-id="53624-176">Horizontal scroll bars</span></span>

<span data-ttu-id="53624-177">Rozdělte dlouhé řádky, aby se nemusely používat vodorovné posuvníky.</span><span class="sxs-lookup"><span data-stu-id="53624-177">Break up long lines to avoid horizontal scroll bars.</span></span> <span data-ttu-id="53624-178">S posuvníky se bloky kódu špatně čtou.</span><span class="sxs-lookup"><span data-stu-id="53624-178">Scroll bars on code blocks make code hard to read.</span></span> <span data-ttu-id="53624-179">Jsou obzvláště problematické u delších bloků kódu, kdy může být nemožné zobrazit současně posuvník a řádek, který chcete číst.</span><span class="sxs-lookup"><span data-stu-id="53624-179">They're especially problematic on longer code blocks, where it may be impossible to see the scroll bar and the line you want to read at the same time.</span></span>

<span data-ttu-id="53624-180">Dobrým postupem pro minimalizaci vodorovných posuvníků v blocích kódu je rozdělit řádky kódu delší než 85 znaků.</span><span class="sxs-lookup"><span data-stu-id="53624-180">A good practice for minimizing horizontal scroll bars on code blocks is to break up code lines longer than 85 characters.</span></span> <span data-ttu-id="53624-181">Mějte ale na paměti, že přítomnost nebo absence posuvníku není jediným kritériem čitelnosti.</span><span class="sxs-lookup"><span data-stu-id="53624-181">But keep in mind that the presence or absence of a scroll bar isn't the only criterion of readability.</span></span> <span data-ttu-id="53624-182">Pokud konec řádku (zalomení) před 85 znakem škodí čitelností nebo pohodlí při kopírování a vkládání, klidně nechejte řádek delší.</span><span class="sxs-lookup"><span data-stu-id="53624-182">If breaking a line before 85 hurts readability or copy-paste convenience, feel free to go over 85.</span></span>

## <a name="inline-code-blocks"></a><span data-ttu-id="53624-183">Vložené bloky kódu</span><span class="sxs-lookup"><span data-stu-id="53624-183">Inline code blocks</span></span>

<span data-ttu-id="53624-184">Používejte vložené bloky kódu, pouze pokud je nepraktické zobrazit kód pomocí odkazu na soubor kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-184">Use inline code blocks only when it's impractical to display code by reference to a code file.</span></span> <span data-ttu-id="53624-185">Vložený kód se obecně obtížněji testuje a udržuje v aktuálním stavu v porovnání se souborem kódu, který je součástí celého projektu.</span><span class="sxs-lookup"><span data-stu-id="53624-185">Inline code is generally more difficult to test and keep up to date compared to a code file that is part of a complete project.</span></span>  <span data-ttu-id="53624-186">A ve vloženém kódu může ještě dojít k vynechání kontextu, který by vývojáři mohl pomoct s pochopením a používáním kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-186">And inline code may omit context that could help the developer to understand and use the code.</span></span> <span data-ttu-id="53624-187">Tyto záležitosti platí hlavně pro programovací jazyky.</span><span class="sxs-lookup"><span data-stu-id="53624-187">These considerations apply mainly to programming languages.</span></span> <span data-ttu-id="53624-188">Vložené bloky kódu se dají také použít pro výstupy a vstupy (například JSON), dotazovací jazyky (například SQL) a skriptovací jazyky (například PowerShell).</span><span class="sxs-lookup"><span data-stu-id="53624-188">Inline code blocks can also be used for outputs and inputs (such as JSON), query languages (such as SQL), and scripting languages (such as PowerShell).</span></span>
  
<span data-ttu-id="53624-189">Existují dva způsoby označení oddílu textu v souboru článku jako blok kódu: jeho *uzavřením* do trojitých zpětných apostrofů (\`\`\`) nebo jeho odsazením.</span><span class="sxs-lookup"><span data-stu-id="53624-189">There are two ways to indicate a section of text in an article file is a code block: by *fencing* it in triple-backticks (\`\`\`) or by indenting it.</span></span> <span data-ttu-id="53624-190">Upřednostňuje se uzavření, protože to umožňuje určit jazyk.</span><span class="sxs-lookup"><span data-stu-id="53624-190">Fencing is preferred because it lets you specify the language.</span></span> <span data-ttu-id="53624-191">Vyhněte se použití odsazení, protože se člověk velmi snadno splete a jiný pisatel pak nemusí chápat váš záměr, když bude potřebovat váš článek upravit.</span><span class="sxs-lookup"><span data-stu-id="53624-191">Avoid using indentation because it's too easy to get wrong and it may be hard for another writer to understand your intent when they need to edit your article.</span></span>

<span data-ttu-id="53624-192">Indikátory jazyka jsou umístěné hned za levými trojitými zpětnými apostrofy, jako v následujícím příkladu:</span><span class="sxs-lookup"><span data-stu-id="53624-192">Language indicators are placed immediately after the opening triple-backticks, as in the following example:</span></span>

<span data-ttu-id="53624-193">Markdown:</span><span class="sxs-lookup"><span data-stu-id="53624-193">Markdown:</span></span>

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

<span data-ttu-id="53624-194">Vykreslení:</span><span class="sxs-lookup"><span data-stu-id="53624-194">Rendered:</span></span>

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

<span data-ttu-id="53624-195">Informace o hodnotách, které můžete použít jako indikátory jazyka, najdete v článku [Názvy jazyků a aliasy](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span><span class="sxs-lookup"><span data-stu-id="53624-195">For information about the values you can use as language indicators, see [Language names and aliases](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).</span></span>

<span data-ttu-id="53624-196">Pokud použijete slovo jazyka nebo prostředí po trojnásobném zpětném apostrofu (\`\`\`), které není podporované, zobrazí se toto slovo v záhlaví oddílu kódu na vykreslené stránce.</span><span class="sxs-lookup"><span data-stu-id="53624-196">If you use a language or environment word after the triple-backticks (\`\`\`) that isn't supported, that word appears in the code section title bar on the rendered page.</span></span> <span data-ttu-id="53624-197">Pokud je to možné, použijte ve vložených blocích kódu indikátor jazyka nebo prostředí.</span><span class="sxs-lookup"><span data-stu-id="53624-197">Whenever possible, use a language or environment indicator in your inline code blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="53624-198">Jestliže zkopírujete a vložíte kód z dokumentu aplikace Word, je nutné, aby neobsahoval žádné „oblé uvozovky“, které v kódu nejsou platné (například `“` a `’`).</span><span class="sxs-lookup"><span data-stu-id="53624-198">If you copy and paste code from a Word document, make sure it has no "curly quotes," which aren't valid in code (for example, `“` and `’`).</span></span> <span data-ttu-id="53624-199">Pokud tam jsou, změňte je zpět na normální uvozovky (`'` a `"`).</span><span class="sxs-lookup"><span data-stu-id="53624-199">If it does, change them back to normal quotes (`'` and `"`).</span></span> <span data-ttu-id="53624-200">Nebo to můžete nechat na Balíčku pro vytváření obsahu na webu Docs a [funkci pro nahrazení inteligentních uvozovek](docs-authoring/smart-quote-replacement.md).</span><span class="sxs-lookup"><span data-stu-id="53624-200">Alternatively, rely on the Docs Authoring Pack, [smart quotes replacement feature](docs-authoring/smart-quote-replacement.md).</span></span>

## <a name="in-repo-snippet-references"></a><span data-ttu-id="53624-201">Odkazy na fragmenty v úložišti</span><span class="sxs-lookup"><span data-stu-id="53624-201">In-repo snippet references</span></span>

<span data-ttu-id="53624-202">Preferovaný způsob, jak zahrnout fragmenty kódu pro programovací jazyky do dokumentů, je pomocí odkazu na soubor kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-202">The preferred way to include code snippets for programming languages in docs is by reference to a code file.</span></span> <span data-ttu-id="53624-203">Tato metoda vám umožňuje zvýraznit řádky kódu a zpřístupňuje širší kontext fragmentu na GitHubu, aby ho vývojáři mohli použít.</span><span class="sxs-lookup"><span data-stu-id="53624-203">This method gives you the ability to highlight lines of code and makes the wider context of the snippet available on GitHub for developers to use.</span></span> <span data-ttu-id="53624-204">Kód můžete zahrnout pomocí formátu trojí dvojtečky (:\:\:) buď ručně, nebo v nástroji Visual Studio Code pomocí [Balíčku pro vytváření obsahu na webu docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="53624-204">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="53624-205">V editoru Visual Studio Code stiskněte <kbd>Alt+M</kbd> nebo <kbd>Option+M</kbd> a vyberte Snippet (Fragment).</span><span class="sxs-lookup"><span data-stu-id="53624-205">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="53624-206">Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="53624-206">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="53624-207">Pokud chcete vyhledávat místně, vyberte Full Search (Úplné vyhledávání).</span><span class="sxs-lookup"><span data-stu-id="53624-207">To search locally, select Full Search.</span></span>
3. <span data-ttu-id="53624-208">Zadejte hledaný termín pro vyhledání souboru.</span><span class="sxs-lookup"><span data-stu-id="53624-208">Enter a search term to find the file.</span></span> <span data-ttu-id="53624-209">Jakmile soubor najdete, vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="53624-209">Once you've found the file, select the file.</span></span>
4. <span data-ttu-id="53624-210">Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu.</span><span class="sxs-lookup"><span data-stu-id="53624-210">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="53624-211">Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).</span><span class="sxs-lookup"><span data-stu-id="53624-211">The options are: **ID**, **Range** and **None**.</span></span>
5. <span data-ttu-id="53624-212">Podle výběru z kroku 4 zadejte v případě potřeby hodnotu.</span><span class="sxs-lookup"><span data-stu-id="53624-212">Based on your selection from Step 4, provide a value if necessary.</span></span>

<span data-ttu-id="53624-213">Zobrazení celého souboru kódu:</span><span class="sxs-lookup"><span data-stu-id="53624-213">Display entire code file:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

<span data-ttu-id="53624-214">Zobrazení části souboru kódu zadáním čísel řádků:</span><span class="sxs-lookup"><span data-stu-id="53624-214">Display part of a code file by specifying line numbers:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="53624-215">Zobrazení části souboru kódu zadáním názvu fragmentu:</span><span class="sxs-lookup"><span data-stu-id="53624-215">Display part of a code file by specifying a snippet name:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="53624-216">Tyto příklady jsou vysvětlené v následujících oddílech:</span><span class="sxs-lookup"><span data-stu-id="53624-216">The following sections explain these examples:</span></span>

* [<span data-ttu-id="53624-217">Použití relativní cesty k souboru kódu</span><span class="sxs-lookup"><span data-stu-id="53624-217">Use a relative path to the code file</span></span>](#path-to-code-file)
* [<span data-ttu-id="53624-218">Zahrnutí jenom vybraných čísel řádků</span><span class="sxs-lookup"><span data-stu-id="53624-218">Include only selected line numbers</span></span>](#selected-line-numbers)
* [<span data-ttu-id="53624-219">Odkaz na pojmenovaný fragment</span><span class="sxs-lookup"><span data-stu-id="53624-219">Refer to a named snippet</span></span>](#named-snippet)
* [<span data-ttu-id="53624-220">Zvýraznění vybraných řádků</span><span class="sxs-lookup"><span data-stu-id="53624-220">Highlight selected lines</span></span>](#highlighting-selected-lines)

<span data-ttu-id="53624-221">Další informace najdete v tématu [Přehled syntaxe fragmentů](#snippet-syntax-reference) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-221">For more information, see [Snippet syntax reference](#snippet-syntax-reference) later in this article.</span></span>

### <a name="path-to-code-file"></a><span data-ttu-id="53624-222">Cesta k souboru kódu</span><span class="sxs-lookup"><span data-stu-id="53624-222">Path to code file</span></span>

<span data-ttu-id="53624-223">Příklad:</span><span class="sxs-lookup"><span data-stu-id="53624-223">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="53624-224">Příklad je z úložiště dokumentů ASP.NET, soubor článku [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md).</span><span class="sxs-lookup"><span data-stu-id="53624-224">The example is from the ASP.NET docs repo, [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md) article file.</span></span> <span data-ttu-id="53624-225">Na soubor kódu odkazuje relativní cesta k [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) ve stejném úložišti.</span><span class="sxs-lookup"><span data-stu-id="53624-225">The code file is referenced by a relative path to [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) in the same repository.</span></span>

### <a name="selected-line-numbers"></a><span data-ttu-id="53624-226">Vybraná čísla řádků</span><span class="sxs-lookup"><span data-stu-id="53624-226">Selected line numbers</span></span>

<span data-ttu-id="53624-227">Příklad:</span><span class="sxs-lookup"><span data-stu-id="53624-227">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

<span data-ttu-id="53624-228">Tento příklad zobrazí jenom řádky 2 až 24 a 26 ze souboru kódu *StudentController.cs*.</span><span class="sxs-lookup"><span data-stu-id="53624-228">This example displays only lines 2-24 and 26 of the *StudentController.cs* code file.</span></span>

<span data-ttu-id="53624-229">Dejte raději přednost pojmenovaným fragmentům před pevnými čísly řádků, jak je vysvětleno v další části.</span><span class="sxs-lookup"><span data-stu-id="53624-229">Prefer named snippets over hard-coded line numbers, as explained in the next section.</span></span>

### <a name="named-snippet"></a><span data-ttu-id="53624-230">Pojmenovaný fragment</span><span class="sxs-lookup"><span data-stu-id="53624-230">Named snippet</span></span>

<span data-ttu-id="53624-231">Příklad:</span><span class="sxs-lookup"><span data-stu-id="53624-231">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

<span data-ttu-id="53624-232">Pro název používejte jenom písmena a podtržítka.</span><span class="sxs-lookup"><span data-stu-id="53624-232">Use only letters and underscores for the name.</span></span>

<span data-ttu-id="53624-233">V příkladu je zobrazený oddíl `snippet_Create` souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-233">The example displays the `snippet_Create` section of the code file.</span></span> <span data-ttu-id="53624-234">Soubor kódu pro tento příklad obsahuje značky fragmentu v komentářích v kódu C#:</span><span class="sxs-lookup"><span data-stu-id="53624-234">The code file for this example has snippet tags in comments in the C# code:</span></span>

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

<span data-ttu-id="53624-235">Vždy, když je to možné, odkazujte na pojmenovanou část a nezadávejte čísla řádků.</span><span class="sxs-lookup"><span data-stu-id="53624-235">Whenever you can, refer to a named section rather than specifying line numbers.</span></span> <span data-ttu-id="53624-236">S odkazy na čísla řádků je třeba zacházet opatrně, protože soubory kódu se nevyhnutelně mění tak, že dochází ke změnám čísel řádků.</span><span class="sxs-lookup"><span data-stu-id="53624-236">Line number references are brittle because code files inevitably change in ways that make line numbers change.</span></span>
<span data-ttu-id="53624-237">Takové změny vám lehce uniknou.</span><span class="sxs-lookup"><span data-stu-id="53624-237">You don't necessarily get notified of such changes.</span></span> <span data-ttu-id="53624-238">Ve vašem článku se nakonec začnou zobrazovat chybné řádky a vy nebudete mít potuchy, že se něco změnilo.</span><span class="sxs-lookup"><span data-stu-id="53624-238">Your article eventually starts showing the wrong lines and you have no clue anything has changed.</span></span>

### <a name="highlighting-selected-lines"></a><span data-ttu-id="53624-239">Zvýraznění vybraných řádků</span><span class="sxs-lookup"><span data-stu-id="53624-239">Highlighting selected lines</span></span>

<span data-ttu-id="53624-240">Příklad:</span><span class="sxs-lookup"><span data-stu-id="53624-240">Example:</span></span>

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

<span data-ttu-id="53624-241">V příkladu jsou zvýrazněné řádky 2 a 5, počítáno od začátku zobrazeného fragmentu.</span><span class="sxs-lookup"><span data-stu-id="53624-241">The example highlights lines 2 and 5, counting from the start of the displayed snippet.</span></span> <span data-ttu-id="53624-242">Čísla zvýrazněných řádků se nepočítají od začátku souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-242">Line numbers to highlight don't count from the start of the code file.</span></span> <span data-ttu-id="53624-243">Jinými slovy jsou zvýrazněné řádky 3 a 6 ze souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-243">In other words, lines 3 and 6 of the code file are highlighted.</span></span>

## <a name="out-of-repo-snippet-references"></a><span data-ttu-id="53624-244">Odkazy na fragmenty mimo úložiště</span><span class="sxs-lookup"><span data-stu-id="53624-244">Out-of-repo snippet references</span></span>

<span data-ttu-id="53624-245">Pokud se soubor kódu, na který chcete odkazovat, nachází v jiném úložišti, nastavte úložiště kódu jako *závislé úložiště*.</span><span class="sxs-lookup"><span data-stu-id="53624-245">If the code file you want to reference is in a different repository, set up the code repository as a *dependent repository*.</span></span> <span data-ttu-id="53624-246">Až tak učiníte, zadejte pro něj název.</span><span class="sxs-lookup"><span data-stu-id="53624-246">When you do that, you specify a name for it.</span></span> <span data-ttu-id="53624-247">Tento název potom pro účely odkazů na kód funguje stejně jako název složky.</span><span class="sxs-lookup"><span data-stu-id="53624-247">That name then acts like a folder name for purposes of code references.</span></span>

<span data-ttu-id="53624-248">Úložiště dokumentů je například *Azure/azure-docs* a úložiště kódu je *Azure/azure-functions-durable-extension*.</span><span class="sxs-lookup"><span data-stu-id="53624-248">For example, the docs repository is *Azure/azure-docs*, and the code repository is *Azure/azure-functions-durable-extension*.</span></span>

<span data-ttu-id="53624-249">Do kořenové složky *azure-docs* přidejte do souboru *.openpublishing.publish.config.json* následující oddíl:</span><span class="sxs-lookup"><span data-stu-id="53624-249">In the root folder of *azure-docs*, add the following section in *.openpublishing.publish.config.json*:</span></span>

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

<span data-ttu-id="53624-250">Teď když budete odkazovat na *samples-durable-functions*, jako by šlo o složku v *azure-docs*, budete ve skutečnosti odkazovat na kořenovou složku v úložišti *azure-functions-durable-extension*.</span><span class="sxs-lookup"><span data-stu-id="53624-250">Now when you refer to *samples-durable-functions* as if it were a folder in *azure-docs*, you're actually referring to the root folder in the *azure-functions-durable-extension* repository.</span></span>

<span data-ttu-id="53624-251">Kód můžete zahrnout pomocí formátu trojí dvojtečky (:\:\:) buď ručně, nebo v nástroji Visual Studio Code pomocí [Balíčku pro vytváření obsahu na webu docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span><span class="sxs-lookup"><span data-stu-id="53624-251">You can include code by using the triple colon format (:\:\:) either manually or in Visual Studio Code with the help of the [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).</span></span>

1. <span data-ttu-id="53624-252">V editoru Visual Studio Code stiskněte <kbd>Alt+M</kbd> nebo <kbd>Option+M</kbd> a vyberte Snippet (Fragment).</span><span class="sxs-lookup"><span data-stu-id="53624-252">In Visual Studio Code, click <kbd>Alt + M</kbd> or <kbd>Option + M</kbd> and select Snippet.</span></span>
2. <span data-ttu-id="53624-253">Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="53624-253">Once Snippet is selected, you will be prompted for Full Search, Scoped Search or Cross-Repository Reference.</span></span> <span data-ttu-id="53624-254">Pokud chcete hledat v jiném úložišti, vyberte Cross-Repository Reference (Odkaz mezi úložišti).</span><span class="sxs-lookup"><span data-stu-id="53624-254">To search across repositories, select Cross-Repository Reference.</span></span>
3. <span data-ttu-id="53624-255">Dostanete možnost vybrat úložiště, která jsou v *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="53624-255">You will be given a selection of repositories that are in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="53624-256">Vyberte úložiště.</span><span class="sxs-lookup"><span data-stu-id="53624-256">Select a repository.</span></span>
4. <span data-ttu-id="53624-257">Zadejte hledaný termín pro vyhledání souboru.</span><span class="sxs-lookup"><span data-stu-id="53624-257">Enter a search term to find the file.</span></span> <span data-ttu-id="53624-258">Jakmile soubor najdete, vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="53624-258">Once you've found the file, select the file.</span></span>
5. <span data-ttu-id="53624-259">Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu.</span><span class="sxs-lookup"><span data-stu-id="53624-259">Next, select an option to determine which line(s) of code should be included in the snippet.</span></span> <span data-ttu-id="53624-260">Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).</span><span class="sxs-lookup"><span data-stu-id="53624-260">The options are: **ID**, **Range** and **None**.</span></span>
6. <span data-ttu-id="53624-261">Podle výběru z 5. kroku zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="53624-261">Based on your selection from Step 5, provide a value.</span></span>

<span data-ttu-id="53624-262">Váš odkaz na fragment bude vypadat nějak takto:</span><span class="sxs-lookup"><span data-stu-id="53624-262">Your snippet reference will look like this:</span></span>

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

<span data-ttu-id="53624-263">V úložišti *azure-functions-durable-extension* je tento soubor kódu ve složce *samples/csx/shared*.</span><span class="sxs-lookup"><span data-stu-id="53624-263">In the *azure-functions-durable-extension* repository, that code file is in the *samples/csx/shared* folder.</span></span> <span data-ttu-id="53624-264">Jak jsme uvedli [dříve](#highlighting-selected-lines), čísla řádků pro zvýraznění jsou relativní vzhledem k začátku fragmentu místo k začátku souboru.</span><span class="sxs-lookup"><span data-stu-id="53624-264">As noted [earlier](#highlighting-selected-lines), line numbers for highlighting are relative to the start of the snippet rather than the start of the file.</span></span>

> [!NOTE]
> <span data-ttu-id="53624-265">Název, který přiřadíte závislému úložišti, je relativní vzhledem ke kořenu hlavního úložiště, ale znak tilda (~) odkazuje na kořen sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="53624-265">The name you assign to the dependent repository is relative to the root of the main repository, but the tilde (~) refers to the root of the doc set.</span></span> <span data-ttu-id="53624-266">Kořen sady dokumentace je určený hodnotou `build_source_folder` v souboru *.openpublishing.publish.config.json*.</span><span class="sxs-lookup"><span data-stu-id="53624-266">The doc set root is determined by `build_source_folder` in *.openpublishing.publish.config.json*.</span></span> <span data-ttu-id="53624-267">Cesta k fragmentu kódu v předchozím příkladu funguje v úložišti azure-docs, protože `build_source_folder` odkazuje na kořen úložiště (`.`).</span><span class="sxs-lookup"><span data-stu-id="53624-267">The path to the snippet in the preceding example works in the azure-docs repo because `build_source_folder` refers to the repo root (`.`).</span></span> <span data-ttu-id="53624-268">Pokud hodnota `build_source_folder` je `articles`, bude cesta začínat `~/../samples-durable-functions` místo `~/samples-durable-functions`.</span><span class="sxs-lookup"><span data-stu-id="53624-268">If `build_source_folder` were `articles`, the path would start with `~/../samples-durable-functions` instead of `~/samples-durable-functions`.</span></span>

## <a name="interactive-code-snippets"></a><span data-ttu-id="53624-269">Interaktivní fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="53624-269">Interactive code snippets</span></span>

### <a name="inline-interactive-code-blocks"></a><span data-ttu-id="53624-270">Vložené interaktivní bloky kódu</span><span class="sxs-lookup"><span data-stu-id="53624-270">Inline interactive code blocks</span></span>

<span data-ttu-id="53624-271">U následujících jazyků je možné fragmenty kódu změnit na spustitelné v okně prohlížeče:</span><span class="sxs-lookup"><span data-stu-id="53624-271">For the following languages, code snippets can be made executable in the browser window:</span></span>

* <span data-ttu-id="53624-272">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="53624-272">Azure Cloud Shell</span></span>
* <span data-ttu-id="53624-273">Azure PowerShell Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="53624-273">Azure PowerShell Cloud Shell</span></span>
* <span data-ttu-id="53624-274">C# REPL</span><span class="sxs-lookup"><span data-stu-id="53624-274">C# REPL</span></span>

<span data-ttu-id="53624-275">Když je povolený interaktivní režim, mají rámečky s vykresleným kódem tlačítka **Vyzkoušet** nebo **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="53624-275">When interactive mode is enabled, the rendered code boxes have a **Try It** or **Run** button.</span></span> <span data-ttu-id="53624-276">Například:</span><span class="sxs-lookup"><span data-stu-id="53624-276">For example:</span></span>

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

<span data-ttu-id="53624-277">se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="53624-277">renders as follows:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

<span data-ttu-id="53624-278">Pokud chcete tuto funkci zapnout u konkrétního bloku kódu, použijte speciální identifikátor jazyka.</span><span class="sxs-lookup"><span data-stu-id="53624-278">To turn on this feature for a particular code block, use a special language identifier.</span></span> <span data-ttu-id="53624-279">Dostupné jsou následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="53624-279">The available options are:</span></span>

* <span data-ttu-id="53624-280">`azurepowershell-interactive` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.</span><span class="sxs-lookup"><span data-stu-id="53624-280">`azurepowershell-interactive` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="53624-281">`azurecli-interactive` – povolí Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="53624-281">`azurecli-interactive` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="53624-282">`csharp-interactive` – povolí C# REPL.</span><span class="sxs-lookup"><span data-stu-id="53624-282">`csharp-interactive` - Enables the C# REPL</span></span>

<span data-ttu-id="53624-283">Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.</span><span class="sxs-lookup"><span data-stu-id="53624-283">For the Azure Cloud Shell and PowerShell Cloud Shell, users can run commands against only their own Azure account.</span></span>

### <a name="code-snippets-included-by-reference"></a><span data-ttu-id="53624-284">Fragmenty kódu zahrnuté pomocí odkazu</span><span class="sxs-lookup"><span data-stu-id="53624-284">Code snippets included by reference</span></span>

<span data-ttu-id="53624-285">Interaktivní režim můžete povolit pro fragmenty kódu, které jsou zahrnuté odkazem.</span><span class="sxs-lookup"><span data-stu-id="53624-285">You can enable interactive mode for code snippets included by reference.</span></span> <span data-ttu-id="53624-286">Tady jsou příklady:</span><span class="sxs-lookup"><span data-stu-id="53624-286">Here are examples:</span></span>

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

<span data-ttu-id="53624-287">Pokud chcete tuto funkci zapnout pro konkrétní blok kódu, použijte atribut `interactive`.</span><span class="sxs-lookup"><span data-stu-id="53624-287">To turn on this feature for a particular code block, use the `interactive` attribute.</span></span> <span data-ttu-id="53624-288">Dostupné hodnoty atributu jsou:</span><span class="sxs-lookup"><span data-stu-id="53624-288">The available attribute values are:</span></span>

* <span data-ttu-id="53624-289">`cloudshell-powershell` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.</span><span class="sxs-lookup"><span data-stu-id="53624-289">`cloudshell-powershell` - Enables the Azure PowerShell Cloud Shell, as in the preceding example</span></span>
* <span data-ttu-id="53624-290">`cloudshell-bash` – povolí Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="53624-290">`cloudshell-bash` - Enables the Azure Cloud Shell</span></span>
* <span data-ttu-id="53624-291">`try-dotnet` – povolí Try .NET.</span><span class="sxs-lookup"><span data-stu-id="53624-291">`try-dotnet` - Enables Try .NET</span></span>
* <span data-ttu-id="53624-292">`try-dotnet-class` – povolí Try .NET s generováním tříd.</span><span class="sxs-lookup"><span data-stu-id="53624-292">`try-dotnet-class` - Enables Try .NET with class scaffolding</span></span>
* <span data-ttu-id="53624-293">`try-dotnet-method` – povolí Try .NET s generováním metod.</span><span class="sxs-lookup"><span data-stu-id="53624-293">`try-dotnet-method` - Enables Try .NET with method scaffolding</span></span>

<span data-ttu-id="53624-294">Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.</span><span class="sxs-lookup"><span data-stu-id="53624-294">For the Azure Cloud Shell and PowerShell Cloud Shell, users can only run commands against their own Azure account.</span></span>

## <a name="snippet-syntax-reference"></a><span data-ttu-id="53624-295">Přehled syntaxe fragmentů</span><span class="sxs-lookup"><span data-stu-id="53624-295">Snippet syntax reference</span></span>

<span data-ttu-id="53624-296">Syntaxe:</span><span class="sxs-lookup"><span data-stu-id="53624-296">Syntax:</span></span>

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> <span data-ttu-id="53624-297">Tato syntaxe je blokové rozšíření Markdownu.</span><span class="sxs-lookup"><span data-stu-id="53624-297">This syntax is a block Markdown extension.</span></span> <span data-ttu-id="53624-298">Musíte ji použít na samostatném řádku.</span><span class="sxs-lookup"><span data-stu-id="53624-298">It must be used on its own line.</span></span>

* <span data-ttu-id="53624-299">`<language>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="53624-299">`<language>` (*optional*)</span></span>
  * <span data-ttu-id="53624-300">Jazyk fragmentu kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-300">Language of the code snippet.</span></span> <span data-ttu-id="53624-301">Další informace najdete v části [Podporované jazyky](#supported-languages) dále v tomto článku.</span><span class="sxs-lookup"><span data-stu-id="53624-301">For more information, see the [Supported languages](#supported-languages) section later in this article.</span></span>

* <span data-ttu-id="53624-302">`<path>` (*povinné*)</span><span class="sxs-lookup"><span data-stu-id="53624-302">`<path>` (*mandatory*)</span></span>
  * <span data-ttu-id="53624-303">Relativní cesta v systému souborů označující soubor fragmentu kódu, na který se má odkazovat</span><span class="sxs-lookup"><span data-stu-id="53624-303">Relative path in the file system that indicates the code snippet file to reference.</span></span>

* <span data-ttu-id="53624-304">`<attribute>` a `<attribute-value>` (*volitelné*)</span><span class="sxs-lookup"><span data-stu-id="53624-304">`<attribute>` and `<attribute-value>` (*optional*)</span></span>

  <span data-ttu-id="53624-305">Společně se používají pro zadání, jak se má kód ze souboru načítat a jak se má zobrazovat:</span><span class="sxs-lookup"><span data-stu-id="53624-305">Used together to specify how the code should be retrieved from the file and how it should be displayed:</span></span>

  * <span data-ttu-id="53624-306">`range`: `1,3-5` Rozsah řádků.</span><span class="sxs-lookup"><span data-stu-id="53624-306">`range`: `1,3-5` A range of lines.</span></span> <span data-ttu-id="53624-307">Tento příklad zahrnuje řádky 1, 3, 4 a 5.</span><span class="sxs-lookup"><span data-stu-id="53624-307">This example includes lines 1, 3, 4, and 5.</span></span>
  * <span data-ttu-id="53624-308">`id`: `snippet_Create` ID fragmentu, který se má vložit ze souboru kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-308">`id`: `snippet_Create` The ID of the snippet that needs to be inserted from the code file.</span></span> <span data-ttu-id="53624-309">Tato hodnota nemůže existovat současně s rozsahem.</span><span class="sxs-lookup"><span data-stu-id="53624-309">This value cannot co-exist with range.</span></span>
  * <span data-ttu-id="53624-310">`highlight`: `2-4,6` Rozsah a/nebo čísla řádků, které se mají zvýraznit ve vygenerovaném fragmentu kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-310">`highlight`: `2-4,6` Range and/or numbers of lines that need to be highlighted in the generated code snippet.</span></span> <span data-ttu-id="53624-311">Číslování je relativní vzhledem k zobrazeným řádkům (jak je určeno rozsahem nebo ID), ne k souboru.</span><span class="sxs-lookup"><span data-stu-id="53624-311">The numbering is relative to the lines displayed (as specified by range or id), not the file.</span></span>
  * <span data-ttu-id="53624-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Hodnota řetězce určuje, jaké druhy interaktivity jsou povolené.</span><span class="sxs-lookup"><span data-stu-id="53624-312">`interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` String value determines what kinds of interactivity are enabled.</span></span>
  * <span data-ttu-id="53624-313">Podrobnosti o reprezentaci názvů značek ve zdrojových souborech fragmentu kódu v jednotlivých jazycích najdete v [pokynech pro DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="53624-313">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="53624-314">Podporované jazyky</span><span class="sxs-lookup"><span data-stu-id="53624-314">Supported languages</span></span>

<span data-ttu-id="53624-315">[Balíček pro vytváření obsahu na webu Docs](how-to-write-docs-auth-pack.md) obsahuje funkci pro dokončování příkazů a ověřování dostupných identifikátorů jazyků pro ohraničené bloky kódu.</span><span class="sxs-lookup"><span data-stu-id="53624-315">The [Docs Authoring Pack](how-to-write-docs-auth-pack.md) includes a feature to provide statement completion and validation of the available language identifiers for code fence blocks.</span></span>

### <a name="fenced-code-blocks"></a><span data-ttu-id="53624-316">Ohraničené bloky kódu</span><span class="sxs-lookup"><span data-stu-id="53624-316">Fenced code blocks</span></span>

| <span data-ttu-id="53624-317">Name</span><span class="sxs-lookup"><span data-stu-id="53624-317">Name</span></span>                           | <span data-ttu-id="53624-318">Platné aliasy</span><span class="sxs-lookup"><span data-stu-id="53624-318">Valid aliases</span></span>                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="53624-319">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="53624-319">.NET Core CLI</span></span>                  | `dotnetcli`                                                                    |
| <span data-ttu-id="53624-320">1C</span><span class="sxs-lookup"><span data-stu-id="53624-320">1C</span></span>                             | `1c`                                                                           |
| <span data-ttu-id="53624-321">ABNF</span><span class="sxs-lookup"><span data-stu-id="53624-321">ABNF</span></span>                           | `abnf`                                                                         |
| <span data-ttu-id="53624-322">Přístupové protokoly</span><span class="sxs-lookup"><span data-stu-id="53624-322">Access logs</span></span>                    | `accesslog`                                                                    |
| <span data-ttu-id="53624-323">Ada</span><span class="sxs-lookup"><span data-stu-id="53624-323">Ada</span></span>                            | `ada`                                                                          |
| <span data-ttu-id="53624-324">Assembler ARM</span><span class="sxs-lookup"><span data-stu-id="53624-324">ARM assembler</span></span>                  | <span data-ttu-id="53624-325">`armasm`, `arm`</span><span class="sxs-lookup"><span data-stu-id="53624-325">`armasm`, `arm`</span></span>                                                                |
| <span data-ttu-id="53624-326">Assembler AVR</span><span class="sxs-lookup"><span data-stu-id="53624-326">AVR assembler</span></span>                  | `avrasm`                                                                       |
| <span data-ttu-id="53624-327">ActionScript</span><span class="sxs-lookup"><span data-stu-id="53624-327">ActionScript</span></span>                   | <span data-ttu-id="53624-328">`actionscript`, `as`</span><span class="sxs-lookup"><span data-stu-id="53624-328">`actionscript`, `as`</span></span>                                                           |
| <span data-ttu-id="53624-329">Alan</span><span class="sxs-lookup"><span data-stu-id="53624-329">Alan</span></span>                           | <span data-ttu-id="53624-330">`alan`, `i`</span><span class="sxs-lookup"><span data-stu-id="53624-330">`alan`, `i`</span></span>                                                                    |
| <span data-ttu-id="53624-331">AngelScript</span><span class="sxs-lookup"><span data-stu-id="53624-331">AngelScript</span></span>                    | <span data-ttu-id="53624-332">`angelscript`, `asc`</span><span class="sxs-lookup"><span data-stu-id="53624-332">`angelscript`, `asc`</span></span>                                                           |
| <span data-ttu-id="53624-333">ANTLR</span><span class="sxs-lookup"><span data-stu-id="53624-333">ANTLR</span></span>                          | `antlr`                                                                        |
| <span data-ttu-id="53624-334">Apache</span><span class="sxs-lookup"><span data-stu-id="53624-334">Apache</span></span>                         | <span data-ttu-id="53624-335">`apache`, `apacheconf`</span><span class="sxs-lookup"><span data-stu-id="53624-335">`apache`, `apacheconf`</span></span>                                                         |
| <span data-ttu-id="53624-336">AppleScript</span><span class="sxs-lookup"><span data-stu-id="53624-336">AppleScript</span></span>                    | <span data-ttu-id="53624-337">`applescript`, `osascript`</span><span class="sxs-lookup"><span data-stu-id="53624-337">`applescript`, `osascript`</span></span>                                                     |
| <span data-ttu-id="53624-338">Arcade</span><span class="sxs-lookup"><span data-stu-id="53624-338">Arcade</span></span>                         | `arcade`                                                                       |
| <span data-ttu-id="53624-339">AsciiDoc</span><span class="sxs-lookup"><span data-stu-id="53624-339">AsciiDoc</span></span>                       | <span data-ttu-id="53624-340">`asciidoc`, `adoc`</span><span class="sxs-lookup"><span data-stu-id="53624-340">`asciidoc`, `adoc`</span></span>                                                             |
| <span data-ttu-id="53624-341">AspectJ</span><span class="sxs-lookup"><span data-stu-id="53624-341">AspectJ</span></span>                        | `aspectj`                                                                      |
| <span data-ttu-id="53624-342">ASPX</span><span class="sxs-lookup"><span data-stu-id="53624-342">ASPX</span></span>                           | `aspx`                                                                         |
| <span data-ttu-id="53624-343">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="53624-343">ASP.NET (C#)</span></span>                   | `aspx-csharp`                                                                  |
| <span data-ttu-id="53624-344">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="53624-344">ASP.NET (VB)</span></span>                   | `aspx-vb`                                                                      |
| <span data-ttu-id="53624-345">AutoHotkey</span><span class="sxs-lookup"><span data-stu-id="53624-345">AutoHotkey</span></span>                     | `autohotkey`                                                                   |
| <span data-ttu-id="53624-346">AutoIt</span><span class="sxs-lookup"><span data-stu-id="53624-346">AutoIt</span></span>                         | `autoit`                                                                       |
| <span data-ttu-id="53624-347">Awk</span><span class="sxs-lookup"><span data-stu-id="53624-347">Awk</span></span>                            | <span data-ttu-id="53624-348">`awk`, `mawk`, `nawk`, `gawk`</span><span class="sxs-lookup"><span data-stu-id="53624-348">`awk`, `mawk`, `nawk`, `gawk`</span></span>                                                  |
| <span data-ttu-id="53624-349">Axapta</span><span class="sxs-lookup"><span data-stu-id="53624-349">Axapta</span></span>                         | `axapta`                                                                       |
| <span data-ttu-id="53624-350">AzCopy</span><span class="sxs-lookup"><span data-stu-id="53624-350">AzCopy</span></span>                         | `azcopy`                                                                       |
| <span data-ttu-id="53624-351">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="53624-351">Azure CLI</span></span>                      | `azurecli`                                                                     |
| <span data-ttu-id="53624-352">Azure CLI (Interactive)</span><span class="sxs-lookup"><span data-stu-id="53624-352">Azure CLI (Interactive)</span></span>        | `azurecli-interactive`                                                         |
| <span data-ttu-id="53624-353">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="53624-353">Azure Powershell</span></span>               | `azurepowershell`                                                              |
| <span data-ttu-id="53624-354">Azure Powershell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="53624-354">Azure Powershell (Interactive)</span></span> | `azurepowershell-interactive`                                                  |
| <span data-ttu-id="53624-355">Bash</span><span class="sxs-lookup"><span data-stu-id="53624-355">Bash</span></span>                           | <span data-ttu-id="53624-356">`bash`, `sh`, `zsh`</span><span class="sxs-lookup"><span data-stu-id="53624-356">`bash`, `sh`, `zsh`</span></span>                                                            |
| <span data-ttu-id="53624-357">Basic</span><span class="sxs-lookup"><span data-stu-id="53624-357">Basic</span></span>                          | `basic`                                                                        |
| <span data-ttu-id="53624-358">BNF</span><span class="sxs-lookup"><span data-stu-id="53624-358">BNF</span></span>                            | `bnf`                                                                          |
| <span data-ttu-id="53624-359">C</span><span class="sxs-lookup"><span data-stu-id="53624-359">C</span></span>                              | `c`                                                                            |
| <span data-ttu-id="53624-360">C#</span><span class="sxs-lookup"><span data-stu-id="53624-360">C#</span></span>                             | <span data-ttu-id="53624-361">`csharp`, `cs`</span><span class="sxs-lookup"><span data-stu-id="53624-361">`csharp`, `cs`</span></span>                                                                 |
| <span data-ttu-id="53624-362">C# (Interactive)</span><span class="sxs-lookup"><span data-stu-id="53624-362">C# (Interactive)</span></span>               | `csharp-interactive`                                                           |
| <span data-ttu-id="53624-363">C++</span><span class="sxs-lookup"><span data-stu-id="53624-363">C++</span></span>                            | <span data-ttu-id="53624-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span><span class="sxs-lookup"><span data-stu-id="53624-364">`cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`</span></span>                                     |
| <span data-ttu-id="53624-365">C++/CX</span><span class="sxs-lookup"><span data-stu-id="53624-365">C++/CX</span></span>                         | `cppcx`                                                                        |
| <span data-ttu-id="53624-366">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="53624-366">C++/WinRT</span></span>                      | `cppwinrt`                                                                     |
| <span data-ttu-id="53624-367">C/AL</span><span class="sxs-lookup"><span data-stu-id="53624-367">C/AL</span></span>                           | `cal`                                                                          |
| <span data-ttu-id="53624-368">Cache Object Script</span><span class="sxs-lookup"><span data-stu-id="53624-368">Cache Object Script</span></span>            | <span data-ttu-id="53624-369">`cos`, `cls`</span><span class="sxs-lookup"><span data-stu-id="53624-369">`cos`, `cls`</span></span>                                                                   |
| <span data-ttu-id="53624-370">CMake</span><span class="sxs-lookup"><span data-stu-id="53624-370">CMake</span></span>                          | <span data-ttu-id="53624-371">`cmake`, `cmake.in`</span><span class="sxs-lookup"><span data-stu-id="53624-371">`cmake`, `cmake.in`</span></span>                                                            |
| <span data-ttu-id="53624-372">Coq</span><span class="sxs-lookup"><span data-stu-id="53624-372">Coq</span></span>                            | `coq`                                                                          |
| <span data-ttu-id="53624-373">CSP</span><span class="sxs-lookup"><span data-stu-id="53624-373">CSP</span></span>                            | `csp`                                                                          |
| <span data-ttu-id="53624-374">CSS</span><span class="sxs-lookup"><span data-stu-id="53624-374">CSS</span></span>                            | `css`                                                                          |
| <span data-ttu-id="53624-375">Cap'n Proto</span><span class="sxs-lookup"><span data-stu-id="53624-375">Cap'n Proto</span></span>                    | <span data-ttu-id="53624-376">`capnproto`, `capnp`</span><span class="sxs-lookup"><span data-stu-id="53624-376">`capnproto`, `capnp`</span></span>                                                           |
| <span data-ttu-id="53624-377">Clojure</span><span class="sxs-lookup"><span data-stu-id="53624-377">Clojure</span></span>                        | <span data-ttu-id="53624-378">`clojure`, `clj`</span><span class="sxs-lookup"><span data-stu-id="53624-378">`clojure`, `clj`</span></span>                                                               |
| <span data-ttu-id="53624-379">CoffeeScript</span><span class="sxs-lookup"><span data-stu-id="53624-379">CoffeeScript</span></span>                   | <span data-ttu-id="53624-380">`coffeescript`, `coffee`, `cson`, `iced`</span><span class="sxs-lookup"><span data-stu-id="53624-380">`coffeescript`, `coffee`, `cson`, `iced`</span></span>                                       |
| <span data-ttu-id="53624-381">Crmsh</span><span class="sxs-lookup"><span data-stu-id="53624-381">Crmsh</span></span>                          | <span data-ttu-id="53624-382">`crmsh`, `crm`, `pcmk`</span><span class="sxs-lookup"><span data-stu-id="53624-382">`crmsh`, `crm`, `pcmk`</span></span>                                                         |
| <span data-ttu-id="53624-383">Crystal</span><span class="sxs-lookup"><span data-stu-id="53624-383">Crystal</span></span>                        | <span data-ttu-id="53624-384">`crystal`, `cr`</span><span class="sxs-lookup"><span data-stu-id="53624-384">`crystal`, `cr`</span></span>                                                                |
| <span data-ttu-id="53624-385">Cypher (Neo4j)</span><span class="sxs-lookup"><span data-stu-id="53624-385">Cypher (Neo4j)</span></span>                 | `cypher`                                                                       |
| <span data-ttu-id="53624-386">D</span><span class="sxs-lookup"><span data-stu-id="53624-386">D</span></span>                              | `d`                                                                            |
| <span data-ttu-id="53624-387">DAX Power BI</span><span class="sxs-lookup"><span data-stu-id="53624-387">DAX Power BI</span></span>                   | `dax`                                                                          |
| <span data-ttu-id="53624-388">Soubor zóny DNS</span><span class="sxs-lookup"><span data-stu-id="53624-388">DNS Zone file</span></span>                  | <span data-ttu-id="53624-389">`dns`, `zone`, `bind`</span><span class="sxs-lookup"><span data-stu-id="53624-389">`dns`, `zone`, `bind`</span></span>                                                          |
| <span data-ttu-id="53624-390">DOS</span><span class="sxs-lookup"><span data-stu-id="53624-390">DOS</span></span>                            | <span data-ttu-id="53624-391">`dos`, `bat`, `cmd`</span><span class="sxs-lookup"><span data-stu-id="53624-391">`dos`, `bat`, `cmd`</span></span>                                                            |
| <span data-ttu-id="53624-392">Dart</span><span class="sxs-lookup"><span data-stu-id="53624-392">Dart</span></span>                           | `dart`                                                                         |
| <span data-ttu-id="53624-393">Delphi</span><span class="sxs-lookup"><span data-stu-id="53624-393">Delphi</span></span>                         | <span data-ttu-id="53624-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span><span class="sxs-lookup"><span data-stu-id="53624-394">`delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm`</span></span> |
| <span data-ttu-id="53624-395">Diff</span><span class="sxs-lookup"><span data-stu-id="53624-395">Diff</span></span>                           | <span data-ttu-id="53624-396">`diff`, `patch`</span><span class="sxs-lookup"><span data-stu-id="53624-396">`diff`, `patch`</span></span>                                                                |
| <span data-ttu-id="53624-397">Django</span><span class="sxs-lookup"><span data-stu-id="53624-397">Django</span></span>                         | <span data-ttu-id="53624-398">`django`, `jinja`</span><span class="sxs-lookup"><span data-stu-id="53624-398">`django`, `jinja`</span></span>                                                              |
| <span data-ttu-id="53624-399">Dockerfile</span><span class="sxs-lookup"><span data-stu-id="53624-399">Dockerfile</span></span>                     | <span data-ttu-id="53624-400">`dockerfile`, `docker`</span><span class="sxs-lookup"><span data-stu-id="53624-400">`dockerfile`, `docker`</span></span>                                                         |
| <span data-ttu-id="53624-401">dsconfig</span><span class="sxs-lookup"><span data-stu-id="53624-401">dsconfig</span></span>                       | `dsconfig`                                                                     |
| <span data-ttu-id="53624-402">DTS (strom zařízení)</span><span class="sxs-lookup"><span data-stu-id="53624-402">DTS (Device Tree)</span></span>              | `dts`                                                                          |
| <span data-ttu-id="53624-403">Dust</span><span class="sxs-lookup"><span data-stu-id="53624-403">Dust</span></span>                           | <span data-ttu-id="53624-404">`dust`, `dst`</span><span class="sxs-lookup"><span data-stu-id="53624-404">`dust`, `dst`</span></span>                                                                  |
| <span data-ttu-id="53624-405">Dylan</span><span class="sxs-lookup"><span data-stu-id="53624-405">Dylan</span></span>                          | `dylan`                                                                        |
| <span data-ttu-id="53624-406">EBNF</span><span class="sxs-lookup"><span data-stu-id="53624-406">EBNF</span></span>                           | `ebnf`                                                                         |
| <span data-ttu-id="53624-407">Elixir</span><span class="sxs-lookup"><span data-stu-id="53624-407">Elixir</span></span>                         | `elixir`                                                                       |
| <span data-ttu-id="53624-408">Elm</span><span class="sxs-lookup"><span data-stu-id="53624-408">Elm</span></span>                            | `elm`                                                                          |
| <span data-ttu-id="53624-409">Erlang</span><span class="sxs-lookup"><span data-stu-id="53624-409">Erlang</span></span>                         | <span data-ttu-id="53624-410">`erlang`, `erl`</span><span class="sxs-lookup"><span data-stu-id="53624-410">`erlang`, `erl`</span></span>                                                                |
| <span data-ttu-id="53624-411">Excel</span><span class="sxs-lookup"><span data-stu-id="53624-411">Excel</span></span>                          | <span data-ttu-id="53624-412">`excel`, `xls`, `xlsx`</span><span class="sxs-lookup"><span data-stu-id="53624-412">`excel`, `xls`, `xlsx`</span></span>                                                         |
| <span data-ttu-id="53624-413">Extempore</span><span class="sxs-lookup"><span data-stu-id="53624-413">Extempore</span></span>                      | <span data-ttu-id="53624-414">`extempore`, `xtlang`, `xtm`</span><span class="sxs-lookup"><span data-stu-id="53624-414">`extempore`, `xtlang`, `xtm`</span></span>                                                   |
| <span data-ttu-id="53624-415">F#</span><span class="sxs-lookup"><span data-stu-id="53624-415">F#</span></span>                             | <span data-ttu-id="53624-416">`fsharp`, `fs`</span><span class="sxs-lookup"><span data-stu-id="53624-416">`fsharp`, `fs`</span></span>                                                                 |
| <span data-ttu-id="53624-417">FIX</span><span class="sxs-lookup"><span data-stu-id="53624-417">FIX</span></span>                            | `fix`                                                                          |
| <span data-ttu-id="53624-418">Fortran</span><span class="sxs-lookup"><span data-stu-id="53624-418">Fortran</span></span>                        | <span data-ttu-id="53624-419">`fortran`, `f90`, `f95`</span><span class="sxs-lookup"><span data-stu-id="53624-419">`fortran`, `f90`, `f95`</span></span>                                                        |
| <span data-ttu-id="53624-420">G-Code</span><span class="sxs-lookup"><span data-stu-id="53624-420">G-Code</span></span>                         | <span data-ttu-id="53624-421">`gcode`, `nc`</span><span class="sxs-lookup"><span data-stu-id="53624-421">`gcode`, `nc`</span></span>                                                                  |
| <span data-ttu-id="53624-422">Gams</span><span class="sxs-lookup"><span data-stu-id="53624-422">Gams</span></span>                           | <span data-ttu-id="53624-423">`gams`, `gms`</span><span class="sxs-lookup"><span data-stu-id="53624-423">`gams`, `gms`</span></span>                                                                  |
| <span data-ttu-id="53624-424">GAUSS</span><span class="sxs-lookup"><span data-stu-id="53624-424">GAUSS</span></span>                          | <span data-ttu-id="53624-425">`gauss`, `gss`</span><span class="sxs-lookup"><span data-stu-id="53624-425">`gauss`, `gss`</span></span>                                                                 |
| <span data-ttu-id="53624-426">GDScript</span><span class="sxs-lookup"><span data-stu-id="53624-426">GDScript</span></span>                       | <span data-ttu-id="53624-427">`godot`, `gdscript`</span><span class="sxs-lookup"><span data-stu-id="53624-427">`godot`, `gdscript`</span></span>                                                            |
| <span data-ttu-id="53624-428">Gherkin</span><span class="sxs-lookup"><span data-stu-id="53624-428">Gherkin</span></span>                        | `gherkin`                                                                      |
| <span data-ttu-id="53624-429">GN for Ninja</span><span class="sxs-lookup"><span data-stu-id="53624-429">GN for Ninja</span></span>                   | <span data-ttu-id="53624-430">`gn`, `gni`</span><span class="sxs-lookup"><span data-stu-id="53624-430">`gn`, `gni`</span></span>                                                                    |
| <span data-ttu-id="53624-431">Go</span><span class="sxs-lookup"><span data-stu-id="53624-431">Go</span></span>                             | <span data-ttu-id="53624-432">`go`, `golang`</span><span class="sxs-lookup"><span data-stu-id="53624-432">`go`, `golang`</span></span>                                                                 |
| <span data-ttu-id="53624-433">Golo</span><span class="sxs-lookup"><span data-stu-id="53624-433">Golo</span></span>                           | <span data-ttu-id="53624-434">`golo`, `gololang`</span><span class="sxs-lookup"><span data-stu-id="53624-434">`golo`, `gololang`</span></span>                                                             |
| <span data-ttu-id="53624-435">Gradle</span><span class="sxs-lookup"><span data-stu-id="53624-435">Gradle</span></span>                         | `gradle`                                                                       |
| <span data-ttu-id="53624-436">Groovy</span><span class="sxs-lookup"><span data-stu-id="53624-436">Groovy</span></span>                         | `groovy`                                                                       |
| <span data-ttu-id="53624-437">HTML</span><span class="sxs-lookup"><span data-stu-id="53624-437">HTML</span></span>                           | <span data-ttu-id="53624-438">`html`, `xhtml`</span><span class="sxs-lookup"><span data-stu-id="53624-438">`html`, `xhtml`</span></span>                                                                |
| <span data-ttu-id="53624-439">HTTP</span><span class="sxs-lookup"><span data-stu-id="53624-439">HTTP</span></span>                           | <span data-ttu-id="53624-440">`http`, `https`</span><span class="sxs-lookup"><span data-stu-id="53624-440">`http`, `https`</span></span>                                                                |
| <span data-ttu-id="53624-441">Haml</span><span class="sxs-lookup"><span data-stu-id="53624-441">Haml</span></span>                           | `haml`                                                                         |
| <span data-ttu-id="53624-442">Handlebars</span><span class="sxs-lookup"><span data-stu-id="53624-442">Handlebars</span></span>                     | <span data-ttu-id="53624-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span><span class="sxs-lookup"><span data-stu-id="53624-443">`handlebars`, `hbs`, `html.hbs`, `html.handlebars`</span></span>                             |
| <span data-ttu-id="53624-444">Haskell</span><span class="sxs-lookup"><span data-stu-id="53624-444">Haskell</span></span>                        | <span data-ttu-id="53624-445">`haskell`, `hs`</span><span class="sxs-lookup"><span data-stu-id="53624-445">`haskell`, `hs`</span></span>                                                                |
| <span data-ttu-id="53624-446">Haxe</span><span class="sxs-lookup"><span data-stu-id="53624-446">Haxe</span></span>                           | <span data-ttu-id="53624-447">`haxe`, `hx`</span><span class="sxs-lookup"><span data-stu-id="53624-447">`haxe`, `hx`</span></span>                                                                   |
| <span data-ttu-id="53624-448">Hy</span><span class="sxs-lookup"><span data-stu-id="53624-448">Hy</span></span>                             | <span data-ttu-id="53624-449">`hy`, `hylang`</span><span class="sxs-lookup"><span data-stu-id="53624-449">`hy`, `hylang`</span></span>                                                                 |
| <span data-ttu-id="53624-450">Ini</span><span class="sxs-lookup"><span data-stu-id="53624-450">Ini</span></span>                            | `ini`                                                                          |
| <span data-ttu-id="53624-451">Inform7</span><span class="sxs-lookup"><span data-stu-id="53624-451">Inform7</span></span>                        | <span data-ttu-id="53624-452">`inform7`, `i7`</span><span class="sxs-lookup"><span data-stu-id="53624-452">`inform7`, `i7`</span></span>                                                                |
| <span data-ttu-id="53624-453">IRPF90</span><span class="sxs-lookup"><span data-stu-id="53624-453">IRPF90</span></span>                         | `irpf90`                                                                       |
| <span data-ttu-id="53624-454">JSON</span><span class="sxs-lookup"><span data-stu-id="53624-454">JSON</span></span>                           | `json`                                                                         |
| <span data-ttu-id="53624-455">Java</span><span class="sxs-lookup"><span data-stu-id="53624-455">Java</span></span>                           | <span data-ttu-id="53624-456">`java`, `jsp`</span><span class="sxs-lookup"><span data-stu-id="53624-456">`java`, `jsp`</span></span>                                                                  |
| <span data-ttu-id="53624-457">JavaScript</span><span class="sxs-lookup"><span data-stu-id="53624-457">JavaScript</span></span>                     | <span data-ttu-id="53624-458">`javascript`, `js`, `jsx`</span><span class="sxs-lookup"><span data-stu-id="53624-458">`javascript`, `js`, `jsx`</span></span>                                                      |
| <span data-ttu-id="53624-459">Kotlin</span><span class="sxs-lookup"><span data-stu-id="53624-459">Kotlin</span></span>                         | <span data-ttu-id="53624-460">`kotlin`, `kt`</span><span class="sxs-lookup"><span data-stu-id="53624-460">`kotlin`, `kt`</span></span>                                                                 |
| <span data-ttu-id="53624-461">Kusto</span><span class="sxs-lookup"><span data-stu-id="53624-461">Kusto</span></span>                          | `kusto`                                                                        |
| <span data-ttu-id="53624-462">Leaf</span><span class="sxs-lookup"><span data-stu-id="53624-462">Leaf</span></span>                           | `leaf`                                                                         |
| <span data-ttu-id="53624-463">Lasso</span><span class="sxs-lookup"><span data-stu-id="53624-463">Lasso</span></span>                          | <span data-ttu-id="53624-464">`lasso`, `ls`, `lassoscript`</span><span class="sxs-lookup"><span data-stu-id="53624-464">`lasso`, `ls`, `lassoscript`</span></span>                                                   |
| <span data-ttu-id="53624-465">Less</span><span class="sxs-lookup"><span data-stu-id="53624-465">Less</span></span>                           | `less`                                                                         |
| <span data-ttu-id="53624-466">LDIF</span><span class="sxs-lookup"><span data-stu-id="53624-466">LDIF</span></span>                           | `ldif`                                                                         |
| <span data-ttu-id="53624-467">Lispu</span><span class="sxs-lookup"><span data-stu-id="53624-467">Lisp</span></span>                           | `lisp`                                                                         |
| <span data-ttu-id="53624-468">LiveCode Server</span><span class="sxs-lookup"><span data-stu-id="53624-468">LiveCode Server</span></span>                | `livecodeserver`                                                               |
| <span data-ttu-id="53624-469">LiveScript</span><span class="sxs-lookup"><span data-stu-id="53624-469">LiveScript</span></span>                     | <span data-ttu-id="53624-470">`livescript`, `ls`</span><span class="sxs-lookup"><span data-stu-id="53624-470">`livescript`, `ls`</span></span>                                                             |
| <span data-ttu-id="53624-471">Lua</span><span class="sxs-lookup"><span data-stu-id="53624-471">Lua</span></span>                            | `lua`                                                                          |
| <span data-ttu-id="53624-472">Makefile (Soubor pravidel)</span><span class="sxs-lookup"><span data-stu-id="53624-472">Makefile</span></span>                       | <span data-ttu-id="53624-473">`makefile`, `mk`, `mak`</span><span class="sxs-lookup"><span data-stu-id="53624-473">`makefile`, `mk`, `mak`</span></span>                                                        |
| <span data-ttu-id="53624-474">Markdown</span><span class="sxs-lookup"><span data-stu-id="53624-474">Markdown</span></span>                       | <span data-ttu-id="53624-475">`markdown`, `md`, `mkdown`, `mkd`</span><span class="sxs-lookup"><span data-stu-id="53624-475">`markdown`, `md`, `mkdown`, `mkd`</span></span>                                              |
| <span data-ttu-id="53624-476">Mathematica</span><span class="sxs-lookup"><span data-stu-id="53624-476">Mathematica</span></span>                    | <span data-ttu-id="53624-477">`mathematica`, `mma`, `wl`</span><span class="sxs-lookup"><span data-stu-id="53624-477">`mathematica`, `mma`, `wl`</span></span>                                                     |
| <span data-ttu-id="53624-478">Matlab</span><span class="sxs-lookup"><span data-stu-id="53624-478">Matlab</span></span>                         | `matlab`                                                                       |
| <span data-ttu-id="53624-479">Maxima</span><span class="sxs-lookup"><span data-stu-id="53624-479">Maxima</span></span>                         | `maxima`                                                                       |
| <span data-ttu-id="53624-480">Maya Embedded Language</span><span class="sxs-lookup"><span data-stu-id="53624-480">Maya Embedded Language</span></span>         | `mel`                                                                          |
| <span data-ttu-id="53624-481">Mercury</span><span class="sxs-lookup"><span data-stu-id="53624-481">Mercury</span></span>                        | `mercury`                                                                      |
| <span data-ttu-id="53624-482">Skriptovací jazyk mIRC</span><span class="sxs-lookup"><span data-stu-id="53624-482">mIRC Scripting Language</span></span>        | <span data-ttu-id="53624-483">`mirc`, `mrc`</span><span class="sxs-lookup"><span data-stu-id="53624-483">`mirc`, `mrc`</span></span>                                                                  |
| <span data-ttu-id="53624-484">Mizar</span><span class="sxs-lookup"><span data-stu-id="53624-484">Mizar</span></span>                          | `mizar`                                                                        |
| <span data-ttu-id="53624-485">Formát MOF (Managed Object Format)</span><span class="sxs-lookup"><span data-stu-id="53624-485">Managed Object Format</span></span>          | `mof`                                                                          |
| <span data-ttu-id="53624-486">Mojolicious</span><span class="sxs-lookup"><span data-stu-id="53624-486">Mojolicious</span></span>                    | `mojolicious`                                                                  |
| <span data-ttu-id="53624-487">Monkey</span><span class="sxs-lookup"><span data-stu-id="53624-487">Monkey</span></span>                         | `monkey`                                                                       |
| <span data-ttu-id="53624-488">Moonscript</span><span class="sxs-lookup"><span data-stu-id="53624-488">Moonscript</span></span>                     | <span data-ttu-id="53624-489">`moonscript`, `moon`</span><span class="sxs-lookup"><span data-stu-id="53624-489">`moonscript`, `moon`</span></span>                                                           |
| <span data-ttu-id="53624-490">MS Graph (Interactive)</span><span class="sxs-lookup"><span data-stu-id="53624-490">MS Graph (Interactive)</span></span>         | `msgraph-interactive`                                                          |
| <span data-ttu-id="53624-491">N1QL</span><span class="sxs-lookup"><span data-stu-id="53624-491">N1QL</span></span>                           | `n1ql`                                                                         |
| <span data-ttu-id="53624-492">NSIS</span><span class="sxs-lookup"><span data-stu-id="53624-492">NSIS</span></span>                           | `nsis`                                                                         |
| <span data-ttu-id="53624-493">Nginx</span><span class="sxs-lookup"><span data-stu-id="53624-493">Nginx</span></span>                          | <span data-ttu-id="53624-494">`nginx`, `nginxconf`</span><span class="sxs-lookup"><span data-stu-id="53624-494">`nginx`, `nginxconf`</span></span>                                                           |
| <span data-ttu-id="53624-495">Nimrod</span><span class="sxs-lookup"><span data-stu-id="53624-495">Nimrod</span></span>                         | <span data-ttu-id="53624-496">`nimrod`, `nim`</span><span class="sxs-lookup"><span data-stu-id="53624-496">`nimrod`, `nim`</span></span>                                                                |
| <span data-ttu-id="53624-497">Nix</span><span class="sxs-lookup"><span data-stu-id="53624-497">Nix</span></span>                            | `nix`                                                                          |
| <span data-ttu-id="53624-498">OCaml</span><span class="sxs-lookup"><span data-stu-id="53624-498">OCaml</span></span>                          | <span data-ttu-id="53624-499">`ocaml`, `ml`</span><span class="sxs-lookup"><span data-stu-id="53624-499">`ocaml`, `ml`</span></span>                                                                  |
| <span data-ttu-id="53624-500">Objective C</span><span class="sxs-lookup"><span data-stu-id="53624-500">Objective C</span></span>                    | <span data-ttu-id="53624-501">`objectivec`, `mm`, `objc`, `obj-c`</span><span class="sxs-lookup"><span data-stu-id="53624-501">`objectivec`, `mm`, `objc`, `obj-c`</span></span>                                            |
| <span data-ttu-id="53624-502">OpenGL Shading Language</span><span class="sxs-lookup"><span data-stu-id="53624-502">OpenGL Shading Language</span></span>        | `glsl`                                                                         |
| <span data-ttu-id="53624-503">OpenSCAD</span><span class="sxs-lookup"><span data-stu-id="53624-503">OpenSCAD</span></span>                       | <span data-ttu-id="53624-504">`openscad`, `scad`</span><span class="sxs-lookup"><span data-stu-id="53624-504">`openscad`, `scad`</span></span>                                                             |
| <span data-ttu-id="53624-505">Oracle Rules Language</span><span class="sxs-lookup"><span data-stu-id="53624-505">Oracle Rules Language</span></span>          | `ruleslanguage`                                                                |
| <span data-ttu-id="53624-506">Oxygene</span><span class="sxs-lookup"><span data-stu-id="53624-506">Oxygene</span></span>                        | `oxygene`                                                                      |
| <span data-ttu-id="53624-507">PF</span><span class="sxs-lookup"><span data-stu-id="53624-507">PF</span></span>                             | <span data-ttu-id="53624-508">`pf`, `pf.conf`</span><span class="sxs-lookup"><span data-stu-id="53624-508">`pf`, `pf.conf`</span></span>                                                                |
| <span data-ttu-id="53624-509">PHP</span><span class="sxs-lookup"><span data-stu-id="53624-509">PHP</span></span>                            | <span data-ttu-id="53624-510">`php`, `php3`, `php4`, `php5`, `php6`</span><span class="sxs-lookup"><span data-stu-id="53624-510">`php`, `php3`, `php4`, `php5`, `php6`</span></span>                                          |
| <span data-ttu-id="53624-511">Parser3</span><span class="sxs-lookup"><span data-stu-id="53624-511">Parser3</span></span>                        | `parser3`                                                                      |
| <span data-ttu-id="53624-512">Perl</span><span class="sxs-lookup"><span data-stu-id="53624-512">Perl</span></span>                           | <span data-ttu-id="53624-513">`perl`, `pl`, `pm`</span><span class="sxs-lookup"><span data-stu-id="53624-513">`perl`, `pl`, `pm`</span></span>                                                             |
| <span data-ttu-id="53624-514">Nešifrovaný text bez zvýraznění</span><span class="sxs-lookup"><span data-stu-id="53624-514">Plaintext no highlight</span></span>         | `plaintext`                                                                    |
| <span data-ttu-id="53624-515">Pony</span><span class="sxs-lookup"><span data-stu-id="53624-515">Pony</span></span>                           | `pony`                                                                         |
| <span data-ttu-id="53624-516">PostgreSQL & PL/pgSQL</span><span class="sxs-lookup"><span data-stu-id="53624-516">PostgreSQL & PL/pgSQL</span></span>          | <span data-ttu-id="53624-517">`pgsql`, `postgres`, `postgresql`</span><span class="sxs-lookup"><span data-stu-id="53624-517">`pgsql`, `postgres`, `postgresql`</span></span>                                              |
| <span data-ttu-id="53624-518">PowerShell</span><span class="sxs-lookup"><span data-stu-id="53624-518">PowerShell</span></span>                     | <span data-ttu-id="53624-519">`powershell`, `ps`</span><span class="sxs-lookup"><span data-stu-id="53624-519">`powershell`, `ps`</span></span>                                                             |
| <span data-ttu-id="53624-520">PowerShell (Interactive)</span><span class="sxs-lookup"><span data-stu-id="53624-520">PowerShell (Interactive)</span></span>       | `powershell-interactive`                                                       |
| <span data-ttu-id="53624-521">Processing</span><span class="sxs-lookup"><span data-stu-id="53624-521">Processing</span></span>                     | `processing`                                                                   |
| <span data-ttu-id="53624-522">Prolog</span><span class="sxs-lookup"><span data-stu-id="53624-522">Prolog</span></span>                         | `prolog`                                                                       |
| <span data-ttu-id="53624-523">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="53624-523">Properties</span></span>                     | `properties`                                                                   |
| <span data-ttu-id="53624-524">Vyrovnávací paměti protokolu</span><span class="sxs-lookup"><span data-stu-id="53624-524">Protocol Buffers</span></span>               | `protobuf`                                                                     |
| <span data-ttu-id="53624-525">Puppet</span><span class="sxs-lookup"><span data-stu-id="53624-525">Puppet</span></span>                         | <span data-ttu-id="53624-526">`puppet`, `pp`</span><span class="sxs-lookup"><span data-stu-id="53624-526">`puppet`, `pp`</span></span>                                                                 |
| <span data-ttu-id="53624-527">Python</span><span class="sxs-lookup"><span data-stu-id="53624-527">Python</span></span>                         | <span data-ttu-id="53624-528">`python`, `py`, `gyp`</span><span class="sxs-lookup"><span data-stu-id="53624-528">`python`, `py`, `gyp`</span></span>                                                          |
| <span data-ttu-id="53624-529">Výsledky profileru Pythonu</span><span class="sxs-lookup"><span data-stu-id="53624-529">Python profiler results</span></span>        | `profile`                                                                      |
| <span data-ttu-id="53624-530">Q#</span><span class="sxs-lookup"><span data-stu-id="53624-530">Q#</span></span>                             | `qsharp`                                                                       |
| <span data-ttu-id="53624-531">Q</span><span class="sxs-lookup"><span data-stu-id="53624-531">Q</span></span>                              | <span data-ttu-id="53624-532">`k`, `kdb`</span><span class="sxs-lookup"><span data-stu-id="53624-532">`k`, `kdb`</span></span>                                                                     |
| <span data-ttu-id="53624-533">QML</span><span class="sxs-lookup"><span data-stu-id="53624-533">QML</span></span>                            | `qml`                                                                          |
| <span data-ttu-id="53624-534">R</span><span class="sxs-lookup"><span data-stu-id="53624-534">R</span></span>                              | `r`                                                                            |
| <span data-ttu-id="53624-535">Razor CSHTML</span><span class="sxs-lookup"><span data-stu-id="53624-535">Razor CSHTML</span></span>                   | <span data-ttu-id="53624-536">`cshtml`, `razor`, `razor-cshtml`</span><span class="sxs-lookup"><span data-stu-id="53624-536">`cshtml`, `razor`, `razor-cshtml`</span></span>                                              |
| <span data-ttu-id="53624-537">ReasonML</span><span class="sxs-lookup"><span data-stu-id="53624-537">ReasonML</span></span>                       | <span data-ttu-id="53624-538">`reasonml`, `re`</span><span class="sxs-lookup"><span data-stu-id="53624-538">`reasonml`, `re`</span></span>                                                               |
| <span data-ttu-id="53624-539">RenderMan RIB</span><span class="sxs-lookup"><span data-stu-id="53624-539">RenderMan RIB</span></span>                  | `rib`                                                                          |
| <span data-ttu-id="53624-540">RenderMan RSL</span><span class="sxs-lookup"><span data-stu-id="53624-540">RenderMan RSL</span></span>                  | `rsl`                                                                          |
| <span data-ttu-id="53624-541">Roboconf</span><span class="sxs-lookup"><span data-stu-id="53624-541">Roboconf</span></span>                       | <span data-ttu-id="53624-542">`graph`, `instances`</span><span class="sxs-lookup"><span data-stu-id="53624-542">`graph`, `instances`</span></span>                                                           |
| <span data-ttu-id="53624-543">Robot Framework</span><span class="sxs-lookup"><span data-stu-id="53624-543">Robot Framework</span></span>                | <span data-ttu-id="53624-544">`robot`, `rf`</span><span class="sxs-lookup"><span data-stu-id="53624-544">`robot`, `rf`</span></span>                                                                  |
| <span data-ttu-id="53624-545">Soubory specifikace RPM</span><span class="sxs-lookup"><span data-stu-id="53624-545">RPM spec files</span></span>                 | <span data-ttu-id="53624-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span><span class="sxs-lookup"><span data-stu-id="53624-546">`rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`</span></span>                          |
| <span data-ttu-id="53624-547">Ruby</span><span class="sxs-lookup"><span data-stu-id="53624-547">Ruby</span></span>                           | <span data-ttu-id="53624-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span><span class="sxs-lookup"><span data-stu-id="53624-548">`ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`</span></span>                              |
| <span data-ttu-id="53624-549">Rust</span><span class="sxs-lookup"><span data-stu-id="53624-549">Rust</span></span>                           | <span data-ttu-id="53624-550">`rust`, `rs`</span><span class="sxs-lookup"><span data-stu-id="53624-550">`rust`, `rs`</span></span>                                                                   |
| <span data-ttu-id="53624-551">SAS</span><span class="sxs-lookup"><span data-stu-id="53624-551">SAS</span></span>                            | <span data-ttu-id="53624-552">`SAS`, `sas`</span><span class="sxs-lookup"><span data-stu-id="53624-552">`SAS`, `sas`</span></span>                                                                   |
| <span data-ttu-id="53624-553">SCSS</span><span class="sxs-lookup"><span data-stu-id="53624-553">SCSS</span></span>                           | `scss`                                                                         |
| <span data-ttu-id="53624-554">SQL</span><span class="sxs-lookup"><span data-stu-id="53624-554">SQL</span></span>                            | `sql`                                                                          |
| <span data-ttu-id="53624-555">STEP Part 21</span><span class="sxs-lookup"><span data-stu-id="53624-555">STEP Part 21</span></span>                   | <span data-ttu-id="53624-556">`p21`, `step`, `stp`</span><span class="sxs-lookup"><span data-stu-id="53624-556">`p21`, `step`, `stp`</span></span>                                                           |
| <span data-ttu-id="53624-557">Scala</span><span class="sxs-lookup"><span data-stu-id="53624-557">Scala</span></span>                          | `scala`                                                                        |
| <span data-ttu-id="53624-558">Scheme</span><span class="sxs-lookup"><span data-stu-id="53624-558">Scheme</span></span>                         | `scheme`                                                                       |
| <span data-ttu-id="53624-559">Scilab</span><span class="sxs-lookup"><span data-stu-id="53624-559">Scilab</span></span>                         | <span data-ttu-id="53624-560">`scilab`, `sci`</span><span class="sxs-lookup"><span data-stu-id="53624-560">`scilab`, `sci`</span></span>                                                                |
| <span data-ttu-id="53624-561">Shape Expressions</span><span class="sxs-lookup"><span data-stu-id="53624-561">Shape Expressions</span></span>              | `shexc`                                                                        |
| <span data-ttu-id="53624-562">Prostředí</span><span class="sxs-lookup"><span data-stu-id="53624-562">Shell</span></span>                          | <span data-ttu-id="53624-563">`shell`, `console`</span><span class="sxs-lookup"><span data-stu-id="53624-563">`shell`, `console`</span></span>                                                             |
| <span data-ttu-id="53624-564">Smali</span><span class="sxs-lookup"><span data-stu-id="53624-564">Smali</span></span>                          | `smali`                                                                        |
| <span data-ttu-id="53624-565">Smalltalk</span><span class="sxs-lookup"><span data-stu-id="53624-565">Smalltalk</span></span>                      | <span data-ttu-id="53624-566">`smalltalk`, `st`</span><span class="sxs-lookup"><span data-stu-id="53624-566">`smalltalk`, `st`</span></span>                                                              |
| <span data-ttu-id="53624-567">Solidity</span><span class="sxs-lookup"><span data-stu-id="53624-567">Solidity</span></span>                       | <span data-ttu-id="53624-568">`solidity`, `sol`</span><span class="sxs-lookup"><span data-stu-id="53624-568">`solidity`, `sol`</span></span>                                                              |
| <span data-ttu-id="53624-569">Stan</span><span class="sxs-lookup"><span data-stu-id="53624-569">Stan</span></span>                           | `stan`                                                                         |
| <span data-ttu-id="53624-570">Stata</span><span class="sxs-lookup"><span data-stu-id="53624-570">Stata</span></span>                          | `stata`                                                                        |
| <span data-ttu-id="53624-571">Structured Text</span><span class="sxs-lookup"><span data-stu-id="53624-571">Structured Text</span></span>                | <span data-ttu-id="53624-572">`iecst`, `scl`, `stl`, `structured-text`</span><span class="sxs-lookup"><span data-stu-id="53624-572">`iecst`, `scl`, `stl`, `structured-text`</span></span>                                       |
| <span data-ttu-id="53624-573">Stylus</span><span class="sxs-lookup"><span data-stu-id="53624-573">Stylus</span></span>                         | <span data-ttu-id="53624-574">`stylus`, `styl`</span><span class="sxs-lookup"><span data-stu-id="53624-574">`stylus`, `styl`</span></span>                                                               |
| <span data-ttu-id="53624-575">SubUnit</span><span class="sxs-lookup"><span data-stu-id="53624-575">SubUnit</span></span>                        | `subunit`                                                                      |
| <span data-ttu-id="53624-576">Supercollider</span><span class="sxs-lookup"><span data-stu-id="53624-576">Supercollider</span></span>                  | <span data-ttu-id="53624-577">`supercollider`, `sc`</span><span class="sxs-lookup"><span data-stu-id="53624-577">`supercollider`, `sc`</span></span>                                                          |
| <span data-ttu-id="53624-578">Swift</span><span class="sxs-lookup"><span data-stu-id="53624-578">Swift</span></span>                          | `swift`                                                                        |
| <span data-ttu-id="53624-579">Tcl</span><span class="sxs-lookup"><span data-stu-id="53624-579">Tcl</span></span>                            | <span data-ttu-id="53624-580">`tcl`, `tk`</span><span class="sxs-lookup"><span data-stu-id="53624-580">`tcl`, `tk`</span></span>                                                                    |
| <span data-ttu-id="53624-581">Terraform (HCL)</span><span class="sxs-lookup"><span data-stu-id="53624-581">Terraform (HCL)</span></span>                | <span data-ttu-id="53624-582">`terraform`, `tf`, `hcl`</span><span class="sxs-lookup"><span data-stu-id="53624-582">`terraform`, `tf`, `hcl`</span></span>                                                       |
| <span data-ttu-id="53624-583">Test Anything Protocol</span><span class="sxs-lookup"><span data-stu-id="53624-583">Test Anything Protocol</span></span>         | `tap`                                                                          |
| <span data-ttu-id="53624-584">TeX</span><span class="sxs-lookup"><span data-stu-id="53624-584">TeX</span></span>                            | `tex`                                                                          |
| <span data-ttu-id="53624-585">Thrift</span><span class="sxs-lookup"><span data-stu-id="53624-585">Thrift</span></span>                         | `thrift`                                                                       |
| <span data-ttu-id="53624-586">TOML</span><span class="sxs-lookup"><span data-stu-id="53624-586">TOML</span></span>                           | `toml`                                                                         |
| <span data-ttu-id="53624-587">TP</span><span class="sxs-lookup"><span data-stu-id="53624-587">TP</span></span>                             | `tp`                                                                           |
| <span data-ttu-id="53624-588">Twig</span><span class="sxs-lookup"><span data-stu-id="53624-588">Twig</span></span>                           | <span data-ttu-id="53624-589">`twig`, `craftcms`</span><span class="sxs-lookup"><span data-stu-id="53624-589">`twig`, `craftcms`</span></span>                                                             |
| <span data-ttu-id="53624-590">TypeScript</span><span class="sxs-lookup"><span data-stu-id="53624-590">TypeScript</span></span>                     | <span data-ttu-id="53624-591">`typescript`, `ts`</span><span class="sxs-lookup"><span data-stu-id="53624-591">`typescript`, `ts`</span></span>                                                             |
| <span data-ttu-id="53624-592">VB.NET</span><span class="sxs-lookup"><span data-stu-id="53624-592">VB.NET</span></span>                         | <span data-ttu-id="53624-593">`vbnet`, `vb`</span><span class="sxs-lookup"><span data-stu-id="53624-593">`vbnet`, `vb`</span></span>                                                                  |
| <span data-ttu-id="53624-594">VBScript</span><span class="sxs-lookup"><span data-stu-id="53624-594">VBScript</span></span>                       | <span data-ttu-id="53624-595">`vbscript`, `vbs`</span><span class="sxs-lookup"><span data-stu-id="53624-595">`vbscript`, `vbs`</span></span>                                                              |
| <span data-ttu-id="53624-596">VHDL</span><span class="sxs-lookup"><span data-stu-id="53624-596">VHDL</span></span>                           | `vhdl`                                                                         |
| <span data-ttu-id="53624-597">Vala</span><span class="sxs-lookup"><span data-stu-id="53624-597">Vala</span></span>                           | `vala`                                                                         |
| <span data-ttu-id="53624-598">Verilog</span><span class="sxs-lookup"><span data-stu-id="53624-598">Verilog</span></span>                        | <span data-ttu-id="53624-599">`verilog`, `v`</span><span class="sxs-lookup"><span data-stu-id="53624-599">`verilog`, `v`</span></span>                                                                 |
| <span data-ttu-id="53624-600">Skript Vim</span><span class="sxs-lookup"><span data-stu-id="53624-600">Vim Script</span></span>                     | `vim`                                                                          |
| <span data-ttu-id="53624-601">X++</span><span class="sxs-lookup"><span data-stu-id="53624-601">X++</span></span>                            | `xpp`                                                                          |
| <span data-ttu-id="53624-602">Sestavení x86</span><span class="sxs-lookup"><span data-stu-id="53624-602">x86 Assembly</span></span>                   | `x86asm`                                                                       |
| <span data-ttu-id="53624-603">XL</span><span class="sxs-lookup"><span data-stu-id="53624-603">XL</span></span>                             | <span data-ttu-id="53624-604">`xl`, `tao`</span><span class="sxs-lookup"><span data-stu-id="53624-604">`xl`, `tao`</span></span>                                                                    |
| <span data-ttu-id="53624-605">XQuery</span><span class="sxs-lookup"><span data-stu-id="53624-605">XQuery</span></span>                         | <span data-ttu-id="53624-606">`xquery`, `xpath`, `xq`</span><span class="sxs-lookup"><span data-stu-id="53624-606">`xquery`, `xpath`, `xq`</span></span>                                                        |
| <span data-ttu-id="53624-607">XAML</span><span class="sxs-lookup"><span data-stu-id="53624-607">XAML</span></span>                           | `xaml`                                                                         |
| <span data-ttu-id="53624-608">XML</span><span class="sxs-lookup"><span data-stu-id="53624-608">XML</span></span>                            | <span data-ttu-id="53624-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span><span class="sxs-lookup"><span data-stu-id="53624-609">`xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`</span></span>                    |
| <span data-ttu-id="53624-610">YAML</span><span class="sxs-lookup"><span data-stu-id="53624-610">YAML</span></span>                           | <span data-ttu-id="53624-611">`yml`, `yaml`</span><span class="sxs-lookup"><span data-stu-id="53624-611">`yml`, `yaml`</span></span>                                                                  |
| <span data-ttu-id="53624-612">Zephir</span><span class="sxs-lookup"><span data-stu-id="53624-612">Zephir</span></span>                         | <span data-ttu-id="53624-613">`zephir`, `zep`</span><span class="sxs-lookup"><span data-stu-id="53624-613">`zephir`, `zep`</span></span>                                                                |

> [!TIP]
> <span data-ttu-id="53624-614">V Balíčku pro vytváření obsahu na webu Docs používá [funkce Dokončování vývojářských jazyků](docs-authoring/dev-lang-completion.md) první platný alias, pokud je k dispozici více aliasů.</span><span class="sxs-lookup"><span data-stu-id="53624-614">The Docs Authoring Pack, [Dev Lang Completion feature](docs-authoring/dev-lang-completion.md) uses the first valid alias when multiple aliases are available.</span></span>

## <a name="next-steps"></a><span data-ttu-id="53624-615">Další kroky</span><span class="sxs-lookup"><span data-stu-id="53624-615">Next steps</span></span>

<span data-ttu-id="53624-616">Informace o formátování textu pro jiné typy obsahu než kód najdete v článku [Pokyny pro formátování textu](text-formatting-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="53624-616">For information on text formatting for content types other than code, see [Text formatting guidelines](text-formatting-guidelines.md).</span></span>
