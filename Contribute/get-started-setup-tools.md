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
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>Instalace nástrojů pro tvorbu obsahu

Tento článek popisuje postup interaktivní instalace nástrojů klienta Git a Visual Studio Code.
> [!div class="checklist"]
> * Instalace [Git pro Windows](https://git-scm.com/download/win)
> * Instalace [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> Pokud provádíte jenom menší změny článku, kroky v tomto článku dělat *nemusíte* a můžete pokračovat přímo na [pracovní postup pro menší/občasné změny](light-workflow.md).
>
> Větším přispěvatelům doporučujeme tyto kroky provést, protože vám umožní používat [pracovní postup pro větší nebo dlouho probíhající změny](full-workflow.md). I když máte oprávnění k zápisu do hlavního úložiště, *důrazně doporučujeme (a tento průvodce to předpokládá), abyste úložiště rozvětvili a naklonovali* a měli tak oprávnění ke čtení/zápisu pro ukládání navrhovaných změn ve své větvi.

## <a name="install-git-client-tools-on-windows"></a>Instalace nástrojů klienta Git ve Windows

 Nainstalujte nejnovější verzi [nástrojů klienta Git od Software Freedom Conservancy](https://git-scm.com/download/). Nainstalujete tím systém správy verzí Git včetně aplikace příkazového řádku Git Bash, která slouží k interakci s místním úložištěm Git.

Pokud před rozhraním příkazového řádku (CLI) dáváte přednost grafickému uživatelskému rozhraní (GUI), k oblíbeným možnostem patří [dostupní klienti GUI od Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop od GitHubu](https://desktop.github.com/) nebo [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx).

Postupujte podle pokynů k instalaci a konfiguraci zvoleného klienta.

V dalším článku [nastavíte místní úložiště Git](get-started-setup-local.md).

   Další materiály pro Git najdete zde: [Terminologie pro Git](https://help.github.com/articles/github-glossary) | [Základy Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Výuka Git a GitHubu](https://help.github.com/articles/good-resources-for-learning-git-and-github/).

## <a name="understand-markdown-editors"></a>Princip editorů Markdownu

Markdown je jednoduchý jazyk využívající značky, který se snadno čte a i snadno učí. Proto se velmi rychle stal oborovým standardem. Abyste mohli v Markdownu psát články, doporučujeme nejdřív stáhnout a nainstalovat editor Markdownu.  Preferovaným nástrojem pro editaci Markdownu v Microsoftu je [Visual Studio Code](https://code.visualstudio.com/). Dalším populárním nástrojem pro editaci Markdownu je [Atom](https://atom.io).

Text Markdownu se ukládá do souborů s příponou .md.

Další podrobnosti o tom, jak psát pomocí Markdownu, včetně základů Markdownu a funkcí podporovaných vlastními rozšířeními Markdownu od OPS, najdete v článku [Jak používat Markdown](how-to-write-use-markdown.md).

## <a name="visual-studio-code"></a>Visual Studio Code

Nástroj [Visual Studio Code](https://code.visualstudio.com/), označované také jako VS Code, je jednoduchý editor, který funguje ve Windows, Linuxu a Macu. Jeho součástí je integrace Gitu a podpora rozšíření.

Stáhněte a nainstalujte [VS Code](https://code.visualstudio.com/). Domovská stránka tohoto nástroje by měla správně určit váš operační systém.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Spuštěním příkazu `code .` na příkazovém řádku nebo v prostředí Bash spustíte VS Code a otevřete aktuální složku. Pokud je aktuální složka součástí místního úložiště Git, dojde k integraci GitHubu v nástroji Visual Studio Code automaticky.

## <a name="next-steps"></a>Další kroky

Teď jste připraveni [nastavit místní úložiště Git](get-started-setup-local.md).
