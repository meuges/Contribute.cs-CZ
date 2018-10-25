---
title: Nadpisy v Markdownu
description: Popisuje požadavky na nadpisy v Markdownu.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084450"
---
# <a name="markdown-headings"></a>Nadpisy v Markdownu

Následující požadavky na ověření platí pro nadpisy v souborech Markdown OPS.

## <a name="h1"></a>H1

`H1` se vztahuje k prvnímu nadpisu v souboru Markdown. Při publikování na docs.microsoft.com se nadpis H1 zobrazí nahoře na stránce velkým písmem.

Nadpis H1 je tvořen úvodním řádkem s jedním znakem hash (`#`) a mezerou, po které následuje text nadpisu. Nadpis H1 například u tohoto článku je tento:

```md
# Markdown headings
```

Následující pravidla se vztahují k nadpisům H1:

- Nadpis H1 se musí nacházet v souboru.
- Může existovat pouze jeden nadpis H1.
- Nadpis H1 musí mít obsah.

  ```markdown
  # 
  This is not allowed.
  ```
- Mezi znakem `#` a obsahem nadpisu H1 musí být mezera. Nadpis H1 bez mezery se na publikované stránce nezobrazí jako nadpis.

  ```markdown
  #This looks bad on the site.
  ```
- Nadpis H1 musí být prvním obsahem v souboru za hlavičkou metadat YML. Mezi koncem hlavičky YML a nadpisem H1 není povolen žádný obsah, jako je text nebo obrázky.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- Nepoužívejte prvek HTML pro nadpisy první úrovně – `<h1>`. Použijte syntaxi Markdownu (`# `).
- Nadpis H1 nesmí být delší než 100 znaků. Toto je pokyn pro správný styl.

## <a name="h2---h6"></a>H2 – H6

V OPS jsou povoleny nadpisy H2 (`## `) až H6 (`###### `). K vytváření nadpisů používejte hlavičky Markdownu, nikoli HTML (`<h2>` - `<h6>`).
