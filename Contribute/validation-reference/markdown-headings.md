---
title: Nadpisy v Markdownu
description: Popisuje požadavky na nadpisy v Markdownu.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084450"
---
# <a name="markdown-headings"></a><span data-ttu-id="1d8af-103">Nadpisy v Markdownu</span><span class="sxs-lookup"><span data-stu-id="1d8af-103">Markdown headings</span></span>

<span data-ttu-id="1d8af-104">Následující požadavky na ověření platí pro nadpisy v souborech Markdown OPS.</span><span class="sxs-lookup"><span data-stu-id="1d8af-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="1d8af-105">H1</span><span class="sxs-lookup"><span data-stu-id="1d8af-105">H1</span></span>

<span data-ttu-id="1d8af-106">`H1` se vztahuje k prvnímu nadpisu v souboru Markdown.</span><span class="sxs-lookup"><span data-stu-id="1d8af-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="1d8af-107">Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.</span><span class="sxs-lookup"><span data-stu-id="1d8af-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="1d8af-108">Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (`#`) a mezerou, po které následuje text nadpisu.</span><span class="sxs-lookup"><span data-stu-id="1d8af-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="1d8af-109">Nadpis H1 například u tohoto článku je tento:</span><span class="sxs-lookup"><span data-stu-id="1d8af-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="1d8af-110">Následující pravidla se vztahují k nadpisům H1:</span><span class="sxs-lookup"><span data-stu-id="1d8af-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="1d8af-111">Nadpis H1 se musí nacházet v souboru.</span><span class="sxs-lookup"><span data-stu-id="1d8af-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="1d8af-112">Může existovat pouze jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="1d8af-112">There can only be one H1.</span></span>
- <span data-ttu-id="1d8af-113">Nadpis H1 musí mít obsah.</span><span class="sxs-lookup"><span data-stu-id="1d8af-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="1d8af-114">Mezi znakem `#` a obsahem nadpisu H1 musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="1d8af-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="1d8af-115">Nadpis H1 bez mezery se na publikované stránce nezobrazí jako nadpis.</span><span class="sxs-lookup"><span data-stu-id="1d8af-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="1d8af-116">Nadpis H1 musí být prvním obsahem v souboru za hlavičkou metadat YML.</span><span class="sxs-lookup"><span data-stu-id="1d8af-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="1d8af-117">Mezi koncem hlavičky YML a nadpisem H1 není povolen žádný obsah, jako je text nebo obrázky.</span><span class="sxs-lookup"><span data-stu-id="1d8af-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="1d8af-118">Nepoužívejte prvek HTML pro nadpisy první úrovně – `<h1>`.</span><span class="sxs-lookup"><span data-stu-id="1d8af-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="1d8af-119">Použijte syntaxi Markdownu (`# `).</span><span class="sxs-lookup"><span data-stu-id="1d8af-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="1d8af-120">Nadpis H1 nesmí být delší než 100 znaků.</span><span class="sxs-lookup"><span data-stu-id="1d8af-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="1d8af-121">Toto je pokyn pro správný styl.</span><span class="sxs-lookup"><span data-stu-id="1d8af-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="1d8af-122">H2 – H6</span><span class="sxs-lookup"><span data-stu-id="1d8af-122">H2 - H6</span></span>

<span data-ttu-id="1d8af-123">V OPS jsou povoleny nadpisy H2 (`## `) až H6 (`###### `).</span><span class="sxs-lookup"><span data-stu-id="1d8af-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="1d8af-124">K vytváření nadpisů používejte hlavičky Markdownu, nikoli HTML (`<h2>` - `<h6>`).</span><span class="sxs-lookup"><span data-stu-id="1d8af-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
