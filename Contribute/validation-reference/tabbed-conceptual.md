---
ms.date: 03/29/2019
title: Koncepce s kartami
ms.openlocfilehash: 3d6f38c1659297182a8bd50bf52b9853bd21b2c8
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841284"
---
# <a name="tabbed-conceptual"></a><span data-ttu-id="0119a-102">Koncepce s kartami</span><span class="sxs-lookup"><span data-stu-id="0119a-102">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0119a-103">Syntaxe pro koncepci s kartami je zastaralá a nové karty by se neměly přidávat.</span><span class="sxs-lookup"><span data-stu-id="0119a-103">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="0119a-104">Ověřování popisovaná v tomto článku se týkají obsahových sad, u kterých bylo schváleno používání koncepce s kartami, než bude k dispozici nahrazující funkčnost.</span><span class="sxs-lookup"><span data-stu-id="0119a-104">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="0119a-105">Syntaxe karet</span><span class="sxs-lookup"><span data-stu-id="0119a-105">Tab syntax</span></span>

<span data-ttu-id="0119a-106">Syntaxe pro karty je následující:</span><span class="sxs-lookup"><span data-stu-id="0119a-106">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="0119a-107">Karta s jednou úrovní:</span><span class="sxs-lookup"><span data-stu-id="0119a-107">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="0119a-108">Volitelná závislá karta:</span><span class="sxs-lookup"><span data-stu-id="0119a-108">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="0119a-109">Příklad oddílu karet s jednou úrovní, ve kterém jsou dvě karty a ukončovací znak skupiny karet (---):</span><span class="sxs-lookup"><span data-stu-id="0119a-109">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="0119a-110">Karty můžou volitelně obsahovat sekundární (závislé) karty.</span><span class="sxs-lookup"><span data-stu-id="0119a-110">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="0119a-111">Tyto karty jsou závislé na výběru v jiné sadě karet.</span><span class="sxs-lookup"><span data-stu-id="0119a-111">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="0119a-112">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="0119a-112">Here's an example:</span></span>

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

<span data-ttu-id="0119a-113">Následující ověřování se týkají syntaxe karet:</span><span class="sxs-lookup"><span data-stu-id="0119a-113">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="0119a-114">Syntaxe karet musí být správná.</span><span class="sxs-lookup"><span data-stu-id="0119a-114">Tab syntax must be correct.</span></span>
- <span data-ttu-id="0119a-115">Závislé karty se musí definovat v předchozí skupině karet.</span><span class="sxs-lookup"><span data-stu-id="0119a-115">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="0119a-116">Povoluje se jenom jedna úroveň závislosti.</span><span class="sxs-lookup"><span data-stu-id="0119a-116">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="0119a-117">Nepovoluje se méně než dvě karty.</span><span class="sxs-lookup"><span data-stu-id="0119a-117">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="0119a-118">Nepovoluje se více než čtyři karty.</span><span class="sxs-lookup"><span data-stu-id="0119a-118">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="0119a-119">Karty musí být schválené.</span><span class="sxs-lookup"><span data-stu-id="0119a-119">Tabs must be approved.</span></span>
- <span data-ttu-id="0119a-120">Dvojice Název karty a ID karty musí být platné.</span><span class="sxs-lookup"><span data-stu-id="0119a-120">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="0119a-121">Stejné ID karty se nesmí v jedné skupině karet vyskytovat vícekrát.</span><span class="sxs-lookup"><span data-stu-id="0119a-121">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="approved-tabs"></a><span data-ttu-id="0119a-122">Schválené karty</span><span class="sxs-lookup"><span data-stu-id="0119a-122">Approved tabs</span></span>

<span data-ttu-id="0119a-123">Následující dvojice Název karty a ID karty jsou schválené.</span><span class="sxs-lookup"><span data-stu-id="0119a-123">The following tab name/tab ID pairs are approved.</span></span> <span data-ttu-id="0119a-124">ID závislých karet nejsou spárované, ale musí být platné ve sloupci ID karty.</span><span class="sxs-lookup"><span data-stu-id="0119a-124">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="0119a-125">V hodnotách se rozlišují malá a velká písmena.</span><span class="sxs-lookup"><span data-stu-id="0119a-125">The values are case-sensitive</span></span>

|<span data-ttu-id="0119a-126">Název karty</span><span class="sxs-lookup"><span data-stu-id="0119a-126">Tab name</span></span>              |<span data-ttu-id="0119a-127">ID karty</span><span class="sxs-lookup"><span data-stu-id="0119a-127">Tab ID</span></span>            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |