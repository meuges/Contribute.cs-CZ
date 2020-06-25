---
title: Používání odkazů v dokumentaci
description: Tento článek obsahuje pokyny k vytváření odkazů na obsah na webu docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: 94ba4cefd9aff70b38502aa397a3761127c8089f
ms.sourcegitcommit: 9852045bac75fd5d90c0ffc88d2a17dd45ba015f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/19/2020
ms.locfileid: "85107114"
---
# <a name="use-links-in-documentation"></a>Použití odkazů v dokumentaci

Tento článek popisuje způsob používání hypertextových odkazů ze stránek hostovaných na webu docs.microsoft.com. Odkazy se snadno přidávají do markdownu pomocí několika různých konvencí. Odkazy směrují uživatele na obsah na stejné stránce, na jiné sousední stránky nebo na externí weby a adresy URL.

Back-end webu docs.microsoft.com používá platformu OPS (Open Publishing Services), která podporuje markdown kompatibilní s verzí [CommonMark][] parsovaný prostřednictvím parsovacího modulu [Markdig][]. Tato varianta markdownu je z větší části kompatibilní s verzí [GFM (GitHub Flavored Markdown)][GFM], protože většina dokumentů je uložená v GitHubu, aby bylo možné je upravovat. Další funkce se přidávají prostřednictvím rozšíření Markdownu.

> [!IMPORTANT]
> Všechny odkazy musí být zabezpečené (`https` versus `http`), když to cíl podporuje (což by měla drtivá většina).

## <a name="link-text"></a>Text odkazu

Slova, která použijete v textu odkazu, by měla být popisná. Jinými slovy by mělo jít o normální slova nebo název stránky, na kterou odkazujete.

> [!IMPORTANT]
> Nepoužívejte „klikněte sem“. Je to špatné pro optimalizaci vyhledávacího webu a adekvátně to nepopisuje cílovou stránku.

**Správně:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**Nesprávně:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Odkazy z jednoho článku na druhý

Systém publikování podporuje dva typy hypertextových odkazů: **adresy URL** a **odkazy na soubory**.

Odkaz URL může být cesta URL relativní ke kořenu webu docs.microsoft.com nebo absolutní adresa URL, která obsahuje úplnou syntaxi adresy URL (například `https://github.com/MicrosoftDocs/PowerShell-Docs`).

- Použijte odkazy URL při odkazování na obsah mimo aktuální sadu dokumentace (_docset_) nebo mezi automaticky generovanými referenčními a koncepčními články v rámci sady dokumentace.
- Nejjednodušší způsob, jak vytvořit relativní odkaz, je zkopírovat adresu URL z prohlížeče a pak z hodnoty, kterou vložíte do markdownu, odebrat `https://docs.microsoft.com/en-us`.
   - Nedávejte do adres URL národní prostředí pro vlastnosti Microsoftu (z adresy URL odeberte například „/en-US“).

Odkaz na soubor se používá k propojení mezi jedním článkem a jiným v rámci sady dokumentace.

- Všechny cesty k souborům používají znaky lomítka (`/`) místo znaků zpětného lomítka.
- Článek odkazuje na jiný článek ve stejném adresáři:

  `[link text](article-name.md)`

- Článek odkazuje na článek v nadřazeném adresáři aktuálního adresáře:

  `[link text](../article-name.md)`

- Článek odkazuje na článek v podadresáři aktuálního adresáře:

  `[link text](directory/article-name.md)`

- Článek odkazuje na článek v podadresáři nadřazeného adresáře aktuálního adresáře:

  `[link text](../directory/article-name.md)`

> [!NOTE]
> V žádném z předchozích příkladů se jako součást odkazu nepoužívá `~/`. Pokud chcete vytvořit odkaz na absolutní cestu, která začíná v kořenovém adresáři úložiště, začněte odkaz znakem `/`. Při zahrnutí řetězce `~/` vznikají neplatné odkazy pro navigaci do zdrojových úložišť na GitHubu. Problém se vyřeší, když bude cesta začínat znakem `/`.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>Struktura odkazů na docs.microsoft.com

Obsah publikovaný na docs.microsoft.com má následující strukturu adresy URL:

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

