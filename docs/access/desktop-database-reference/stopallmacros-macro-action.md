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
ms.localizationpriority: medium
ms.openlocfilehash: 7a80017a58f0d0e1c1f9e50fbeb751e587822dcd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601787"
---
# <a name="stopallmacros-macro-action"></a>StopAllMacros マクロ アクション


**適用先**: Access 2013、Office 2013

"StopAllMacros/全マクロの中止" アクションを使用すると、現在実行中のすべてのマクロを中止できます。

## <a name="setting"></a>設定

"StopAllMacros/全マクロの中止" アクションには、引数はありません。

## <a name="remarks"></a>注釈

通常、このアクションは、エラーが発生したためにすべてのマクロを中止する必要が生じた場合に使用します。このアクションが定義されているマクロ内のアクション行に条件式を指定できます。条件式の評価が True (–1) の場合、Microsoft Access はすべてのマクロを中止します。

For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros. If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.

If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。

