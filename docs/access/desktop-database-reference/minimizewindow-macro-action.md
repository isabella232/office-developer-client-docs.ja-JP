---
title: MinimizeWindow マクロ アクション
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0afc47135ad5ba74fe8490d5046999a1111d7e3b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597213"
---
# <a name="minimizewindow-macro-action"></a>MinimizeWindow マクロ アクション

**適用先**: Access 2013、Office 2013

タブ付きドキュメントを使用せずにウィンドウを重ねて使用するように Access が構成されている場合、" **MinimizeWindow/ウィンドウの最小化** " アクションを使用してアクティブ ウィンドウを縮小し、Access ウィンドウの下部に小さなタイトル バーとして表示することができます。

> [!NOTE]
> [!メモ] このアクションは、Visual Basic Editor のコード ウィンドウには適用できません。コード ウィンドウへの影響の詳細については、 **WindowState** プロパティのトピックを参照してください。

## <a name="setting"></a>設定

"MinimizeWindow/ウィンドウの最小化" アクションには、引数はありません。

## <a name="remarks"></a>注釈

You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.

The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.

**ヒント**

- You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.

- To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.

- アクティブ ウィンドウを非表示にするには、[ **表示**] メニューの [ **このウィンドウの管理**] をクリックし、[ **表示しない**] をクリックします。この場合、ウィンドウは最小化されるのではなく、非表示になります。同じく [ **表示**] メニューの [ **再表示**] をクリックすると、ウィンドウを再度表示できます。これらのコマンドをマクロから実行するには、"RunMenuCommand/メニューコマンドの実行" アクションを使用します。

- You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.

To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.