Příklady:

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` – Identifikuje jazyk článku (příklad: en-us nebo cs-cz).
- `<product-service>` – Název produktu nebo služby (příklad: powershell, dotnet nebo azure).
- `[<feature-service>]` – (nepovinné) Název funkce nebo dílčí služby produktu (například: csharp nebo load-balancer).
- `[<subfolder>]` – (nepovinné) Název podsložky v rámci funkce.
- `<topic>` – Název souboru článku pro téma (například: prehled-nastroje-pro-vyrovnavani-zatizeni nebo prehled).
- `[?view=\<view-name>]` – (nepovinné) Název zobrazení používaný selektorem verzí pro obsah, který má více dostupných verzí (například: azps-3.5.0).

> [!TIP]
> Ve většině případů mají články ve stejné sadě _docset_ stejný fragment adresy URL `<product-service>`. Například:
> - Stejná sada docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - Různé sady docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>Odkazy na záložky

Pro odkaz na záložku na nadpis v *aktuálním* souboru použijte symbol hash následovaný slovy nadpisu malými písmeny. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami:

```markdown
[Managed Disks](#managed-disks)
```

K odkazu na nadpis záložky v jiném článku použijte odkaz na daný soubor nebo web, za kterým bude následovat symbol hash a text nadpisu. Odeberte z nadpisu interpunkci a nahraďte mezery pomlčkami:

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Odkaz na záložku můžete také zkopírovat z adresy URL. Pokud chcete najít adresu URL, najeďte myší na řádek nadpisu na docs.microsoft.com. Měla by se zobrazit ikona odkazu:

![Ikona odkazu v nadpisu článku](media/how-to-write-links/bookmark-link.png)

Klikněte na ikonu odkazu a pak zkopírujte text ukotvení záložky z adresy URL (tj. část za znakem hash).

> [!NOTE]
> Rozšíření Docs obsahuje také nástroje, které vám pomůžou s vytvářením odkazů.

### <a name="explicit-anchor-links"></a>Explicitní odkazy na ukotvení

Explicitní odkazy na ukotvení používající značku `<a>` jazyka HTML není nutné přidávat a ani se to nedoporučuje, s výjimkou centra a cílových stránek. Místo toho použijte automaticky generované záložky, jak je popsáno v části [odkazy na záložky](#bookmark-links). Pro centrum a cílové stránky deklarujte ukotvení následujícím způsobem:

```markdown
## <a id="anchortext" />Header text
```

nebo

```markdown
## <a name="anchortext" />Header text
```

A následující text k propojení na ukotvení:

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> Text ukotvení musí být vždycky malými písmeny a nesmí obsahovat mezery.

## <a name="xref-cross-reference-links"></a>Křížové odkazy (XRef)

Odkazy XRef jsou doporučeným způsobem, jak odkazovat na rozhraní API, protože jsou ověřovány při sestavení. K odkazování na automaticky generované referenční stránky rozhraní API v aktuální sadě dokumentace nebo v jiných sadách dokumentace použijte odkazy XRef s jedinečným ID ([UID](#determine-the-uid)) typu nebo člena.

> [!TIP]
> K vložení odkazů XRref pro .NET, které jsou umístěny v [Prohlížeč rozhraní .NET API][], můžete použít [rozšíření Docs Markdown pro VS Code][docsextension] (součást balíčku pro vytváření obsahu na webu Docs).

Ověřte, jestli rozhraní API, ke kterému chcete vytvořit odkaz, je na webu [docs.microsoft.com][docs], zadáním jeho celého názvu nebo části názvu do vyhledávacího pole [Prohlížeč rozhraní .NET API][] nebo [Windows UPW][]. Pokud se nezobrazí žádné výsledky, typ ještě není na docs.microsoft.com.

Můžete použít jednu z následujících syntaxí:

- Automatické odkazy:

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   Ve výchozím nastavení text odkazu zobrazuje pouze název člena nebo typu. Volitelný parametr dotazu `displayProperty=nameWithType` vytvoří plně kvalifikovaný text odkazu, tj. **namespace.type**, pro typy a **type.member** pro členy typu, včetně členů výčtového typu.

- Odkazy ve stylu Markdownu:

   ```markdown
   [link text](xref:UID)
   ```

   Použijte odkazy ve stylu Markdownu pro odkazy XRef, když chcete přizpůsobit zobrazený text odkazu.

Příklady:

- **\<xref:System.String>** se zobrazí jako <xref:System.String>

- **\<xref:System.String?displayProperty=nameWithType>** se zobrazí jako <xref:System.String?displayProperty=nameWithType>

- **\[String class](xref:System.String)** se zobrazí jako [String class](xref:System.String).

Parametr dotazu `displayProperty=fullName` funguje stejným způsobem jako `displayProperty=nameWithType` pro třídy. To znamená, že text odkazu se změní na **namespace.classname**. Členům se ale text odkazu zobrazuje jako **namespace.classname.membername**, což může být nežádoucí.

> [!NOTE]
> U identifikátorů UID se rozlišuje velikost písmen. Například `<xref:System.Object>` se přeloží správně, ale `<xref:system.object>` ne.

### <a name="xref-build-warnings-and-incremental-builds"></a>Upozornění sestavení odkazu XRef a přírůstková sestavení

Přírůstkové sestavení (build) sestaví pouze soubory, které byly změněny nebo ovlivněny změnou. Pokud se zobrazí upozornění sestavení týkající se neplatného odkazu XRef, ale odkaz je ve skutečnosti platný, může to být proto, že sestavení bylo přírůstkové. Soubor, který způsobil upozornění, se nezměnil, takže nebyl sestaven a byla znovu přehrána minulá upozornění. Když se soubor změní nebo když spustíte úplné sestavení (úplné sestavení můžete spustit na ops.microsoft.com), upozornění zmizí. To je nevýhoda přírůstkových sestavení, protože DocFX neumí zjistit aktualizaci dat uvnitř služby XREF.

### <a name="determine-the-uid"></a>Určení UID

Identifikátor UID je obvykle plně kvalifikovaná třída nebo název člena. Existují alespoň dva způsoby, jak určit UID:

- Klikněte pravým tlačítkem myši na stránku [Docs][docs] pro typ nebo člena, vyberte **Zobrazit zdroj** a potom zkopírujte hodnotu **content** pro **ms.assetid**:

  ![ms.assetid ve zdroji pro webovou stránku](media/how-to-write-links/ms-assetid.png)

- Použijte [web automatického dokončování][] připojením části názvu typu nebo celého názvu typu k adrese URL. Například zadáním `https://xref.docs.microsoft.com/autocomplete?text=Writeline` do panelu Adresa v prohlížeči se zobrazí všechny typy a metody, které v názvu obsahují **Writeline**, spolu s jejich UID.

#### <a name="verify-the-uid"></a>Ověření UID

Pokud chcete otestovat, jestli máte správné UID, nahraďte **System.String** v následující adrese URL vaším UID a pak ho vložte do panelu Adresa v prohlížeči:

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> V UID v adrese URL se rozlišují velká a malá písmena, a pokud kontrolujete UID přetížení metody, nepoužívejte mezi typy parametrů mezery.

Pokud se zobrazí něco podobného, máte správné UID:

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

Pokud se na stránce zobrazuje jenom `[]`, máte nesprávné UID.

### <a name="percent-encoding-of-urls"></a>Procentové kódování adres URL

Speciální znaky v UID musí být kódovány ve formátu HTML následujícím způsobem:

| Znak | Kódování HTML |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

Tady najdete úplný seznam [procentových kódů](https://en.wikipedia.org/wiki/Percent-encoding).

Příklady kódování:

- ``System.Threading.Tasks.Task`1`` se kóduje jako `System.Threading.Tasks.Task%601` (viz [oddíl o obecných typech](#generic-types)).

- `System.Exception.#ctor` se kóduje jako `System.Exception.%23ctor`.

- `System.Object.Equals*` se kóduje jako `System.Object.Equals%2A`.

### <a name="generic-types"></a>Obecné typy

Obecné typy jsou tyto typy jako například `System.Collections.Generic.List<T>`. Pokud přejdete na tento typ v [prohlížeči .NET API](https://docs.microsoft.com/dotnet/api/) a podíváte se na jeho adresu URL, uvidíte, že `<T>` je v adrese URL napsáno jako `-1`, což ve skutečnosti představuje **`1**:

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

Pokud chcete vytvořit odkaz na obecný typ, například **List\<T>** , zakódujte znak pro zpětný apostrof **\`** jako **%60**, jak je znázorněno v následujícím příkladu:

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>Metody

Pokud chcete vytvořit odkaz na metodu, můžete buď vytvořit odkaz na obecnou stránku metody přidáním hvězdičky (`*`) za název metody, nebo na konkrétní přetížení. Obecnou stránku například použijte, když chcete vytvořit odkaz na metodu `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` bez specifických typů parametrů. Znak hvězdičky je kódován jako `%2A`. Například:

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` je odkaz na <xref:System.Object.Equals%2A?displayProperty=nameWithType>.

Jestliže chcete vytvořit odkaz na konkrétní přetížení, přidejte za název metody závorky a doplňte úplný název typu každého parametru. Nedávejte mezeru mezi názvy typů, jinak odkaz nebude fungovat. Například:

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` je odkaz na <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>.

## <a name="links-from-includes"></a>Odkazy z vložených souborů

Jelikož jsou vložené soubory umístěné v jiném adresáři, musíte použít delší relativní cesty. Pokud chcete vytvořit odkaz na článek z vloženého souboru, použijte tento formát:

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> Rozšíření [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) pro Visual Studio Code vám pomůže správně vkládat relativní odkazy a záložky bez únavného řešení cest.

## <a name="links-in-selectors"></a>Odkazy v selektorech

Volič je součást navigace, která se v článku dokumentace zobrazuje ve formě rozevíracího seznamu. Když čtenář vybere nějakou hodnotu v tomto rozevíracím seznamu, otevře prohlížeč vybraný článek. Seznam voliče zpravidla obsahuje odkazy na související články, například na stejnou problematiku v několika programovacích jazycích nebo na úzce související sérii článků.

Pokud máte voliče, které jsou začleněné ve vloženém souboru, použijte následující strukturu odkazu:

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>Odkazy z referencí

Pokud chcete, aby byl váš zdrojový obsah lépe čitelný, můžete použít odkazy z referencí. Odkazy z referencí nahradí syntax hotlinku jednodušší syntaxí, která vám umožní přesunout dlouhé adresy URL na konec článku. Zde je příklad z webu [Daring Fireball](https://daringfireball.net/projects/markdown/):

Vložený text:

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Odkazy referencí na konci článku:

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

Nezapomeňte mezi dvojtečkou a odkazem vytvořit mezeru. Pokud odkazujete na ostatní technické články a zapomenete mezeru vytvořit, odkaz nebude v publikovaném článku fungovat.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Odkazování na stránky, které nejsou součástí sady technické dokumentace

Pokud chcete vytvořit odkaz na jiný web ve vlastnictví Microsoftu (jako je stránka s ceníkem, stránka SLA nebo cokoli jiného, co není článek dokumentace), použijte absolutní adresu URL, ale vynechejte národní prostředí. Cílem je, aby odkazy fungovaly v GitHubu a na zobrazené stránce:

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>Odkazy na weby třetích stran

Nejlepší uživatelské prostředí minimalizuje odchod uživatelů na jiný web. Odkazy na weby třetích stran, které jsou občas potřeba, proto vytvářejte na základě těchto informací:

- **Odpovědnost:** Když jde o informace, které má sdílet třetí strana, odkazujte na obsah třetí strany. Úkolem Microsoftu například není říkat lidem, jak používat vývojářské nástroje pro Android – to má udělat Google. Pokud je to potřeba, můžeme vysvětlit, jak vývojářské nástroje pro Android používat *se* službou Azure, ale jak tyto nástroje celkově používat by měl vysvětlit Google.
- **Schválení od PM:** O schválení obsahu třetí strany požádejte Microsoft. Odkazování na takový obsah znamená, že mu důvěřujeme, a zahrnuje odpovědnost, pokud se lidé těmito pokyny budou řídit.
- **Kontroly aktuálnosti:** Ověřujte, jestli jsou informace třetí strany stále aktuální, správné a relevantní a jestli se odkaz nezměnil.
- **Přesměrování ven:** Informujte uživatele, že budou přesměrováni na jiný web. Pokud to není jasné z kontextu, přidejte vysvětlení. Například: „Požadavky zahrnují vývojářské nástroje pro Android, které si můžete stáhnout z webu Android Studio.“
- **Další kroky:** V oddíle Další kroky můžete přidat odkaz například na blog MVP. Jen uživatele znovu nezapomeňte informovat, že budou přesměrováni na jiný web.
- **Právní náležitosti:** Jsme právně krytí částí **Odkazy na weby třetích stran** v **Podmínkách použití** uvedených v zápatí každé stránky microsoft.com.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Prohlížeč rozhraní .NET API]: https://docs.microsoft.com/dotnet/api/
[Windows UPW]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[web automatického dokončování]: https://xref.docs.microsoft.com/autocomplete?text=
