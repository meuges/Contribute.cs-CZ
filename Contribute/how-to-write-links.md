---
title: Používání odkazů v dokumentaci
description: Tento článek obsahuje pokyny k vytváření odkazů na obsah na webu docs.microsoft.com.
ms.date: 06/29/2017
ms.openlocfilehash: dad0460cfb36594c17cef1b079c5fc14191f56f7
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251448"
---
# <a name="using-links-in-documentation"></a>Používání odkazů v dokumentaci
Tento článek popisuje způsob používání hypertextových odkazů ze stránek hostovaných na webu docs.microsoft.com. Odkazy se snadno přidávají do markdownu pomocí několika různých konvencí. Odkazy přesměrovávají uživatele na obsah na stejné stránce, na jiné sousední stránky nebo na externí weby a adresy URL.

Back-end webu docs.microsoft.com používá systém OPS (Open Publishing Services), který implementuje DFM (DocFX Flavored Markdown). DFM je vysoce kompatibilní s GFM (GitHub Flavored Markdown) a přidává další funkce prostřednictvím rozšíření Markdownu.

> [!IMPORTANT]
> Všechny odkazy musí být zabezpečené (`https` versus `http`), když to cíl podporuje (což by měla drtivá většina).

## <a name="link-text"></a>Text odkazu

Slova, která použijete v textu odkazu, by měla být popisná. Jinými slovy by mělo jít o normální slova nebo název stránky, na kterou odkazujete.

> [!IMPORTANT]
> Nepoužívejte „klikněte sem“. Není to dobré pro SEO a nepopisuje to dostatečně cíl odkazu.

**Správně:**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Nesprávně:**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Odkazy z jednoho článku na druhý

Pokud chcete vytvořit hotlink z technického článku na webu Docs na jiný technický článek webu Docs v rámci stejné sady docset, použijte následující syntax pro odkazy:

- Článek v adresáři odkazuje na jiný článek ve stejném adresáři:

  `[link text](article-name.md)`

- Článek z podadresáře odkazuje na článek v kořenovém adresáři:

  `[link text](../article-name.md)`

- Článek v kořenovém adresáři odkazuje na článek v podadresáři:

  `[link text](./directory/article-name.md)`

- Článek v podadresáři odkazuje na článek v jiném podadresáři:

  `[link text](../directory/article-name.md)`

- Článek odkazující na různé sady docset (i ve stejném úložišti): `[link text](./directory/article-name)`

> [!IMPORTANT]
> V žádném z výše uvedených příkladů se jako součást odkazu nepoužívá `~/`. Pokud vytváříte odkaz na cestu v kořeni úložiště, začněte znakem `/`. Při zahrnutí řetězce `~/` vznikají neplatné odkazy pro navigaci do zdrojových úložišť na GitHubu. Problém se vyřeší, když bude cesta začínat znakem `/`.

## <a name="links-to-anchors"></a>Odkazy na ukotvení

Ukotvení vytvářet nemusíte. Generují se automaticky pro všechny nadpisy H2 při publikování. Jediné, co musíte udělat, je vytvořit odkazy na oddíly H2.

- Vytvoření odkazu na nadpis ve stejném článku:

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- Vytvoření odkazu na ukotvení z jiného článku ve stejném podadresáři:

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- Vytvoření odkazu na ukotvení v jiném podadresáři služby:

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Odkazy z vložených souborů

Jelikož jsou vložené soubory umístěné v jiném adresáři, musíte použít delší relativní cesty. Pokud chcete vytvořit odkaz na článek z vloženého souboru, použijte tento formát:

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a>Odkazy v selektorech

Pokud máte selektory, které jsou vložené do vloženého souboru, jak to má tým dokumentace Azure, použijte následující strukturu odkazu:

    > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
    - [(Text1 | Example1 )](../articles/folder/article-name1.md)
    - [(Text1 | Example2 )](../articles/folder/article-name2.md)
    - [(Text2 | Example3 )](../articles/folder/article-name3.md)
    - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->

## <a name="reference-style-links"></a>Odkazy z referencí

