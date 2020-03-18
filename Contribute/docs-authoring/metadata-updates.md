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
# <a name="update-metadata"></a><span data-ttu-id="41fe0-103">Aktualizace metadat</span><span class="sxs-lookup"><span data-stu-id="41fe0-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="41fe0-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="41fe0-104">Summary</span></span>

<span data-ttu-id="41fe0-105">V souboru Markdownu ( *\*.md*) jsou v místní nabídce k dispozici dvě položky pro metadata.</span><span class="sxs-lookup"><span data-stu-id="41fe0-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="41fe0-106">Když kliknete pravým tlačítkem myši na jakékoli místo v textovém editoru, zobrazí se nabídka s položkami podobná této:</span><span class="sxs-lookup"><span data-stu-id="41fe0-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Místní nabídka pro aktualizaci metadat":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="41fe0-108">Update `ms.date` metadata value</span><span class="sxs-lookup"><span data-stu-id="41fe0-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="41fe0-109">Když vyberete možnost **Update `ms.date` Metadata Value** (Aktualizovat hodnotu metadat `ms.date`), nastaví se jako aktuální hodnota `ms.date` v markdownových souborech dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="41fe0-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="41fe0-110">V případě, že pole metadat `ms.date` v dokumentu ještě není, nedojde k žádné akci.</span><span class="sxs-lookup"><span data-stu-id="41fe0-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="41fe0-111">Update implicit metadata values</span><span class="sxs-lookup"><span data-stu-id="41fe0-111">Update implicit metadata values</span></span>

<span data-ttu-id="41fe0-112">Když vyberete možnost **Update implicit metadata values** (Aktualizovat implicitní hodnoty metadat), dojde k vyhledání a nahrazení všech možných hodnot metadat, které by mohly být určené implicitně.</span><span class="sxs-lookup"><span data-stu-id="41fe0-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="41fe0-113">Hodnoty metadat jsou implicitně určené v souboru *docfx.json* a uzlu `build/fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="41fe0-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="41fe0-114">Každý pár klíč-hodnota v uzlu `fileMetadata` představuje výchozí hodnoty metadat.</span><span class="sxs-lookup"><span data-stu-id="41fe0-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="41fe0-115">Například soubor Markdownu v adresáři *top-level/sub-folder*, který vynechává hodnotu metadat `ms.author`, může implicitně určovat výchozí hodnotu používanou v uzlu `fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="41fe0-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

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

<span data-ttu-id="41fe0-116">V takovém případě všechny soubory Markdownu implicitně převezmou hodnotu metadat `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="41fe0-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="41fe0-117">Tato funkce pracuje s implicitním nastavením nalezeným v souboru *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="41fe0-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="41fe0-118">Pokud soubor Markdownu obsahuje metadata s hodnotami explicitně nastavenými na jinou hodnotu než jsou hodnoty implicitní, dojde k jejich přepsání.</span><span class="sxs-lookup"><span data-stu-id="41fe0-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="41fe0-119">Podívejte se na následující metadata souboru Markdownu, který se nachází v **top-level/sub-folder/includes/example.md**:</span><span class="sxs-lookup"><span data-stu-id="41fe0-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="41fe0-120">Pokud byste u tohoto souboru zvolili možnost **Update implicit metadata values** (Aktualizovat implicitní hodnoty metadat), předpokládaný obsah souboru *docfx.json* nad hodnotou metadat by se aktualizoval na `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="41fe0-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="41fe0-121">V praxi</span><span class="sxs-lookup"><span data-stu-id="41fe0-121">In action</span></span>

<span data-ttu-id="41fe0-122">Tady vidíte krátkou ukázku této funkce:</span><span class="sxs-lookup"><span data-stu-id="41fe0-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="41fe0-123">[![Ukázka aktualizace metadat](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="41fe0-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
