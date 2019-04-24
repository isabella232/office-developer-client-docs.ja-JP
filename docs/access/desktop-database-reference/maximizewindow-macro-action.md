---
title: MaximizeWindow マクロ アクション
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289750"
---
# <a name="maximizewindow-macro-action"></a>MaximizeWindow マクロ アクション

**適用先:** Access 2013、Office 2013

タブ付きドキュメントではなく、重なっているウィンドウを使用するように Access が構成されている場合は、[**最大化] ウィンドウ**アクションを使用してアクティブウィンドウを拡大し、access ウィンドウに表示されるようにすることができます。 このアクションを使用すると、アクティブ ウィンドウ内でのオブジェクトの表示範囲を拡大できます。

> [!NOTE]
> [!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。

## <a name="setting"></a>Setting

"MaximizeWindow/ウィンドウの最大化" アクションには、引数はありません。

## <a name="remarks"></a>注釈

This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.

You can use the **RestoreWindow** action to restore a maximized window to its previous size.

> [!TIP]
> - You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.
> - When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.

To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.

