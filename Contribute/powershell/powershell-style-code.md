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
# <a name="formatting-code-samples"></a>Formátování vzorového kódu

Ve stávající dokumentaci se postupně používalo více stylů, protože se pravidla formátování několikrát měnila. V dokumentaci se snažíme zavést pro bloky kódu a výstupy PowerShellu jednotný styl.

Markdown podporuje dva různé styly kódu:

- Rozsahy kódu (vložené) – označené jedním znakem apostrofu (`` ` ``). Používá se uvnitř odstavce, nikoli jako samostatný blok. Nejčastěji se používá k ohraničení názvů rutin. Další informace viz [Syntaktické prvky formátování příkazů](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Bloky kódu – více řádkový blok ohraničený třemi zpětnými apostrofy (`` ``` ``).

## <a name="using-code-blocks"></a>Použití bloků kódu

V Markdownu můžete blok kódu označit odsazením. Tento způsob ale může být problematický, a proto byste ho neměli používat. Všechny bloky kódu musí být ohraničené tzv. kódovým plotem. Kódový plot je blok kódu, který je ohraničený třemi zpětnými apostrofy (`` ``` ``). Značky kódového plotu musí být na samostatném řádku před a za vzorovým kódem. Značka na začátku bloku kódu může mít libovolný jazykový popisek. V systému OPS (Open Publishing System) Microsoftu se jazykový popisek používá k podpoře funkce zvýraznění syntaxe.

Systém OPS také přidá **kopírovací** tlačítko, které zkopíruje obsah bloku kódu do schránky. Tlačítkem můžete ukázku kódu rychle vložit do skriptu, abyste ji mohli otestovat. Všechny ukázky kódu v naší dokumentaci ale nejdou tímto způsobem spouštět. Některé bloky kódu můžou představovat jednoduchou ukázku principu PowerShellu nebo může jít o obecný příklad syntaxe.

V naší dokumentaci se používají dva typy bloků kódu:

1. Názorné příklady
2. Spustitelné příklady

## <a name="formatting-illustrative-examples"></a>Formátování názorných příkladů

Ilustrativní příklady se používají k vysvětlení principů PowerShellu. Nejsou určené ke zkopírování do schránky ani ke spuštění. Nejčastěji se používají jako jednoduché příklady, které se dají jednoduše napsat.
Používají se také v příkladech syntaxe k ilustrování syntaxe příkazu.

V ilustrativních příkladech se k označení začátku a konce bloku kódu používá tzv. holý kódový plot. Blok kódu může obsahovat i ukázkový výstup vysvětlovaného příkazu.

### <a name="syntax-block"></a>Syntaktický blok

Tento příklad ilustruje všechny možné parametry rutiny `Get-Command`.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

Tento příklad obecným způsobem popisuje výraz `for`:

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Jednoduchý ilustrativní příklad

Tady je příklad, který ilustruje srovnávací operátory PowerShellu:

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

Všimněte si zjednodušeného příkazového řádku PowerShellu a zobrazeného výsledného výstupu. V tomto případě nechceme, aby čtenář tento příklad kopíroval ani spouštěl.

## <a name="formatting-executable-examples"></a>Formátování spustitelných příkladů

Ve složitějších případech nebo v příkladech, které má smysl kopírovat a spouštět, byste měli použít následující označení stylu bloku:

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

Výstup zobrazený příkazy PowerShellu by měl být ohraničen jako blok kódu **Output** (Výstup), aby se zabránilo zvýraznění syntaxe. Například:

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

Označení kódu **Output** nepředstavuje oficiální jazyk podporovaný systémem zvýrazňování syntaxe.
Přesto je toto označení užitečné, protože OPS přidá označení „Output“ do pole kódu na webové stránce.
V poli kódu „Output“ nebude zvýrazněna syntaxe.

## <a name="coding-style-rules"></a>Pravidla stylu psaní kódu

### <a name="avoid-line-continuation-in-code-samples"></a>V ukázkách kódu se vyhýbejte pokračování řádku

V ukázkách kódu PowerShellu se vyhýbejte požití znaků (`` ` ``), které označují pokračování řádku. Tyto znaky jsou špatně viditelné a můžou způsobovat problémy, pokud jsou na konci řádku nadbytečné mezery.

- K omezení délky řádků v rutinách, které mají hodně parametrů, použijte seskupování PowerShellu.
- Použijte možnosti přirozeného dělení řádků v PowerShellu, jako je třeba znak svislé čáry (`|`) nebo počáteční, oblé či hranaté závorky.

### <a name="avoid-using-powershell-prompts-in-examples"></a>V příkladech raději nepoužívejte výzvy PowerShellu

Nedoporučuje se používat řetězec, který označuje výzvu. Použijte ho jenom ve scénářích, které ilustrují použití příkazového řádku. Výzvy jsou nutné v příkladech, které ilustrují příkazy měnící výzvu, nebo když má zobrazená cesta určitý význam v popisovaném scénáři.

- Výzvy PowerShellu byste měli používat jenom v ilustrativních příkladech. Ve většině příkladů by řetězec výzvy měl být „`PS>`“. Tato výzva nezávisí na ukazatelích určitého operačního systému.
- Výzvy by se **NEMĚLY** používat ve spustitelných příkladech.

Následující příklad ilustruje způsob změny výzvy při použití zprostředkovatele registru.

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

### <a name="do-not-use-aliases-in-examples"></a>Nepoužívejte v příkladech aliasy

Vždy byste měli používat celý název všech rutin a parametrů, pokud výslovně nehovoříte o aliasu. V názvech rutin a parametrů je potřeba dodržovat správné psaní velkých a malých písmen podle jazyka Pascal, které je definované v kódu.

### <a name="using-parameters-in-examples"></a>Používání parametrů v příkladech

Vyhýbejte se používání pozičních parametrů. Obecně platí, že příklad by měl vždy obsahovat název parametru, a to i tehdy, když jde o poziční parametr. Zmenší se tím pravděpodobnost, že příklad nebude srozumitelný.
