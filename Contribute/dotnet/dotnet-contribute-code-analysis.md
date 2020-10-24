---
title: Přispívání do dokumentace pro pravidla analýzy kódu .NET do úložiště dokumentace platformy .NET
description: Tento článek popisuje postup, jak přispívat do článků a vzorového kódu pro pravidla analýzy kódu .NET v úložišti dokumentace platformy .NET.
author: mavasani
ms.author: mavasani
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 10/09/2020
ms.openlocfilehash: 27ae1a31c55c41aa1c97bf1f88dbf28bec35a80a
ms.sourcegitcommit: f1535713b66ff9b840f1138583746bc2bf182b4f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2020
ms.locfileid: "91957043"
---
# <a name="contribute-docs-for-net-code-analysis-rules-to-the-net-docs-repository"></a>Přispívání do dokumentace pro pravidla analýzy kódu .NET do úložiště dokumentace platformy .NET

Analyzátory platformy .NET Compiler Platform (Roslyn) kontrolují kód jazyka C# nebo Visual Basic z hlediska problémů s kvalitou a stylem kódu. Od verze .NET 5.0 jsou tyto analyzátory [obsažené v .NET SDK](/dotnet/fundamentals/code-analysis/overview).

- [Analýza kvality kódu (pravidla CAxxxx)](/dotnet/fundamentals/code-analysis/overview#code-quality-analysis):
  - Implementováno [tady](https://github.com/dotnet/roslyn-analyzers/tree/master/src/NetAnalyzers) v úložišti `dotnet/roslyn-analyzers`.
  - Dokumentováno [tady](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) v úložišti `dotnet/docs`. Podívejte se do části [Přispívání do dokumentace pro pravidla CAxxxx](#contribute-docs-for-caxxxx-rules).
- [Analýza stylu kódu (pravidla IDExxxx)](/dotnet/fundamentals/code-analysis/overview#code-style-analysis):
  - Implementováno [tady](https://github.com/dotnet/roslyn/tree/master/src/Analyzers) v úložišti `dotnet/roslyn`.
  - Dokumentováno [tady](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) v úložišti `dotnet/docs`. Podívejte se do části [Přispívání do dokumentace pro pravidla IDExxxx](#contribute-docs-for-idexxxx-rules).

## <a name="contribute-docs-for-caxxxx-rules"></a>Přispívání do dokumentace pro pravidla CAxxxx

Podle následujících pokynů můžete přispívat do dokumentace pro pravidla analýzy kvality kódu v úložišti [dotnet/docs](https://github.com/dotnet/docs):

1. Určete `Rule ID` a `Category`: Ujistěte se, že znáte ID a kategorii pravidla CAxxxx pro pravidlo, které má být dokumentováno. To znamená, že váš analyzátor CA byl sloučen do úložiště [dotnet/roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) nebo máte otevřené PR se schváleným ID a kategorií, která byla přiřazena k pravidlu.
2. Přidejte dokumentaci pravidla:
   1. Naklonujte existující soubor pravidla CA v [kořenové](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) složce, například `ca1000.md`, a změňte jeho název.
   2. Aktualizujte odpovídajícím způsobem obsah souboru.
3. Přidejte položku pro pravidlo do následujících tabulek:
   - V souboru [obsahu](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml) v seznamu kategorií pravidla. Například pro pravidlo CA s kategorií `Performance` vyhledejte v souboru výraz `- name: Performance rules` a přidejte položku do seznamu. Pokud žádný neexistuje, vytvořte nový seznam kategorií v části `- name: Code quality rules`.
   - V [indexovém souboru pravidel nejvyšší úrovně](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules/index.md).
   - V indexovém souboru pravidel založeném na kategorii `category`:
     1. Identifikujte indexový soubor založený na kategorii v [kořenové](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/quality-rules) složce. Například pro pravidlo CA s kategorií `Performance` má tento soubor název `performance-warnings.md`. Pokud žádný takový soubor neexistuje, vytvořte nový indexový soubor založený na kategorii naklonováním existujícího souboru.
     2. Přidejte do tohoto souboru položku pro ID pravidla.

> [!TIP]
> Vyhledejte v úložišti `dotnet/docs` známé, existující ID pravidla CA, abyste identifikovali potenciální místa, která mohou vyžadovat aktualizaci. Podívejte se například na <https://github.com/dotnet/docs/search?q=CA2000>.

## <a name="contribute-docs-for-idexxxx-rules"></a>Přispívání do dokumentace pro pravidla IDExxxx

Podle následujících pokynů můžete přispívat do dokumentace pro pravidla analýzy stylu kódu v úložišti [dotnet/docs](https://github.com/dotnet/docs):

1. Určete `Rule ID` a možnosti stylu kódu, pokud existují: Ujistěte se, že znáte ID pravidla IDExxxx a možnosti stylu kódu pro pravidlo, které má být dokumentováno. To znamená, že váš analyzátor IDE byl sloučen do úložiště [dotnet/roslyn](https://github.com/dotnet/roslyn) nebo máte otevřené PR se schváleným ID a možnostmi stylu kódu, které byly přiřazeny k pravidlu.
2. Určete `subcategory` pro pravidlo: Pravidla IDE mají kategorii `Style`. Určete podkategorii pravidla podle postupu, který si můžete přečíst v úvodní části článku o [pravidlech stylu kódu](/dotnet/fundamentals/code-analysis/style-rules/index). Většina pravidel stylu kódu IDE patří do podkategorie `Language`.
3. Určete `preference group` pro pravidlo: Určete `preference group` pro pravidlo tak, že si přečtete záhlaví předvoleb [tady](/dotnet/fundamentals/code-analysis/style-rules/language-rules#net-style-rules).
   - Pokud má pravidlo známé, přidružené možnosti stylu kódu, bude skupina předvoleb odpovídat skupině `OptionGroup` uvedené v deklaraci možnosti stylu kódu.
   - V opačném případě určete, jestli pravidlo patří do existující skupiny předvoleb, nebo potřebuje novou skupinu předvoleb.
4. Přidejte dokumentaci pravidla:
   1. Naklonujte existující soubor pravidla IDE v [kořenové](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) složce, například `ide0011.md`, a změňte jeho název.
   2. Aktualizujte odpovídajícím způsobem obsah souboru.
5. Přidejte položku pro pravidlo IDE nebo možnosti stylu kódu do následujících tabulek:
   - V souboru [obsahu](https://github.com/dotnet/docs/blob/master/docs/fundamentals/toc.yml) v podkategorii pravidla a seznamu předvoleb. Například pro pravidlo stylu kódu IDE s podkategorií `Language` a skupinou `Modifier preferences` vyhledejte v souboru výraz `- name: Language rules` a podřízený uzel `- name: Modifier preferences` a přidejte položku do seznamu. Pokud seznam podkategorií nebo seznam předvoleb v podkategorii neexistuje, vytvořte nový v části `- name: Code style rules`.
   - V [indexovém souboru založeném na možnostech stylu kódu](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/language-rules.md).
   - V [indexovém souboru pravidla založeném na ID](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules/index.md).
   - V indexovém souboru pravidla založeném na `preferences group`:
     1. V [kořenové](https://github.com/dotnet/docs/blob/master/docs/fundamentals/code-analysis/style-rules) složce identifikujte indexový soubor založený na skupině předvoleb. Například pro pravidlo IDE pro `Modifier preferences` má tento soubor název `modifier-preferences.md`. Pokud žádný takový soubor neexistuje, vytvořte nový indexový soubor založený na skupině předvoleb klonováním existujícího souboru.
     2. Přidejte do tohoto souboru položku pro ID pravidla.

> [!TIP]
> Vyhledejte v úložišti `dotnet/docs` známé, existující pravidlo IDE nebo možnosti stylu kódu, abyste identifikovali potenciální místa, která mohou vyžadovat aktualizaci. Podívejte se například na <https://github.com/dotnet/docs/search?q=IDE0011> a <https://github.com/dotnet/docs/search?q=csharp_prefer_braces>.

## <a name="see-also"></a>Viz také

- [Psaní příspěvků do úložišť dokumentace k .NET](dotnet-contribute.md)
