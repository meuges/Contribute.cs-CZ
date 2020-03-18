---
title: Šablona a stručná nápověda k článkům o PowerShellu
description: V tomto článku najdete praktickou šablonu, kterou můžete použít k vytvoření nových článků tvořících dokumentaci k PowerShellu.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 073a44240b1aa4baa9e655dab069097d21cdd66d
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331922"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>Průvodce správným stylem jazyka Markdown pro dokumentaci k PowerShellu

Tento článek obsahuje konkrétní pokyny týkající se stylu obsahu dokumentace k PowerShellu.

Další pokyny, které se týkají stylu psaní, najdete v [průvodci správným stylem od Microsoftu](https://docs.microsoft.com/style-guide/welcome/).

## <a name="metadata"></a>Metadata

Tato šablona obsahuje příklady syntaxe jazyka Markdown a pokyny k nastavení metadat.
Při vytváření souboru Markdown byste měli přiloženou šablonu zkopírovat do nového souboru, vyplnit metadata podle tohoto návodu a nastavit záhlaví H1 jako nadpis článku.

Požadovaný blok metadat je v následujícím ukázkovém bloku metadat:

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Mezi dvojtečkou (:) a hodnotou prvku metadat **musí** být mezera.
- Dvojtečky v hodnotě (třeba v nadpisu) způsobí chybu analyzátoru metadat. V takovém případě dejte nadpis do dvojitých uvozovek (příklad: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author** (autor): Pole autora musí obsahovat **uživatelské jméno autora na GitHubu**.
- **description** (popis): Shrnuje obsah článku. Většinou se zobrazuje na stránce s výsledky hledání, ale nepoužívá se k řazení výsledků hledání. Měl by mít 115–145 znaků (včetně mezer).
- **ms.date**: Datum poslední významné aktualizace. U stávajících článků datum aktualizujte, pokud zkontrolujete a aktualizujete celý článek. U malých oprav, jako jsou opravy překlepů apod., nejde o aktualizaci.
- **title** (název): Zobrazí se ve výsledcích vyhledávačů. Nadpis nemusí přesně odpovídat názvu v nadpisu H1, ale měl by mít maximálně 60 znaků.

Ke každému článku jsou připojená další metadata, ale většinu hodnot metadat obvykle používáme na úrovni složky zadané v souboru **docfx.json**.

## <a name="product-terminology"></a>Terminologie produktu

Existují různé varianty PowerShellu. V této tabulce jsou definované různé výrazy používané k vysvětlení PowerShellu.

- **PowerShell** – výchozí produkt. PowerShell je produkt, který dodáváme. Výraz PowerShell může popisovat libovolnou edici produktu.
- **PowerShell Core** – PowerShell vytvořený v modulu .NET Core Common Language Runtime (CoreCLR) pro některou z podporovaných platforem.
- **Windows PowerShell** – PowerShell vytvořený v modulu .NET Framework Common Language Runtime (CLR). Windows PowerShell se dodává jenom ve Windows a vyžaduje celý modul .Net Framework CLR.

Obecně platí, že odkazy na „Windows PowerShell“ můžete v dokumentaci změnit na „PowerShell“.
„Windows PowerShell“ byste ale **neměli** měnit, pokud mluvíte o určité technologii Windows.

## <a name="basic-markdown-gfm-and-special-characters"></a>Základy jazyka Markdown (GFM) a speciální znaky

Základy jazyka Markdown také označované jako GitHub Flavored Markdown (GFM) a určité přípony OPS najdete v článku [Referenční informace k jazyku Markdown](../markdown-reference.md).

Markdown používá k formátování zvláštní znaky, například \*, \` a \#. Pokud chcete některý z těchto znaků přidat do obsahu, máte na výběr dvě možnosti:

- Dejte před speciální znak zpětné lomítko, abyste znak vyloučili (třeba `\*` pro \*).
- Použijte pro znak [kód entity HTML](http://www.ascii.cl/htmlcodes.htm) (třeba `&#42;` pro &#42;).
- Soubory Markdown by měly používat prostý text v kódování ASCII nebo UTF-8. Vyhýbejte se ale vícebajtovým znakům v kódování UTF-8. Raději použijte prvek HTML. Například pro symbol autorských práv použijte `&copy;`.
  Vykreslí se jako &copy;.

## <a name="hyperlinks"></a>Hypertextové odkazy

- Vyhýbejte se používání neupravených adres URL. Odkazy by měly mít syntaxi jazyka Markdown: `[friendlyname](url-or-path)`.
- Odkazy musí mít popisný název. Většinou je to nadpis propojeného tématu.
- Všechny položky v závěrečném oddílu Související odkazy musí být hypertextové odkazy.
- Při vytváření odkazů na jiný obsah, který je hostovaný na webu **docs.microsoft.com**, použijte relativní odkazy.
- V závorkách hypertextového odkazu nepoužívejte zpětné apostrofy, tučné písmo ani jiné značky.

Podrobnější informace o vytváření odkazů najdete v tématu [Používání odkazů v dokumentaci](../how-to-write-links.md).

## <a name="filenames"></a>Názvy souborů

Názvy souborů se řídí následujícími pravidly:

- Obsahují jenom písmena, číslice a pomlčky.
- Nesmí obsahovat mezery ani interpunkční znaménka. K oddělení slov a čísel v názvu souboru používejte pomlčky.
- Používejte slovesa, která vyjadřují určitou činnost, třeba develop (vyvíjet), buy (koupit), build (sestavit) nebo troubleshoot (řešit potíže). Nepoužívejte slova s koncovkou -ing.
- Nepoužívejte krátká slova (nepoužívejte členy a spojky a, and, the, in, or atd.).
- Musí být ve formátu Markdown a mít příponu souboru .md.
- Názvy souborů musí být krátké, protože tvoří část adresy URL vašich článků.

## <a name="blank-lines-spaces-and-tabs"></a>Prázdné řádky, mezery a tabulátory

Odeberte duplicitní prázdné řádky. Více prázdných řádků se v HTML vykreslí jako jeden prázdný řádek, takže není potřeba používat více prázdných řádků.

Prázdné řádky v jazyce Markdown také signalizují konec bloku. Mezi různými typy bloků jazyka Markdown (například mezi odstavcem a seznamem nebo nadpisem) by měl být jeden prázdný řádek.

> [!NOTE]
> Mezery jsou v jazyce Markdown důležité. Vždy používejte mezery, nikoli pevné tabulátory. Odeberte nadbytečné mezery na konci řádků.

## <a name="titles-and-headings"></a>Nadpisy a záhlaví

Používejte jenom [nadpisy ATX][atx] (hlavičky ve tvaru # místo tvaru `=` nebo `-`).

- Používejte velká písmena jako ve větě. Velkým písmenem by měla začínat jenom vlastní jména a první písmeno nadpisu nebo záhlaví.
- Mezi znakem `#` a prvním písmenem nadpisu musí být jedna mezera.
- Nadpisy musí být obklopeny jedním prázdným řádkem.
- Dokument má jenom jeden nadpis H1.
- Úrovně nadpisů by se měly zvyšovat vždy o jednu úroveň. Nepřeskakujte úrovně.
- Nepoužívejte v nadpisech zpětné apostrofy, tučné písmo ani jiné značky.

> [!CAUTION]
> Schéma odkazů na referenční rutiny v modulu [PlatyPS][platyPS] vyžaduje zvláštní nadpisy H2 a H3. Přidání nebo odebrání nadpisů může poškodit sestavení. Další informace najdete v [referenčním průvodci správným stylem rutin](powershell-style-reference.md).

## <a name="limit-line-length-to-100-characters"></a>Omezení délky řádku na 100 znaků

Zjednoduší se tím výstup příkazového řádku v podobě rozdílů a historie.

Toto pravidlo neplatilo u většiny stávajícího obsahu v dokumentaci k PowerShellu, ale postupně pracujeme na jeho zavedení. Budeme rádi, když nám pomůžete. K jednoduchému přeformátování odstavců na tuto délku můžete v editoru Visual Studio Code (VSCode) použít [rozšíření reflow][reflow].

## <a name="lists"></a>Seznamy

Pokud seznam obsahuje několik vět nebo odstavců, raději místo seznamu použijte podnadpis nižší úrovně.

Kolem seznamu musí být jeden prázdný řádek.

### <a name="unordered-lists"></a>Neuspořádané seznamy

Nezakončujte položky seznamu tečkou, pokud neobsahují více vět. Jako odrážky u položek seznamu používejte znak spojovníku (`-`). Vyhnete se tím záměně se značkou tučného písma nebo kurzívy, kterou je hvězdička [`*`]. Pokud chcete do položky s odrážkou zahrnout odstavec nebo jiné prvky, vložte konec řádku a zarovnejte odsazení podle prvního znaku za odrážkou.

Například:

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

Tento seznam obsahuje pod odrážkou dílčí prvky.

- Odrážka první položky

  Věta, která vysvětluje první odrážku.

  - Dílčí odrážka s položkou

    Věta, která vysvětluje dílčí odrážku.

- Odrážka druhé položky
- Odrážka třetí položky

### <a name="ordered-lists"></a>Uspořádané seznamy

Pokud položka číslovaného seznamu obsahuje odstavec nebo jiné prvky, zarovnejte odsazení s prvním znakem za číslem položky.

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

Jak to udělat:

> 1. U prvního prvku vložte za číslo 1 jednu mezeru. Dlouhá souvětí musí být zalomena na další řádek a musí být zarovnaná s prvním znakem za značkou číslovaného seznamu.
>
>    Pokud chcete přidat druhý prvek (viz tento příklad), vložte za první prvek zalomení řádku a zarovnejte odsazení. Odsazení druhého prvku musí být zarovnané s prvním znakem, který je za značkou číslovaného seznamu. U jednociferných položek, jako je například tato, odsadíte text do 4. sloupce. U dvouciferných položek, jako je například položka číslo 10, odsadíte text do 5. sloupce.
>
> 1. Tady začíná další číslovaná položka.

Všechny položky číslovaného seznamu musí mít číslo `1.` místo zvyšujícího se čísla u každé položky.
Markdown při vykreslení hodnotu automaticky zvýší. Tím se zjednoduší změna pořadí položek a standardizuje se odsazení podřízeného obsahu.

## <a name="formatting-command-syntax-elements"></a>Syntaktické prvky formátování příkazů

- Názvy rutin PowerShellu používají [psaní velkých a malých písmen podle jazyka Pascal][pascal-case]. Slovesa jsou od podstatných jmen oddělena pomlčkou. U rutin a parametrů vždy používejte jejich plný název s velkými a malými písmeny jako v jazyce Pascal. Raději nepoužívejte aliasy, pokud o nich výslovně nehovoříte.

- V odstavci ohraničte klíčová slova jazyka, názvy rutin a odkazy na proměnné znaky zpětného apostrofu (`` ` ``). Názvy vlastností, parametrů a tříd mají být **tučně**.

  Například:

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- Když odkazujete na parametr jeho názvem, měl by být tento název **tučným písmem**. Když popisujete použití parametru s předponou ve tvaru spojovníku, dejte parametr do zpětných apostrofů. Například:

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- V odkazech na externí příkazy (soubory EXE, skripty apod.) by měl být název příkazu tučným písmem, všechna písmena malá (nebo s velkým počátečním písmenem, pokud jde o začátek věty) a měl by být včetně příslušné přípony souboru. Například:

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- Pokud předvádíte příklad použití externího příkazu, měli byste ho dát do zpětných apostrofů.
  Pokud název koliduje s aliasem, musíte v ukázkovém příkladu uvést i příponu souboru. Například:

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- Při psaní koncepčního článku (na rozdíl od referenčního obsahu), musí první instance názvu rutiny představovat hypertextový odkaz na dokumentaci k dané rutině. V závorkách hypertextového odkazu nepoužívejte zpětné apostrofy, tučné písmo ani jiné značky.

  Například:

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  Další informace najdete v části [Hypertextové odkazy](#hyperlinks) v průvodci správným stylem.

## <a name="images"></a>Obrázky

Syntaxe pro začlenění obrázku:

```Syntax
![[alt text]](<folderPath>)
```

Příklad:

```markdown
![Introduction](./media/overview/Introduction.png)
```

`alt text` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku. Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku. Tento text je také užitečný v případě chyby na webu, kdy obrázek nejde vykreslit.

Obrázky by se měly ukládat do složky `media/<article-name>`, která je ve složce obsahující váš článek. Obrázky by se neměly mezi články sdílet. Ve složce `media` vytvořte složku, která odpovídá názvu souboru vašeho článku. Obrázky k danému článku zkopírujte do této nové složky. Pokud se obrázek používá ve více článcích, musí být v každé složce obrázků také kopie daného obrázkového souboru. Takový postup brání tomu, aby změna obrázku v jednom článku měli vliv na jiný článek.

V některých případech chcete sdílet obrázky, třeba loga a ikony, ve více článcích. Takové obrázky se ukládají do složky `/media/shared` v kořenovém adresáři úložiště.

Podporované jsou následující typy obrázkových souborů: *.png, *.gif, *.jpeg, *.jpg a *.svg.

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
