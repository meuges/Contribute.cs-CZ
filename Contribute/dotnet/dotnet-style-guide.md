---
title: Šablona a stručná nápověda k článkům o .NET
description: V tomto článku najdete praktickou šablonu, kterou můžete použít k vytvoření nových článků pro úložiště dokumentace k .NET.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 15288ccb1831e994fd078f47788ad4c2f502775c
ms.sourcegitcommit: 92d06515af1d9d0e5abf632fc3b6425c487174d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/21/2020
ms.locfileid: "90837205"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>Metadata a šablona v Markdownu pro dokumentaci k .NET

Tato šablona pro dotnet/dokumentaci obsahuje příklady syntaxe jazyka Markdown a pokyny k nastavení metadat.

Při vytváření souboru Markdown zkopírujte přiloženou šablonu do nového souboru, vyplňte metadata podle návodu níže a nastavte nadpis H1 výše na název článku.

## <a name="metadata"></a>Metadata

Požadovaný blok metadat je v následujícím ukázkovém bloku metadat:

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Mezi dvojtečkou (:) a hodnotou prvku metadat **musí** být mezera.
- Dvojtečky v hodnotě (třeba v nadpisu) způsobí chybu analyzátoru metadat. V takovém případě dejte nadpis do dvojitých uvozovek (příklad: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title** (název): Zobrazí se ve výsledcích vyhledávačů. Nadpis nemusí být stejný jako nadpis v záhlaví H1 a nesmí být delší než 60 znaků.
- **description** (popis): Shrnuje obsah článku. Většinou se zobrazuje na stránce s výsledky hledání, ale nepoužívá se k řazení výsledků hledání. Měl by mít 115–145 znaků (včetně mezer).
- **author** (autor): Pole autora musí obsahovat **uživatelské jméno autora na GitHubu**.
- **ms.date**: Datum poslední významné aktualizace. U stávajících článků datum aktualizujte, pokud zkontrolujete a aktualizujete celý článek. U malých oprav, jako jsou opravy překlepů apod., nejde o aktualizaci.

Ke každému článku jsou připojená další metadata, ale většinu hodnot metadat obvykle používáme na úrovni složky zadané v souboru **docfx.json**.

## <a name="basic-markdown-gfm-and-special-characters"></a>Základy jazyka Markdown (GFM) a speciální znaky

Základní informace o jazyce Markdown, variantě GitHub Flavored Markdown (GFM) a rozšířeních specifických pro OPS najdete v článku [Referenční informace k jazyku Markdown](../markdown-reference.md).

Markdown používá k formátování zvláštní znaky, například \*, \` a \#. Pokud chcete některý z těchto znaků přidat do obsahu, máte na výběr dvě možnosti:

- Dejte před speciální znak zpětné lomítko jako „řídicí znak“ (například `\*` pro \*).
- Použijte pro znak [kód entity HTML](http://www.ascii.cl/htmlcodes.htm) (třeba `&#42;` pro &#42;).

## <a name="file-names"></a>Názvy souborů

Pro názvy souborů platí následující pravidla:

* Smí obsahovat jenom malá písmena, číslice a pomlčky.
* Nesmí obsahovat mezery ani interpunkční znaménka. K oddělení slov a čísel v názvu souboru používejte pomlčky.
* Používejte slovesa, která vyjadřují určitou činnost, třeba develop (vyvíjet), buy (koupit), build (sestavit) nebo troubleshoot (řešit potíže). Nepoužívejte slova s koncovkou -ing.
* Nepoužívejte krátká slova (nepoužívejte členy a spojky a, and, the, in, or atd.).
* Musí být ve formátu Markdown a mít příponu souboru .md.
* Názvy souborů musí být krátké, protože tvoří část adresy URL vašich článků.

## <a name="headings"></a>Nadpisy

Používejte velká písmena jako při psaní věty. První slovo v nadpisu musí začínat velkým písmenem.

## <a name="text-styling"></a>Styl textu

*Kurzíva*\
Použijte pro soubory, složky, cesty (dlouhé položky dejte na samostatný řádek) a nové výrazy.

**Tučné**\
Použijte pro prvky uživatelského rozhraní.

`Code`\
Použijte pro vložený kód, klíčová slova jazyka, názvy balíčků NuGet, příkazy příkazového řádku, názvy databázových tabulek a sloupců a pro adresy URL, které nemají fungovat jako odkaz, na který se dá kliknout.

## <a name="links"></a>Odkazy

Informace o ukotveních, interních odkazech, odkazech na jiné dokumenty, zahrnutém kódu a externích odkazech najdete v obecném článku o [odkazech](../how-to-write-links.md).

Tým pro dokumentaci k .NET používá následující konvence:

- Ve většině případů používáme relativní odkazy. V odkazech nedoporučujeme používat znak `~/`, protože relativní odkazy se překládají ve zdroji na GitHubu. Pokud ale odkazujeme na soubor v závislém úložišti, použijeme v cestě znak `~/`. Soubory v závislém úložišti jsou v GitHubu umístěné jinde, a proto se tyto odkazy nepřeloží správně s relativními odkazy bez ohledu na způsob jejich zápisu.
- Specifikace jazyka C# a specifikace jazyka Visual Basic zahrnete do dokumentace k .NET tak, že uvedete zdroj z jazykových úložišť. Zdroje v Markdownu jsou spravované v úložištích [csharplang](https://github.com/dotnet/csharplang) a [vblang](https://github.com/dotnet/vblang).

Odkazy na specifikaci musí mířit na zdrojové adresáře s touto specifikací. Pro C# je to **~/_csharplang/spec** a pro VB je to **~/_vblang/spec**, jak vidíte v následujícím příkladu:

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>Odkazy na rozhraní API

Kompilační systém má několik přípon, které umožňují vytvořit odkaz na rozhraní .NET API bez použití externích odkazů. Použijte jednu z následujících syntaxí:

1. Automatické propojení: `<xref:UID>` nebo `<xref:UID?displayProperty=nameWithType>`

   Parametr dotazu `displayProperty` vytvoří plně kvalifikovaný text odkazu. Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu.

2. Odkaz Markdownu: `[link text](xref:UID)`

   Tento způsob použijte, když chcete přizpůsobit zobrazený text odkazu.

Příklady:

- `<xref:System.String>` se zobrazí jako [String](https://docs.microsoft.com/dotnet/api/system.string).
- `<xref:System.String?displayProperty=nameWithType>` se zobrazí jako [System.String](https://docs.microsoft.com/dotnet/api/system.string).
- `[String class](xref:System.String)` se zobrazí jako [třída String](https://docs.microsoft.com/dotnet/api/system.string).

Další informace o použití tohoto zápisu najdete v části [Použití křížového odkazu](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).

Některé identifikátory uživatele (UID) obsahují speciální znaky \`, \# nebo \*. Hodnota UID pak musí být zakódovaná do HTML jako `%60`, `%23` nebo `%2A`. Někdy v tomto formátu uvidíte i závorky, není to ale povinné.

Příklady:

- System.Threading.Tasks.Task\`1 se změní na `System.Threading.Tasks.Task%601`.
- System.Exception.\#ctor se změní na `System.Exception.%23ctor`.
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) se změní na `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`.

Identifikátory UID typů, seznam přetížení členů nebo určitého přetíženého člena najdete na adrese `https://xref.docs.microsoft.com/autocomplete`. Řetězec dotazu `?text=*\<type-member-name>*` identifikuje typ nebo člena, jehož identifikátory UID chcete vidět. Třeba `https://xref.docs.microsoft.com/autocomplete?text=string.format` načte přetížení [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format). Nástroj vyhledá zadaný parametr dotazu `text` v libovolné části identifikátoru UID. Můžete třeba hledat jméno člena (ToString), část jména člena (ToStri), typ a jméno člena (Double.ToString) atd.

Pokud za UID přidáte \* (nebo `%2A`), představuje tento odkaz stránku přetížení, nikoli určité rozhraní API. Můžete to například použít, pokud chcete odkazovat na stránku [metody List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) obecným způsobem namísto konkrétního přetížení, jako je [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_). Znaky \* také můžete použít k odkazu na stránku člena, pokud není přetížený, abyste v identifikátoru UID nemuseli uvádět seznam parametrů.

Pokud chcete vytvořit odkaz na určité přetížení metody, musíte do všech parametrů metody zahrnout úplně určený název typu. Například \<xref:System.DateTime.ToString> odkazuje na metodu [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) bez parametrů, zatímco \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> odkazuje na metodu [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).

Pokud chcete vytvořit odkaz na obecný typ, třeba na [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), použijte znak \` (`%60`) a za něj uveďte počet parametrů obecného typu. Například `<xref:System.Nullable%601>` odkazuje na typ [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), zatímco `<xref:System.Func%602>` odkazuje na delegáta [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).

## <a name="code"></a>Kód

Nejlepší způsob, jak zahrnout kód, je použít fragmenty kódu z funkční ukázky. Vytvořte ukázku podle pokynů v článku o [příspěvcích pro .NET](dotnet-contribute.md#contribute-to-samples). Tím, že zahrnete fragmenty kódu z celých programů, zajistíte spustitelnost veškerého kódu v našem systému kontinuální integrace (CI). Pokud ale chcete předvést něco, co způsobuje chyby při kompilaci nebo spuštění, můžete použít vložené bloky kódu.

Informace o syntaxi Markdown pro zobrazení kódu v dokumentech najdete v tématu [Jak do dokumentů vkládat kód](../code-in-docs.md).

## <a name="images"></a>Obrázky

### <a name="static-image-or-animated-gif"></a>Statický obrázek nebo animovaný GIF

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Propojený obrázek

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Videa

V současnosti můžete ke vkládání videí služeb Channel 9 a YouTube použít následující syntaxi:

### <a name="channel-9"></a>Channel9

```markdown
> [!VIDEO <channel9_video_link>]
```

Pokud chcete získat správnou adresu URL videa, vyberte kartu **Vložit** pod snímkem videa a zkopírujte adresu URL z prvku `<iframe>`. Například:

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Pokud chcete získat správnou adresu URL videa, klikněte na něj pravým tlačítkem, vyberte **Kopírovat kód pro vložení** a zkopírujte adresu URL z prvku `<iframe>`.

```markdown
> [!VIDEO <youtube_video_link>]
```

Například:

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>docs.microsoft extensions

Další rozšíření dialektu GitHub Flavored Markdown najdete v dokumentaci na webu docs.microsoft.

### <a name="checked-lists"></a>Seznamy se zaškrtávacími políčky

Pro seznamy je k dispozici vlastní styl. Můžete zobrazit seznamy se zelenými zaškrtnutími.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Zobrazí se takto:

> [!div class="checklist"]
> * Vytvoření aplikace v .NET Core
> * Přidání odkazu do balíčku Microsoft.XmlSerializer.Generator
> * Úprava souboru MyApp.csproj a přidání závislostí
> * Přidání třídy a objektu XmlSerializer
> * Sestavení a spuštění aplikace

Příklad použití seznamů se zaškrtávacími políčky najdete v [dokumentaci k .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).

### <a name="buttons"></a>Tlačítka

Odkazy na tlačítka:

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Zobrazí se takto:

> [!div class="button"]
> [odkazy na tlačítka](dotnet-contribute.md)

Příklad použití tlačítek najdete v [dokumentaci k sadě Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).

### <a name="step-by-steps"></a>Postupy

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

Příklad použití postupů najdete v [příručce k jazyku C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).
