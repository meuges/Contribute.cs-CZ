---
title: Místní nastavení úložiště Git
description: Tento článek poskytuje pokyny pro vytvoření místního úložiště Git a pro přispívání do dokumentace, včetně postupu vytváření forků a klonování.
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: 285c25fe0e5df067ceeaa5a42da1bad5533d2c84
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247401"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="d614e-103">Místní nastavení úložiště Git pro dokumentaci</span><span class="sxs-lookup"><span data-stu-id="d614e-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="d614e-104">Tento článek popisuje postup nastavení úložiště Git na místním počítači se záměrem pro přispívání do dokumentace Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="d614e-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="d614e-105">Přispěvatelé můžou použít místně naklonované úložiště k přidávání nových článků, provádění významných úprav existujících článků nebo ke změně obrázků.</span><span class="sxs-lookup"><span data-stu-id="d614e-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="d614e-106">Abyste mohli začít přispívat, provedete následující jednorázová nastavení:</span><span class="sxs-lookup"><span data-stu-id="d614e-106">You run these one-time setup activities to start contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="d614e-107">Určení vhodného úložiště</span><span class="sxs-lookup"><span data-stu-id="d614e-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="d614e-108">Rozvětvení úložiště do vašeho účtu GitHubu</span><span class="sxs-lookup"><span data-stu-id="d614e-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="d614e-109">Volba místní složky pro klonované soubory</span><span class="sxs-lookup"><span data-stu-id="d614e-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="d614e-110">Klonování úložiště do místního počítače</span><span class="sxs-lookup"><span data-stu-id="d614e-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="d614e-111">Konfigurace vzdálené hodnoty upstreamu</span><span class="sxs-lookup"><span data-stu-id="d614e-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d614e-112">Pokud děláte jenom menší změny článku, kroky v tomto článku provádět *nemusíte*.</span><span class="sxs-lookup"><span data-stu-id="d614e-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="d614e-113">Můžete pokračovat přímo na [pracovní postup pro rychlé změny](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="d614e-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="d614e-114">Přehled</span><span class="sxs-lookup"><span data-stu-id="d614e-114">Overview</span></span>

<span data-ttu-id="d614e-115">Pokud chcete přispívat na web s dokumentací Microsoftu, můžete vytvářet a upravovat soubory Markdown místně, a to klonováním odpovídajícího úložiště dokumentace.</span><span class="sxs-lookup"><span data-stu-id="d614e-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="d614e-116">Microsoft vyžaduje vytvoření forku příslušného úložiště do vlastního účtu GitHubu, abyste měli oprávnění ke čtení a zápisu pro ukládání navrhovaných změn.</span><span class="sxs-lookup"><span data-stu-id="d614e-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="d614e-117">Pomocí žádostí o přijetí změn pak změny sloučíte do centrálního sdíleného úložiště určeného jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="d614e-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![Trojúhelník GitHubu](./media/git-and-github-initial-setup.png)

<span data-ttu-id="d614e-119">Pokud je pro vás GitHub novinkou, podívejte se na toto video s koncepčním přehledem procesu vytvoření forku a klonování:</span><span class="sxs-lookup"><span data-stu-id="d614e-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="d614e-120">Určení úložiště</span><span class="sxs-lookup"><span data-stu-id="d614e-120">Determine the repository</span></span>

