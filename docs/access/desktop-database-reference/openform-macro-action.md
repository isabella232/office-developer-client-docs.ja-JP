---
title: OpenForm マクロ アクション
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c45f71ed079badfaa6843b5a12734bb82a2e553a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611911"
---
# <a name="openform-macro-action"></a>OpenForm マクロ アクション

**適用先**: Access 2013、Office 2013

" **OpenForm/フォームを開く** " アクションを使用すると、フォーム ビュー、フォーム デザイン ビュー、印刷プレビュー、またはデータシート ビューのいずれかで、フォームを開くことができます。フォームを開くときのデータ入力モードやウィンドウ モードの設定を行ったり、フォームで表示するレコードを制限したりできます。

## <a name="setting"></a>設定

**OpenForm/フォームを開く** アクションの引数は次のとおりです。

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
<td><p><strong>Form Name/フォーム名</strong></p></td>
<td><p>開くフォームの名前を指定します。 [マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>フォーム名</strong>] ボックスには、カレント データベース内のフォームがすべて表示されます。 この引数は省略できません。 ライブラリ データベースで "<strong>OpenForm/フォームを開く</strong>" アクションが定義されているマクロを実行すると、この名前のフォームが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>表示</strong></p></td>
<td><p>フォームを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>フォーム ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>データシート ビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>フォーム ビュー</strong>] です。  
 
</p><p><strong>メモ</strong>:<STRONG>引数 View は</STRONG>、フォームの DefaultView プロパティと<STRONG>ViewsAllowed</STRONG>プロパティの設定を上書きします。 <STRONG></STRONG> たとえば、フォームの "<STRONG>ViewsAllowed/ビュー設定</STRONG>" プロパティが [<STRONG>データシート</STRONG>] に設定されていても、"<STRONG>OpenForm/フォームを開く</STRONG>" アクションを使用すると、フォーム ビューでフォームを開くことができます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Filter Name/フィルター名</strong></p></td>
<td><p>フォームのレコードを制限するか並べ替えるフィルターを指定します。既存のクエリ名、またはクエリとして保存されているフィルターの名前を入力することができます。ただし、そのクエリでは、開こうとしているフォーム内のすべてのフィールドを含めるか、クエリの "<strong>OutputAllFields/全フィールド表示</strong>" プロパティを [<strong>はい</strong>] に設定する必要があります。</p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>フォームのSQLテーブルまたはクエリからレコードを選択するために Access が使用する WHERE 句 (WHERE という単語を含む) または式を指定します。 引数 Filter <strong>Name</strong> でフィルターを選択した場合、Access はフィルターの結果にこの WHERE 句を適用します。 フォームを開き、そのレコードを別のフォームのコントロールの値で指定されたレコードに制限するには、次の式<strong>を</strong>使用します。 [<em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>他のフォームの controlname</em><strong>]</strong> <em>フィールド</em>名を、開くフォームの基になるテーブルまたはクエリ内のフィールドの名前に置き換える。 他 <em>のフォームの formname</em> と <em>controlname</em> を他のフォームの名前と、最初のフォームのレコードに一致する値を含む他のフォームのコントロールを置き換える。</p><p><strong>注</strong>: 引数 <STRONG>Where Condition</STRONG> の最大長は 255 文字です。 これより長くて複雑な SQL WHERE 句を入力する必要がある場合は、代わりに Visual Basic for Applications (VBA) モジュールで、<STRONG>DoCmd</STRONG> オブジェクトの <STRONG>OpenForm</STRONG> メソッドを使用します。 VBA では、最大 32,768 バイトの SQL WHERE 句のステートメントを入力できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>フォームを開くときのデータ入力モードを指定します。 これはフォーム ビューまたはデータシート ビューで開いているフォームにのみ適用されます。 新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。 既定値は [ <strong>編集</strong>] です。 <strong>メモ</strong></p>
<ul>
<li><p>"<strong>Data Mode/データ モード</strong>" 引数の設定は、フォームの "<strong>AllowEdits/更新の許可</strong>"、"<strong>AllowDeletions/削除の許可</strong>"、"<strong>AllowAdditions/追加の許可</strong>"、および "<strong>DataEntry/データ入力用</strong>" プロパティの設定よりも優先されます。たとえば、フォームの "<strong>AllowEdits/更新の許可</strong>" プロパティが [<strong>いいえ</strong>] に設定されていても、"<strong>OpenForm/フォームを開く</strong>" アクションを使用すると、編集モードでフォームを開くことができます。</p></li>
<li><p>この引数を指定しないと、フォームは、そのフォームの "<strong>AllowEdits/更新の許可</strong>"、"<strong>AllowDeletions/削除の許可</strong>"、"<strong>AllowAdditions/追加の許可</strong>"、および "<strong>DataEntry/データ入力用</strong>" プロパティによって設定されたデータ入力モードで開きます。</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Window Mode/ウィンドウ モード</strong></p></td>
<td><p>フォームを開くときのウィンドウ モードを指定します。フォームのプロパティで設定されたモードで開く場合は [<strong>標準</strong>]、フォームを非表示にする場合は [<strong>非表示</strong>]、画面の下部に小さなタイトル バーにフォームを最小化する場合は [<strong>アイコン</strong>]、フォームの "<strong>Modal/作業ウィンドウ固定</strong>" および "<strong>PopUp/ポップアップ</strong>" プロパティを [<strong>はい</strong>] に設定する場合は [<strong>ダイアログ</strong>] をクリックします。既定値は [<strong>標準</strong>] です。</p><p><strong>注</strong>: タブ <STRONG>付きドキュメントを</STRONG> 使用する場合、一部のウィンドウ モードの引数設定は適用されません。 ウィンドウを重ねて表示するように切り替えるには、次の操作を行います。</p>
<ol>
<li><p>[ファイル] タブをクリックし、[オプション] <strong>をクリックします</strong>。</p></li>
<li><p>[ <strong>Access のオプション</strong>] ダイアログ ボックスの [ <strong>カレント データベース</strong>] をクリックします。</p></li>
<li><p>[<strong>アプリケーション オプション</strong>] の [<strong>ドキュメント ウィンドウ オプション</strong>] で [<strong>ウィンドウを重ねて表示する</strong>] をクリックします。</p></li>
<li><p>[<strong>OK</strong>] をクリックして、データベースを閉じて再度開きます。</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでフォームをダブルクリックした場合や、ナビゲーション ウィンドウでフォームを右クリックしてビューを選択した場合と同じです。

