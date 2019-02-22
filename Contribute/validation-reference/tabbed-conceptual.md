# <a name="tabbed-conceptual"></a><span data-ttu-id="6dc14-101">Koncepce s kartami</span><span class="sxs-lookup"><span data-stu-id="6dc14-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6dc14-102">Syntaxe pro koncepci s kartami je zastaralá a nové karty by se neměly přidávat.</span><span class="sxs-lookup"><span data-stu-id="6dc14-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="6dc14-103">Ověřování popisovaná v tomto článku se týkají obsahových sad, u kterých bylo schváleno používání koncepce s kartami, než bude k dispozici nahrazující funkčnost.</span><span class="sxs-lookup"><span data-stu-id="6dc14-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="6dc14-104">Syntaxe karet</span><span class="sxs-lookup"><span data-stu-id="6dc14-104">Tab syntax</span></span>

<span data-ttu-id="6dc14-105">Syntaxe pro karty je následující:</span><span class="sxs-lookup"><span data-stu-id="6dc14-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="6dc14-106">Karta s jednou úrovní:</span><span class="sxs-lookup"><span data-stu-id="6dc14-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="6dc14-107">Volitelná závislá karta:</span><span class="sxs-lookup"><span data-stu-id="6dc14-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="6dc14-108">Příklad oddílu karet s jednou úrovní, ve kterém jsou dvě karty a ukončovací znak skupiny karet (---):</span><span class="sxs-lookup"><span data-stu-id="6dc14-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="6dc14-109">Karty můžou volitelně obsahovat sekundární (závislé) karty.</span><span class="sxs-lookup"><span data-stu-id="6dc14-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="6dc14-110">Tyto karty jsou závislé na výběru v jiné sadě karet.</span><span class="sxs-lookup"><span data-stu-id="6dc14-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="6dc14-111">Tady je příklad:</span><span class="sxs-lookup"><span data-stu-id="6dc14-111">Here's an example:</span></span>

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

<span data-ttu-id="6dc14-112">Následující ověřování se týkají syntaxe karet:</span><span class="sxs-lookup"><span data-stu-id="6dc14-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="6dc14-113">Syntaxe karet musí být správná.</span><span class="sxs-lookup"><span data-stu-id="6dc14-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="6dc14-114">Závislé karty se musí definovat v předchozí skupině karet.</span><span class="sxs-lookup"><span data-stu-id="6dc14-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="6dc14-115">Povoluje se jenom jedna úroveň závislosti.</span><span class="sxs-lookup"><span data-stu-id="6dc14-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="6dc14-116">Nepovoluje se méně než dvě karty.</span><span class="sxs-lookup"><span data-stu-id="6dc14-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="6dc14-117">Nepovoluje se více než čtyři karty.</span><span class="sxs-lookup"><span data-stu-id="6dc14-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="6dc14-118">Karty musí být v seznamu povolených karet.</span><span class="sxs-lookup"><span data-stu-id="6dc14-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="6dc14-119">Dvojice Název karty a ID karty musí být platné.</span><span class="sxs-lookup"><span data-stu-id="6dc14-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="6dc14-120">Stejné ID karty se nesmí v jedné skupině karet vyskytovat vícekrát.</span><span class="sxs-lookup"><span data-stu-id="6dc14-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="6dc14-121">Seznam povolených karet</span><span class="sxs-lookup"><span data-stu-id="6dc14-121">Tab whitelist</span></span>

<span data-ttu-id="6dc14-122">Následující dvojice Název karty a ID karty jsou v seznamu povolených karet.</span><span class="sxs-lookup"><span data-stu-id="6dc14-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="6dc14-123">ID závislých karet nejsou spárované, ale musí být platné ve sloupci ID karty.</span><span class="sxs-lookup"><span data-stu-id="6dc14-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="6dc14-124">V hodnotách se rozlišují malá a velká písmena.</span><span class="sxs-lookup"><span data-stu-id="6dc14-124">The values are case-sensitive</span></span>

|<span data-ttu-id="6dc14-125">Název karty</span><span class="sxs-lookup"><span data-stu-id="6dc14-125">Tab name</span></span>              |<span data-ttu-id="6dc14-126">ID karty</span><span class="sxs-lookup"><span data-stu-id="6dc14-126">Tab ID</span></span>            |
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