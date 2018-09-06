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
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308817"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Rychlý start: Nastavení a načtení tajného kódu ze služby Azure Key Vault

V tomto rychlém startu se dozvíte, jak uložit tajný kód do trezoru klíčů a jak ho načíst pomocí webové aplikace. Pokud chcete zobrazit hodnotu tajného kódu, musíte webovou aplikaci spustit v Azure. V tomto rychlém startu se používá Node.js a identity spravovaných služeb (MSI).

> [!div class="checklist"]
> * Vytvoření trezoru klíčů
> * Uložení tajného kódu do trezoru klíčů
> * Načtení tajného kódu z trezoru klíčů
> * Vytvoření webové aplikace Azure
> * [Povolení identit spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)
> * Udělení požadovaných oprávnění webové aplikaci ke čtení dat z trezoru klíčů

Než budete pokračovat, ujistěte se, že znáte [základní koncepty](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

> [!NOTE]
> Abyste pochopili, proč následující kurz představuje osvědčený postup, je potřeba porozumět několika konceptům. Trezor klíčů je centrální úložiště sloužící k programovému ukládání tajných kódů. Aby to bylo možné, musí se aplikace nebo uživatelé nejprve vůči trezoru klíčů ověřit, tedy předložit tajný kód. Kvůli dodržování osvědčených postupů zabezpečení se navíc tento první tajný kód musí pravidelně obměňovat. Při použití [Identity spravované služby](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) se však aplikacím spouštěným v Azure udělí identita, kterou automaticky spravuje Azure. To pomůže vyřešit **problém se zavedením tajného kódu**, takže uživatelé a aplikace budou dodržovat osvědčené postupy bez starostí o obměňování prvního tajného kódu.

## <a name="prerequisites"></a>Požadavky

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"
* [Visual Studio 2017 verze 15.7.3 nebo novější](https://www.microsoft.com/net/download/windows) s následujícími úlohami:
  * Vývoj pro ASP.NET a web
  * Vývoj pro různé platformy pomocí rozhraní .NET Core
* [Sada .NET Core 2.1 SDK nebo novější](https://www.microsoft.com/net/download/windows) ::: zone-end
* Git ([stáhnout](https://git-scm.com/downloads)).
* Předplatné Azure. Pokud předplatné Azure ještě nemáte, vytvořte si [bezplatný účet](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) předtím, než začnete.
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) verze 2.0.4 nebo novější. K dispozici pro Windows, Mac a Linux.

## <a name="login-to-azure"></a>Přihlášení k Azure

Pokud se chcete přihlásit k Azure pomocí rozhraní příkazového řádku, můžete zadat:

```azurecli
az login
```

## <a name="create-resource-group"></a>Vytvoření skupiny prostředků

Vytvořte skupinu prostředků pomocí příkazu [az group create](/cli/azure/group#az-group-create). Skupina prostředků Azure je logický kontejner, ve kterém se nasazují a spravují prostředky Azure.

Vyberte název skupiny prostředků a nahraďte zástupný text.
Následující příklad vytvoří skupinu prostředků s názvem *<YourResourceGroupName>* v umístění *eastus*.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

V tomto kurzu se používá skupina prostředků, kterou jste právě vytvořili.

## <a name="create-an-azure-key-vault"></a>Vytvoření trezoru klíčů Azure

Dále s použitím skupiny prostředků vytvořené v předchozím kroku vytvoříte trezor klíčů. Přestože se v tomto článku jako název pro trezor klíčů používá ContosoKeyVault, musíte použít jedinečný název. Zadejte tyto údaje:

* Název trezoru – **tady vyberte název trezoru klíčů**.
* Název skupiny prostředků – **tady vyberte název skupiny prostředků**.
* Umístění – **Východní USA**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

V tuto chvíli je váš účet Azure jediným účtem autorizovaným k provádění jakýchkoli operací s tímto novým trezorem.

## <a name="add-a-secret-to-key-vault"></a>Přidání tajného kódu do trezoru klíčů

Tajný kód přidáváme proto, abychom ukázali, jak to funguje. Mohli byste uložit připojovací řetězec SQL nebo jakýkoli jiný údaj, který potřebujete udržet v tajnosti, ale zároveň zpřístupnit vaší aplikaci. V tomto kurzu se heslo bude označovat jako **AppSecret** a bude v něm uložená hodnota **MySecret**.

Zadáním následujících příkazů vytvořte v trezoru klíčů tajný kód **AppSecret**, který bude uchovávat hodnotu **MySecret**:

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Hodnotu v tajném kódu zobrazíte jako prostý text takto:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Tento příkaz zobrazí informace o tajném kódu včetně identifikátoru URI. Po dokončení tohoto postupu byste měli mít identifikátor URI v tajném kódu ve službě Azure Key Vault. Tento údaj si poznamenejte. Budete ho potřebovat později.

## <a name="clone-the-repo"></a>Klonování úložiště

Spuštěním následujícího příkazu naklonujte úložiště, abyste získali místní kopii umožňující úpravu zdroje:

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Instalace závislostí

Teď nainstalujeme závislosti. Spusťte následující příkazy: cd key-vault-node-quickstart npm install

Tento projekt používal 2 moduly uzlu:

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Publikování webové aplikace do Azure

Následuje několik kroků, které je potřeba provést.

* Prvním krokem je vytvořit plán služby [Azure App Service](https://azure.microsoft.com/services/app-service/). Do tohoto plánu můžete uložit několik webových aplikací.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Dále vytvoříme webovou aplikaci. V následujícím příkladu nahraďte <app_name> globálně jedinečným názvem aplikace (platné znaky jsou a–z, 0–9 a -). Modul runtime je nastavený na NODE|6.9. Pokud chcete zobrazit všechny podporované moduly runtime, spusťte příkaz az webapp list-runtimes.

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Po vytvoření webové aplikace zobrazí Azure CLI výstup podobný následujícímu příkladu:

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
    Přejděte do své nově vytvořené webové aplikace. Měla by se zobrazit funkční webová aplikace. Nahraďte <app_name> jedinečným názvem aplikace.

    ```text
    http://<app name>.azurewebsites.net
    ```
    Výše uvedený příkaz také vytvoří aplikaci s podporou Gitu, která umožňuje nasazení do Azure z místního Gitu. 
    Místní Git má nakonfigurovanou adresu URL https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git.

* Vytvořte uživatele nasazení. Po dokončení předchozího příkazu můžete do místního úložiště Git přidat vzdálené úložiště Azure. Nahraďte <url> adresou URL vzdáleného úložiště Git, kterou jste získali při povolení Gitu pro vaši aplikaci.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>Otevření a úprava řešení

Upravte soubor program.cs, abyste ukázku mohli spustit s konkrétním názvem trezoru klíčů:

1. Přejděte do složky key-vault-dotnet-core-quickstart.
2. V sadě Visual Studio 2017 otevřete soubor key-vault-dotnet-core-quickstart.sln.
3. Otevřete soubor Program.cs a aktualizujte zástupný text *YourKeyVaultName* názvem dříve vytvořeného trezoru klíčů.

Toto řešení používá knihovny NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) a [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).

## <a name="run-the-app"></a>Spuštění aplikace

V hlavní nabídce sady Visual Studio 2017 vyberte **Ladit** > **Spustit** bez ladění. Jakmile se zobrazí prohlížeč, přejděte na stránku **O aplikaci**. Zobrazí se hodnota **AppSecret**.

## <a name="publish-the-web-application-to-azure"></a>Publikování webové aplikace do Azure

Publikujte tuto aplikaci do Azure, abyste ji viděli jako webovou aplikaci v ostrém provozu a zjistili, jestli můžete načíst hodnotu tajného kódu:

1. V sadě Visual Studio vyberte projekt **key-vault-dotnet-core-quickstart**.
2. Vyberte **Publikovat** > **Spustit**.
3. Vytvořte novou službu **App Service** a pak vyberte **Publikovat**.
4. Změňte název aplikace na **keyvaultdotnetcorequickstart**.
5. Vyberte **Vytvořit**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>Povolení identit spravované služby

Azure Key Vault nabízí možnost bezpečného ukládání přihlašovacích údajů a jiných klíčů a tajných kódů, ale váš kód se musí ověřit vůči službě Azure Key Vault, aby je mohl načíst. Identita spravované služby to usnadňuje tím, že poskytuje službám Azure automaticky spravovanou identitu v Azure Active Directory (Azure AD). Pomocí této identity se můžete ověřit vůči libovolné službě, která podporuje ověřování Azure AD, včetně služby Key Vault, aniž byste ve vašem kódu museli mít přihlašovací údaje.

1. Vraťte se k Azure CLI.
2. Spuštěním příkazu assign-identity vytvořte identitu pro tuto aplikaci:

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>Příkaz v této proceduře je ekvivalentem přechodu na portál a nastavení **Identity spravované služby** na hodnotu **Zapnuto** ve vlastnostech webové aplikace.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Přiřazení oprávnění vaší aplikaci ke čtení tajných kódů z trezoru klíčů

Poznamenejte si výstup, který se zobrazí, když aplikaci publikujete do Azure. Měl by mít následující formát:

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Potom spusťte tento příkaz s použitím názvu vašeho trezoru klíčů a hodnoty **PrincipalId**:

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Nasazení aplikace Node do Azure a načtení hodnoty tajného kódu

Teď je vše nastavené. Spuštěním následujícího příkazu nasaďte aplikaci do Azure.

```bash
git push azure master
```

Když teď přejdete na adresu https://<app_name>.azurewebsites.net, zobrazí se hodnota tajného kódu.
Ujistěte se, že jste nahradili název <YourKeyVaultName> názvem vašeho trezoru.

::: zone-end

::: zone pivot="dotnet" Když teď spustíte aplikaci, měla by se zobrazit načtená hodnota vašeho tajného kódu.
::: zone-end

## <a name="next-steps"></a>Další kroky

::: zone pivot="nodejs"
* [Domovská stránka služby Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Dokumentace ke službě Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK pro Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Reference k rozhraní Azure REST API](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end

::: zone pivot="dotnet"
* [Domovská stránka služby Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Dokumentace ke službě Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [Sada Azure SDK pro .NET](https://github.com/Azure/azure-sdk-for-net)
* [Reference k rozhraní Azure REST API](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end
