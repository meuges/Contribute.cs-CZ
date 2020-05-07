---
title: Dokončování vývojářských jazyků – Balíček pro vytváření obsahu na webu Docs
description: Tady se dozvíte, jak dokončování vývojářských jazyků pomáhá přispěvatelům v Balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336789"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="9baa7-103">Dokončování vývojářských jazyků</span><span class="sxs-lookup"><span data-stu-id="9baa7-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="9baa7-104">Shrnutí</span><span class="sxs-lookup"><span data-stu-id="9baa7-104">Summary</span></span>

<span data-ttu-id="9baa7-105">Přispěvatelé potřebují pomoc při určování platných identifikátorů jazyků (vývojářských jazyků), které můžou následovat po trojitém zpětném apostrofu (otevření ohraničení kódu) v souboru Markdownu.</span><span class="sxs-lookup"><span data-stu-id="9baa7-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="9baa7-106">Bohužel neexistuje ověřování vývojářských jazyků v době sestavování.</span><span class="sxs-lookup"><span data-stu-id="9baa7-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="9baa7-107">Výsledkem jsou různorodé reprezentace jednoho jazyka v rámci stejné koncepční sady dokumentace.</span><span class="sxs-lookup"><span data-stu-id="9baa7-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="9baa7-108">Podívejme se například na C#.</span><span class="sxs-lookup"><span data-stu-id="9baa7-108">Consider C# as an example.</span></span> <span data-ttu-id="9baa7-109">Přispěvatelé použili `c#`, `C#`, `cs`, `csharp` a jiné identifikátory jako reprezentace vývojářských jazyků tohoto jazyka.</span><span class="sxs-lookup"><span data-stu-id="9baa7-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="9baa7-110">Které z předchozích reprezentací jsou správné?</span><span class="sxs-lookup"><span data-stu-id="9baa7-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="9baa7-111">Funkce *Dokončování vývojářských jazyků* do situace přináší řád a zobrazuje seznam známých vývojářských jazyků.</span><span class="sxs-lookup"><span data-stu-id="9baa7-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="9baa7-112">Při výběru názvu vývojářského jazyka z IntelliSense:</span><span class="sxs-lookup"><span data-stu-id="9baa7-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="9baa7-113">Ochranné ohraničení kódu se uzavře.</span><span class="sxs-lookup"><span data-stu-id="9baa7-113">The code fence is closed.</span></span>
* <span data-ttu-id="9baa7-114">Kurzor je umístěn v ohraničení kódu.</span><span class="sxs-lookup"><span data-stu-id="9baa7-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="9baa7-115">Předvolby</span><span class="sxs-lookup"><span data-stu-id="9baa7-115">Preferences</span></span>

<span data-ttu-id="9baa7-116">Tuto funkci není možné zakázat.</span><span class="sxs-lookup"><span data-stu-id="9baa7-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="9baa7-117">K dispozici jsou následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="9baa7-117">The following settings are available:</span></span>

* [<span data-ttu-id="9baa7-118">Zobrazit běžně používané vývojářské jazyky</span><span class="sxs-lookup"><span data-stu-id="9baa7-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="9baa7-119">Zobrazit všechny známé vývojářské jazyky</span><span class="sxs-lookup"><span data-stu-id="9baa7-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="9baa7-120">Zobrazit běžně používané vývojářské jazyky</span><span class="sxs-lookup"><span data-stu-id="9baa7-120">Display commonly used dev langs</span></span>

<span data-ttu-id="9baa7-121">V jedné sadě dokumentace se použije jenom podmnožina platných vývojářských jazyků.</span><span class="sxs-lookup"><span data-stu-id="9baa7-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="9baa7-122">Rozšíření možností uživatele:</span><span class="sxs-lookup"><span data-stu-id="9baa7-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="9baa7-123">V nástroji Visual Studio Code otevřete sadu dokumentace do kořenového adresáře.</span><span class="sxs-lookup"><span data-stu-id="9baa7-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="9baa7-124">Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="9baa7-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="9baa7-125">Klikněte na odkaz **Upravit v settings.json** v oddílu **Markdown: Jazyky sady dokumentace**.</span><span class="sxs-lookup"><span data-stu-id="9baa7-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="9baa7-126">Do souboru *settings.json* přidejte následující vlastnost `markdown.docsetLanguages`:</span><span class="sxs-lookup"><span data-stu-id="9baa7-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="9baa7-127">Umístěte kurzor do prázdného pole vlastnosti a aktivujte IntelliSense (přes <kbd>Ctrl</kbd> + <kbd>mezerník</kbd>).</span><span class="sxs-lookup"><span data-stu-id="9baa7-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="9baa7-128">Zobrazí se seznam známých názvů vývojářských jazyků.</span><span class="sxs-lookup"><span data-stu-id="9baa7-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="9baa7-129">Přidávejte názvy vývojářských jazyků do pole, až bude seznam podle vašich představ.</span><span class="sxs-lookup"><span data-stu-id="9baa7-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="9baa7-130">Například v následujícím seznamu se uživateli po zadání tří apostrofů zobrazí čtyři názvy vývojářských jazyků:</span><span class="sxs-lookup"><span data-stu-id="9baa7-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="9baa7-131">Uložte změny do souboru *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="9baa7-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="9baa7-132">Prázdné pole `markdown.docsetLanguages` způsobí, že se zobrazí všechny známé vývojářské jazyky.</span><span class="sxs-lookup"><span data-stu-id="9baa7-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="9baa7-133">Zobrazit všechny známé vývojářské jazyky</span><span class="sxs-lookup"><span data-stu-id="9baa7-133">Display all known dev langs</span></span>

<span data-ttu-id="9baa7-134">Ve výchozím nastavení se v IntelliSense zobrazují všechny známé názvy vývojářských jazyků.</span><span class="sxs-lookup"><span data-stu-id="9baa7-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="9baa7-135">Toto nastavení přepisuje vlastnost `markdown.docsetLanguages` popsanou v části [Zobrazit běžně používané vývojářské jazyky](#display-commonly-used-dev-langs).</span><span class="sxs-lookup"><span data-stu-id="9baa7-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="9baa7-136">Změna tohoto nastavení:</span><span class="sxs-lookup"><span data-stu-id="9baa7-136">To change this setting:</span></span>

1. <span data-ttu-id="9baa7-137">Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.</span><span class="sxs-lookup"><span data-stu-id="9baa7-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="9baa7-138">Přepněte nastavení v oddíle **Markdown: Všechny dostupné jazyky**.</span><span class="sxs-lookup"><span data-stu-id="9baa7-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="9baa7-139">V praxi</span><span class="sxs-lookup"><span data-stu-id="9baa7-139">In action</span></span>

<span data-ttu-id="9baa7-140">Tady vidíte krátkou ukázku této funkce:</span><span class="sxs-lookup"><span data-stu-id="9baa7-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="9baa7-141">[![Dokončování vývojářských jazyků](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9baa7-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
