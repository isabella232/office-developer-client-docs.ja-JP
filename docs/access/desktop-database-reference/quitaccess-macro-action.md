---
title: QuitAccess マクロ アクション
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 143ece00d7adb9b4011bd2fe92db069d8beec0e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617707"
---
# <a name="quitaccess-macro-action"></a>QuitAccess マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"QuitAccess/Accessの終了" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>オプション</strong></p></td>
<td><p>Access の終了時の未保存のオブジェクトに対する処理を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オプション</strong>] ボックスで、ダイアログ ボックスを表示してオブジェクトごとに保存するかどうかを指定する場合は [<strong>確認</strong>]、ダイアログ ボックスを表示せずにすべてのオブジェクトを保存する場合は [<strong>すべて保存</strong>]、オブジェクトを保存せずに終了する場合は [<strong>終了</strong>] をクリックします。既定値は [<strong>すべて保存</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

マクロ内で "QuitAccess/Accessの終了" アクションより後に設定されたアクションは実行されません。

You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.

This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.

You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.

To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.

