---
title: StopAllMacros マクロ アクション
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314477"
---
# <a name="stopallmacros-macro-action"></a>StopAllMacros マクロ アクション


**適用先:** Access 2013、Office 2013

"StopAllMacros/全マクロの中止" アクションを使用すると、現在実行中のすべてのマクロを中止できます。

## <a name="setting"></a>Setting

"StopAllMacros/全マクロの中止" アクションには、引数はありません。

## <a name="remarks"></a>注釈

通常、このアクションは、エラーが発生したためにすべてのマクロを中止する必要が生じた場合に使用します。このアクションが定義されているマクロ内のアクション行に条件式を指定できます。条件式の評価が True (–1) の場合、Microsoft Access はすべてのマクロを中止します。

For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.

If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。

