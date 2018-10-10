---
title: "'StopAllMacros/全マクロの中止' マクロ アクション"
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 80da04f7b5f99fd0b249164caaeaca9f25edd172
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476278"
---
# <a name="stopallmacros-macro-action"></a>"StopAllMacros/全マクロの中止" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**中止**を使用すると、現在実行されているすべてのマクロを停止します。

## <a name="setting"></a>設定値

**中止**引数はありません。

## <a name="remarks"></a>解説

この操作は、エラー状態では、すべてのマクロを停止するために必要なときに使用します。 このアクションが定義されているマクロ内のアクション行に条件式を指定できます。 式は、 **True** (-1) に評価されると、Microsoft Access は、すべてのマクロを停止します。

などの他のマクロの実行を含む、複雑なアクションの数の 1 つとしてメッセージ ボックスを表示するマクロがあります。 ユーザーは、このメッセージ ボックスで**キャンセル**をクリックすると、**中止**は、実行されているすべてのマクロを停止できます。

マクロは、エコーやシステム メッセージの表示を有効にするのには**エコー** "や" **SetWarnings**アクションを使用するには場合、**中止**に自動的にオンに戻ります。

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。

