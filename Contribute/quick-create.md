---
title: 'Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault | Microsoft Docs'
description: 'Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805729"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="a2ccf-103">Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="a2ccf-104">V tomto rychlém startu se dozvíte, jak uložit tajný kód do trezoru klíčů a jak ho načíst pomocí webové aplikace.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="a2ccf-105">Pokud chcete zobrazit hodnotu tajného kódu, musíte webovou aplikaci spustit v Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="a2ccf-106">V tomto rychlém startu se používá Node.js a identity spravovaných služeb (MSI).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-106">The quickstart uses Node.js and Managed service identities (MSIs).</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="a2ccf-107">Vytvoření trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="a2ccf-108">Uložení tajného kódu do trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-108">Store a secret in the Key Vault.</span></span>
> * <span data-ttu-id="a2ccf-109">Načtení tajného kódu z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="a2ccf-110">Vytvoření webové aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="a2ccf-111">[Povolení identit spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)</span><span class="sxs-lookup"><span data-stu-id="a2ccf-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="a2ccf-112">Udělení požadovaných oprávnění webové aplikaci ke čtení dat z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="a2ccf-113">Než budete pokračovat, ujistěte se, že znáte [základní koncepty](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="a2ccf-114">Abyste pochopili, proč následující kurz představuje osvědčený postup, je potřeba porozumět několika konceptům.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="a2ccf-115">Trezor klíčů je centrální úložiště sloužící k programovému ukládání tajných kódů.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="a2ccf-116">Aby to bylo možné, musí se aplikace nebo uživatelé nejprve vůči trezoru klíčů ověřit, tedy předložit tajný kód.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="a2ccf-117">Kvůli dodržování osvědčených postupů zabezpečení se navíc tento první tajný kód musí pravidelně obměňovat.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="a2ccf-118">Při použití [Identity spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) se však aplikacím spouštěným v Azure udělí identita, kterou automaticky spravuje Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="a2ccf-119">To pomůže vyřešit **problém se zavedením tajného kódu**, takže uživatelé a aplikace budou dodržovat osvědčené postupy bez starostí o obměňování prvního tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a2ccf-120">Požadavky</span><span class="sxs-lookup"><span data-stu-id="a2ccf-120">Prerequisites</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="a2ccf-121">Node JS</span><span class="sxs-lookup"><span data-stu-id="a2ccf-121">Node JS</span></span>](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* <span data-ttu-id="a2ccf-122">[Visual Studio 2017 verze 15.7.3 nebo novější](https://www.microsoft.com/net/download/windows) s následujícími úlohami:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-122">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="a2ccf-123">Vývoj pro ASP.NET a web</span><span class="sxs-lookup"><span data-stu-id="a2ccf-123">ASP.NET and web development</span></span>
  * <span data-ttu-id="a2ccf-124">Vývoj pro různé platformy pomocí rozhraní .NET Core</span><span class="sxs-lookup"><span data-stu-id="a2ccf-124">.NET Core cross-platform development</span></span>
* [<span data-ttu-id="a2ccf-125">Sada .NET Core 2.1 SDK nebo novější</span><span class="sxs-lookup"><span data-stu-id="a2ccf-125">.NET Core 2.1 SDK or later</span></span>](https://www.microsoft.com/net/download/windows)
::: zone-end
* <span data-ttu-id="a2ccf-126">Git ([stáhnout](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-126">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="a2ccf-127">Předplatné Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-127">An Azure subscription.</span></span> <span data-ttu-id="a2ccf-128">Pokud předplatné Azure ještě nemáte, vytvořte si [bezplatný účet](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) předtím, než začnete.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-128">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="a2ccf-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) verze 2.0.4 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-129">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="a2ccf-130">K dispozici pro Windows, Mac a Linux.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-130">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="a2ccf-131">Přihlášení k Azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-131">Login to Azure</span></span>

<span data-ttu-id="a2ccf-132">Pokud se chcete přihlásit k Azure pomocí rozhraní příkazového řádku, můžete zadat:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-132">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="a2ccf-133">Vytvoření skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="a2ccf-133">Create resource group</span></span>

<span data-ttu-id="a2ccf-134">Vytvořte skupinu prostředků pomocí příkazu [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-134">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="a2ccf-135">Skupina prostředků Azure je logický kontejner, ve kterém se nasazují a spravují prostředky Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-135">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="a2ccf-136">Vyberte název skupiny prostředků a nahraďte zástupný text.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-136">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="a2ccf-137">Následující příklad vytvoří skupinu prostředků s názvem *<YourResourceGroupName>* v umístění *eastus*.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-137">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="a2ccf-138">V tomto kurzu se používá skupina prostředků, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-138">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="a2ccf-139">Vytvoření trezoru klíčů Azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-139">Create an Azure Key Vault</span></span>

<span data-ttu-id="a2ccf-140">Dále s použitím skupiny prostředků vytvořené v předchozím kroku vytvoříte trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-140">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="a2ccf-141">Přestože se v tomto článku jako název pro trezor klíčů používá ContosoKeyVault, musíte použít jedinečný název.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-141">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="a2ccf-142">Zadejte tyto údaje:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-142">Provide the following information:</span></span>

* <span data-ttu-id="a2ccf-143">Název trezoru – **tady vyberte název trezoru klíčů**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-143">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="a2ccf-144">Název skupiny prostředků – **tady vyberte název skupiny prostředků**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-144">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="a2ccf-145">Umístění – **Východní USA**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-145">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="a2ccf-146">V tuto chvíli je váš účet Azure jediným účtem autorizovaným k provádění jakýchkoli operací s tímto novým trezorem.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-146">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="a2ccf-147">Přidání tajného kódu do trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-147">Add a secret to key vault</span></span>

<span data-ttu-id="a2ccf-148">Tajný kód přidáváme proto, abychom ukázali, jak to funguje.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-148">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="a2ccf-149">Mohli byste uložit připojovací řetězec SQL nebo jakýkoli jiný údaj, který potřebujete udržet v tajnosti, ale zároveň zpřístupnit vaší aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-149">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="a2ccf-150">V tomto kurzu se heslo bude označovat jako **AppSecret** a bude v něm uložená hodnota **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-150">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="a2ccf-151">Zadáním následujících příkazů vytvořte v trezoru klíčů tajný kód **AppSecret**, který bude uchovávat hodnotu **MySecret**:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-151">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="a2ccf-152">Hodnotu v tajném kódu zobrazíte jako prostý text takto:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-152">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="a2ccf-153">Tento příkaz zobrazí informace o tajném kódu včetně identifikátoru URI.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-153">This command shows the secret information including the URI.</span></span> <span data-ttu-id="a2ccf-154">Po dokončení tohoto postupu byste měli mít identifikátor URI v tajném kódu ve službě Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-154">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="a2ccf-155">Tento údaj si poznamenejte.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-155">Write this information down.</span></span> <span data-ttu-id="a2ccf-156">Budete ho potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-156">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="a2ccf-157">Klonování úložiště</span><span class="sxs-lookup"><span data-stu-id="a2ccf-157">Clone the Repo</span></span>

<span data-ttu-id="a2ccf-158">Spuštěním následujícího příkazu naklonujte úložiště, abyste získali místní kopii umožňující úpravu zdroje:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-158">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a><span data-ttu-id="a2ccf-159">Instalace závislostí</span><span class="sxs-lookup"><span data-stu-id="a2ccf-159">Install dependencies</span></span>

<span data-ttu-id="a2ccf-160">Teď nainstalujeme závislosti.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-160">Here we install the dependencies.</span></span> <span data-ttu-id="a2ccf-161">Spusťte následující příkazy:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-161">Run the following commands:</span></span>

    cd key-vault-node-quickstart
    npm install

<span data-ttu-id="a2ccf-162">Tento projekt používal 2 moduly uzlu:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-162">This project used 2 node modules:</span></span>

* [<span data-ttu-id="a2ccf-163">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-163">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="a2ccf-164">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-164">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="a2ccf-165">Publikování webové aplikace do Azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-165">Publish the web application to Azure</span></span>

<span data-ttu-id="a2ccf-166">Níže je uvedeno několik kroků, kterými je potřeba aplikaci publikovat do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-166">Below are the few steps we need to do to publish the application to Azure.</span></span>

* <span data-ttu-id="a2ccf-167">Prvním krokem je vytvořit plán služby [Azure App Service](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-167">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="a2ccf-168">Do tohoto plánu můžete uložit několik webových aplikací.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-168">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="a2ccf-169">Dále vytvoříme webovou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-169">Next we create a web app.</span></span> <span data-ttu-id="a2ccf-170">V následujícím příkladu nahraďte <app_name> globálně jedinečným názvem aplikace (platné znaky jsou a–z, 0–9 a -).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-170">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="a2ccf-171">Modul runtime je nastavený na NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-171">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="a2ccf-172">Pokud chcete zobrazit všechny podporované moduly runtime, spusťte příkaz `az webapp list-runtimes`.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-172">To see all supported runtimes, run `az webapp list-runtimes`</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="a2ccf-173">Po vytvoření webové aplikace zobrazí Azure CLI výstup podobný následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-173">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    <span data-ttu-id="a2ccf-174">Přejděte do své nově vytvořené webové aplikace. Měla by se zobrazit funkční webová aplikace.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-174">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="a2ccf-175">Nahraďte <app_name> jedinečným názvem aplikace.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-175">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="a2ccf-176">Výše uvedený příkaz také vytvoří aplikaci s podporou Gitu, která umožňuje nasazení do Azure z místního Gitu.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-176">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="a2ccf-177">Místní Git má nakonfigurovanou adresu URL https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-177">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="a2ccf-178">Vytvořte uživatele nasazení. Po dokončení předchozího příkazu můžete do místního úložiště Git přidat vzdálené úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-178">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="a2ccf-179">Nahraďte <url> adresou URL vzdáleného úložiště Git, kterou jste získali při povolení Gitu pro vaši aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-179">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="a2ccf-180">Otevření a úprava řešení</span><span class="sxs-lookup"><span data-stu-id="a2ccf-180">Open and edit the solution</span></span>

<span data-ttu-id="a2ccf-181">Upravte soubor program.cs, abyste ukázku mohli spustit s konkrétním názvem trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-181">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="a2ccf-182">Přejděte do složky key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-182">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="a2ccf-183">V sadě Visual Studio 2017 otevřete soubor key-vault-dotnet-core-quickstart.sln.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-183">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="a2ccf-184">Otevřete soubor Program.cs a aktualizujte zástupný text *YourKeyVaultName* názvem dříve vytvořeného trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-184">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="a2ccf-185">Toto řešení používá knihovny NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) a [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-185">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="a2ccf-186">Spuštění aplikace</span><span class="sxs-lookup"><span data-stu-id="a2ccf-186">Run the app</span></span>

<span data-ttu-id="a2ccf-187">V hlavní nabídce sady Visual Studio 2017 vyberte **Ladit** > **Spustit** bez ladění.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-187">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="a2ccf-188">Jakmile se zobrazí prohlížeč, přejděte na stránku **O aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-188">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="a2ccf-189">Zobrazí se hodnota **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-189">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="a2ccf-190">Publikování webové aplikace do Azure</span><span class="sxs-lookup"><span data-stu-id="a2ccf-190">Publish the web application to Azure</span></span>

<span data-ttu-id="a2ccf-191">Publikujte tuto aplikaci do Azure, abyste ji viděli jako webovou aplikaci v ostrém provozu a zjistili, jestli můžete načíst hodnotu tajného kódu:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-191">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="a2ccf-192">V sadě Visual Studio vyberte projekt **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-192">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="a2ccf-193">Vyberte **Publikovat** > **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-193">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="a2ccf-194">Vytvořte novou službu **App Service** a pak vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-194">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="a2ccf-195">Změňte název aplikace na **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-195">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="a2ccf-196">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-196">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a><span data-ttu-id="a2ccf-197">Povolení identit spravované služby</span><span class="sxs-lookup"><span data-stu-id="a2ccf-197">Enable managed service identities</span></span>

<span data-ttu-id="a2ccf-198">Azure Key Vault nabízí možnost bezpečného ukládání přihlašovacích údajů a jiných klíčů a tajných kódů, ale váš kód se musí ověřit vůči službě Azure Key Vault, aby je mohl načíst.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-198">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="a2ccf-199">Identita spravované služby to usnadňuje tím, že poskytuje službám Azure automaticky spravovanou identitu v Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="a2ccf-199">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="a2ccf-200">Pomocí této identity se můžete ověřit vůči libovolné službě, která podporuje ověřování Azure AD, včetně služby Key Vault, aniž byste ve vašem kódu museli mít přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-200">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="a2ccf-201">Vraťte se k Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-201">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="a2ccf-202">Spuštěním příkazu assign-identity vytvořte identitu pro tuto aplikaci:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-202">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="a2ccf-203">Příkaz v této proceduře je ekvivalentem přechodu na portál a nastavení **Identity spravované služby** na hodnotu **Zapnuto** ve vlastnostech webové aplikace.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-203">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="a2ccf-204">Přiřazení oprávnění vaší aplikaci ke čtení tajných kódů z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="a2ccf-204">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="a2ccf-205">Poznamenejte si výstup, který se zobrazí, když aplikaci publikujete do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-205">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="a2ccf-206">Měl by mít následující formát:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-206">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="a2ccf-207">Potom spusťte tento příkaz s použitím názvu vašeho trezoru klíčů a hodnoty **PrincipalId**:</span><span class="sxs-lookup"><span data-stu-id="a2ccf-207">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="a2ccf-208">Nasazení aplikace Node do Azure a načtení hodnoty tajného kódu</span><span class="sxs-lookup"><span data-stu-id="a2ccf-208">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="a2ccf-209">Teď je vše nastavené.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-209">Now that everything is set.</span></span> <span data-ttu-id="a2ccf-210">Spuštěním následujícího příkazu nasaďte aplikaci do Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-210">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="a2ccf-211">Když teď přejdete na adresu https://<app_name>.azurewebsites.net, zobrazí se hodnota tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-211">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="a2ccf-212">Ujistěte se, že jste nahradili název <YourKeyVaultName> názvem vašeho trezoru.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-212">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

::: zone-end

::: zone pivot="dotnet"
<span data-ttu-id="a2ccf-213">Když teď aplikaci spustíte, měla by se zobrazit načtená hodnota vašeho tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="a2ccf-213">Now when you run the application, you should see your secret value retrieved.</span></span>
::: zone-end

## <a name="next-steps"></a><span data-ttu-id="a2ccf-214">Další kroky</span><span class="sxs-lookup"><span data-stu-id="a2ccf-214">Next steps</span></span>

::: zone pivot="nodejs"
* [<span data-ttu-id="a2ccf-215">Domovská stránka služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-215">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="a2ccf-216">Dokumentace ke službě Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-216">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="a2ccf-217">Azure SDK pro Node</span><span class="sxs-lookup"><span data-stu-id="a2ccf-217">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [<span data-ttu-id="a2ccf-218">Referenční informace k rozhraní Azure REST API</span><span class="sxs-lookup"><span data-stu-id="a2ccf-218">Azure REST API Reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [<span data-ttu-id="a2ccf-219">Domovská stránka služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-219">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="a2ccf-220">Dokumentace ke službě Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="a2ccf-220">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="a2ccf-221">Sada Azure SDK pro .NET</span><span class="sxs-lookup"><span data-stu-id="a2ccf-221">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* [<span data-ttu-id="a2ccf-222">Referenční informace k rozhraní Azure REST API</span><span class="sxs-lookup"><span data-stu-id="a2ccf-222">Azure REST API reference</span></span>](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
