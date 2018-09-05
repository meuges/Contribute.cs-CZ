---
title: 'Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault | Microsoft Docs'
description: 'Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239528"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="1f32e-103">Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1f32e-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="1f32e-104">V tomto rychlém startu se dozvíte, jak uložit tajný kód do trezoru klíčů a jak ho načíst pomocí webové aplikace.</span><span class="sxs-lookup"><span data-stu-id="1f32e-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="1f32e-105">Pokud chcete zobrazit hodnotu tajného kódu, musíte webovou aplikaci spustit v Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="1f32e-106">V tomto rychlém startu se používá Node.js a identity spravovaných služeb (MSI).</span><span class="sxs-lookup"><span data-stu-id="1f32e-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="1f32e-107">Vytvoření trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="1f32e-108">Uložení tajného kódu do trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="1f32e-109">Načtení tajného kódu z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="1f32e-110">Vytvoření webové aplikace Azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="1f32e-111">[Povolení identit spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)</span><span class="sxs-lookup"><span data-stu-id="1f32e-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="1f32e-112">Udělení požadovaných oprávnění webové aplikaci ke čtení dat z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="1f32e-113">Než budete pokračovat, ujistěte se, že znáte [základní koncepty](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="1f32e-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

>[!NOTE]
<span data-ttu-id="1f32e-114">Abyste pochopili, proč následující kurz představuje osvědčený postup, je potřeba porozumět několika konceptům.</span><span class="sxs-lookup"><span data-stu-id="1f32e-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="1f32e-115">Trezor klíčů je centrální úložiště sloužící k programovému ukládání tajných kódů.</span><span class="sxs-lookup"><span data-stu-id="1f32e-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="1f32e-116">Aby to bylo možné, musí se aplikace nebo uživatelé nejprve vůči trezoru klíčů ověřit, tedy předložit tajný kód.</span><span class="sxs-lookup"><span data-stu-id="1f32e-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="1f32e-117">Kvůli dodržování osvědčených postupů zabezpečení se navíc tento první tajný kód musí pravidelně obměňovat.</span><span class="sxs-lookup"><span data-stu-id="1f32e-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="1f32e-118">Při použití [Identity spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) se však aplikacím spouštěným v Azure udělí identita, kterou automaticky spravuje Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="1f32e-119">To pomůže vyřešit **problém se zavedením tajného kódu**, takže uživatelé a aplikace budou dodržovat osvědčené postupy bez starostí o obměňování prvního tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="1f32e-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1f32e-120">Požadavky</span><span class="sxs-lookup"><span data-stu-id="1f32e-120">Prerequisites</span></span>

<span data-ttu-id="1f32e-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="1f32e-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="1f32e-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span></span>

