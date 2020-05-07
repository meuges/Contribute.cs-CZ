---
title: Dokončování vývojářských jazyků – Balíček pro vytváření obsahu na webu Docs
description: Tady se dozvíte, jak dokončování vývojářských jazyků pomáhá přispěvatelům v Balíčku pro vytváření obsahu na webu Docs (rozšíření pro Visual Studio Code).
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336789"
---
# <a name="dev-lang-completion"></a>Dokončování vývojářských jazyků

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Shrnutí

Přispěvatelé potřebují pomoc při určování platných identifikátorů jazyků (vývojářských jazyků), které můžou následovat po trojitém zpětném apostrofu (otevření ohraničení kódu) v souboru Markdownu. Bohužel neexistuje ověřování vývojářských jazyků v době sestavování. Výsledkem jsou různorodé reprezentace jednoho jazyka v rámci stejné koncepční sady dokumentace.

Podívejme se například na C#. Přispěvatelé použili `c#`, `C#`, `cs`, `csharp` a jiné identifikátory jako reprezentace vývojářských jazyků tohoto jazyka. Které z předchozích reprezentací jsou správné?

Funkce *Dokončování vývojářských jazyků* do situace přináší řád a zobrazuje seznam známých vývojářských jazyků. Při výběru názvu vývojářského jazyka z IntelliSense:

* Ochranné ohraničení kódu se uzavře.
* Kurzor je umístěn v ohraničení kódu.

## <a name="preferences"></a>Předvolby

Tuto funkci není možné zakázat. K dispozici jsou následující nastavení:

* [Zobrazit běžně používané vývojářské jazyky](#display-commonly-used-dev-langs)
* [Zobrazit všechny známé vývojářské jazyky](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>Zobrazit běžně používané vývojářské jazyky

V jedné sadě dokumentace se použije jenom podmnožina platných vývojářských jazyků. Rozšíření možností uživatele:

1. V nástroji Visual Studio Code otevřete sadu dokumentace do kořenového adresáře.
1. Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.
1. Klikněte na odkaz **Upravit v settings.json** v oddílu **Markdown: Jazyky sady dokumentace**.
1. Do souboru *settings.json* přidejte následující vlastnost `markdown.docsetLanguages`:

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Umístěte kurzor do prázdného pole vlastnosti a aktivujte IntelliSense (přes <kbd>Ctrl</kbd> + <kbd>mezerník</kbd>). Zobrazí se seznam známých názvů vývojářských jazyků.
1. Přidávejte názvy vývojářských jazyků do pole, až bude seznam podle vašich představ. Například v následujícím seznamu se uživateli po zadání tří apostrofů zobrazí čtyři názvy vývojářských jazyků:

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. Uložte změny do souboru *settings.json*.

> [!WARNING]
> Prázdné pole `markdown.docsetLanguages` způsobí, že se zobrazí všechny známé vývojářské jazyky.

### <a name="display-all-known-dev-langs"></a>Zobrazit všechny známé vývojářské jazyky

Ve výchozím nastavení se v IntelliSense zobrazují všechny známé názvy vývojářských jazyků. Toto nastavení přepisuje vlastnost `markdown.docsetLanguages` popsanou v části [Zobrazit běžně používané vývojářské jazyky](#display-commonly-used-dev-langs).

Změna tohoto nastavení:

1. Vyberte **Soubor** > **Předvolby** > **Nastavení** a vyfiltrujte hodnoty podle *Rozšíření Docs Markdown*.
1. Přepněte nastavení v oddíle **Markdown: Všechny dostupné jazyky**.

## <a name="in-action"></a>V praxi

Tady vidíte krátkou ukázku této funkce:

[![Dokončování vývojářských jazyků](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