フォームは作業ウィンドウ固定 (モーダル) またはモードレスで使用できます。作業ウィンドウ固定 (モーダル) の場合、フォームを閉じるか非表示にしないとユーザーが他のアクションを実行できません。モードレスの場合は、フォームを開いたままユーザーが他のウィンドウに移動できます。また、ポップアップ フォームとしてフォームを開くこともできます。これは、情報の表示または収集に使用されるフォームで、常に他の Access ウィンドウよりも前面に表示されます。" **Modal/作業ウィンドウ固定** " または " **PopUp/ポップアップ** " プロパティは、フォームをデザインするときに設定します。" **Window Mode/ウィンドウ モード** " 引数に [ **標準**] を指定すると、フォームはこれらのプロパティの設定で指定されたモードで開きます。 **Window Mode/ウィンドウ モード** " 引数に [ **ダイアログ**] を指定すると、プロパティは両方とも [ **はい** ] に設定されます。非表示のフォームを表示した場合、またはアイコンとして開かれたフォームのサイズを元に戻した場合は、プロパティによって指定されたモードになります。

" **Window Mode/ウィンドウ モード** " 引数を [ **ダイアログ**] に設定してフォームを開くと、フォームが閉じるか非表示になるまでマクロが中断されます。フォームを非表示にするには、" **SetValue/値の代入** " アクションを使用して、 **Visible** プロパティを **No** に設定します。

> [!TIP]
> [!ヒント] フォームをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、フォームをフォーム ビューで開く " **OpenForm/フォームを開く** " アクションが自動的に作成されます。

フィルターおよび WHERE 条件式を指定すると、フォームの "**Filter/フィルター**" プロパティの設定値として使用されます。

## <a name="examples"></a>例

**マクロによるコントロールの値の設定**

次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクション</p></th>
<th><p>引数: 設定値</p></th>
<th><p>コメント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>いいえ</strong></p></td>
<td><p>マクロの実行中に画面の更新を停止します。</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>フォームオブジェクト名</strong>: 製品リスト<strong>保存</strong>: <strong>いいえ</strong></p></td>
<td><p>製品/サービス項目の一覧フォームを閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: 製品<strong>ビュー</strong>: <strong>フォームデータ モード</strong>: <strong>追加ウィンドウ モード</strong>: <strong>標準</strong></p></td>
<td><p>[商品] フォームを開きます。</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</p></td>
<td><p>[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p>"<strong>Control Name/コントロール名</strong>":商品コード</p></td>
<td><p>[カテゴリ ID] コントロールに移動します。</p></td>
</tr>
</tbody>
</table>


次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。

**マクロによるフォームの同期**

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
<td><p><strong>Echo On/エコーの設定</strong>: <strong>いいえ</strong></p></td>
<td><p>マクロの実行中に画面の更新を停止します。</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。 <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: サプライヤーの選択</p></td>
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
<td><p><strong>フォーム名</strong>: 製品一 <strong>覧ビュー</strong>: <strong>データシートフィルター名</strong>: <strong>条件</strong>: [SupplierID] = [Forms]![サプライヤー]![SupplierID] <strong>データ モード</strong>: <strong>読み取り専用Window モード</strong>: <strong>標準</strong></p></td>
<td><p>[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>右</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</p></td>
<td><p>[製品リスト] を [仕入先] フォームの右下に配置します。</p></td>
</tr>
</tbody>
</table>

