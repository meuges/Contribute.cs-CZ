---
title: Zvláštní pokyny týkající se psaní vzorových skriptů
description: V tomto článku jsou zvláštní pravidla platná pro formátování vzorového kódu v PowerShellu. Pravidla platí pro obecné články s příklady i pro referenční rutiny.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290258"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="acbbd-104">Formátování vzorového kódu</span><span class="sxs-lookup"><span data-stu-id="acbbd-104">Formatting code samples</span></span>

<span data-ttu-id="acbbd-105">Ve stávající dokumentaci se postupně používalo více stylů, protože se pravidla formátování několikrát měnila.</span><span class="sxs-lookup"><span data-stu-id="acbbd-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="acbbd-106">V dokumentaci se snažíme zavést pro bloky kódu a výstupy PowerShellu jednotný styl.</span><span class="sxs-lookup"><span data-stu-id="acbbd-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="acbbd-107">Markdown podporuje dva různé styly kódu:</span><span class="sxs-lookup"><span data-stu-id="acbbd-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="acbbd-108">Rozsahy kódu (vložené) – označené jedním znakem apostrofu (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="acbbd-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="acbbd-109">Používá se uvnitř odstavce, nikoli jako samostatný blok.</span><span class="sxs-lookup"><span data-stu-id="acbbd-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="acbbd-110">Nejčastěji se používá k ohraničení názvů rutin.</span><span class="sxs-lookup"><span data-stu-id="acbbd-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="acbbd-111">Další informace viz [Syntaktické prvky formátování příkazů](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="acbbd-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="acbbd-112">Bloky kódu – více řádkový blok ohraničený třemi zpětnými apostrofy (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="acbbd-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="acbbd-113">Použití bloků kódu</span><span class="sxs-lookup"><span data-stu-id="acbbd-113">Using code blocks</span></span>

<span data-ttu-id="acbbd-114">V Markdownu můžete blok kódu označit odsazením. Tento způsob ale může být problematický, a proto byste ho neměli používat.</span><span class="sxs-lookup"><span data-stu-id="acbbd-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="acbbd-115">Všechny bloky kódu musí být ohraničené tzv. kódovým plotem.</span><span class="sxs-lookup"><span data-stu-id="acbbd-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="acbbd-116">Kódový plot je blok kódu, který je ohraničený třemi zpětnými apostrofy (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="acbbd-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="acbbd-117">Značky kódového plotu musí být na samostatném řádku před a za vzorovým kódem.</span><span class="sxs-lookup"><span data-stu-id="acbbd-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="acbbd-118">Značka na začátku bloku kódu může mít libovolný jazykový popisek.</span><span class="sxs-lookup"><span data-stu-id="acbbd-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="acbbd-119">V systému OPS (Open Publishing System) Microsoftu se jazykový popisek používá k podpoře funkce zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="acbbd-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="acbbd-120">Systém OPS také přidá **kopírovací** tlačítko, které zkopíruje obsah bloku kódu do schránky.</span><span class="sxs-lookup"><span data-stu-id="acbbd-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="acbbd-121">Tlačítkem můžete ukázku kódu rychle vložit do skriptu, abyste ji mohli otestovat.</span><span class="sxs-lookup"><span data-stu-id="acbbd-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="acbbd-122">Všechny ukázky kódu v naší dokumentaci ale nejdou tímto způsobem spouštět.</span><span class="sxs-lookup"><span data-stu-id="acbbd-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="acbbd-123">Některé bloky kódu můžou představovat jednoduchou ukázku principu PowerShellu nebo může jít o obecný příklad syntaxe.</span><span class="sxs-lookup"><span data-stu-id="acbbd-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="acbbd-124">V naší dokumentaci se používají dva typy bloků kódu:</span><span class="sxs-lookup"><span data-stu-id="acbbd-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="acbbd-125">Názorné příklady</span><span class="sxs-lookup"><span data-stu-id="acbbd-125">Illustrative examples</span></span>
2. <span data-ttu-id="acbbd-126">Spustitelné příklady</span><span class="sxs-lookup"><span data-stu-id="acbbd-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="acbbd-127">Formátování názorných příkladů</span><span class="sxs-lookup"><span data-stu-id="acbbd-127">Formatting illustrative examples</span></span>

<span data-ttu-id="acbbd-128">Ilustrativní příklady se používají k vysvětlení principů PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="acbbd-129">Nejsou určené ke zkopírování do schránky ani ke spuštění.</span><span class="sxs-lookup"><span data-stu-id="acbbd-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="acbbd-130">Nejčastěji se používají jako jednoduché příklady, které se dají jednoduše napsat.</span><span class="sxs-lookup"><span data-stu-id="acbbd-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="acbbd-131">Používají se také v příkladech syntaxe k ilustrování syntaxe příkazu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="acbbd-132">V ilustrativních příkladech se k označení začátku a konce bloku kódu používá tzv. holý kódový plot.</span><span class="sxs-lookup"><span data-stu-id="acbbd-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="acbbd-133">Blok kódu může obsahovat i ukázkový výstup vysvětlovaného příkazu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="acbbd-134">Syntaktický blok</span><span class="sxs-lookup"><span data-stu-id="acbbd-134">Syntax block</span></span>

<span data-ttu-id="acbbd-135">Tento příklad ilustruje všechny možné parametry rutiny `Get-Command`.</span><span class="sxs-lookup"><span data-stu-id="acbbd-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="acbbd-136">Tento příklad obecným způsobem popisuje výraz `for`:</span><span class="sxs-lookup"><span data-stu-id="acbbd-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="acbbd-137">Jednoduchý ilustrativní příklad</span><span class="sxs-lookup"><span data-stu-id="acbbd-137">Simple illustration example</span></span>

<span data-ttu-id="acbbd-138">Tady je příklad, který ilustruje srovnávací operátory PowerShellu:</span><span class="sxs-lookup"><span data-stu-id="acbbd-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="acbbd-139">Všimněte si zjednodušeného příkazového řádku PowerShellu a zobrazeného výsledného výstupu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="acbbd-140">V tomto případě nechceme, aby čtenář tento příklad kopíroval ani spouštěl.</span><span class="sxs-lookup"><span data-stu-id="acbbd-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="acbbd-141">Formátování spustitelných příkladů</span><span class="sxs-lookup"><span data-stu-id="acbbd-141">Formatting executable examples</span></span>

<span data-ttu-id="acbbd-142">Ve složitějších případech nebo v příkladech, které má smysl kopírovat a spouštět, byste měli použít následující označení stylu bloku:</span><span class="sxs-lookup"><span data-stu-id="acbbd-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="acbbd-143">Výstup zobrazený příkazy PowerShellu by měl být ohraničen jako blok kódu **Output** (Výstup), aby se zabránilo zvýraznění syntaxe.</span><span class="sxs-lookup"><span data-stu-id="acbbd-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="acbbd-144">Například:</span><span class="sxs-lookup"><span data-stu-id="acbbd-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="acbbd-145">Označení kódu **Output** nepředstavuje oficiální jazyk podporovaný systémem zvýrazňování syntaxe.</span><span class="sxs-lookup"><span data-stu-id="acbbd-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="acbbd-146">Přesto je toto označení užitečné, protože OPS přidá označení „Output“ do pole kódu na webové stránce.</span><span class="sxs-lookup"><span data-stu-id="acbbd-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="acbbd-147">V poli kódu „Output“ nebude zvýrazněna syntaxe.</span><span class="sxs-lookup"><span data-stu-id="acbbd-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="acbbd-148">Pravidla stylu psaní kódu</span><span class="sxs-lookup"><span data-stu-id="acbbd-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="acbbd-149">V ukázkách kódu se vyhýbejte pokračování řádku</span><span class="sxs-lookup"><span data-stu-id="acbbd-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="acbbd-150">V ukázkách kódu PowerShellu se vyhýbejte požití znaků (`` ` ``), které označují pokračování řádku.</span><span class="sxs-lookup"><span data-stu-id="acbbd-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="acbbd-151">Tyto znaky jsou špatně viditelné a můžou způsobovat problémy, pokud jsou na konci řádku nadbytečné mezery.</span><span class="sxs-lookup"><span data-stu-id="acbbd-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="acbbd-152">K omezení délky řádků v rutinách, které mají hodně parametrů, použijte seskupování PowerShellu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="acbbd-153">Použijte možnosti přirozeného dělení řádků v PowerShellu, jako je třeba znak svislé čáry (`|`) nebo počáteční, oblé či hranaté závorky.</span><span class="sxs-lookup"><span data-stu-id="acbbd-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="acbbd-154">V příkladech raději nepoužívejte výzvy PowerShellu</span><span class="sxs-lookup"><span data-stu-id="acbbd-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="acbbd-155">Nedoporučuje se používat řetězec, který označuje výzvu. Použijte ho jenom ve scénářích, které ilustrují použití příkazového řádku.</span><span class="sxs-lookup"><span data-stu-id="acbbd-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="acbbd-156">Výzvy jsou nutné v příkladech, které ilustrují příkazy měnící výzvu, nebo když má zobrazená cesta určitý význam v popisovaném scénáři.</span><span class="sxs-lookup"><span data-stu-id="acbbd-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="acbbd-157">Výzvy PowerShellu byste měli používat jenom v ilustrativních příkladech.</span><span class="sxs-lookup"><span data-stu-id="acbbd-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="acbbd-158">Ve většině příkladů by řetězec výzvy měl být „`PS>`“.</span><span class="sxs-lookup"><span data-stu-id="acbbd-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="acbbd-159">Tato výzva nezávisí na ukazatelích určitého operačního systému.</span><span class="sxs-lookup"><span data-stu-id="acbbd-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="acbbd-160">Výzvy by se **NEMĚLY** používat ve spustitelných příkladech.</span><span class="sxs-lookup"><span data-stu-id="acbbd-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="acbbd-161">Následující příklad ilustruje způsob změny výzvy při použití zprostředkovatele registru.</span><span class="sxs-lookup"><span data-stu-id="acbbd-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="acbbd-162">Nepoužívejte v příkladech aliasy</span><span class="sxs-lookup"><span data-stu-id="acbbd-162">Do not use aliases in examples</span></span>

<span data-ttu-id="acbbd-163">Vždy byste měli používat celý název všech rutin a parametrů, pokud výslovně nehovoříte o aliasu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="acbbd-164">V názvech rutin a parametrů je potřeba dodržovat správné psaní velkých a malých písmen podle jazyka Pascal, které je definované v kódu.</span><span class="sxs-lookup"><span data-stu-id="acbbd-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="acbbd-165">Používání parametrů v příkladech</span><span class="sxs-lookup"><span data-stu-id="acbbd-165">Using parameters in examples</span></span>

<span data-ttu-id="acbbd-166">Vyhýbejte se používání pozičních parametrů.</span><span class="sxs-lookup"><span data-stu-id="acbbd-166">Avoid using positional parameters.</span></span> <span data-ttu-id="acbbd-167">Obecně platí, že příklad by měl vždy obsahovat název parametru, a to i tehdy, když jde o poziční parametr.</span><span class="sxs-lookup"><span data-stu-id="acbbd-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="acbbd-168">Zmenší se tím pravděpodobnost, že příklad nebude srozumitelný.</span><span class="sxs-lookup"><span data-stu-id="acbbd-168">This reduces the chance of confusion in your examples.</span></span>
