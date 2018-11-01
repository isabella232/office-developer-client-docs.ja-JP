---
title: "'RestoreWindow/ウィンドウを元のサイズに戻す' マクロ アクション"
TOCTitle: RestoreWindow Macro Action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e250bb94f77dd8cfc31c667e9562861b549c23c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875637"
---
# <a name="restorewindow-macro-action"></a>"RestoreWindow/ウィンドウを元のサイズに戻す" マクロ アクション


**適用されます**Access 2013、Office 2013。

**RestoreWindow**アクションを使用すると、元のサイズを最大化または最小化されたウィンドウを復元します。


> [!NOTE]
> <P>[!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 <STRONG>WindowState</STRONG> プロパティのトピックを参照してください。</P>



## <a name="setting"></a>設定値

**RestoreWindow**アクション引数はありません。

## <a name="remarks"></a>解説

この操作は、選択したオブジェクトに対して機能します。 オブジェクトが最小化されている場合、 **SelectObject**アクションを使用して選択して、 **RestoreWindow**アクションを使用して元のサイズに復元できます。

移動または復元したウィンドウのサイズは、 **MoveAndSizeWindow**アクションを使用できます。

**RestoreWindow**アクションは、ウィンドウの右上隅で [**復元**] ボタンをクリックするか、ウィンドウの**コントロール**メニューの [**復元**] コマンドをクリックすると同じです。

Visual Basic for Applications (VBA) モジュールに**RestoreWindow**アクションを実行するには、 **DoCmd**オブジェクトの**復元**方法を使用します。

