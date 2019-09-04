---
title: title-missing
description: Vysvětlení a řešení problému sestavení title-missing na webu Docs
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236576"
---
# <a name="title-missing"></a>title-missing

## <a name="warning"></a>Upozornění

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a>Řešení

Přidejte text nadpisu, který se má zobrazovat ve výsledcích hledání. Obecně by nadpisy měly mít délku 19 až 59 znaků, měly by se lišit od hlavního nadpisu (H1) článku a měly by obsahovat příslušná brandingová slova. Do nadpisu byste neměli zahrnovat řetězec „| Microsoft Docs“ – ten automaticky přidává služba Docs. Pokud ho explicitně přidáte, bude ignorován. Pokud chcete do všech nadpisů v sadě obsahu přidat další branding, například řetězec „– Azure“, nastavte globálně nebo pro danou složku hodnotu metadat `titleSuffix`.

Náhled vzhledu vašeho nadpisu v Googlu si můžete zobrazit na stránce [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).

Pokud jste zaměstnancem Microsoft, podívejte se na [základy SEO](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) v interní příručce pro přispěvatele, kde najdete další informace o vhodných nadpisech a optimalizaci vyhledávacích webů (SEO).

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
