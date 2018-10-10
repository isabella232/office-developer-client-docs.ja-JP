---
title: "\"CancelEvent/イベントのキャンセル\" マクロ アクション"
TOCTitle: CancelEvent Macro Action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 52822d45b30c631dcabe3c38b6722398e96f489f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478763"
---
# <a name="cancelevent-macro-action"></a>"CancelEvent/イベントのキャンセル" マクロ アクション


**適用されます**Access 2013 |。Office 2013


" **CancelEvent/イベントのキャンセル** " アクションを使用して、このアクションが定義されたマクロが Access で実行される原因となったイベントを取り消すことができます。" **BeforeUpdate/更新前処理** "、" **OnOpen/開く時** "、" **OnUnload/読み込み解除時** "、" **OnPrint/印刷時** " などのイベント プロパティに、このマクロ名を設定します。

## <a name="setting"></a>設定値

**モーダル**引数はありません。

## <a name="remarks"></a>解説

フォームでは、通常に、 **BeforeUpdate**イベントのプロパティに入力検査マクロで**イベントのキャンセル**操作を使用します。 コントロールまたはレコードにデータを入力すると、ときに、データベースにデータを追加する前にマクロが実行されます。 データには、マクロの入力検査の条件が失敗した場合、**イベントのキャンセル**操作は、開始する前に更新処理をキャンセルします。

多くの場合、アクションを使用するこのアクションが**メッセージ ボックス**で、データの入力検査の条件が失敗したことを示すために、入力されるデータの種類に関する有用な情報を提供します。

次のイベントは、**イベントのキャンセル**操作をキャンセルできます。

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
> <P><STRONG>MouseDown</STRONG>イベントと<STRONG>イベントのキャンセル</STRONG>操作を使用するにはオブジェクトを右クリックしたときに発生するイベントをキャンセルするだけです。</P>



コントロールの**OnDblClick**イベント プロパティの設定は、**イベントのキャンセル**操作を含むマクロを指定する場合、アクションは、 **DblClick**イベントをキャンセルします。

取り消し可能なイベントでは、イベントのマクロが実行された後に、イベントの既定の動作 (イベント発生時の通常の動作) が実行されます。したがって、既定の動作を取り消すことができます。たとえば、テキスト ボックスでカーソル位置にある単語をダブルクリックすると、通常は、その単語が選択されます。 **DblClick** イベントのマクロで、この既定の動作を取り消し、テキスト ボックスのデータに関する情報を表示するフォームを開くなどの別のアクションを実行することができます。取り消し不可能なイベントでは、イベントのマクロが実行される前に、既定の動作が実行されます。


> [!NOTE]
> <P>フォームの<STRONG>OnUnload</STRONG>イベント プロパティは、<STRONG>イベントのキャンセル</STRONG>操作を実行するマクロを指定する場合、フォームを閉じることはできません。 <STRONG>イベントのキャンセル</STRONG>操作を実行するか、マクロを開くし、<STRONG>イベントのキャンセル</STRONG>操作を削除する原因となった条件を修正する必要がありますか。 フォームがモーダル フォームの場合は、マクロを開くことはできません。</P>



アクションを実行するには、**イベントのキャンセル**Visual Basic for Applications (VBA) のモジュールで、 **DoCmd**オブジェクトの**CancelEvent**メソッドを使用します。

## <a name="example"></a>使用例

マクロによるデータの入力検査

次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。 このマクロでは、" **StopMacro/マクロの中止** "、" **MessageBox/メッセージボックス** "、" **CancelEvent/イベントのキャンセル** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。 条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。 都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。 これは、し、郵便番号] コントロールに戻り、エラーを修正することができます。 このマクロは "仕入先" フォームの " **BeforeUpdate/更新前処理** " プロパティに設定します。

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
<th><p>コメント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IsNull([CountryRegion])</p></td>
<td><p>StopMacro</p></td>
<td><p></p></td>
<td><p>[都道府県] が<strong>Null</strong>の場合は、郵便番号を検証できません。</p></td>
</tr>
<tr class="even">
<td><p>[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len ([郵便番号]) &lt; &gt; 5</p></td>
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
<td><p>[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len ([郵便番号]) &lt; &gt; 4</p></td>
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
<td><p>([都道府県] =&quot;カナダ&quot;)([郵便番号] が気に入らない&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
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

