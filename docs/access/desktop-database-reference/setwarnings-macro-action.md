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
ms.openlocfilehash: 7642c7a727853005cb6cf664bf44f29bcd6e14ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997973"
---
# <a name="setwarnings-macro-action"></a>SetWarnings マクロ アクション

**適用されます**Access 2013、Office 2013。

**よって**を使用すると、システム メッセージを有効または無効にします。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。 

## <a name="setting"></a>設定値

**よって**では、次の引数があります。

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


## <a name="remarks"></a>解説

このアクションを使用すると、モーダルな通知やメッセージ ボックスによってマクロが停止しないようにすることができます。ただし、エラー メッセージは常に表示されます。また、[ **OK**]、[ **キャンセル**]、[ **はい**]、[ **いいえ**] などのボタンをクリックする以外に、テキストの入力やオプションの選択を必要とするダイアログ ボックスも表示されます。

"Warnings On/メッセージの表示" 引数を [ **いいえ**] に設定してこのアクションを実行すると、通知やメッセージ ボックスが表示されたときに **Enter** キーを押した場合と同じ動作になります。通常、通知やメッセージが表示された場合は、[ **OK**] ボタンまたは [ **はい**] ボタンを選択します。

マクロが完了すると、自動的にシステム メッセージの表示がオンに戻ります。

多くの場合、それが完了するまで、マクロの結果を非表示にする**エコー**のアクションでは、このアクションを使用します。 **よって**を使用すると、警告と同様のメッセージ ボックスを非表示にします。

> [!WARNING]
> **よって**がマクロとのやりとりを簡略化できますが、システム メッセージを無効にするには注意が必要です。 状況によっては、特定の警告メッセージが表示される場合は、マクロを続行するはありません。 しない限り、すべてのマクロ アクションの結果を確実に把握して、このアクションの使用を避ける必要があります。

実行するには**よって**を Visual Basic for Applications (VBA) モジュールで**DoCmd**オブジェクトの**SetWarnings**メソッドを使用します。

