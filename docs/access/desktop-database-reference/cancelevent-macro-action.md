---
title: CancelEvent マクロ アクション
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b55fc51f70bcc2c9d2f7e93cf9c79228cd2fe440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296634"
---
# <a name="cancelevent-macro-action"></a>CancelEvent マクロ アクション

**適用先:** Access 2013、Office 2013

" **CancelEvent/イベントのキャンセル** " アクションを使用して、このアクションが定義されたマクロが Access で実行される原因となったイベントを取り消すことができます。" **BeforeUpdate/更新前処理** "、" **OnOpen/開く時** "、" **OnUnload/読み込み解除時** "、" **OnPrint/印刷時** " などのイベント プロパティに、このマクロ名を設定します。

## <a name="setting"></a>Setting

"CancelEvent/イベントのキャンセル" アクションには、引数はありません。

## <a name="remarks"></a>注釈

In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property. When a user enters data in a control or record, Access runs the macro before adding the data to the database. If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.

Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.

The following events can be canceled by the **CancelEvent** action.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Exit</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filter</strong></p></td>
<td><p><strong>Open</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Format</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Delete</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.

If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.

取り消し可能なイベントでは、イベントのマクロが実行された後に、イベントの既定の動作 (イベント発生時の通常の動作) が実行されます。したがって、既定の動作を取り消すことができます。たとえば、テキスト ボックスでカーソル位置にある単語をダブルクリックすると、通常は、その単語が選択されます。 **DblClick** イベントのマクロで、この既定の動作を取り消し、テキスト ボックスのデータに関する情報を表示するフォームを開くなどの別のアクションを実行することができます。取り消し不可能なイベントでは、イベントのマクロが実行される前に、既定の動作が実行されます。

> [!NOTE]
> If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form. You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action. If the form is a modal form, you won't be able to open the macro.

To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.

## <a name="example"></a>例

マクロによるデータの入力検査

次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。このマクロでは、"StopMacro/マクロの中止"、"MessageBox/メッセージボックス"、"CancelEvent/イベントのキャンセル"、および "GoToControl/コントロールの移動" の各アクションの使い方を示します。条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。その後、[郵便番号] コントロールに戻り、エラーを修正することができます。このマクロは "仕入先" フォームの "BeforeUpdate/更新前処理" プロパティに設定します。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>条件</p></th>
<th><p>アクション</p></th>
<th><p>引数: 設定値</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull ([都道府県])</p></td>
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>If CountryRegion is <strong>Null</strong>, postal code can't be validated.</p></td>
</tr>
<tr class="even">
<td><p>地域In (&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) および Len ([郵便番号]) &lt; &gt; 5</p></td>
<td><p>MessageBox</p></td>
<td><p>"Message/メッセージ": 郵便番号は 7 文字である必要があります。 "Beep/警告音": <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </p></td>
<td><p>郵便番号が 7 文字でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>"Control Name/コントロール名": 郵便番号</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>地域In (&quot;オーストラリア&quot;、&quot;シンガポール&quot;) および Len ([郵便番号]) &lt; &gt; 4</p></td>
<td><p>MessageBox</p></td>
<td><p>"Message/メッセージ": 郵便番号は 7 文字である必要があります。 "Beep/警告音": <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </p></td>
<td><p>郵便番号が 7 文字でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>"Control Name/コントロール名": 郵便番号</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([都道府県] = &quot;カナダ&quot;)And ([郵便番号] Not Like&quot;[0-9] [0-9] [0-9] [0-9] ([a-z] [0-9]&quot;)</p></td>
<td><p>MessageBox</p></td>
<td><p>"Message/メッセージ": 郵便番号が無効です。たとえば、広島県の郵便番号の上 3 桁は 720 ～ 739 です。 Beep/警告音: <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </p></td>
<td><p>[都道府県] が広島県で、郵便番号の上 3 桁が 720 ～ 739 でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
</tbody>
</table>