<span data-ttu-id="d614e-121">Dokumentace hostovaná na webu [docs.microsoft.com](https://docs.microsoft.com) se nachází v několika různých úložištích na webu [github.com](https://www.github.com).</span><span class="sxs-lookup"><span data-stu-id="d614e-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="d614e-122">Pokud nevíte, jaké úložiště použít, navštivte tento článek na webu [docs.microsoft.com](https://docs.microsoft.com) ve svém webovém prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="d614e-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="d614e-123">Vyberte odkaz **Upravit** (ikona tužky) v pravém horním rohu článku.</span><span class="sxs-lookup"><span data-stu-id="d614e-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Kliknutím na Upravit určete úložiště a umístění souboru.](media/index/edit-article.png)

2. <span data-ttu-id="d614e-125">Tento odkaz vás nasměruje na umístění webu github.com s odpovídajícím souborem Markdown v příslušném úložišti.</span><span class="sxs-lookup"><span data-stu-id="d614e-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="d614e-126">Poznačte si adresu URL a zjistěte název úložiště.</span><span class="sxs-lookup"><span data-stu-id="d614e-126">Note the URL to view the repository name.</span></span>

   ![Z adresy URL určete umístění úložiště.](media/public-repo.png)

   <span data-ttu-id="d614e-128">Pro veřejné příspěvky jsou například dostupná tato oblíbená úložiště:</span><span class="sxs-lookup"><span data-stu-id="d614e-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="d614e-129">Dokumentace k Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="d614e-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="d614e-130">Dokumentace k SQL Serveru [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="d614e-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="d614e-131">Dokumentace k sadě Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="d614e-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="d614e-132">Dokumentace k rozhraní .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="d614e-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="d614e-133">Dokumentace k sadě Azure .Net SDK [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="d614e-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>
   - <span data-ttu-id="d614e-134">Dokumentace ke ConfigMgr [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span><span class="sxs-lookup"><span data-stu-id="d614e-134">ConfigMgr documentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="d614e-135">Rozvětvení úložiště</span><span class="sxs-lookup"><span data-stu-id="d614e-135">Fork the repository</span></span>
<span data-ttu-id="d614e-136">Ve vhodném úložišti vytvořte fork úložiště do vlastního účtu GitHubu pomocí webu GitHub.</span><span class="sxs-lookup"><span data-stu-id="d614e-136">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="d614e-137">Osobní fork se vyžaduje, protože všechna hlavní úložiště dokumentace poskytují přístup jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="d614e-137">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="d614e-138">Pokud chcete změny provádět, musíte z vlastního forku odeslat [žádost o přijetí změn](git-github-fundamentals.md#pull-requests) do hlavního úložiště.</span><span class="sxs-lookup"><span data-stu-id="d614e-138">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="d614e-139">Abyste tento proces usnadnili, potřebujete nejprve vlastní kopii úložiště, ve které máte oprávnění k zápisu.</span><span class="sxs-lookup"><span data-stu-id="d614e-139">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="d614e-140">K tomuto účelu slouží *fork* Githubu.</span><span class="sxs-lookup"><span data-stu-id="d614e-140">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="d614e-141">Přejděte na stránku GitHubu hlavního úložiště a vpravo nahoře klikněte na tlačítko **Fork**.</span><span class="sxs-lookup"><span data-stu-id="d614e-141">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Příklad profilu na GitHubu](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="d614e-143">Pokud k tomu budete vyzváni, vyberte dlaždici účtu GitHub jako cíl, do kterého se má fork vytvořit.</span><span class="sxs-lookup"><span data-stu-id="d614e-143">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="d614e-144">Tímto se ve vašem účtu GitHub vytvoří kopie úložiště, která se označuje jako fork.</span><span class="sxs-lookup"><span data-stu-id="d614e-144">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="d614e-145">Výběr místní složky</span><span class="sxs-lookup"><span data-stu-id="d614e-145">Choose a local folder</span></span>
<span data-ttu-id="d614e-146">Vytvořte místní složku, ve které bude uložená místní kopie úložiště.</span><span class="sxs-lookup"><span data-stu-id="d614e-146">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="d614e-147">Některá úložiště mohou být velká. Pro dokumentaci k Azure je to například až 5 GB.</span><span class="sxs-lookup"><span data-stu-id="d614e-147">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="d614e-148">Zvolte umístění s dostupným místem na disku.</span><span class="sxs-lookup"><span data-stu-id="d614e-148">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="d614e-149">Zvolte název složky, který si snadno zapamatujete a budete ho moci snadno zadat.</span><span class="sxs-lookup"><span data-stu-id="d614e-149">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="d614e-150">Zvažte například kořenovou složku `C:\docs\` nebo vytvořte složku v adresáři profilu uživatele `~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="d614e-150">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="d614e-151">Nepoužívejte cestu k místní složce, která je vnořená v umístění jiné složky úložiště Git.</span><span class="sxs-lookup"><span data-stu-id="d614e-151">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="d614e-152">I když klonované složky Gitu mohou existovat vedle sebe, vnoření složky Gitu do jiné způsobí chyby sledování souboru.</span><span class="sxs-lookup"><span data-stu-id="d614e-152">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="d614e-153">Spusťte Git Bash.</span><span class="sxs-lookup"><span data-stu-id="d614e-153">Launch Git Bash</span></span>

   ![Spuštění Git Bashe](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="d614e-155">Výchozím umístěním, ze kterého se Git Bash spouští, je obvykle domovský adresář (~) nebo `/c/users/<Windows-user-account>/` v operačním systému Windows.</span><span class="sxs-lookup"><span data-stu-id="d614e-155">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="d614e-156">Aktuální adresář určíte zadáním příkazu `pwd` do příkazového řádku $.</span><span class="sxs-lookup"><span data-stu-id="d614e-156">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="d614e-157">Změňte adresář (cd) na složku, kterou jste vytvořili pro místní hostování úložiště.</span><span class="sxs-lookup"><span data-stu-id="d614e-157">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="d614e-158">Všimněte si, že Git Bash používá pro cesty ke složkám linuxovou konvenci lomítek místo zpětných lomítek.</span><span class="sxs-lookup"><span data-stu-id="d614e-158">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="d614e-159">Příklad: `cd /c/docs/ ` nebo `cd ~/Documents/docs/`</span><span class="sxs-lookup"><span data-stu-id="d614e-159">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="d614e-160">Vytvoření místního klonu</span><span class="sxs-lookup"><span data-stu-id="d614e-160">Create a local clone</span></span>

<span data-ttu-id="d614e-161">Pomocí Git Bashe se připravte na spuštění příkazu **clone**, kterým do svého zařízení v aktuálním adresáři stáhnete kopii úložiště (fork).</span><span class="sxs-lookup"><span data-stu-id="d614e-161">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="d614e-162">Ověření pomocí Git Credential Manageru</span><span class="sxs-lookup"><span data-stu-id="d614e-162">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="d614e-163">Pokud jste nainstalovali nejnovější verzi Gitu pro Windows a přijali výchozí instalaci, Git Credential Manager je ve výchozím nastavení zapnutý.</span><span class="sxs-lookup"><span data-stu-id="d614e-163">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="d614e-164">Správce přihlašovacích údajů Gitu velmi usnadňuje ověřování, protože si při obnovování ověřených nebo vzdálených připojení ke GitHubu nemusíte pamatovat svůj osobní přístupový token.</span><span class="sxs-lookup"><span data-stu-id="d614e-164">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="d614e-165">Zadáním názvu úložiště spusťte příkaz **clone**.</span><span class="sxs-lookup"><span data-stu-id="d614e-165">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="d614e-166">Při klonování se na místní počítač stáhne (naklonuje) forkované úložiště.</span><span class="sxs-lookup"><span data-stu-id="d614e-166">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="d614e-167">Adresu URL vašeho forku GitHubu pro klonovací příkaz můžete získat z tlačítka **Clone or download** (Klonovat nebo stáhnout) v uživatelském rozhraní GitHubu:</span><span class="sxs-lookup"><span data-stu-id="d614e-167">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Clone or download (Klonovat nebo stáhnout)](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="d614e-169">Při klonování zadejte cestu ke *svému forku*, ne k hlavnímu úložišti, ze kterého jste fork vytvořili.</span><span class="sxs-lookup"><span data-stu-id="d614e-169">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="d614e-170">V opačném případě nemůžete přidávat změny.</span><span class="sxs-lookup"><span data-stu-id="d614e-170">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="d614e-171">Váš fork se uvádí s osobním uživatelským účtem GitHubu, například `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="d614e-171">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="d614e-172">Klonovací příkaz by mohl například vypadat nějak takto:</span><span class="sxs-lookup"><span data-stu-id="d614e-172">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="d614e-173">Po zobrazení výzvy zadejte své přihlašovací údaje GitHubu.</span><span class="sxs-lookup"><span data-stu-id="d614e-173">When you're prompted, enter your GitHub credentials.</span></span>

    ![Přihlašovací obrazovka GitHubu](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="d614e-175">Po zobrazení výzvy zadejte svůj ověřovací kód dvojúrovňového ověřování.</span><span class="sxs-lookup"><span data-stu-id="d614e-175">When you're prompted, enter your two-factor authentication code.</span></span>

    ![Dvojúrovňové ověřování GitHubu](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="d614e-177">Vaše přihlašovací údaje se uloží a použijí se k ověření při budoucích požadavcích GitHubu.</span><span class="sxs-lookup"><span data-stu-id="d614e-177">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="d614e-178">Toto ověření je třeba provést na každém počítači jen jednou.</span><span class="sxs-lookup"><span data-stu-id="d614e-178">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="d614e-179">Klonovací příkaz se spustí a stáhne kopii souborů úložiště z vašeho forku do nového forku na místním disku.</span><span class="sxs-lookup"><span data-stu-id="d614e-179">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="d614e-180">V aktuální složce se vytvoří nová složka.</span><span class="sxs-lookup"><span data-stu-id="d614e-180">A new folder is made within the current folder.</span></span> <span data-ttu-id="d614e-181">Může to trvat několik minut podle toho, jak je úložiště velké.</span><span class="sxs-lookup"><span data-stu-id="d614e-181">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="d614e-182">Po dokončení si můžete projít strukturu složky.</span><span class="sxs-lookup"><span data-stu-id="d614e-182">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="d614e-183">Konfigurace vzdáleného upstreamu</span><span class="sxs-lookup"><span data-stu-id="d614e-183">Configure remote upstream</span></span>
<span data-ttu-id="d614e-184">Po naklonování úložiště nastavte vzdálené připojení jen pro čtení k hlavnímu úložišti označovanému jako **upstream**.</span><span class="sxs-lookup"><span data-stu-id="d614e-184">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="d614e-185">Adresa URL upstreamu vám bude sloužit k udržení místního úložiště synchronizovaného s nejnovějšími změnami provedených ostatními.</span><span class="sxs-lookup"><span data-stu-id="d614e-185">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="d614e-186">Příkaz **git remote** slouží k nastavení konfigurační hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d614e-186">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="d614e-187">K aktualizaci informací o větvi z úložiště upstream použijte příkaz **fetch**.</span><span class="sxs-lookup"><span data-stu-id="d614e-187">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="d614e-188">Pokud používáte **Git Credential Manager**, použijte tyto příkazy.</span><span class="sxs-lookup"><span data-stu-id="d614e-188">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="d614e-189">Nahraďte zástupné symboly \<repo\> a \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="d614e-189">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="d614e-190">Podívejte se na nakonfigurované hodnoty a zkontrolujte, že jsou adresy URL správné.</span><span class="sxs-lookup"><span data-stu-id="d614e-190">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="d614e-191">Ujistěte se, že **původní** adresy URL odkazují na váš osobní fork.</span><span class="sxs-lookup"><span data-stu-id="d614e-191">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="d614e-192">Ujistěte se, že adresy URL **upstreamu** odkazují na hlavní úložiště, například MicrosoftDocs nebo Azure.</span><span class="sxs-lookup"><span data-stu-id="d614e-192">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="d614e-193">Na obrázku je uveden příklad vzdáleného výstupu.</span><span class="sxs-lookup"><span data-stu-id="d614e-193">Example remote output is shown.</span></span> <span data-ttu-id="d614e-194">Fiktivní účet Gitu s názvem MyGitAccount je nakonfigurován s osobním přístupovým tokenem pro přístup k úložišti azure-docs:</span><span class="sxs-lookup"><span data-stu-id="d614e-194">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="d614e-195">Pokud uděláte chybu, můžete vzdálenou hodnotu odebrat.</span><span class="sxs-lookup"><span data-stu-id="d614e-195">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="d614e-196">Pokud chcete odebrat hodnotu upstreamu, spusťte příkaz `git remote remove upstream`.</span><span class="sxs-lookup"><span data-stu-id="d614e-196">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d614e-197">Další kroky</span><span class="sxs-lookup"><span data-stu-id="d614e-197">Next steps</span></span>
- <span data-ttu-id="d614e-198">Pokud se chcete dozvědět další informace o přidávání a aktualizaci obsahu, pokračujte tématem, který se zabývá [pracovním postupem přispívání na GitHub](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="d614e-198">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
