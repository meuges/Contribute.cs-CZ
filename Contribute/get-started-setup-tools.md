---
title: Instalace nástrojů pro tvorbu obsahu
description: Tento článek vám pomůže stáhnout a nainstalovat klientské nástroje, které jsou potřeba pro Git a úpravy souborů markdownu.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="bb3d1-103">Instalace nástrojů pro tvorbu obsahu</span><span class="sxs-lookup"><span data-stu-id="bb3d1-103">Install content authoring tools</span></span>

<span data-ttu-id="bb3d1-104">Tento článek popisuje postup interaktivní instalace nástrojů klienta Git a Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="bb3d1-105">Instalace [Git pro Windows](https://git-scm.com/download/win)</span><span class="sxs-lookup"><span data-stu-id="bb3d1-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="bb3d1-106">Instalace [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="bb3d1-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="bb3d1-107">Pokud děláte jenom menší změny článku, kroky v tomto článku dělat *nemusíte* a můžete pokračovat přímo na [pracovní postup pro rychlé změny](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="bb3d1-108">Větším přispěvatelům doporučujeme tyto kroky provést, protože vám umožní používat [pracovní postup pro větší nebo dlouho probíhající změny](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="bb3d1-109">I když máte oprávnění k zápisu do hlavního úložiště, *důrazně doporučujeme (a tento průvodce to předpokládá), abyste úložiště rozvětvili a naklonovali* a měli tak oprávnění ke čtení/zápisu pro ukládání navrhovaných změn ve své větvi.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="bb3d1-110">Instalace nástrojů klienta Git ve Windows</span><span class="sxs-lookup"><span data-stu-id="bb3d1-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="bb3d1-111">Nainstalujte nejnovější verzi [nástrojů klienta Git od Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="bb3d1-112">Nainstalujete tím systém správy verzí Git včetně aplikace příkazového řádku Git Bash, která slouží k interakci s místním úložištěm Git.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="bb3d1-113">Pokud před rozhraním příkazového řádku (CLI) dáváte přednost grafickému uživatelskému rozhraní (GUI), k oblíbeným možnostem patří [dostupní klienti GUI od Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop od GitHubu](https://desktop.github.com/) nebo [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="bb3d1-114">Postupujte podle pokynů k instalaci a konfiguraci zvoleného klienta.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="bb3d1-115">V dalším článku [nastavíte místní úložiště Git](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="bb3d1-116">Další materiály pro Git najdete zde: [Terminologie pro Git](https://help.github.com/articles/github-glossary) | [Základy Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Výuka Git a GitHubu](https://help.github.com/articles/good-resources-for-learning-git-and-github/).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="bb3d1-117">Princip editorů Markdownu</span><span class="sxs-lookup"><span data-stu-id="bb3d1-117">Understand Markdown editors</span></span>

<span data-ttu-id="bb3d1-118">Markdown je jednoduchý jazyk využívající značky, který se snadno čte a i snadno učí.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="bb3d1-119">Proto se velmi rychle stal oborovým standardem.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="bb3d1-120">Abyste mohli v Markdownu psát články, doporučujeme nejdřív stáhnout a nainstalovat editor Markdownu.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="bb3d1-121">Preferovaným nástrojem pro editaci Markdownu v Microsoftu je [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="bb3d1-122">Dalším populárním nástrojem pro editaci Markdownu je [Atom](https://atom.io).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="bb3d1-123">Text Markdownu se ukládá do souborů s příponou .md.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="bb3d1-124">Další podrobnosti o tom, jak psát pomocí Markdownu, včetně základů Markdownu a funkcí podporovaných vlastními rozšířeními Markdownu od OPS, najdete v článku [Jak používat Markdown](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="bb3d1-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="bb3d1-125">Visual Studio Code</span></span>

<span data-ttu-id="bb3d1-126">Nástroj [Visual Studio Code](https://code.visualstudio.com/), označované také jako VS Code, je jednoduchý editor, který funguje ve Windows, Linuxu a Macu.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="bb3d1-127">Jeho součástí je integrace Gitu a podpora rozšíření.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="bb3d1-128">Stáhněte a nainstalujte [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="bb3d1-129">Domovská stránka tohoto nástroje by měla správně určit váš operační systém.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="bb3d1-130">Windows</span><span class="sxs-lookup"><span data-stu-id="bb3d1-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="bb3d1-131">Mac</span><span class="sxs-lookup"><span data-stu-id="bb3d1-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="bb3d1-132">Linux</span><span class="sxs-lookup"><span data-stu-id="bb3d1-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="bb3d1-133">Spuštěním příkazu `code .` na příkazovém řádku nebo v prostředí Bash spustíte VS Code a otevřete aktuální složku.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="bb3d1-134">Pokud je aktuální složka součástí místního úložiště Git, dojde k integraci GitHubu v nástroji Visual Studio Code automaticky.</span><span class="sxs-lookup"><span data-stu-id="bb3d1-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bb3d1-135">Další kroky</span><span class="sxs-lookup"><span data-stu-id="bb3d1-135">Next steps</span></span>

<span data-ttu-id="bb3d1-136">Teď jste připraveni [nastavit místní úložiště Git](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="bb3d1-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
