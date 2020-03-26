---
title: Referenční informace k jazyku Markdown pro docs.microsoft.com
description: Informace o funkcích a syntaxi jazyka Markdown používaných na platformě Microsoft Docs
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: c1568264c687ebaf26048f5432fdea7d5132c012
ms.sourcegitcommit: 216ef77ca2cd1eeb31c6c89d96778b178fc0d540
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "80070083"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="d8688-103">Referenční informace k jazyku Markdown pro Docs</span><span class="sxs-lookup"><span data-stu-id="d8688-103">Docs Markdown reference</span></span>

<span data-ttu-id="d8688-104">Tento článek obsahuje referenční informace o psaní jazyka Markdown pro docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="d8688-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="d8688-105">[Markdown](https://daringfireball.net/projects/markdown/) je jednoduchý jazyk využívající značky se syntaxí formátování prostého textu.</span><span class="sxs-lookup"><span data-stu-id="d8688-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="d8688-106">Web Docs podporuje Markdown kompatibilní s verzí [CommonMark](https://commonmark.org/), který k parsování používá parsovací modul [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="d8688-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="d8688-107">Podporuje také vlastní rozšíření Markdownu, které na webu poskytuje bohatší obsah.</span><span class="sxs-lookup"><span data-stu-id="d8688-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="d8688-108">Markdown sice můžete psát v jakémkoliv textovém editoru, doporučujeme ale použít [Visual Studio Code](https://code.visualstudio.com/) s [balíčkem pro vytváření obsahu na webu Docs](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="d8688-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="d8688-109">Balíček pro vytváření obsahu na webu Docs obsahuje nástroje pro úpravy a funkci náhledu, díky které se můžete podívat, jak bude váš článek po publikování na webu Docs vypadat.</span><span class="sxs-lookup"><span data-stu-id="d8688-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="d8688-110">Výstrahy – Note (Poznámka), Tip, Important (Důležité), Caution (Pozor), Warning (Upozornění)</span><span class="sxs-lookup"><span data-stu-id="d8688-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="d8688-111">Výstrahy představují rozšíření Markdownu určené k vytváření blokových citací zobrazovaných na webu docs.microsoft.com s barvami a ikonami, které označují důležitost obsahu.</span><span class="sxs-lookup"><span data-stu-id="d8688-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="d8688-112">Podporují se následující typy výstrah:</span><span class="sxs-lookup"><span data-stu-id="d8688-112">The following alert types are supported:</span></span>

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="d8688-113">Tyto výstrahy vypadají na webu docs.microsoft.com takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="d8688-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="d8688-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="d8688-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="d8688-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d8688-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="d8688-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="d8688-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="d8688-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="d8688-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="d8688-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d8688-119">Ostré závorky</span><span class="sxs-lookup"><span data-stu-id="d8688-119">Angle brackets</span></span>

<span data-ttu-id="d8688-120">Pokud v textu v souboru používáte ostré závorky, třeba k vyznačení zástupného symbolu, musíte pro ně použít kód.</span><span class="sxs-lookup"><span data-stu-id="d8688-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="d8688-121">Jinak je Markdown bude považovat za značku HTML.</span><span class="sxs-lookup"><span data-stu-id="d8688-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d8688-122">Například `<script name>` přepište kódem jako `&lt;script name&gt;` nebo `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="d8688-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="d8688-123">Hranaté závorky nemusí být uvozené v textu formátovaném jako vložený kód ani v blocích kódu.</span><span class="sxs-lookup"><span data-stu-id="d8688-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d8688-124">Apostrofy a uvozovky</span><span class="sxs-lookup"><span data-stu-id="d8688-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d8688-125">Pokud do editoru Markdownu kopírujete z Wordu, může text obsahovat „inteligentní“ (oblé) jednoduché nebo dvojité uvozovky.</span><span class="sxs-lookup"><span data-stu-id="d8688-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d8688-126">Pro ty je nutné použít kód nebo je změnit na základní uvozovky.</span><span class="sxs-lookup"><span data-stu-id="d8688-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d8688-127">Jinak se při publikování souboru zobrazí nějak takto: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="d8688-127">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d8688-128">Pro „inteligentní“ verze interpunkčních znamének se používají tyto kódy:</span><span class="sxs-lookup"><span data-stu-id="d8688-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d8688-129">Levá (otevírací) uvozovka: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="d8688-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d8688-130">Pravá (uzavírací) uvozovka: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="d8688-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d8688-131">Pravá (uzavírací) jednoduchá uvozovka nebo apostrof: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="d8688-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d8688-132">Levá (otevírací) jednoduchá uvozovka (používaná zřídka): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="d8688-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="d8688-133">Blokové citace</span><span class="sxs-lookup"><span data-stu-id="d8688-133">Blockquotes</span></span>

<span data-ttu-id="d8688-134">Blokové citace se vytvářejí pomocí znaku `>`:</span><span class="sxs-lookup"><span data-stu-id="d8688-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="d8688-135">Předchozí příklad se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="d8688-136">This is a blockquote.</span><span class="sxs-lookup"><span data-stu-id="d8688-136">This is a blockquote.</span></span> <span data-ttu-id="d8688-137">It is usually rendered indented and with a different background color.</span><span class="sxs-lookup"><span data-stu-id="d8688-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="d8688-138">Tučné písmo a kurzíva</span><span class="sxs-lookup"><span data-stu-id="d8688-138">Bold and italic text</span></span>

<span data-ttu-id="d8688-139">Pokud chcete text naformátovat jako **tučný**, použijte dvě hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="d8688-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="d8688-140">Pokud chcete text naformátovat jako *kurzívu*, použijte jednu hvězdičku z obou stran:</span><span class="sxs-lookup"><span data-stu-id="d8688-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="d8688-141">Pokud chcete text naformátovat jako ***tučný i kurzívu***, použijte tři hvězdičky z obou stran:</span><span class="sxs-lookup"><span data-stu-id="d8688-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="d8688-142">Fragmenty kódu</span><span class="sxs-lookup"><span data-stu-id="d8688-142">Code snippets</span></span>

<span data-ttu-id="d8688-143">Markdown pro Docs podporuje umístění fragmentů kódu vložením do věty i jako samostatný ohraničený blok mezi větami.</span><span class="sxs-lookup"><span data-stu-id="d8688-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d8688-144">Podrobnosti najdete v tématu věnovaném [přidávání kódu na webu Docs](code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="d8688-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="d8688-145">Sloupce</span><span class="sxs-lookup"><span data-stu-id="d8688-145">Columns</span></span>

<span data-ttu-id="d8688-146">Rozšíření Markdownu pro **sloupce** umožňuje autorům webu Docs přidávat rozložení obsahu založená na sloupcích, která jsou flexibilnější a výkonnější než základní tabulky Markdownu (ty se hodí jen pro skutečná tabulková data).</span><span class="sxs-lookup"><span data-stu-id="d8688-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="d8688-147">Můžete přidat až čtyři sloupce a pomocí volitelného atributu `span` spojit dva nebo více sloupců.</span><span class="sxs-lookup"><span data-stu-id="d8688-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="d8688-148">Syntaxe pro sloupce je následující:</span><span class="sxs-lookup"><span data-stu-id="d8688-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="d8688-149">Sloupce by měly obsahovat jen základní Markdown, a to včetně obrázků.</span><span class="sxs-lookup"><span data-stu-id="d8688-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="d8688-150">Záhlaví, tabulky, tabulátory ani další složité struktury nevkládejte.</span><span class="sxs-lookup"><span data-stu-id="d8688-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="d8688-151">Mimo sloupec nesmí být na řádku žádný obsah.</span><span class="sxs-lookup"><span data-stu-id="d8688-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="d8688-152">Tento Markdown například vytvoří jeden sloupec, který pokrývá dvě šířky sloupců, a jeden standardní sloupec (bez `span`):</span><span class="sxs-lookup"><span data-stu-id="d8688-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="d8688-153">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="d8688-154">**This is a 2-span column with lots of text.**</span><span class="sxs-lookup"><span data-stu-id="d8688-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="d8688-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="d8688-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="d8688-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="d8688-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="d8688-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="d8688-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="d8688-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="d8688-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="d8688-159">**This is a single-span column with an image in it.**</span><span class="sxs-lookup"><span data-stu-id="d8688-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="d8688-161">Nadpisy</span><span class="sxs-lookup"><span data-stu-id="d8688-161">Headings</span></span>

<span data-ttu-id="d8688-162">Web Docs podporuje šest úrovní nadpisů Markdownu:</span><span class="sxs-lookup"><span data-stu-id="d8688-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="d8688-163">Mezi posledním symbolem `#` a textem nadpisu musí být mezera.</span><span class="sxs-lookup"><span data-stu-id="d8688-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="d8688-164">Každý soubor Markdownu musí mít právě jeden nadpis H1.</span><span class="sxs-lookup"><span data-stu-id="d8688-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="d8688-165">Nadpis H1 musí být prvním obsahem v souboru za blokem metadat YML.</span><span class="sxs-lookup"><span data-stu-id="d8688-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="d8688-166">Nadpisy H2 se automaticky objeví v pravé navigační nabídce publikovaného souboru.</span><span class="sxs-lookup"><span data-stu-id="d8688-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="d8688-167">Nadpisy nižších úrovní nikoliv, takže nadpisy H2 můžete strategicky použít k navigaci čtenářů v obsahu.</span><span class="sxs-lookup"><span data-stu-id="d8688-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="d8688-168">Nadpisy HTML (například `<h1>`) se nedoporučují a v některých případech způsobí upozornění sestavení.</span><span class="sxs-lookup"><span data-stu-id="d8688-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="d8688-169">Odkazy na jednotlivé nadpisy v souboru můžete realizovat pomocí [odkazů na záložky](how-to-write-links.md#links-to-anchors).</span><span class="sxs-lookup"><span data-stu-id="d8688-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#links-to-anchors).</span></span>

## <a name="html"></a><span data-ttu-id="d8688-170">HTML</span><span class="sxs-lookup"><span data-stu-id="d8688-170">HTML</span></span>

<span data-ttu-id="d8688-171">Ačkoli Markdown podporuje vložený kód HTML, pro publikování na webu Docs se HTML nedoporučuje a až na omezený seznam hodnot způsobí chyby a upozornění při sestavování.</span><span class="sxs-lookup"><span data-stu-id="d8688-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> 

## <a name="images"></a><span data-ttu-id="d8688-172">Obrázky</span><span class="sxs-lookup"><span data-stu-id="d8688-172">Images</span></span>

<span data-ttu-id="d8688-173">Pro obrázky se standardně podporují tyto typy souborů:</span><span class="sxs-lookup"><span data-stu-id="d8688-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="d8688-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="d8688-174">.jpg</span></span>
- <span data-ttu-id="d8688-175">.png</span><span class="sxs-lookup"><span data-stu-id="d8688-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="d8688-176">Standardní konceptuální obrázky (výchozí Markdown)</span><span class="sxs-lookup"><span data-stu-id="d8688-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="d8688-177">Základní syntaxe Markdownu pro vložení obrázku je následující:</span><span class="sxs-lookup"><span data-stu-id="d8688-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="d8688-178">`<alt text>` je stručný popis obrázku a `<folder path>` je relativní cesta k obrázku.</span><span class="sxs-lookup"><span data-stu-id="d8688-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="d8688-179">Alternativní text se vyžaduje pro čtečky obrazovky, které používají lidé s vadami zraku.</span><span class="sxs-lookup"><span data-stu-id="d8688-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="d8688-180">Je rovněž užitečný, pokud je na webu chyba a obrázek se nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="d8688-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="d8688-181">Podtržítka se v alternativním textu zobrazí správně jen tehdy, pokud je uvedete předponou zpětného lomítka (`\_`).</span><span class="sxs-lookup"><span data-stu-id="d8688-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="d8688-182">Jako alternativní text ale nepoužívejte zkopírovaný název souborů.</span><span class="sxs-lookup"><span data-stu-id="d8688-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="d8688-183">Například namísto tohoto:</span><span class="sxs-lookup"><span data-stu-id="d8688-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d8688-184">Napište toto:</span><span class="sxs-lookup"><span data-stu-id="d8688-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="d8688-185">Standardní konceptuální obrázky (Markdown pro Docs)</span><span class="sxs-lookup"><span data-stu-id="d8688-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="d8688-186">Vlastní rozšíření `:::image:::` pro web Docs podporuje standardní obrázky, složité obrázky a ikony.</span><span class="sxs-lookup"><span data-stu-id="d8688-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="d8688-187">I když u standardních obrázků bude i nadále fungovat starší syntaxe Markdownu, doporučujeme použít toto nové rozšíření, protože podporuje výkonnější funkce, jako je specifikace rozsahu lokalizace, která se liší od nadřazeného tématu.</span><span class="sxs-lookup"><span data-stu-id="d8688-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="d8688-188">V budoucnu budou k dispozici i další pokročilé funkce, například možnost výběru ze sdílené galerie obrázků namísto specifikace místního obrázku.</span><span class="sxs-lookup"><span data-stu-id="d8688-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="d8688-189">Nová syntaxe vypadá takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="d8688-190">V případě výchozího `type="content"` se vyžaduje `source` i `alt-text`.</span><span class="sxs-lookup"><span data-stu-id="d8688-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="d8688-191">Složité obrázky s dlouhými popisy</span><span class="sxs-lookup"><span data-stu-id="d8688-191">Complex images with long descriptions</span></span>

<span data-ttu-id="d8688-192">Díky tomuto rozšíření můžete také přidávat obrázky s dlouhým popisem, který přečte čtečka obrazovky, ale vizuálně se na publikované stránce nevykreslí.</span><span class="sxs-lookup"><span data-stu-id="d8688-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="d8688-193">Dlouhé popisy představují požadavek na přístupnost u složitých obrázků (například grafů).</span><span class="sxs-lookup"><span data-stu-id="d8688-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="d8688-194">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="d8688-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="d8688-195">V případě `type="complex"` se vyžaduje `source`, `alt-text`, dlouhý popis i značka `:::image-end:::`.</span><span class="sxs-lookup"><span data-stu-id="d8688-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="d8688-196">Specifikace rozsahu lokalizace</span><span class="sxs-lookup"><span data-stu-id="d8688-196">Specifying loc-scope</span></span>

<span data-ttu-id="d8688-197">Někdy se rozsah lokalizace obrázku liší od rozsahu článku nebo modulu, který ho obsahuje.</span><span class="sxs-lookup"><span data-stu-id="d8688-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="d8688-198">To může způsobit potíže uživatelům z různých částí světa – například pokud se snímek obrazovky s produktem omylem lokalizuje do jazyka, v němž není produkt k dispozici.</span><span class="sxs-lookup"><span data-stu-id="d8688-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="d8688-199">Chcete-li tomu zabránit, můžete v obrázcích typu `content` a `complex` zadat volitelný atribut `loc-scope`.</span><span class="sxs-lookup"><span data-stu-id="d8688-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="d8688-200">Ikony</span><span class="sxs-lookup"><span data-stu-id="d8688-200">Icons</span></span>

<span data-ttu-id="d8688-201">Rozšíření pro obrázky podporuje ikony, které neobsahují alternativní text a slouží jako dekorativní obrázky.</span><span class="sxs-lookup"><span data-stu-id="d8688-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="d8688-202">Syntaxe pro ikony je následující:</span><span class="sxs-lookup"><span data-stu-id="d8688-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="d8688-203">V případě výchozího `type="icon"` je potřeba specifikovat jen `source`.</span><span class="sxs-lookup"><span data-stu-id="d8688-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="d8688-204">Zahrnuté soubory Markdownu</span><span class="sxs-lookup"><span data-stu-id="d8688-204">Included Markdown files</span></span>

<span data-ttu-id="d8688-205">Tam, kde se mají soubory Markdownu opakovat ve více článcích, můžete použít soubor k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="d8688-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="d8688-206">Tato funkce říká webu Docs, že má v době sestavování nahradit odkaz obsahem zahrnutého souboru.</span><span class="sxs-lookup"><span data-stu-id="d8688-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="d8688-207">Soubory k zahrnutí můžete používat dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="d8688-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="d8688-208">Vložení: Umožňuje znovu použít běžný vložený fragment textu v rámci věty.</span><span class="sxs-lookup"><span data-stu-id="d8688-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="d8688-209">Blok: Umožňuje znovu použít celý soubor Markdownu jako blok vnořený do oddílu článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="d8688-210">Soubor k zahrnutí typu Vložení nebo Blok je soubor Markdownu (.md).</span><span class="sxs-lookup"><span data-stu-id="d8688-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="d8688-211">Ty mohou obsahovat jakýkoli platný Markdown.</span><span class="sxs-lookup"><span data-stu-id="d8688-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="d8688-212">Zahrnuté soubory se obvykle nachází ve společném podadresáři *includes* v kořenovém adresáři úložiště.</span><span class="sxs-lookup"><span data-stu-id="d8688-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="d8688-213">Při publikování článku se do něho zahrnutý soubor bezproblémově integruje.</span><span class="sxs-lookup"><span data-stu-id="d8688-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="d8688-214">Zahrnutá syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8688-214">Includes syntax</span></span>

<span data-ttu-id="d8688-215">Soubor typu Blok má vlastní řádek:</span><span class="sxs-lookup"><span data-stu-id="d8688-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="d8688-216">Soubor typu Vložení je součástí řádku:</span><span class="sxs-lookup"><span data-stu-id="d8688-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="d8688-217">`<title>` představuje název souboru a `<filepath>` relativní cestu k souboru.</span><span class="sxs-lookup"><span data-stu-id="d8688-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="d8688-218">`INCLUDE` musí být velkými písmeny a před `<title>` se musí nacházet čárka.</span><span class="sxs-lookup"><span data-stu-id="d8688-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="d8688-219">Tady jsou požadavky a důležité informace týkající se souborů k zahrnutí:</span><span class="sxs-lookup"><span data-stu-id="d8688-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="d8688-220">Zahrnutí typu Blok používejte na výrazná množství obsahu – jeden nebo dva odstavce, sdílený postup nebo sdílený oddíl.</span><span class="sxs-lookup"><span data-stu-id="d8688-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d8688-221">Nepoužívejte je na nic menšího než větu.</span><span class="sxs-lookup"><span data-stu-id="d8688-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d8688-222">Zahrnuté soubory se nevykreslí v zobrazení článku vykresleném GitHubem, protože závisejí na rozšířeních pro Docs.</span><span class="sxs-lookup"><span data-stu-id="d8688-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="d8688-223">Vykreslí se až po zveřejnění.</span><span class="sxs-lookup"><span data-stu-id="d8688-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d8688-224">Dbejte na to, aby byl všechen text v souboru k zahrnutí napsaný v úplných větách nebo frázích, které nezávisí na předchozím nebo následujícím textu v článku, který na daný soubor odkazuje.</span><span class="sxs-lookup"><span data-stu-id="d8688-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="d8688-225">Ignorováním tohoto pravidla vznikne v článku nepřeložitelný řetězec.</span><span class="sxs-lookup"><span data-stu-id="d8688-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="d8688-226">Nevkládejte zahrnuté soubory do jiných zahrnutých souborů.</span><span class="sxs-lookup"><span data-stu-id="d8688-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="d8688-227">Multimediální soubory umístěte do složky s multimédii konkrétního podadresáře zahrnutí, třeba do složky `<repo>` */includes/media*.</span><span class="sxs-lookup"><span data-stu-id="d8688-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="d8688-228">Adresář *media* nesmí ve svém kořenu obsahovat obrázky.</span><span class="sxs-lookup"><span data-stu-id="d8688-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="d8688-229">Pokud soubor k zahrnutí obrázky nemá, pak odpovídající adresář *media* není potřeba.</span><span class="sxs-lookup"><span data-stu-id="d8688-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="d8688-230">Stejně jako v případě běžných článků nesdílejte multimédia mezi soubory zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="d8688-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d8688-231">Pro každé zahrnutí a článek použijte samostatný soubor s jedinečným názvem.</span><span class="sxs-lookup"><span data-stu-id="d8688-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="d8688-232">Multimediální soubor uložte do složky multimédií spojené se zahrnutím.</span><span class="sxs-lookup"><span data-stu-id="d8688-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="d8688-233">Nepoužívejte zahrnutí jako jediný obsah článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="d8688-234">Zahrnutí mají být doplněním obsahu ve zbytku článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="d8688-235">Odkazy</span><span class="sxs-lookup"><span data-stu-id="d8688-235">Links</span></span>

<span data-ttu-id="d8688-236">Informace o syntaxi odkazů najdete v tématu [Použití odkazů v dokumentaci](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="d8688-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="d8688-237">Seznamy (číslované, odrážkové, kontrolní)</span><span class="sxs-lookup"><span data-stu-id="d8688-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="d8688-238">Číslovaný seznam</span><span class="sxs-lookup"><span data-stu-id="d8688-238">Numbered list</span></span>

<span data-ttu-id="d8688-239">Při vytváření číslovaného seznamu můžete všude použít jedničky (1).</span><span class="sxs-lookup"><span data-stu-id="d8688-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="d8688-240">Ty se při publikování zobrazí jako sekvenční seznam ve vzestupném pořadí.</span><span class="sxs-lookup"><span data-stu-id="d8688-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="d8688-241">Kvůli lepší čitelnosti zdrojového kódu můžete seznamy inkrementovat ručně.</span><span class="sxs-lookup"><span data-stu-id="d8688-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="d8688-242">Nepoužívejte v seznamech ani vnořených seznamech písmena.</span><span class="sxs-lookup"><span data-stu-id="d8688-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="d8688-243">Při publikování na webu Docs se nezobrazí správně. Vnořené seznamy používající čísla se při publikování zobrazí jako malá písmena.</span><span class="sxs-lookup"><span data-stu-id="d8688-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="d8688-244">Například:</span><span class="sxs-lookup"><span data-stu-id="d8688-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="d8688-245">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-245">This renders as follows:</span></span>

1. <span data-ttu-id="d8688-246">This is</span><span class="sxs-lookup"><span data-stu-id="d8688-246">This is</span></span>
1. <span data-ttu-id="d8688-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="d8688-247">a parent numbered list</span></span>
   1. <span data-ttu-id="d8688-248">and this is</span><span class="sxs-lookup"><span data-stu-id="d8688-248">and this is</span></span>
   1. <span data-ttu-id="d8688-249">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="d8688-249">a nested numbered list</span></span>
1. <span data-ttu-id="d8688-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="d8688-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="d8688-251">Seznam s odrážkami</span><span class="sxs-lookup"><span data-stu-id="d8688-251">Bulleted list</span></span>

<span data-ttu-id="d8688-252">Pokud chcete vytvořit seznam s odrážkami, použijte na začátku každého řádku znak `-` nebo `*` následovaný mezerou:</span><span class="sxs-lookup"><span data-stu-id="d8688-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="d8688-253">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-253">This renders as follows:</span></span>

- <span data-ttu-id="d8688-254">This is</span><span class="sxs-lookup"><span data-stu-id="d8688-254">This is</span></span>
- <span data-ttu-id="d8688-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="d8688-255">a parent bulleted list</span></span>
  - <span data-ttu-id="d8688-256">and this is</span><span class="sxs-lookup"><span data-stu-id="d8688-256">and this is</span></span>
  - <span data-ttu-id="d8688-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="d8688-257">a nested bulleted list</span></span>
- <span data-ttu-id="d8688-258">All done!</span><span class="sxs-lookup"><span data-stu-id="d8688-258">All done!</span></span>

<span data-ttu-id="d8688-259">Ať už se rozhodnete pro `-` nebo `*`, používejte jeden typ syntaxe konzistentně v rámci celého článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="d8688-260">Kontrolní seznam</span><span class="sxs-lookup"><span data-stu-id="d8688-260">Checklist</span></span>

<span data-ttu-id="d8688-261">Kontrolní seznamy jsou webu Docs dostupné jen při použití vlastního rozšíření Markdownu:</span><span class="sxs-lookup"><span data-stu-id="d8688-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="d8688-262">Tento příklad se na webu Docs zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="d8688-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="d8688-263">List item 1</span></span>
> * <span data-ttu-id="d8688-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="d8688-264">List item 2</span></span>
> * <span data-ttu-id="d8688-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="d8688-265">List item 3</span></span>

<span data-ttu-id="d8688-266">Ke shrnutí probírané látky nebo k její rekapitulaci použijte kontrolní seznamy, které přidáte na začátek nebo na konec článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="d8688-267">Nepřidávejte do svých článků náhodné kontrolní seznamy.</span><span class="sxs-lookup"><span data-stu-id="d8688-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="d8688-268">Akce dalšího kroku</span><span class="sxs-lookup"><span data-stu-id="d8688-268">Next step action</span></span>

<span data-ttu-id="d8688-269">K přidání tlačítka akce dalšího kroku na stránky Docs můžete použít vlastní rozšíření.</span><span class="sxs-lookup"><span data-stu-id="d8688-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="d8688-270">Syntaxe je následující:</span><span class="sxs-lookup"><span data-stu-id="d8688-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="d8688-271">Například:</span><span class="sxs-lookup"><span data-stu-id="d8688-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="d8688-272">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="d8688-273">Learn about adding code to articles</span><span class="sxs-lookup"><span data-stu-id="d8688-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="d8688-274">V akci dalšího kroku můžete použít jakýkoli podporovaný odkaz včetně odkazu Markdownu na jinou webovou stránku.</span><span class="sxs-lookup"><span data-stu-id="d8688-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="d8688-275">Ve většině případů bude odkaz na další akci relativním odkazem na jiný soubor ve stejné sadě dokumentace.</span><span class="sxs-lookup"><span data-stu-id="d8688-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="d8688-276">Nelokalizované řetězce</span><span class="sxs-lookup"><span data-stu-id="d8688-276">Non-localized strings</span></span>

<span data-ttu-id="d8688-277">Pomocí vlastního rozšíření Markdownu `no-loc` můžete identifikovat řetězce obsahu, které má proces lokalizace ignorovat.</span><span class="sxs-lookup"><span data-stu-id="d8688-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="d8688-278">Ve všech příslušných řetězcích se budou rozlišovat velká a malá písmena, což znamená, že musí být specifikované naprosto přesně, aby se mohly ignorovat.</span><span class="sxs-lookup"><span data-stu-id="d8688-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="d8688-279">Pokud chcete řetězec označit jako nelokalizovaný, použijte tuto syntaxi:</span><span class="sxs-lookup"><span data-stu-id="d8688-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="d8688-280">Například v následujícím příkladu se během procesu lokalizace bude ignorovat jen jedna instance `Document`:</span><span class="sxs-lookup"><span data-stu-id="d8688-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="d8688-281">K uvození speciálních znaků použijte `\`:</span><span class="sxs-lookup"><span data-stu-id="d8688-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="d8688-282">Pomocí metadat v hlavičce YAML můžete také označit jako nelokalizované všechny instance řetězce v aktuálním souboru Markdownu:</span><span class="sxs-lookup"><span data-stu-id="d8688-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="d8688-283">Nelokalizovaná metadata se v souboru *docfx.json* nepodporují jako globální metadata.</span><span class="sxs-lookup"><span data-stu-id="d8688-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="d8688-284">Lokalizační kanál nečte soubor *docfx.json*, takže je potřeba tato metadata přidat do každého ze zdrojových souborů.</span><span class="sxs-lookup"><span data-stu-id="d8688-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="d8688-285">V následujícím příkladu bude proces lokalizace ignorovat slovo `title` jak v `Document` metadat, tak i v hlavičce Markdownu.</span><span class="sxs-lookup"><span data-stu-id="d8688-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="d8688-286">V `description` metadat a v hlavním obsahu Markdownu se slovo `document` lokalizuje, protože nezačíná velkým písmenem `D`.</span><span class="sxs-lookup"><span data-stu-id="d8688-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="d8688-287">Voliče</span><span class="sxs-lookup"><span data-stu-id="d8688-287">Selectors</span></span>

<span data-ttu-id="d8688-288">Voliče jsou prvky uživatelského rozhraní, které umožňují uživateli přepínat mezi různými variantami jednoho článku.</span><span class="sxs-lookup"><span data-stu-id="d8688-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="d8688-289">Využívají se v některých sadách dokumentace k řešení rozdílné implementace napříč technologiemi a platformami.</span><span class="sxs-lookup"><span data-stu-id="d8688-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d8688-290">Voliče se zpravidla nejvíce hodí pro obsah určený pro vývojářské mobilní platformy.</span><span class="sxs-lookup"><span data-stu-id="d8688-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="d8688-291">Protože do každého souboru článku ve výběru přijde stejný Markdown voliče, doporučujeme umístit volič pro článek do souboru k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="d8688-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="d8688-292">Pak můžete na daný soubor k zahrnutí odkázat ve všech souborech článků, které daný volič používají.</span><span class="sxs-lookup"><span data-stu-id="d8688-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="d8688-293">K dispozici jsou dva typy voličů – jednoduchý a vícenásobný volič.</span><span class="sxs-lookup"><span data-stu-id="d8688-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="d8688-294">Jeden selektor</span><span class="sxs-lookup"><span data-stu-id="d8688-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="d8688-295">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="d8688-304">Vícenásobný selektor</span><span class="sxs-lookup"><span data-stu-id="d8688-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="d8688-305">...se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platforma" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows Universal C# | .NET)](how-to-write-links.md)
> - [(Windows Universal C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="d8688-318">Dolní index a horní index</span><span class="sxs-lookup"><span data-stu-id="d8688-318">Subscript and superscript</span></span>

<span data-ttu-id="d8688-319">Dolní a horní index používejte jen tam, kde jsou potřeba k zajištění technické přesnosti, například v článcích o matematických vzorcích.</span><span class="sxs-lookup"><span data-stu-id="d8688-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="d8688-320">Nepoužívejte je v nestandardních stylech, jako jsou poznámky pod čarou.</span><span class="sxs-lookup"><span data-stu-id="d8688-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="d8688-321">V obou případech použijte HTML:</span><span class="sxs-lookup"><span data-stu-id="d8688-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="d8688-322">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-322">This renders as follows:</span></span>

<span data-ttu-id="d8688-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="d8688-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="d8688-324">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-324">This renders as follows:</span></span>

<span data-ttu-id="d8688-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="d8688-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="d8688-326">Tabulky</span><span class="sxs-lookup"><span data-stu-id="d8688-326">Tables</span></span>

<span data-ttu-id="d8688-327">Nejjednodušším způsobem, jak v Markdownu vytvořit tabulku, je použít svislé čáry a řádky.</span><span class="sxs-lookup"><span data-stu-id="d8688-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="d8688-328">Pokud chcete vytvořit standardní tabulku se záhlavím, za první řádek vložte čárkovaný řádek:</span><span class="sxs-lookup"><span data-stu-id="d8688-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="d8688-329">Toto se zobrazí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-329">This renders as follows:</span></span>

|<span data-ttu-id="d8688-330">This is</span><span class="sxs-lookup"><span data-stu-id="d8688-330">This is</span></span>   |<span data-ttu-id="d8688-331">a simple</span><span class="sxs-lookup"><span data-stu-id="d8688-331">a simple</span></span>   |<span data-ttu-id="d8688-332">table header</span><span class="sxs-lookup"><span data-stu-id="d8688-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="d8688-333">table</span><span class="sxs-lookup"><span data-stu-id="d8688-333">table</span></span>     |<span data-ttu-id="d8688-334">data</span><span class="sxs-lookup"><span data-stu-id="d8688-334">data</span></span>       |<span data-ttu-id="d8688-335">here</span><span class="sxs-lookup"><span data-stu-id="d8688-335">here</span></span>        |
|<span data-ttu-id="d8688-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="d8688-336">it doesn't</span></span>|<span data-ttu-id="d8688-337">actually</span><span class="sxs-lookup"><span data-stu-id="d8688-337">actually</span></span>   |<span data-ttu-id="d8688-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="d8688-338">have to line up nicely!</span></span>||

<span data-ttu-id="d8688-339">Sloupce můžete zarovnat pomocí dvojtečky:</span><span class="sxs-lookup"><span data-stu-id="d8688-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d8688-340">Se vykreslí takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-340">Renders as follows:</span></span>

| <span data-ttu-id="d8688-341">Fun</span><span class="sxs-lookup"><span data-stu-id="d8688-341">Fun</span></span>                  | <span data-ttu-id="d8688-342">With</span><span class="sxs-lookup"><span data-stu-id="d8688-342">With</span></span>                 | <span data-ttu-id="d8688-343">Tabulky</span><span class="sxs-lookup"><span data-stu-id="d8688-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d8688-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d8688-344">left-aligned column</span></span>  | <span data-ttu-id="d8688-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d8688-345">right-aligned column</span></span> | <span data-ttu-id="d8688-346">centered column</span><span class="sxs-lookup"><span data-stu-id="d8688-346">centered column</span></span> |
| <span data-ttu-id="d8688-347">$100</span><span class="sxs-lookup"><span data-stu-id="d8688-347">$100</span></span>                 | <span data-ttu-id="d8688-348">$100</span><span class="sxs-lookup"><span data-stu-id="d8688-348">$100</span></span>                 | <span data-ttu-id="d8688-349">$100</span><span class="sxs-lookup"><span data-stu-id="d8688-349">$100</span></span>            |
| <span data-ttu-id="d8688-350">$10</span><span class="sxs-lookup"><span data-stu-id="d8688-350">$10</span></span>                  | <span data-ttu-id="d8688-351">$10</span><span class="sxs-lookup"><span data-stu-id="d8688-351">$10</span></span>                  | <span data-ttu-id="d8688-352">$10</span><span class="sxs-lookup"><span data-stu-id="d8688-352">$10</span></span>             |
| <span data-ttu-id="d8688-353">$1</span><span class="sxs-lookup"><span data-stu-id="d8688-353">$1</span></span>                   | <span data-ttu-id="d8688-354">$1</span><span class="sxs-lookup"><span data-stu-id="d8688-354">$1</span></span>                   | <span data-ttu-id="d8688-355">$1</span><span class="sxs-lookup"><span data-stu-id="d8688-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="d8688-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span><span class="sxs-lookup"><span data-stu-id="d8688-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="d8688-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="d8688-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="d8688-358">Konce řádků ve slovech v libovolných buňkách tabulky</span><span class="sxs-lookup"><span data-stu-id="d8688-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="d8688-359">Dlouhá slova v markdownové tabulce můžou způsobit, že bude tabulka zasahovat do navigace napravo a stane se nečitelnou.</span><span class="sxs-lookup"><span data-stu-id="d8688-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="d8688-360">Tento problém vyřešíte tak, že webu Docs umožníte při zobrazování automaticky vkládat konce řádků do slov tam, kde je to potřeba.</span><span class="sxs-lookup"><span data-stu-id="d8688-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="d8688-361">Tabulku stačí zalomit pomocí vlastní třídy `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="d8688-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="d8688-362">Toto je ukázka tabulky v Markdownu se třemi řádky, která se zalomí pomocí `div` s názvem třídy `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="d8688-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="d8688-363">Zobrazí se takto:</span><span class="sxs-lookup"><span data-stu-id="d8688-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="d8688-364">Name</span><span class="sxs-lookup"><span data-stu-id="d8688-364">Name</span></span>|<span data-ttu-id="d8688-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8688-365">Syntax</span></span>|<span data-ttu-id="d8688-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="d8688-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="d8688-367">Description</span><span class="sxs-lookup"><span data-stu-id="d8688-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="d8688-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="d8688-368">Quiet</span></span>|<span data-ttu-id="d8688-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="d8688-369">/quiet</span></span>|<span data-ttu-id="d8688-370">Yes</span><span class="sxs-lookup"><span data-stu-id="d8688-370">Yes</span></span>|<span data-ttu-id="d8688-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="d8688-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="d8688-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="d8688-372">NoRestart</span></span>|<span data-ttu-id="d8688-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="d8688-373">/norestart</span></span>|<span data-ttu-id="d8688-374">No</span><span class="sxs-lookup"><span data-stu-id="d8688-374">No</span></span>|<span data-ttu-id="d8688-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="d8688-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="d8688-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="d8688-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="d8688-377">Help</span><span class="sxs-lookup"><span data-stu-id="d8688-377">Help</span></span>|<span data-ttu-id="d8688-378">/help</span><span class="sxs-lookup"><span data-stu-id="d8688-378">/help</span></span>|<span data-ttu-id="d8688-379">No</span><span class="sxs-lookup"><span data-stu-id="d8688-379">No</span></span>|<span data-ttu-id="d8688-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="d8688-380">Provides help and quick reference.</span></span> <span data-ttu-id="d8688-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="d8688-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="d8688-382">Konce řádků ve slovech v buňkách druhého sloupce tabulky</span><span class="sxs-lookup"><span data-stu-id="d8688-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="d8688-383">Je možné, že budete potřebovat automaticky vkládat konce řádků do slov jen ve druhém sloupci tabulky.</span><span class="sxs-lookup"><span data-stu-id="d8688-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="d8688-384">Pokud chcete konce řádků omezit právě jen na druhý sloupec, použijte třídu `mx-tdCol2BreakAll` pomocí syntaxe obálky `div`, jak bylo uvedeno dříve.</span><span class="sxs-lookup"><span data-stu-id="d8688-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="d8688-385">Tabulky matic dat</span><span class="sxs-lookup"><span data-stu-id="d8688-385">Data matrix tables</span></span>

<span data-ttu-id="d8688-386">Tabulka matic dat má záhlaví a vážený první sloupec. Výsledkem je matice s prázdnou buňkou v levém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="d8688-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="d8688-387">Dokumentace (Docs) obsahuje vlastní Markdown pro tabulky matic dat:</span><span class="sxs-lookup"><span data-stu-id="d8688-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="d8688-388">Každá položka v prvním sloupci musí být naformátovaná jako tučná (`**bold**`); jinak tabulky nebudou přístupné pro čtečky obrazovky ani platné pro dokumentaci (Docs).</span><span class="sxs-lookup"><span data-stu-id="d8688-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="d8688-389">Tabulky HTML</span><span class="sxs-lookup"><span data-stu-id="d8688-389">HTML Tables</span></span>

<span data-ttu-id="d8688-390">Tabulky HTML se na webu docs.microsoft.com nedoporučují.</span><span class="sxs-lookup"><span data-stu-id="d8688-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="d8688-391">Nejsou ve zdrojovém kódu čitelné pro člověka, což je klíčový princip Markdownu.</span><span class="sxs-lookup"><span data-stu-id="d8688-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
