---
title: SetWarnings マクロ アクション
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0e25214d4ca7e6779efa127da71f63edef429e23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585320"
---
# <a name="setwarnings-macro-action"></a>SetWarnings マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **SetWarnings** action to turn system messages on or off.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"SetWarnings/メッセージの設定" アクションの引数は次のとおりです。

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
<td><p><strong>Warnings On/メッセージの表示</strong></p></td>
<td><p>システム メッセージを表示するかどうかを指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] にある [<strong>メッセージの表示</strong>] ボックスで、システム メッセージを表示する場合は [<strong>はい</strong>]、システム メッセージを表示しない場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>いいえ</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションを使用すると、モーダルな通知やメッセージ ボックスによってマクロが停止しないようにすることができます。ただし、エラー メッセージは常に表示されます。また、[ **OK**]、[ **キャンセル**]、[ **はい**]、[ **いいえ**] などのボタンをクリックする以外に、テキストの入力やオプションの選択を必要とするダイアログ ボックスも表示されます。

"Warnings On/メッセージの表示" 引数を [ **いいえ**] に設定してこのアクションを実行すると、通知やメッセージ ボックスが表示されたときに **Enter** キーを押した場合と同じ動作になります。通常、通知やメッセージが表示された場合は、[ **OK**] ボタンまたは [ **はい**] ボタンを選択します。

マクロが完了すると、自動的にシステム メッセージの表示がオンに戻ります。

Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished. You can use the **SetWarnings** action to hide the warnings and message boxes as well.

> [!WARNING]
> Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off. In some situations, you won't want to continue a macro if a certain warning message is displayed. Unless you're confident of the outcome of all macro actions, you should avoid using this action.

To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.