Pokud chcete, aby byl váš zdrojový obsah lépe čitelný, můžete použít odkazy z referencí. Odkazy z referencí nahradí syntax hotlinku jednodušší syntaxí, která vám umožní přesunout dlouhé adresy URL na konec článku. Zde je příklad z webu [Daring Fireball](https://daringfireball.net/projects/markdown/):

Vložený text:

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

Odkazy referencí na konci článku:

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

Nezapomeňte mezi dvojtečkou a odkazem vytvořit mezeru. Pokud odkazujete na ostatní technické články a zapomenete mezeru vytvořit, odkaz nebude v publikovaném článku fungovat.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Odkazování na stránky, které nejsou součástí sady technické dokumentace

Pokud chcete vytvořit odkaz na jiný web ve vlastnictví Microsoftu (jako je stránka s ceníkem, stránka SLA nebo cokoli jiného, co není článek dokumentace), použijte absolutní adresu URL, ale vynechejte národní prostředí. Cílem je, aby odkazy fungovaly v GitHubu a na zobrazené stránce:

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a>Odkazy na weby třetích stran

Nejlepší uživatelské prostředí minimalizuje odchod uživatelů na jiný web. Odkazy na weby třetích stran, které jsou občas potřeba, proto vytvářejte na základě těchto informací:

- **Odpovědnost:** Na obsah třetích stran odkazujte, když jde o informace, které má sdílet třetí strana. Úkolem Microsoftu například není říkat lidem, jak používat vývojářské nástroje pro Android – to má udělat Google. Pokud je to potřeba, můžeme vysvětlit, jak vývojářské nástroje pro Android používat *se* službou Azure, ale jak tyto nástroje celkově používat by měl vysvětlit Google.
- **Schválení od PM**: Požádejte Microsoft o schválení obsahu třetí strany. Odkazování na takový obsah znamená, že mu důvěřujeme, a zahrnuje odpovědnost, pokud se lidé těmito pokyny budou řídit.
- **Ověření čerstvosti:** Ověřte, že informace třetí strany jsou stále aktuální, správné a relevantní a že se odkaz nezměnil.
- **Přesměrování ven:** Informujte uživatele, že budou přesměrováni na jiný web. Pokud to není jasné z kontextu, přidejte vysvětlení. Například: „Požadavky zahrnují vývojářské nástroje pro Android, které si můžete stáhnout z webu Android Studio“.
- **Další kroky:** V sekci Další kroky můžete přidat odkaz například na blog MVP. Jen uživatele znovu nezapomeňte informovat, že budou přesměrováni na jiný web.
- **Právní náležitosti:** Jsme právně krytí částí **Odkazy na weby třetích stran** v **Podmínkách použití** uvedených v zápatí každé stránky ms.com.

## <a name="links-to-msdn-or-technet"></a>Odkazy na MSDN nebo TechNet

Když budete potřebovat odkázat na MSDN nebo Technet, použijte celý odkaz na téma a odeberte z odkazu jazyk národního prostředí „en-us“.

## <a name="links-to-azure-powershell-reference-content"></a>Odkazy na referenční obsah Azure PowerShell

Referenční obsah Azure PowerShell prošel od listopadu 2016 několika změnami. Pro odkazování na tento obsah z jiných článků na webu docs.microsoft.com použijte následující pokyny.

Struktura adresy URL:

* Pro rutiny:
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Pro koncepční témata:
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

Část &lt;moniker-name&gt; je volitelná. Pokud ji vynecháte, budete přesměrováni na nejnovější verzi obsahu. Část &lt;service-name&gt; je jedním z příkladů uvedených v následujících základních adresách URL:

- Obsah Azure PowerShell (AzureRM): [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Obsah Azure PowerShell (ASM): [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Obsah Azure Active Directory (AzureAD) PowerShell: [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- Azure Service Fabric PowerShell: [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- Azure Information Protection PowerShell: [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- Azure Elastic DB Jobs PowerShell: [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

Když tyto adresy URL použijete, budete přesměrováni na nejnovější verzi obsahu. Tímto způsobem nemusíte určovat verzi parametru moniker. Nebudete tak mít odkazy na koncepční obsah, které se musí při změně verze aktualizovat.

Pokud chcete vytvořit odkaz, najděte ve svém prohlížeči stránku, na kterou chcete odkázat, a zkopírujte její adresu URL.
Potom odeberte https://docs.microsoft.com a informace o národním prostředí.

Když odkazujete z obsahu stránky, musíte použít celou adresu URL bez informace o národním prostředí.

Příklad Markdownu:

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
