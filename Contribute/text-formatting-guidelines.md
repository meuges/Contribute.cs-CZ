---
title: Pravidla formátování textu
description: Podívejte se, kdy použít tučné písmo, kurzívu, kód a další styly textu v článcích publikovaných na webu docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336502"
---
# <a name="text-formatting-guidelines"></a>Pravidla formátování textu

Konzistentní a správné použití tučného písma, kurzívy a stylu kódu u textových prvků zlepšuje čitelnost a pomáhá vyhnout se nedorozuměním.

## <a name="bold"></a>Tučné

Používá se pro prvky uživatelského rozhraní, jako jsou například možnosti v nabídkách, názvy dialogových oken a názvy vstupních polí.

### <a name="examples"></a>Příklady

* **Správně**: V **Průzkumníku řešení** klikněte pravým tlačítkem myši na uzel projektu a vyberte **Přidat > Nová položka**.
* **Špatně**: V Průzkumníku řešení klikněte pravým tlačítkem myši na uzel projektu a vyberte Přidat > Nová položka.
* **Špatně**: V *Průzkumníku řešení* klikněte pravým tlačítkem myši na uzel projektu a vyberte *Přidat > Nová položka*.

## <a name="italics"></a>Kurzíva

Kurzíva se používá pro:

* Představení nových termínů společně s definicí nebo vysvětlením
* Názvy souborů, názvy složek, cesty
* Vstup uživatele

### <a name="examples"></a>Příklady

* **Správně**: Ve službě App Service běží aplikace v *plánu služby App Service*. Plán služby App Service definuje sadu výpočetních prostředků, ve které má běžet webová aplikace.
* **Špatně**: Ve službě App Service běží aplikace v „plánu služby App Service“. Plán služby App Service definuje sadu výpočetních prostředků, ve které má běžet webová aplikace.
* **Správně**: Nahraďte kód v souboru *HttpTriggerCSharp.cs* následujícím kódem.
* **Špatně**: Nahraďte kód v `HttpTriggerCSharp.cs` následujícím kódem.
* **Správně**: Jako **Název** zadejte *ContosoUniversity* a potom vyberte **Přidat**.
* **Špatně**: Jako **Název** zadejte „ContosoUniversity“ a potom vyberte **Přidat**.

## <a name="code-style"></a>Styl kódu

Styl kódu se používá pro:

* Prvky kódu, jako jsou názvy metod, názvy vlastností a klíčová slova jazyka
* SQL příkazy
* Názvy balíčků NuGet
* Příkazy příkazového řádku
* Názvy tabulek a sloupců databáze
* Názvy prostředků, které se nemají lokalizovat (například názvy virtuálních počítačů)
* Adresy URL, na které nemá být možné kliknout

**Proč?** Ve starších pokynech ke stylu je u mnoha těchto textových prvků uvedené, že se mají psát tučně. Většina dokumentace Microsoftu se ale lokalizuje (překládá do jiných jazyků) a styl kódu napovídá překladateli, že má danou část textu nechat nepřeloženou.

Styl kódu může být *přiřazený* (uzavřeno do \`) nebo v podobě *ohraničených* bloků kódu (uzavřeno do \`\`\`) na více řádcích. Delší fragmenty kódu a cesty umístěte do ohraničených bloků kódu.

### <a name="examples-using-inline-styles"></a>Příklady použití přiřazených stylů

* **Správně**: Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem `Id` nebo `ClassnameID` jako primární klíč.
* **Špatně**: Ve výchozím nastavení interpretuje Entity Framework vlastnost s názvem *Id* nebo *ClassnameID* jako primární klíč.
* **Správně**: Balíček `Microsoft.EntityFrameworkCore` podporuje runtime pro jádro EF Core.
* **Špatně**: Balíček *Microsoft.EntityFrameworkCore* podporuje runtime jádra EF Core.

### <a name="examples-of-fenced-code-blocks"></a>Příklady ohraničených bloků kódu

* **Správně**: Do databáze se neposílají žádné příkazy na základě výrazů, které mění pouze `IQueryable`, jako například následující kód:

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **Špatně**: Do databáze se neposílají žádné příkazy na základě výrazů, které mění pouze **IQueryable**, jako je například **var students = context.Students.Where(s => s.LastName == "Davolio")** .

* **Správně**: Pokud chcete například spustit skript `Get-ServiceLog.ps1` v adresáři `C:\Scripts`, zadejte:

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **Špatně**: Pokud chcete například spustit skript **Get-ServiceLog.ps1** v adresáři **C:\Scripts**, zadejte: „C:\Scripts\Get-ServiceLog.ps1.“

* **Všechny**ohraničené bloky kódu musí mít schválenou značku jazyka. Seznam podporovaných značek najdete v tématu [Jak do dokumentů vkládat kód](./code-in-docs.md#supported-languages).

## <a name="headings-and-link-text"></a>Záhlaví a text odkazu

Nepoužívejte přiřazený styl, jako je kurzíva, tučné písmo nebo kód, u nadpisů a textu hypertextových odkazů.

**Proč?**

Lidé očekávají, že textové prvky, jako jsou odkazy, na které se dá kliknout, budou mít podobu standardního hypertextového odkazu. Pokud se například nastaví u odkazu styl kódu, může to zakrýt skutečnost, že text je odkaz. Nadpisy mají svoje vlastní styly a kombinace s jinými styly nevypadají v nadpisech dobře.

### <a name="examples"></a>Příklady

* **Správně**: Soubor *function.json* generuje balíček NuGet [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).
* **Špatně**: Soubor *function.json* generuje balíček NuGet Microsoft.NET.Sdk.Functions [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).

* **Správně**:

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **Špatně**:

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>Klávesy a klávesové zkratky

Při odkazování na klávesy nebo jejich kombinace se řiďte těmito zvyklostmi:

* První písmeno v názvu klávesy pište velké.
* Nepoužívejte přiřazený styl, jako je kurzíva, tučné písmo nebo kód.
* Klávesy, které se mají stisknout současně, spojujte pomocí znaku „+“.

### <a name="examples"></a>Příklady

* **Správně**: Vyberte Alt+Ctrl+S.
* **Špatně**: Stiskněte **ALT+CTRL+S**.
* **Špatně**: Zmáčkněte `ALT+CTRL+S`.

Další informace najdete v článku věnovaném [popisování interakce s uživatelským rozhraním](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472).

## <a name="exceptions"></a>Výjimky

Pokyny týkající se stylu nejsou pevně daná pravidla. Tam, kde by docházelo k horší čitelnosti, zvolte jiná řešení. Pokud například použijete tabulku HTML u převážně kódových prvků, může to být díky všudypřítomnému stylu kódu poněkud nepřehledné. V tomto kontextu můžete použít tučné písmo.

V případě, že zvolíte jiný styl tam, kde se běžně používá kód, je potřeba zajistit, že v lokalizovaných verzích článku nebudou potíže s přeložením textu. Kód je jediný styl, který automaticky brání překládání. Pokyny pro scénáře, v nichž se má zabránit lokalizaci bez použití stylu kódu, najdete v části [Nelokalizované řetězce](markdown-reference.md#non-localized-strings).
