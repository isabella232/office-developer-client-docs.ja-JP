---
title: GoToControl マクロ アクション
TOCTitle: GoToControl Macro Action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2617544bf04aa0b26ccbb9d7ce8d7329d42ed1e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477725"
---
# <a name="gotocontrol-macro-action"></a>GoToControl マクロ アクション


**適用されます**Access 2013 |。Office 2013



" **GoToControl/コントロールの移動** " アクションを使用すると、開いているフォーム、フォームのデータシート、テーブルのデータシート、またはクエリのデータシートのカレント レコードの、指定したフィールドまたはコントロールにフォーカスを移動できます。このアクションにより、特定のフィールドまたはコントロールにフォーカスを移動することができます。このフィールドまたはコントロールは、比較を行ったり " **FindRecord/レコードの検索** " アクションを実行したりするときに使用します。また、このアクションを使用して、フォーム内を一定の条件に従って移動することもできます。たとえば、"健康保険" フォームの [既婚] コントロールに [いいえ] が設定されると、自動的に [配偶者またはパートナーの名前] コントロールをスキップして、次のコントロールにフォーカスを移動することができます。

## <a name="setting"></a>設定


> [!NOTE]
> <P>[!メモ] このアクションは、データ アクセス ページでは使用できません。</P>



" **GoToControl/コントロールの移動** " アクションの引数は次のとおりです。

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
<td><p><strong>コントロール名</strong></p></td>
<td><p>フォーカスの移動先のフィールドまたはコントロールの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>コントロール名</strong>] ボックスにフィールドまたはコントロールの名前を入力します。この引数は省略できません。  
 
</p>

> [!NOTE]
> <P>"<STRONG>Control Name/コントロール名</STRONG>" 引数には、完全な識別子 (<フォーム>!<製品>![製品 ID] など) ではなく、フィールドまたはコントロールの名前のみを入力してください。</P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

" **GoToControl/コントロールの移動** " アクションで、非表示のフォームのコントロールにフォーカスを移動することはできません。


> [!TIP]
> <P>[!ヒント] " <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使用すると、サブフォームに移動することもできます (サブフォームはコントロールの一種です)。移動後に、サブフォームの特定のレコードに移動するには、" <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使用します。" <STRONG>GoToControl/コントロールの移動</STRONG> " アクションを使って、サブフォームの特定のコントロールに移動することもできます。それには、サブフォームに移動してから、サブフォームのコントロールに移動します。</P>



Visual Basic for Applications (VBA) モジュールで " **GoToControl/コントロールの移動** " アクションを実行するには、 **DoCmd** オブジェクトの **GoToControl** メソッドを使用します。 **SetFocus** メソッドを使用して、フォームまたはフォームまたはそのサブフォームのコントロール、開いているテーブル、クエリ、またはフォーム データシートのフィールドにフォーカスを移動することもできます。

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
<th><p>コンポーネント</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></p></td>
<td><p>画面の更新は停止しますが、マクロは実行されています。</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></p></td>
<td><p>[製品リスト] フォームを閉じます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></p></td>
<td><p>[製品] フォームを開きます。</p></td>
</tr>
<tr class="even">
<td><p><strong>値の代入</strong></p></td>
<td><p><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</p></td>
<td><p>[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: CategoryID</p></td>
<td><p>[カテゴリ ID] コントロールに移動します。</p></td>
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
<td><p>[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len ([郵便番号]) &lt; &gt; 5</p></td>
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
<td><p>[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len ([郵便番号]) &lt; &gt; 4</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p>"Message/メッセージ": 郵便番号は 7 文字である必要があります。 <strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</p></td>
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

