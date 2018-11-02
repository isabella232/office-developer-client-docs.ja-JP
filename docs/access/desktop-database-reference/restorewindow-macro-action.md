---
title: RestoreWindow マクロ アクション
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb857e7eda7860150feb7af07babcc2574c3972f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929049"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow マクロ アクション


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