<span data-ttu-id="1f32e-123">::: zone pivot="dotnet, windows"</span><span class="sxs-lookup"><span data-stu-id="1f32e-123">::: zone pivot="dotnet, windows"</span></span>
* <span data-ttu-id="1f32e-124">[Visual Studio 2017 verze 15.7.3 nebo novější](https://www.microsoft.com/net/download/windows) s následujícími úlohami:</span><span class="sxs-lookup"><span data-stu-id="1f32e-124">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="1f32e-125">Vývoj pro ASP.NET a web</span><span class="sxs-lookup"><span data-stu-id="1f32e-125">ASP.NET and web development</span></span>
  * <span data-ttu-id="1f32e-126">Vývoj pro různé platformy pomocí rozhraní .NET Core</span><span class="sxs-lookup"><span data-stu-id="1f32e-126">.NET Core cross-platform development</span></span>
* <span data-ttu-id="1f32e-127">[Sada .NET Core 2.1 SDK nebo novější](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-127">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) :::zone-end</span></span>

<span data-ttu-id="1f32e-128">::: zone pivot="dotnet, mac"</span><span class="sxs-lookup"><span data-stu-id="1f32e-128">::: zone pivot="dotnet, mac"</span></span>
* <span data-ttu-id="1f32e-129">Viz [Co je nového v sadě Visual Studio pro Mac](https://visualstudio.microsoft.com/vs/mac/).</span><span class="sxs-lookup"><span data-stu-id="1f32e-129">See [What’s New in Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).</span></span>
<span data-ttu-id="1f32e-130">:::zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-130">:::zone-end</span></span>

* <span data-ttu-id="1f32e-131">Git ([stáhnout](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="1f32e-131">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="1f32e-132">Předplatné Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-132">An Azure subscription.</span></span> <span data-ttu-id="1f32e-133">Pokud předplatné Azure ještě nemáte, vytvořte si [bezplatný účet](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) předtím, než začnete.</span><span class="sxs-lookup"><span data-stu-id="1f32e-133">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="1f32e-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) verze 2.0.4 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="1f32e-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="1f32e-135">K dispozici pro Windows, Mac a Linux.</span><span class="sxs-lookup"><span data-stu-id="1f32e-135">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="1f32e-136">Přihlášení k Azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-136">Login to Azure</span></span>

<span data-ttu-id="1f32e-137">Pokud se chcete přihlásit k Azure pomocí rozhraní příkazového řádku, můžete zadat:</span><span class="sxs-lookup"><span data-stu-id="1f32e-137">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="1f32e-138">Vytvoření skupiny prostředků</span><span class="sxs-lookup"><span data-stu-id="1f32e-138">Create resource group</span></span>

<span data-ttu-id="1f32e-139">Vytvořte skupinu prostředků pomocí příkazu [az group create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="1f32e-139">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="1f32e-140">Skupina prostředků Azure je logický kontejner, ve kterém se nasazují a spravují prostředky Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-140">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="1f32e-141">Vyberte název skupiny prostředků a nahraďte zástupný text.</span><span class="sxs-lookup"><span data-stu-id="1f32e-141">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="1f32e-142">Následující příklad vytvoří skupinu prostředků s názvem *<YourResourceGroupName>* v umístění *eastus*.</span><span class="sxs-lookup"><span data-stu-id="1f32e-142">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="1f32e-143">V tomto kurzu se používá skupina prostředků, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="1f32e-143">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="1f32e-144">Vytvoření trezoru klíčů Azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-144">Create an Azure Key Vault</span></span>

<span data-ttu-id="1f32e-145">Dále s použitím skupiny prostředků vytvořené v předchozím kroku vytvoříte trezor klíčů.</span><span class="sxs-lookup"><span data-stu-id="1f32e-145">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="1f32e-146">Přestože se v tomto článku jako název pro trezor klíčů používá ContosoKeyVault, musíte použít jedinečný název.</span><span class="sxs-lookup"><span data-stu-id="1f32e-146">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="1f32e-147">Zadejte tyto údaje:</span><span class="sxs-lookup"><span data-stu-id="1f32e-147">Provide the following information:</span></span>

* <span data-ttu-id="1f32e-148">Název trezoru – **tady vyberte název trezoru klíčů**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-148">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="1f32e-149">Název skupiny prostředků – **tady vyberte název skupiny prostředků**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-149">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="1f32e-150">Umístění – **Východní USA**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-150">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="1f32e-151">V tuto chvíli je váš účet Azure jediným účtem autorizovaným k provádění jakýchkoli operací s tímto novým trezorem.</span><span class="sxs-lookup"><span data-stu-id="1f32e-151">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="1f32e-152">Přidání tajného kódu do trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-152">Add a secret to key vault</span></span>

<span data-ttu-id="1f32e-153">Tajný kód přidáváme proto, abychom ukázali, jak to funguje.</span><span class="sxs-lookup"><span data-stu-id="1f32e-153">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="1f32e-154">Mohli byste uložit připojovací řetězec SQL nebo jakýkoli jiný údaj, který potřebujete udržet v tajnosti, ale zároveň zpřístupnit vaší aplikaci.</span><span class="sxs-lookup"><span data-stu-id="1f32e-154">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="1f32e-155">V tomto kurzu se heslo bude označovat jako **AppSecret** a bude v něm uložená hodnota **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-155">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="1f32e-156">Zadáním následujících příkazů vytvořte v trezoru klíčů tajný kód **AppSecret**, který bude uchovávat hodnotu **MySecret**:</span><span class="sxs-lookup"><span data-stu-id="1f32e-156">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="1f32e-157">Hodnotu v tajném kódu zobrazíte jako prostý text takto:</span><span class="sxs-lookup"><span data-stu-id="1f32e-157">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="1f32e-158">Tento příkaz zobrazí informace o tajném kódu včetně identifikátoru URI.</span><span class="sxs-lookup"><span data-stu-id="1f32e-158">This command shows the secret information including the URI.</span></span> <span data-ttu-id="1f32e-159">Po dokončení tohoto postupu byste měli mít identifikátor URI v tajném kódu ve službě Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f32e-159">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="1f32e-160">Tento údaj si poznamenejte.</span><span class="sxs-lookup"><span data-stu-id="1f32e-160">Write this information down.</span></span> <span data-ttu-id="1f32e-161">Budete ho potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="1f32e-161">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="1f32e-162">Klonování úložiště</span><span class="sxs-lookup"><span data-stu-id="1f32e-162">Clone the Repo</span></span>

<span data-ttu-id="1f32e-163">Spuštěním následujícího příkazu naklonujte úložiště, abyste získali místní kopii umožňující úpravu zdroje:</span><span class="sxs-lookup"><span data-stu-id="1f32e-163">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="1f32e-164">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="1f32e-164">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="1f32e-165">Instalace závislostí</span><span class="sxs-lookup"><span data-stu-id="1f32e-165">Install dependencies</span></span>

<span data-ttu-id="1f32e-166">Teď nainstalujeme závislosti.</span><span class="sxs-lookup"><span data-stu-id="1f32e-166">Here we install the dependencies.</span></span> <span data-ttu-id="1f32e-167">Spusťte následující příkazy: cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="1f32e-167">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="1f32e-168">Tento projekt používal 2 moduly uzlu:</span><span class="sxs-lookup"><span data-stu-id="1f32e-168">This project used 2 node modules:</span></span>

* [<span data-ttu-id="1f32e-169">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-169">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="1f32e-170">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="1f32e-170">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="1f32e-171">Publikování webové aplikace do Azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-171">Publish the web application to Azure</span></span>

<span data-ttu-id="1f32e-172">Následuje několik kroků, které je potřeba provést.</span><span class="sxs-lookup"><span data-stu-id="1f32e-172">Below are the few steps we need to do</span></span>

* <span data-ttu-id="1f32e-173">Prvním krokem je vytvořit plán služby [Azure App Service](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="1f32e-173">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="1f32e-174">Do tohoto plánu můžete uložit několik webových aplikací.</span><span class="sxs-lookup"><span data-stu-id="1f32e-174">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="1f32e-175">Dále vytvoříme webovou aplikaci.</span><span class="sxs-lookup"><span data-stu-id="1f32e-175">Next we create a web app.</span></span> <span data-ttu-id="1f32e-176">V následujícím příkladu nahraďte <app_name> globálně jedinečným názvem aplikace (platné znaky jsou a–z, 0–9 a -).</span><span class="sxs-lookup"><span data-stu-id="1f32e-176">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="1f32e-177">Modul runtime je nastavený na NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="1f32e-177">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="1f32e-178">Pokud chcete zobrazit všechny podporované moduly runtime, spusťte příkaz az webapp list-runtimes.</span><span class="sxs-lookup"><span data-stu-id="1f32e-178">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="1f32e-179">Po vytvoření webové aplikace zobrazí Azure CLI výstup podobný následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="1f32e-179">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="1f32e-180">Přejděte do své nově vytvořené webové aplikace. Měla by se zobrazit funkční webová aplikace.</span><span class="sxs-lookup"><span data-stu-id="1f32e-180">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="1f32e-181">Nahraďte <app_name> jedinečným názvem aplikace.</span><span class="sxs-lookup"><span data-stu-id="1f32e-181">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="1f32e-182">Výše uvedený příkaz také vytvoří aplikaci s podporou Gitu, která umožňuje nasazení do Azure z místního Gitu.</span><span class="sxs-lookup"><span data-stu-id="1f32e-182">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="1f32e-183">Místní Git má nakonfigurovanou adresu URL https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.</span><span class="sxs-lookup"><span data-stu-id="1f32e-183">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="1f32e-184">Vytvořte uživatele nasazení. Po dokončení předchozího příkazu můžete do místního úložiště Git přidat vzdálené úložiště Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-184">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="1f32e-185">Nahraďte <url> adresou URL vzdáleného úložiště Git, kterou jste získali při povolení Gitu pro vaši aplikaci.</span><span class="sxs-lookup"><span data-stu-id="1f32e-185">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
<span data-ttu-id="1f32e-186">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-186">::: zone-end</span></span>

<span data-ttu-id="1f32e-187">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="1f32e-187">::: zone pivot="dotnet"</span></span>

## <a name="open-and-edit-the-solution"></a><span data-ttu-id="1f32e-188">Otevření a úprava řešení</span><span class="sxs-lookup"><span data-stu-id="1f32e-188">Open and edit the solution</span></span>

<span data-ttu-id="1f32e-189">Upravte soubor program.cs, abyste ukázku mohli spustit s konkrétním názvem trezoru klíčů:</span><span class="sxs-lookup"><span data-stu-id="1f32e-189">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="1f32e-190">Přejděte do složky key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="1f32e-190">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="1f32e-191">V sadě Visual Studio 2017 otevřete soubor key-vault-dotnet-core-quickstart.sln.</span><span class="sxs-lookup"><span data-stu-id="1f32e-191">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="1f32e-192">Otevřete soubor Program.cs a aktualizujte zástupný text *YourKeyVaultName* názvem dříve vytvořeného trezoru klíčů.</span><span class="sxs-lookup"><span data-stu-id="1f32e-192">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="1f32e-193">Toto řešení používá knihovny NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) a [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="1f32e-193">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="1f32e-194">Spuštění aplikace</span><span class="sxs-lookup"><span data-stu-id="1f32e-194">Run the app</span></span>

<span data-ttu-id="1f32e-195">V hlavní nabídce sady Visual Studio 2017 vyberte **Ladit** > **Spustit** bez ladění.</span><span class="sxs-lookup"><span data-stu-id="1f32e-195">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="1f32e-196">Jakmile se zobrazí prohlížeč, přejděte na stránku **O aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-196">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="1f32e-197">Zobrazí se hodnota **AppSecret**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-197">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="1f32e-198">Publikování webové aplikace do Azure</span><span class="sxs-lookup"><span data-stu-id="1f32e-198">Publish the web application to Azure</span></span>

<span data-ttu-id="1f32e-199">Publikujte tuto aplikaci do Azure, abyste ji viděli jako webovou aplikaci v ostrém provozu a zjistili, jestli můžete načíst hodnotu tajného kódu:</span><span class="sxs-lookup"><span data-stu-id="1f32e-199">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="1f32e-200">V sadě Visual Studio vyberte projekt **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-200">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="1f32e-201">Vyberte **Publikovat** > **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-201">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="1f32e-202">Vytvořte novou službu **App Service** a pak vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-202">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="1f32e-203">Změňte název aplikace na **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-203">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="1f32e-204">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="1f32e-204">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

<span data-ttu-id="1f32e-205">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-205">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="1f32e-206">Povolení identit spravované služby</span><span class="sxs-lookup"><span data-stu-id="1f32e-206">Enable managed service identities</span></span>

<span data-ttu-id="1f32e-207">Azure Key Vault nabízí možnost bezpečného ukládání přihlašovacích údajů a jiných klíčů a tajných kódů, ale váš kód se musí ověřit vůči službě Azure Key Vault, aby je mohl načíst.</span><span class="sxs-lookup"><span data-stu-id="1f32e-207">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="1f32e-208">Identita spravované služby to usnadňuje tím, že poskytuje službám Azure automaticky spravovanou identitu v Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1f32e-208">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="1f32e-209">Pomocí této identity se můžete ověřit vůči libovolné službě, která podporuje ověřování Azure AD, včetně služby Key Vault, aniž byste ve vašem kódu museli mít přihlašovací údaje.</span><span class="sxs-lookup"><span data-stu-id="1f32e-209">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="1f32e-210">Vraťte se k Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="1f32e-210">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="1f32e-211">Spuštěním příkazu assign-identity vytvořte identitu pro tuto aplikaci:</span><span class="sxs-lookup"><span data-stu-id="1f32e-211">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="1f32e-212">Příkaz v této proceduře je ekvivalentem přechodu na portál a nastavení **Identity spravované služby** na hodnotu **Zapnuto** ve vlastnostech webové aplikace.</span><span class="sxs-lookup"><span data-stu-id="1f32e-212">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="1f32e-213">Přiřazení oprávnění vaší aplikaci ke čtení tajných kódů z trezoru klíčů</span><span class="sxs-lookup"><span data-stu-id="1f32e-213">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="1f32e-214">Poznamenejte si výstup, který se zobrazí, když aplikaci publikujete do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-214">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="1f32e-215">Měl by mít následující formát:</span><span class="sxs-lookup"><span data-stu-id="1f32e-215">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="1f32e-216">Potom spusťte tento příkaz s použitím názvu vašeho trezoru klíčů a hodnoty **PrincipalId**:</span><span class="sxs-lookup"><span data-stu-id="1f32e-216">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="1f32e-217">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="1f32e-217">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="1f32e-218">Nasazení aplikace Node do Azure a načtení hodnoty tajného kódu</span><span class="sxs-lookup"><span data-stu-id="1f32e-218">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="1f32e-219">Teď je vše nastavené.</span><span class="sxs-lookup"><span data-stu-id="1f32e-219">Now that everything is set.</span></span> <span data-ttu-id="1f32e-220">Spuštěním následujícího příkazu nasaďte aplikaci do Azure.</span><span class="sxs-lookup"><span data-stu-id="1f32e-220">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="1f32e-221">Když teď přejdete na adresu https://<app_name>.azurewebsites.net, zobrazí se hodnota tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="1f32e-221">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="1f32e-222">Ujistěte se, že jste název <YourKeyVaultName> nahradili názvem vašeho trezoru.</span><span class="sxs-lookup"><span data-stu-id="1f32e-222">Make sure that you replaced the name <YourKeyVaultName> with your vault name ::: zone-end</span></span>

<span data-ttu-id="1f32e-223">::: zone pivot="dotnet" Když teď spustíte aplikaci, měla by se zobrazit načtená hodnota vašeho tajného kódu.</span><span class="sxs-lookup"><span data-stu-id="1f32e-223">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="1f32e-224">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-224">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="1f32e-225">Další kroky</span><span class="sxs-lookup"><span data-stu-id="1f32e-225">Next steps</span></span>

<span data-ttu-id="1f32e-226">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="1f32e-226">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="1f32e-227">Domovská stránka služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1f32e-227">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="1f32e-228">Dokumentace ke službě Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1f32e-228">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="1f32e-229">Azure SDK pro Node</span><span class="sxs-lookup"><span data-stu-id="1f32e-229">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="1f32e-230">[Reference k rozhraní Azure REST API](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-230">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="1f32e-231">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="1f32e-231">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="1f32e-232">Domovská stránka služby Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1f32e-232">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="1f32e-233">Dokumentace ke službě Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="1f32e-233">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="1f32e-234">Sada Azure SDK pro .NET</span><span class="sxs-lookup"><span data-stu-id="1f32e-234">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="1f32e-235">[Reference k rozhraní Azure REST API](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="1f32e-235">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>