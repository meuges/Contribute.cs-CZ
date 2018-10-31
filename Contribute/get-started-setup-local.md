---
title: Místní nastavení úložiště Git
description: Tento článek poskytuje pokyny pro vytvoření místního úložiště Git a pro přispívání do dokumentace, včetně postupu vytváření forků a klonování.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 895c0fb0d64708e8e3d0f632c10a060791d15b65
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805670"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>Místní nastavení úložiště Git pro dokumentaci

Tento článek popisuje postup nastavení úložiště Git na místním počítači se záměrem pro přispívání do dokumentace Microsoftu. Přispěvatelé můžou použít místně naklonované úložiště k přidávání nových článků, provádění významných úprav existujících článků nebo ke změně obrázků.

Abyste mohli začít přispívat, provedete následující jednorázová nastavení:
> [!div class="checklist"]
> * Určení vhodného úložiště
> * Rozvětvení úložiště do vašeho účtu GitHubu
> * Volba místní složky pro klonované soubory
> * Klonování úložiště do místního počítače
> * Konfigurace vzdálené hodnoty upstreamu

> [!IMPORTANT]
> Pokud děláte jenom menší změny článku, kroky v tomto článku provádět *nemusíte*. Můžete pokračovat přímo na [pracovní postup pro rychlé změny](index.md#quick-edits-to-existing-documents).
>

## <a name="overview"></a>Přehled

Pokud chcete přispívat na web s dokumentací Microsoftu, můžete vytvářet a upravovat soubory Markdown místně, a to klonováním odpovídajícího úložiště dokumentace. Microsoft vyžaduje, abyste příslušné úložiště rozvětvili do svého vlastního účtu GitHubu, a měli tak oprávnění ke čtení a zápisu pro ukládání navrhovaných změn. Pomocí žádostí o přijetí změn pak změny sloučíte do centrálního sdíleného úložiště určeného jen pro čtení.

![Trojúhelník GitHubu](./media/git-and-github-initial-setup.png)

Pokud je pro vás GitHub novinkou, podívejte se na toto video s koncepčním přehledem procesu vytvoření forku a klonování:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>Určení úložiště

Dokumentace hostovaná na webu [docs.microsoft.com](https://docs.microsoft.com) se nachází v několika různých úložištích na webu [github.com](https://www.github.com).

1. Pokud nevíte, které úložiště použít, navštivte tento článek na webu docs.microsoft.com pomocí svého webového prohlížeče. Vyberte odkaz **Upravit** (ikona tužky) v pravém horním rohu článku.

   ![Kliknutím na Upravit určete úložiště a umístění souboru.](media/index/edit-article.png)

2. Tento odkaz vás nasměruje na umístění webu github.com s odpovídajícím souborem Markdown v příslušném úložišti. Poznačte si adresu URL a zjistěte název úložiště.

   ![Z adresy URL určete umístění úložiště.](media/public-repo.png)

   Pro veřejné příspěvky jsou například dostupná tato oblíbená úložiště:
   - Dokumentace k Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - Dokumentace k SQL Serveru [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Dokumentace k sadě Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - Dokumentace k rozhraní .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - Dokumentace k sadě Azure .Net SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)

## <a name="fork-the-repository"></a>Rozvětvení úložiště
Ve vhodném úložišti vytvořte fork úložiště do vlastního účtu GitHubu pomocí webu GitHub.

Osobní fork se vyžaduje, protože všechna hlavní úložiště dokumentace poskytují přístup jen pro čtení. Pokud chcete změny provádět, musíte z vlastního forku odeslat [žádost o přijetí změn](git-github-fundamentals.md#pull-requests) do hlavního úložiště. Abyste tento proces usnadnili, potřebujete nejprve vlastní kopii úložiště, ve které máte oprávnění k zápisu. K tomuto účelu slouží *fork* Githubu.

1. Přejděte na stránku GitHubu hlavního úložiště a vpravo nahoře klikněte na tlačítko **Fork**.

   ![Příklad profilu na GitHubu](./media/contribute-get-started-setup-local/fork.png)

2. Pokud k tomu budete vyzváni, vyberte dlaždici účtu GitHub jako cíl, do kterého se má fork vytvořit. Tímto se ve vašem účtu GitHub vytvoří kopie úložiště, která se označuje jako fork.

## <a name="choose-a-local-folder"></a>Výběr místní složky
Vytvořte místní složku, ve které bude uložená místní kopie úložiště. Některá úložiště mohou být velká. Pro dokumentaci k Azure je to například až 5 GB. Zvolte umístění s dostupným místem na disku.

1. Zvolte název složky, který si snadno zapamatujete a budete ho moci snadno zadat. Zvažte například kořenovou složku `C:\docs\` nebo vytvořte složku v adresáři profilu uživatele `~/Documents/docs/`.

   > [!IMPORTANT]
   > Nepoužívejte cestu k místní složce, která je vnořená v umístění jiné složky úložiště Git. I když klonované složky Gitu mohou existovat vedle sebe, vnoření složky Gitu do jiné způsobí chyby sledování souboru.

2. Spusťte Git Bash.

   ![Spuštění Git Bashe](./media/contribute-get-started-setup-local/gitbash-start.png)

   Výchozím umístěním, ze kterého se Git Bash spouští, je obvykle domovský adresář (~) nebo `/c/users/<Windows-user-account>/` v operačním systému Windows.

   Aktuální adresář určíte zadáním příkazu `pwd` do příkazového řádku $. 

3. Změňte adresář (cd) na složku, kterou jste vytvořili pro místní hostování úložiště. Všimněte si, že Git Bash používá pro cesty ke složkám linuxovou konvenci lomítek místo zpětných lomítek.

   Příklad: `cd /c/docs/ ` nebo `cd ~/Documents/docs/`

## <a name="create-a-local-clone"></a>Vytvoření místního klonu

Pomocí Git Bashe se připravte na spuštění příkazu **clone**, kterým do svého zařízení v aktuálním adresáři stáhnete kopii úložiště (fork). 

### <a name="authenticate-by-using-git-credential-manager"></a>Ověření pomocí Git Credential Manageru
Pokud jste nainstalovali nejnovější verzi Gitu pro Windows a přijali výchozí instalaci, Git Credential Manager je ve výchozím nastavení zapnutý. Git Credential Manager velmi usnadňuje ověření, protože si nemusíte svůj osobní přístupový token pamatovat, když pomocí GitHubu obnovujete ověřená spojení a vzdálená připojení.

1. Zadáním názvu úložiště spusťte příkaz **clone**. Při klonování se na místní počítač stáhne (naklonuje) forkované úložiště. 

    > [!Tip]
    > Adresu URL vašeho forku GitHubu pro klonovací příkaz můžete získat z tlačítka **Clone or download** (Klonovat nebo stáhnout) v uživatelském rozhraní GitHubu:
    >
    > ![Clone or download (Klonovat nebo stáhnout)](./media/contribute-get-started-setup-local/clone-or-download.png)

    Při klonování zadejte cestu ke *svému forku*, ne k hlavnímu úložišti, ze kterého jste fork vytvořili. V opačném případě nemůžete přidávat změny. Váš fork se uvádí s osobním uživatelským účtem GitHubu, například `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Klonovací příkaz by mohl například vypadat nějak takto:

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. Po zobrazení výzvy zadejte své přihlašovací údaje GitHubu.

    ![Přihlašovací obrazovka GitHubu](./media/contribute-get-started-setup-local/github-login.png)

3. Po zobrazení výzvy zadejte svůj ověřovací kód dvojúrovňového ověřování.

    ![Dvojúrovňové ověřování GitHubu](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Vaše přihlašovací údaje se uloží a použijí se k ověření při budoucích požadavcích GitHubu. Toto ověření je třeba provést na každém počítači jen jednou. 

4. Klonovací příkaz se spustí a stáhne kopii souborů úložiště z vašeho forku do nového forku na místním disku. V aktuální složce se vytvoří nová složka. Může to trvat několik minut podle toho, jak je úložiště velké. Po dokončení si můžete projít strukturu složky.

## <a name="configure-remote-upstream"></a>Konfigurace vzdáleného upstreamu
Po naklonování úložiště nastavte vzdálené připojení jen pro čtení k hlavnímu úložišti označovanému jako **upstream**. Adresa URL upstreamu vám bude sloužit k udržení místního úložiště synchronizovaného s nejnovějšími změnami provedených ostatními. Příkaz **git remote** slouží k nastavení konfigurační hodnoty. K aktualizaci informací o větvi z úložiště upstream použijte příkaz **fetch**.

1. Pokud používáte **Git Credential Manager**, použijte tyto příkazy. Nahraďte zástupné symboly \<repo\> a \<organization\>.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Podívejte se na nakonfigurované hodnoty a zkontrolujte, že jsou adresy URL správné. Ujistěte se, že **původní** adresy URL odkazují na váš osobní fork. Ujistěte se, že adresy URL **upstreamu** odkazují na hlavní úložiště, například MicrosoftDocs nebo Azure. 
   ```bash
   git remote -v 
   ```

   Na obrázku je uveden příklad vzdáleného výstupu. Fiktivní účet Gitu s názvem MyGitAccount je nakonfigurován s osobním přístupovým tokenem pro přístup k úložišti azure-docs:
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Pokud uděláte chybu, můžete vzdálenou hodnotu odebrat. Pokud chcete odebrat hodnotu upstreamu, spusťte příkaz `git remote remove upstream`.

## <a name="next-steps"></a>Další kroky
- Pokud se chcete dozvědět další informace o přidávání a aktualizaci obsahu, pokračujte tématem, který se zabývá [pracovním postupem přispívání na GitHub](how-to-write-workflows-major.md).
