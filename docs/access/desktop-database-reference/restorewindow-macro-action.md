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
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718834"
---
# <a name="restorewindow-macro-action"></a>RestoreWindow マクロ アクション

**適用されます**Access 2013、Office 2013。

**RestoreWindow**アクションを使用すると、元のサイズを最大化または最小化されたウィンドウを復元します。

> [!NOTE]
> [!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。

## <a name="setting"></a>設定値

**RestoreWindow**アクション引数はありません。

## <a name="remarks"></a>解説

この操作は、選択したオブジェクトに対して機能します。 オブジェクトが最小化されている場合、 **SelectObject**アクションを使用して選択して、 **RestoreWindow**アクションを使用して元のサイズに復元できます。

移動または復元したウィンドウのサイズは、 **MoveAndSizeWindow**アクションを使用できます。

**RestoreWindow**アクションは、ウィンドウの右上隅で [**復元**] ボタンをクリックするか、ウィンドウの**コントロール**メニューの [**復元**] コマンドをクリックすると同じです。

Visual Basic for Applications (VBA) モジュールに**RestoreWindow**アクションを実行するには、 **DoCmd**オブジェクトの**復元**方法を使用します。

