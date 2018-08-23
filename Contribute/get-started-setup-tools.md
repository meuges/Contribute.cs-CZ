---
title: Instalace nástrojů pro tvorbu obsahu
description: Tento článek vám pomůže stáhnout a nainstalovat klientské nástroje, které jsou potřeba pro Git a úpravy souborů markdownu.
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.openlocfilehash: 9f22a416810711c076645a9483f022112a3a7642
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251463"
---
# <a name="install-content-authoring-tools"></a>Instalace nástrojů pro tvorbu obsahu

Tento článek popisuje postup interaktivní instalace nástrojů klienta Git a Visual Studio Code.
> [!div class="checklist"]
> * Instalace [Gitu](https://git-scm.com/)
> * Instalace [Visual Studio Code](https://code.visualstudio.com/)
> * Instalace [balíčku pro vytváření obsahu na webu Docs](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> Pokud děláte jenom menší změny článku, kroky v tomto článku dělat *nemusíte* a můžete pokračovat přímo na [pracovní postup pro rychlé změny](index.md#quick-edits-to-existing-documents).
>
> Větším přispěvatelům doporučujeme tyto kroky provést, protože vám umožní používat [pracovní postup pro větší nebo dlouho probíhající změny](how-to-write-workflows-major.md). I když máte oprávnění k zápisu do hlavního úložiště, *důrazně doporučujeme (a tento průvodce to předpokládá), abyste úložiště rozvětvili a naklonovali* a měli tak oprávnění ke čtení/zápisu pro ukládání navrhovaných změn ve své větvi.

## <a name="install-git-client-tools"></a>Instalace nástrojů klienta Git 

 Nainstalujte nejnovější verzi [nástrojů klienta Git od Software Freedom Conservancy](https://git-scm.com/download/) pro svou platformu. 

* [Git pro Windows](https://git-scm.com/download/win) Tím nainstalujete systém správy verzí Git včetně aplikace příkazového řádku Git Bash, která slouží k interakci s místním úložištěm Git.
* Git pro Mac se dodává jakou součást nástrojů příkazového řádku Xcode. Jednoduše spusťte `git` z příkazového řádku. V případě potřeby budete vyzváni k instalaci nástrojů příkazového řádku. [Git pro Mac](https://git-scm.com/download/mac) si také můžete stáhnout od Software Freedom Conservancy.
* [Git pro Linux a Unix](https://git-scm.com/download/linux)

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

## <a name="docs-authoring-pack"></a>Balíček pro vytváření obsahu na webu Docs
Nainstalujte balíček pro vytváření obsahu na webu Docs pro Visual Studio Code. Tato sada rozšíření obsahuje základní podporu pro vytváření obsahu, která vám pomůže s psaním Markdownu, a funkci náhledu, abyste si mohli prohlédnout, jak Markdown vypadá ve stylu webu docs.microsoft.com.

   Navštivte tuto [stránku marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) a vyberte **Nainstalovat**, nebo vyhledejte `docsmsft.docs-authoring-pack` v seznamu rozšíření v okně VS Code. 

   Balíček pro vytváření obsahu na webu Docs zpřístupníte stisknutím kláves Alt+M v sadě VS Code. Panel nástrojů je standardně skrytý, dá se ale zobrazit. Zobrazíte ho úpravou nastavení sady VS Code (Ctrl+čárka) a přidáním uživatelského nastavení `"markdown.showToolbar": true`.

   Další informace najdete na stránce [Balíček pro vytváření obsahu na webu Docs](how-to-write-docs-auth-pack.md).


## <a name="next-steps"></a>Další kroky

Teď jste připraveni [nastavit místní úložiště Git](get-started-setup-local.md).
