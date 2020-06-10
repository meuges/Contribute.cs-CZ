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
# <a name="how-to-include-code-in-docs"></a>Jak do dokumentů vkládat kód

Kód se dá do článku, který se má publikovat na docs.microsoft.com, přidat několika způsoby:

* Jednotlivé elementy (slova) v rámci řádku.

  Tady je příklad stylu kódu: `code`.

  Použijte formát kódu při odkazování na pojmenované parametry a proměnné v okolním bloku kódu v textu. Formát kódu jde také použít pro vlastnosti, metody, třídy a klíčová slova jazyka. Další informace najdete v tématu [Elementy kódu](#code-elements) dále v tomto článku.

* Bloky kódu v souboru Markdown článku.

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Používejte vložené bloky kódu, pokud je nepraktické zobrazit kód pomocí odkazu na soubor kódu. Další informace najdete v tématu [Bloky kódu](#inline-code-blocks) dále v tomto článku.

* Bloky kódu pomocí odkazu na soubor kódu v místním úložišti.

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Další informace najdete v tématu [Odkazy na fragmenty v úložišti](#in-repo-snippet-references) dále v tomto článku.

* Bloky kódu pomocí odkazu na soubor kódu v jiném úložišti.

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Další informace najdete v tématu [Odkazy na fragmenty mimo úložiště](#out-of-repo-snippet-references) dále v tomto článku.
  
* Bloky kódu, které umožní uživateli spustit kód v prohlížeči.

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Další informace najdete v tématu [Interaktivní fragmenty kódu](#interactive-code-snippets) dále v tomto článku.

Mimo vysvětlení k souboru Markdown pro každý z těchto způsobů, jak přidat kód, článek obsahuje některé [obecné pokyny pro všechny bloky kódu](#code-blocks).

## <a name="code-elements"></a>Elementy kódu

Element kódu je klíčové slovo programovacího jazyka, název třídy, název vlastnosti a tak dále. Není vždy zřejmé, co se považuje za kód. Například názvy balíčků NuGet by se měly považovat za kód. Pokud máte pochybnosti, podívejte se do článku [Pokyny k formátování textu](text-formatting-guidelines.md).

### <a name="inline-code-style"></a>Styl vloženého kódu

Pokud chcete zahrnout element kódu do textu článku, dejte ho do zpětných apostrofů (\`), kterými označíte styl kódu.
Styl vloženého kódu by neměl používat formát s trojnásobným zpětným apostrofem.

|Markdown |Vykreslení |
|---------|---------|
|Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem \`Id\` nebo \`ClassnameID\` jako primární klíč.|Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem `Id` nebo `ClassnameID` jako primární klíč.|

Když se článek lokalizuje (přeloží do jiných jazyků), text ve stylu kódu zůstane nepřeložený. Pokud chcete zabránit lokalizaci bez použití stylu kódu, najdete informace v části [Nelokalizované řetězce](markdown-reference.md#non-localized-strings).

### <a name="bold-style"></a>Tučný styl

Některé starší návody určují tučný styl za vložený kód. Tučné písmo se dá použít, pokud je styl kódu tak vlezlý, že je to na úkor čitelnosti. Pokud například máte tabulku Markdown s převážně kódovými elementy, může být vinou všudypřítomného stylu kódu dost nepřehledná. Pokud se rozhodnete použít tučný styl, použijte [syntaxi nelokalizovaných řetězců](markdown-reference.md#non-localized-strings), abyste zajistili, že kód není lokalizovaný.

### <a name="links"></a>Odkazy

Odkaz na referenční dokumentaci může být v některých kontextech užitečnější než formát kódu. Jestliže použijete odkaz, nepoužívejte pro text odkazu formát kódu. Pokud se u odkazu nastaví styl kódu, může to zakrýt skutečnost, že text je odkaz.

Když použijete odkaz a později ve stejném kontextu budete na stejný element odkazovat, udělejte následující instance ve formátu kódu místo odkazů.

### <a name="placeholders"></a>Zástupné symboly

Pokud chcete, aby uživatel nahradil oddíl zobrazeného kódu vlastními hodnotami, použijte zástupný text vyznačený lomenými závorkami nebo složenými závorkami. Například: `az group delete -n <ResourceGroupName>`. Vysvětlete, že při nahrazování skutečnými hodnotami se musí závorky odebrat.

## <a name="code-blocks"></a>Bloky kódu

Syntaxe pro zahrnutí kódu v dokumentu závisí na tom, kde se nachází kód:

* [V souboru Markdown článku](#inline-code-blocks)
* [V souboru kódu ve stejném úložišti](#in-repo-snippet-references)
* [V souboru kódu v jiném úložišti](#out-of-repo-snippet-references)

Pokyny, které platí pro všechny tři typy bloků kódu, jsou následující:

* [Automatizujte ověření kódu.](#code-validation)
* [Zvýrazněte klíčové řádky kódu.](#highlighting)
* [Vyhněte se vodorovným posuvníkům.](#horizontal-scroll-bars)

### <a name="screenshots"></a>Snímky obrazovky

Všechny metody uvedené v předchozí části mají za následek použitelné bloky kódu:

* Můžete z nich kopírovat a vkládat.
* Jsou indexovány vyhledávacími weby.
* Jsou přístupné pro čtečky obrazovky.

To je jen několik důvodů z mnoha, proč se snímky obrazovky integrovaného vývojového prostředí (IDE) nedoporučují jako metoda zahrnutí kódu do článku. Snímky obrazovky IDE použijte pro kód pouze v případě, že ukazujete něco o samotném IDE, například IntelliSense. Nepoužívejte snímky obrazovky pouze k zobrazení barev a zvýraznění.

### <a name="code-validation"></a>Ověření kódu

Některá úložiště mají implementované procesy, které automaticky zkompilují celý vzorový kód a zkontrolují, jestli neobsahuje chyby. Toto dělá úložiště .NET. Další informace najdete v článku [Příspěvky](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) v úložišti .NET.

Pokud zahrnujete bloky kódu z jiného úložiště, spolupracujte s vlastníky na strategii údržby pro kód tak, aby se váš zahrnutý kód nepokazil nebo nezastaral, když se pak budou vydávat nové verze knihoven, které kód používá.

### <a name="highlighting"></a>Zvýrazňování

Fragmenty obvykle obsahují více kódu, než je nezbytné pro získání kontextu. Budou se líp číst, když ve fragmentu zvýrazníte klíčové řádky, jako v následujícím příkladu:

![Příklad zobrazující zvýrazněný kód](media/code-in-docs/highlighted-code.png)

Kód nemůžete zvýraznit, když ho zahrnete do souboru Markdown článku. Funguje to jenom u fragmentů kódu, které jsou zahrnuté odkazem na soubor kódu.

### <a name="horizontal-scroll-bars"></a>Vodorovné posuvníky

Rozdělte dlouhé řádky, aby se nemusely používat vodorovné posuvníky. S posuvníky se bloky kódu špatně čtou. Jsou obzvláště problematické u delších bloků kódu, kdy může být nemožné zobrazit současně posuvník a řádek, který chcete číst.

Dobrým postupem pro minimalizaci vodorovných posuvníků v blocích kódu je rozdělit řádky kódu delší než 85 znaků. Mějte ale na paměti, že přítomnost nebo absence posuvníku není jediným kritériem čitelnosti. Pokud konec řádku (zalomení) před 85 znakem škodí čitelností nebo pohodlí při kopírování a vkládání, klidně nechejte řádek delší.

## <a name="inline-code-blocks"></a>Vložené bloky kódu

Používejte vložené bloky kódu, pouze pokud je nepraktické zobrazit kód pomocí odkazu na soubor kódu. Vložený kód se obecně obtížněji testuje a udržuje v aktuálním stavu v porovnání se souborem kódu, který je součástí celého projektu.  A ve vloženém kódu může ještě dojít k vynechání kontextu, který by vývojáři mohl pomoct s pochopením a používáním kódu. Tyto záležitosti platí hlavně pro programovací jazyky. Vložené bloky kódu se dají také použít pro výstupy a vstupy (například JSON), dotazovací jazyky (například SQL) a skriptovací jazyky (například PowerShell).
  
Existují dva způsoby označení oddílu textu v souboru článku jako blok kódu: jeho *uzavřením* do trojitých zpětných apostrofů (\`\`\`) nebo jeho odsazením. Upřednostňuje se uzavření, protože to umožňuje určit jazyk. Vyhněte se použití odsazení, protože se člověk velmi snadno splete a jiný pisatel pak nemusí chápat váš záměr, když bude potřebovat váš článek upravit.

Indikátory jazyka jsou umístěné hned za levými trojitými zpětnými apostrofy, jako v následujícím příkladu:

Markdown:

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

Vykreslení:

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Informace o hodnotách, které můžete použít jako indikátory jazyka, najdete v článku [Názvy jazyků a aliasy](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

Pokud použijete slovo jazyka nebo prostředí po trojnásobném zpětném apostrofu (\`\`\`), které není podporované, zobrazí se toto slovo v záhlaví oddílu kódu na vykreslené stránce. Pokud je to možné, použijte ve vložených blocích kódu indikátor jazyka nebo prostředí.

> [!NOTE]
> Jestliže zkopírujete a vložíte kód z dokumentu aplikace Word, je nutné, aby neobsahoval žádné „oblé uvozovky“, které v kódu nejsou platné (například `“` a `’`). Pokud tam jsou, změňte je zpět na normální uvozovky (`'` a `"`). Nebo to můžete nechat na Balíčku pro vytváření obsahu na webu Docs a [funkci pro nahrazení inteligentních uvozovek](docs-authoring/smart-quote-replacement.md).

## <a name="in-repo-snippet-references"></a>Odkazy na fragmenty v úložišti

Preferovaný způsob, jak zahrnout fragmenty kódu pro programovací jazyky do dokumentů, je pomocí odkazu na soubor kódu. Tato metoda vám umožňuje zvýraznit řádky kódu a zpřístupňuje širší kontext fragmentu na GitHubu, aby ho vývojáři mohli použít. Kód můžete zahrnout pomocí formátu trojí dvojtečky (:\:\:) buď ručně, nebo v nástroji Visual Studio Code pomocí [Balíčku pro vytváření obsahu na webu docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. V editoru Visual Studio Code stiskněte <kbd>Alt+M</kbd> nebo <kbd>Option+M</kbd> a vyberte Snippet (Fragment).
2. Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti). Pokud chcete vyhledávat místně, vyberte Full Search (Úplné vyhledávání).
3. Zadejte hledaný termín pro vyhledání souboru. Jakmile soubor najdete, vyberte ho.
4. Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu. Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).
5. Podle výběru z kroku 4 zadejte v případě potřeby hodnotu.

Zobrazení celého souboru kódu:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Zobrazení části souboru kódu zadáním čísel řádků:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Zobrazení části souboru kódu zadáním názvu fragmentu:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Tyto příklady jsou vysvětlené v následujících oddílech:

* [Použití relativní cesty k souboru kódu](#path-to-code-file)
* [Zahrnutí jenom vybraných čísel řádků](#selected-line-numbers)
* [Odkaz na pojmenovaný fragment](#named-snippet)
* [Zvýraznění vybraných řádků](#highlighting-selected-lines)

Další informace najdete v tématu [Přehled syntaxe fragmentů](#snippet-syntax-reference) dále v tomto článku.

### <a name="path-to-code-file"></a>Cesta k souboru kódu

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Příklad je z úložiště dokumentů ASP.NET, soubor článku [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). Na soubor kódu odkazuje relativní cesta k [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) ve stejném úložišti.

### <a name="selected-line-numbers"></a>Vybraná čísla řádků

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Tento příklad zobrazí jenom řádky 2 až 24 a 26 ze souboru kódu *StudentController.cs*.

Dejte raději přednost pojmenovaným fragmentům před pevnými čísly řádků, jak je vysvětleno v další části.

### <a name="named-snippet"></a>Pojmenovaný fragment

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Pro název používejte jenom písmena a podtržítka.

V příkladu je zobrazený oddíl `snippet_Create` souboru kódu. Soubor kódu pro tento příklad obsahuje značky fragmentu v komentářích v kódu C#:

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Vždy, když je to možné, odkazujte na pojmenovanou část a nezadávejte čísla řádků. S odkazy na čísla řádků je třeba zacházet opatrně, protože soubory kódu se nevyhnutelně mění tak, že dochází ke změnám čísel řádků.
Takové změny vám lehce uniknou. Ve vašem článku se nakonec začnou zobrazovat chybné řádky a vy nebudete mít potuchy, že se něco změnilo.

### <a name="highlighting-selected-lines"></a>Zvýraznění vybraných řádků

Příklad:

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

V příkladu jsou zvýrazněné řádky 2 a 5, počítáno od začátku zobrazeného fragmentu. Čísla zvýrazněných řádků se nepočítají od začátku souboru kódu. Jinými slovy jsou zvýrazněné řádky 3 a 6 ze souboru kódu.

## <a name="out-of-repo-snippet-references"></a>Odkazy na fragmenty mimo úložiště

Pokud se soubor kódu, na který chcete odkazovat, nachází v jiném úložišti, nastavte úložiště kódu jako *závislé úložiště*. Až tak učiníte, zadejte pro něj název. Tento název potom pro účely odkazů na kód funguje stejně jako název složky.

Úložiště dokumentů je například *Azure/azure-docs* a úložiště kódu je *Azure/azure-functions-durable-extension*.

Do kořenové složky *azure-docs* přidejte do souboru *.openpublishing.publish.config.json* následující oddíl:

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

Teď když budete odkazovat na *samples-durable-functions*, jako by šlo o složku v *azure-docs*, budete ve skutečnosti odkazovat na kořenovou složku v úložišti *azure-functions-durable-extension*.

Kód můžete zahrnout pomocí formátu trojí dvojtečky (:\:\:) buď ručně, nebo v nástroji Visual Studio Code pomocí [Balíčku pro vytváření obsahu na webu docs.microsoft.com](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. V editoru Visual Studio Code stiskněte <kbd>Alt+M</kbd> nebo <kbd>Option+M</kbd> a vyberte Snippet (Fragment).
2. Po výběru možnosti Snippet (Fragment) se zobrazí možnosti Full Search (Úplné vyhledávání), Scoped Search (Vyhledávání v oboru) a Cross-Repository Reference (Odkaz mezi úložišti). Pokud chcete hledat v jiném úložišti, vyberte Cross-Repository Reference (Odkaz mezi úložišti).
3. Dostanete možnost vybrat úložiště, která jsou v *.openpublishing.publish.config.json*. Vyberte úložiště.
4. Zadejte hledaný termín pro vyhledání souboru. Jakmile soubor najdete, vyberte ho.
5. Dále vyberte možnost, jež určuje, které řádky kódu by se měly zahrnout do fragmentu. Možnosti jsou: **ID**, **Range** (Rozsah) a **None** (Žádný).
6. Podle výběru z 5. kroku zadejte hodnotu.

Váš odkaz na fragment bude vypadat nějak takto:

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

V úložišti *azure-functions-durable-extension* je tento soubor kódu ve složce *samples/csx/shared*. Jak jsme uvedli [dříve](#highlighting-selected-lines), čísla řádků pro zvýraznění jsou relativní vzhledem k začátku fragmentu místo k začátku souboru.

> [!NOTE]
> Název, který přiřadíte závislému úložišti, je relativní vzhledem ke kořenu hlavního úložiště, ale znak tilda (~) odkazuje na kořen sady dokumentace. Kořen sady dokumentace je určený hodnotou `build_source_folder` v souboru *.openpublishing.publish.config.json*. Cesta k fragmentu kódu v předchozím příkladu funguje v úložišti azure-docs, protože `build_source_folder` odkazuje na kořen úložiště (`.`). Pokud hodnota `build_source_folder` je `articles`, bude cesta začínat `~/../samples-durable-functions` místo `~/samples-durable-functions`.

## <a name="interactive-code-snippets"></a>Interaktivní fragmenty kódu

### <a name="inline-interactive-code-blocks"></a>Vložené interaktivní bloky kódu

U následujících jazyků je možné fragmenty kódu změnit na spustitelné v okně prohlížeče:

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Když je povolený interaktivní režim, mají rámečky s vykresleným kódem tlačítka **Vyzkoušet** nebo **Spustit**. Například:

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

se vykreslí takto:

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Pokud chcete tuto funkci zapnout u konkrétního bloku kódu, použijte speciální identifikátor jazyka. Dostupné jsou následující možnosti:

* `azurepowershell-interactive` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.
* `azurecli-interactive` – povolí Azure Cloud Shell.
* `csharp-interactive` – povolí C# REPL.

Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.

### <a name="code-snippets-included-by-reference"></a>Fragmenty kódu zahrnuté pomocí odkazu

Interaktivní režim můžete povolit pro fragmenty kódu, které jsou zahrnuté odkazem. Tady jsou příklady:

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Pokud chcete tuto funkci zapnout pro konkrétní blok kódu, použijte atribut `interactive`. Dostupné hodnoty atributu jsou:

* `cloudshell-powershell` – povolí Azure PowerShell Cloud Shell, jako v předchozím příkladu.
* `cloudshell-bash` – povolí Azure Cloud Shell.
* `try-dotnet` – povolí Try .NET.
* `try-dotnet-class` – povolí Try .NET s generováním tříd.
* `try-dotnet-method` – povolí Try .NET s generováním metod.

Pro prostředí Azure Cloud Shell a PowerShell Cloud Shell můžou uživatelé spouštět příkazy jenom se svým vlastním účtem Azure.

## <a name="snippet-syntax-reference"></a>Přehled syntaxe fragmentů

Syntaxe:

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Tato syntaxe je blokové rozšíření Markdownu. Musíte ji použít na samostatném řádku.

* `<language>` (*volitelné*)
  * Jazyk fragmentu kódu. Další informace najdete v části [Podporované jazyky](#supported-languages) dále v tomto článku.

* `<path>` (*povinné*)
  * Relativní cesta v systému souborů označující soubor fragmentu kódu, na který se má odkazovat

* `<attribute>` a `<attribute-value>` (*volitelné*)

  Společně se používají pro zadání, jak se má kód ze souboru načítat a jak se má zobrazovat:

  * `range`: `1,3-5` Rozsah řádků. Tento příklad zahrnuje řádky 1, 3, 4 a 5.
  * `id`: `snippet_Create` ID fragmentu, který se má vložit ze souboru kódu. Tato hodnota nemůže existovat současně s rozsahem.
  * `highlight`: `2-4,6` Rozsah a/nebo čísla řádků, které se mají zvýraznit ve vygenerovaném fragmentu kódu. Číslování je relativní vzhledem k zobrazeným řádkům (jak je určeno rozsahem nebo ID), ne k souboru.
  * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Hodnota řetězce určuje, jaké druhy interaktivity jsou povolené.
  * Podrobnosti o reprezentaci názvů značek ve zdrojových souborech fragmentu kódu v jednotlivých jazycích najdete v [pokynech pro DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

## <a name="supported-languages"></a>Podporované jazyky

[Balíček pro vytváření obsahu na webu Docs](how-to-write-docs-auth-pack.md) obsahuje funkci pro dokončování příkazů a ověřování dostupných identifikátorů jazyků pro ohraničené bloky kódu.

### <a name="fenced-code-blocks"></a>Ohraničené bloky kódu

| Name                           | Platné aliasy                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| .NET Core CLI                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Přístupové protokoly                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| Assembler ARM                  | `armasm`, `arm`                                                                |
| Assembler AVR                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure PowerShell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Cache Object Script            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| Soubor zóny DNS                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (strom zařízení)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lispu                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile (Soubor pravidel)                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| Skriptovací jazyk mIRC        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| Formát MOF (Managed Object Format)          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Nešifrovaný text bez zvýraznění         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Vlastnosti                     | `properties`                                                                   |
| Vyrovnávací paměti protokolu               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Výsledky profileru Pythonu        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| Soubory specifikace RPM                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Prostředí                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Structured Text                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Skript Vim                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| Sestavení x86                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> V Balíčku pro vytváření obsahu na webu Docs používá [funkce Dokončování vývojářských jazyků](docs-authoring/dev-lang-completion.md) první platný alias, pokud je k dispozici více aliasů.

## <a name="next-steps"></a>Další kroky

Informace o formátování textu pro jiné typy obsahu než kód najdete v článku [Pokyny pro formátování textu](text-formatting-guidelines.md).
