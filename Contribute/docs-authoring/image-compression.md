---
title: Komprese obrázků – Balíček pro vytváření obsahu na webu Docs
description: Tady najdete informace, jak komprimovat obrázky v Balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336651"
---
# <a name="image-compression"></a><span data-ttu-id="43bf0-103">Komprese obrázků</span><span class="sxs-lookup"><span data-stu-id="43bf0-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="43bf0-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="43bf0-104">Summary</span></span>

<span data-ttu-id="43bf0-105">Veškerá dokumentace je poskytována přes web, s výjimkou verzí dokumentů PDF. Při poskytování statického obsahu je nejlepší minimalizovat počet bajtů posílaných po drátě.</span><span class="sxs-lookup"><span data-stu-id="43bf0-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="43bf0-106">Jedním ze způsobů je komprimovat obrázky v klidovém stavu.</span><span class="sxs-lookup"><span data-stu-id="43bf0-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="43bf0-107">Rozšíření Balíčku pro vytváření obsahu na webu Docs obsahuje položky kontextové nabídky pro kompresi obrázků.</span><span class="sxs-lookup"><span data-stu-id="43bf0-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="43bf0-108">Podporují se tyto typy obrázků a rozšíření:</span><span class="sxs-lookup"><span data-stu-id="43bf0-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="43bf0-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="43bf0-109">*\*.png*</span></span>
* <span data-ttu-id="43bf0-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="43bf0-110">*\*.jpg*</span></span>
* <span data-ttu-id="43bf0-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="43bf0-111">*\*.jpeg*</span></span>
* <span data-ttu-id="43bf0-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="43bf0-112">*\*.gif*</span></span>
* <span data-ttu-id="43bf0-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="43bf0-113">*\*.svg*</span></span>
* <span data-ttu-id="43bf0-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="43bf0-114">*\*.webp*</span></span>

<span data-ttu-id="43bf0-115">Kde je to možné, používají se bezeztrátové algoritmy komprese obrázků.</span><span class="sxs-lookup"><span data-stu-id="43bf0-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="43bf0-116">Komprese obrázku</span><span class="sxs-lookup"><span data-stu-id="43bf0-116">Compress image</span></span>

<span data-ttu-id="43bf0-117">V navigačním podokně **Průzkumníka** klikněte pravým tlačítkem na soubor obrázku a potom vyberte možnost **Komprimovat obrázek**.</span><span class="sxs-lookup"><span data-stu-id="43bf0-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="43bf0-118">Obrázek se pak komprimuje.</span><span class="sxs-lookup"><span data-stu-id="43bf0-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="43bf0-119">Komprese obrázků ve složce</span><span class="sxs-lookup"><span data-stu-id="43bf0-119">Compress images in folder</span></span>

<span data-ttu-id="43bf0-120">V navigačním podokně **Průzkumníka** klikněte pravým tlačítkem na složku s obrázky a potom vyberte možnost **Komprimovat obrázky ve složce**.</span><span class="sxs-lookup"><span data-stu-id="43bf0-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="43bf0-121">Všechny obrázky ve složce se zkomprimují.</span><span class="sxs-lookup"><span data-stu-id="43bf0-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="43bf0-122">Důležité informace</span><span class="sxs-lookup"><span data-stu-id="43bf0-122">Considerations</span></span>

<span data-ttu-id="43bf0-123">Obrázky s vysokým rozlišením se zmenšují automaticky.</span><span class="sxs-lookup"><span data-stu-id="43bf0-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="43bf0-124">Maximální rozměry jsou založené na maximální šířce `1,200px` doporučené platformou.</span><span class="sxs-lookup"><span data-stu-id="43bf0-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="43bf0-125">Maximální hodnota se používá pouze v případě, že jsou obrázky větší, než je jejich doporučená velikost. Při automatické změně velikosti se zachová poměr stran.</span><span class="sxs-lookup"><span data-stu-id="43bf0-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="43bf0-126">Předvolby</span><span class="sxs-lookup"><span data-stu-id="43bf0-126">Preferences</span></span>

<span data-ttu-id="43bf0-127">Maximální rozměry se dají konfigurovat, ale existuje výchozí maximální šířka `1200` pixelů.</span><span class="sxs-lookup"><span data-stu-id="43bf0-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="43bf0-128">Pokud chcete nakonfigurovat maximální rozměry, vyberte **Soubor -> Předvolby -> Nastavení** a filtrujte podle hodnoty `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="43bf0-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Konfigurace komprese obrázků":::

> [!NOTE]
> <span data-ttu-id="43bf0-130">Hodnota `0` pro **Maximální šířku** nebo **Maximální výšku** bude jednoduše ignorovat odchylky rozlišení.</span><span class="sxs-lookup"><span data-stu-id="43bf0-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="43bf0-131">V praxi</span><span class="sxs-lookup"><span data-stu-id="43bf0-131">In action</span></span>

<span data-ttu-id="43bf0-132">Tady vidíte krátkou ukázku této funkce.</span><span class="sxs-lookup"><span data-stu-id="43bf0-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="43bf0-133">[![Ukázka komprese obrázku](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="43bf0-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
