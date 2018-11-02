---
title: MessageBox マクロ アクション
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f501b5884a8149850df7c1d16a141f345da90e52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925430"
---
# <a name="messagebox-macro-action"></a>MessageBox マクロ アクション


**適用されます**Access 2013、Office 2013。




" **MessageBox/メッセージボックス** " アクションを使用すると、警告または情報メッセージが含まれるメッセージ ボックスを表示できます。たとえば、" **MessageBox/メッセージボックス** " アクションは入力検査マクロで使用できます。コントロールまたはレコードがマクロの入力検査の条件に適合しない場合は、メッセージ ボックスが表示され、エラー メッセージと入力できるデータの種類に関する説明が示されます。

## <a name="setting"></a>設定

**MessageBox/メッセージボックス** アクションの引数は次のとおりです。

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
<td><p><strong>Message</strong></p></td>
<td><p>メッセージ ボックス内のテキストです。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>メッセージ</strong>] ボックスに、メッセージ テキストを入力します。255 文字までの文字列または式を入力できます (式の前には等号 (=) を付けます)。</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>メッセージが表示されるときにコンピューターのスピーカーから警告音を鳴らすかどうかを指定します。[<strong>はい</strong>] (警告音を鳴らす) または [<strong>いいえ</strong>] (警告音を鳴らさない) をクリックします。既定値は [<strong>はい</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>型</strong></p></td>
<td><p>メッセージ ボックスの種類を指定します。種類ごとにアイコンが異なります。[<strong>なし</strong>]、[<strong>警告</strong>]、[<strong>注意?</strong>]、[<strong>注意!</strong>]、または [<strong>情報</strong>] をクリックします。既定値は [<strong>なし</strong>] です。</p></td>
</tr>
<tr class="even">
<td><p><strong>タイトル</strong></p></td>
<td><p>メッセージ ボックスのタイトル バーに表示されるテキストです。 タイトル バーの表示を持つことができますたとえば、&quot;顧客 ID の検証&quot;。 この引数を空白のままにする場合は、 &quot;Access&quot;が表示されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

" **MessageBox/メッセージボックス** " アクションを使用すると、Microsoft Access によって表示される組み込みエラー メッセージに似た書式のエラー メッセージを作成できます。" **MessageBox/メッセージボックス** " アクションにより、"Message/メッセージ" 引数の 3 つのセクションにメッセージを入力できます。各セクションは "@" 記号で区切ります。

次の例では、書式設定されたメッセージ ボックスを表示します。このメッセージ ボックスのメッセージはセクションに分けられています。メッセージのテキストの最初のセクションは、太字の見出しとして表示されます。2 番目のセクションは、見出しの下にプレーン テキストとして表示されます。3 番目のセクションは、2 番目のセクションの下にプレーン テキストとして表示されます。2 番目のセクションと 3 番目のセクションの間には空白行が挿入されます。

" **Message/メッセージ** " 引数に次の文字列を入力します。

**間違ったボタン\!@This ボタンは、work.@Try は別です。**

Visual Basic for Applications (VBA) モジュールでは " **MessageBox/メッセージボックス** " アクションを実行することはできません。代わりに **MsgBox** 関数を使用します。

## <a name="examples"></a>例

**マクロによるフォームの同期**

次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。

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
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></p></td>
<td><p>画面の更新は停止しますが、マクロは実行されています。</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。 <strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: 仕入先を選択します。</p></td>
<td><p>[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: 会社名</p></td>
<td><p>フォーカスを [仕入先名] コントロールに移動します。</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>マクロを停止します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: 製品リストの<strong>表示</strong>: <strong>DatasheetFilter の名前</strong>: <strong>Where 条件式</strong>: [仕入先コード] = [Forms]![仕入先]![仕入先コード]<strong>データ モード</strong>:<strong>読み取り OnlyWindow モード</strong>:<strong>標準</strong></p></td>
<td><p>[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>右</strong>: 0.7799&quot; <strong>ダウン</strong>: 1.8&quot;</p></td>
<td><p>[製品リスト] を [仕入先] フォームの右下に配置します。</p></td>
</tr>
</tbody>
</table>


**マクロによるデータの入力検査**

次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。このマクロでは、" **StopMacro/マクロの中止** "、" **MessageBox/メッセージボックス** "、" **CancelEvent/イベントのキャンセル** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。その後、PostalCode コントロールに戻り、エラーを修正することができます。このマクロは "仕入先" フォームの " **BeforeUpdate/更新前処理** " プロパティに設定します。

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
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>[都道府県] の値が <strong>Null</strong> の場合は、郵便番号を検証できません。</p></td>
</tr>
<tr class="even">
<td><p>[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: 郵便番号のコードは 5 文字である必要があります。 <strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</p></td>
<td><p>郵便番号が 7 文字でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>コントロール名</strong>: [郵便番号]</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: 郵便番号のコードは 4 文字である必要があります。 <strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</p></td>
<td><p>郵便番号が 7 文字でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>コントロール名</strong>: [郵便番号]</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([都道府県] =&quot;カナダ&quot;)([郵便番号] が気に入らない&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: 郵便番号のコードが有効ではありません。 カナダのコードの例: H1J 1C 3<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号コードのエラー</p></td>
<td><p>[都道府県] が広島県で、郵便番号の上 3 桁が 720 ～ 739 でない場合にメッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>イベントを取り消します。</p></td>
</tr>
</tbody>
</table>

