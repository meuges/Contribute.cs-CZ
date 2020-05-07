---
title: Komprese obrázků – Balíček pro vytváření obsahu na webu Docs
description: Tady najdete informace, jak komprimovat obrázky v Balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336651"
---
# <a name="image-compression"></a>Komprese obrázků

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>Shrnutí

Veškerá dokumentace je poskytována přes web, s výjimkou verzí dokumentů PDF. Při poskytování statického obsahu je nejlepší minimalizovat počet bajtů posílaných po drátě. Jedním ze způsobů je komprimovat obrázky v klidovém stavu.

Rozšíření Balíčku pro vytváření obsahu na webu Docs obsahuje položky kontextové nabídky pro kompresi obrázků. Podporují se tyto typy obrázků a rozšíření:

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

Kde je to možné, používají se bezeztrátové algoritmy komprese obrázků.

## <a name="compress-image"></a>Komprese obrázku

V navigačním podokně **Průzkumníka** klikněte pravým tlačítkem na soubor obrázku a potom vyberte možnost **Komprimovat obrázek**. Obrázek se pak komprimuje.

## <a name="compress-images-in-folder"></a>Komprese obrázků ve složce

V navigačním podokně **Průzkumníka** klikněte pravým tlačítkem na složku s obrázky a potom vyberte možnost **Komprimovat obrázky ve složce**. Všechny obrázky ve složce se zkomprimují.

## <a name="considerations"></a>Důležité informace

Obrázky s vysokým rozlišením se zmenšují automaticky. Maximální rozměry jsou založené na maximální šířce `1,200px` doporučené platformou. Maximální hodnota se používá pouze v případě, že jsou obrázky větší, než je jejich doporučená velikost. Při automatické změně velikosti se zachová poměr stran.

## <a name="preferences"></a>Předvolby

Maximální rozměry se dají konfigurovat, ale existuje výchozí maximální šířka `1200` pixelů. Pokud chcete nakonfigurovat maximální rozměry, vyberte **Soubor -> Předvolby -> Nastavení** a filtrujte podle hodnoty `"Docs Image Extension"`.

:::image type="content" source="media/configure-image-compression.png" alt-text="Konfigurace komprese obrázků":::

> [!NOTE]
> Hodnota `0` pro **Maximální šířku** nebo **Maximální výšku** bude jednoduše ignorovat odchylky rozlišení.

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce.

[![Ukázka komprese obrázku](media/compress-image.gif)](media/compress-image.gif#lightbox)
