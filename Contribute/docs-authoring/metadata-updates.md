---
title: Aktualizace metadat – Balíček pro vytváření obsahu na webu Docs
description: Přečtěte si, jak aktualizovat metadata v balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336628"
---
# <a name="update-metadata"></a>Aktualizace metadat

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

V souboru Markdownu ( *\*.md*) jsou v místní nabídce k dispozici dvě položky pro metadata. Když kliknete pravým tlačítkem myši na jakékoli místo v textovém editoru, zobrazí se nabídka s položkami podobná této:

:::image type="content" source="media/update-metadata-menu.png" alt-text="Místní nabídka pro aktualizaci metadat":::

## <a name="update-msdate-metadata-value"></a>Update `ms.date` metadata value

Když vyberete možnost **Update `ms.date` Metadata Value** (Aktualizovat hodnotu metadat `ms.date`), nastaví se jako aktuální hodnota `ms.date` v markdownových souborech dnešní datum. V případě, že pole metadat `ms.date` v dokumentu ještě není, nedojde k žádné akci.

## <a name="update-implicit-metadata-values"></a>Update implicit metadata values

Když vyberete možnost **Update implicit metadata values** (Aktualizovat implicitní hodnoty metadat), dojde k vyhledání a nahrazení všech možných hodnot metadat, které by mohly být určené implicitně. Hodnoty metadat jsou implicitně určené v souboru *docfx.json* a uzlu `build/fileMetadata`. Každý pár klíč-hodnota v uzlu `fileMetadata` představuje výchozí hodnoty metadat. Například soubor Markdownu v adresáři *top-level/sub-folder*, který vynechává hodnotu metadat `ms.author`, může implicitně určovat výchozí hodnotu používanou v uzlu `fileMetadata`.

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

V takovém případě všechny soubory Markdownu implicitně převezmou hodnotu metadat `ms.author: dapine`. Tato funkce pracuje s implicitním nastavením nalezeným v souboru *docfx.json*. Pokud soubor Markdownu obsahuje metadata s hodnotami explicitně nastavenými na jinou hodnotu než jsou hodnoty implicitní, dojde k jejich přepsání.

Podívejte se na následující metadata souboru Markdownu, který se nachází v **top-level/sub-folder/includes/example.md**:

```markdown
---
ms.author: someone-else
---

# Content
```

Pokud byste u tohoto souboru zvolili možnost **Update implicit metadata values** (Aktualizovat implicitní hodnoty metadat), předpokládaný obsah souboru *docfx.json* nad hodnotou metadat by se aktualizoval na `ms.author: dapine`.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce:

[![Ukázka aktualizace metadat](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
