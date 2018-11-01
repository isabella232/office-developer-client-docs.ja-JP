---
title: SetValue マクロ アクション
TOCTitle: SetValue Macro Action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36dd3e511a3ff252ca44aa6d10fd1be4acd5c5fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878690"
---
# <a name="setvalue-macro-action"></a>SetValue マクロ アクション


**適用されます**Access 2013、Office 2013。


" **SetValue/値の代入** " アクションを使用すると、フォーム、フォーム データシート、またはレポートの Microsoft Access フィールド、コントロール、あるいはプロパティの値を設定できます。


> [!NOTE]
> <P>[!メモ] " <STRONG>SetValue/値の代入</STRONG> " アクションを使用して、オブジェクトを返す Access プロパティの値を設定することはできません。</P>




> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定

" **SetValue/値の代入** " アクションの引数は次のとおりです。

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
<td><p><strong>Item</strong></p></td>
<td><p>値を設定するフィールド、コントロール、またはプロパティの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>アイテム</strong>] ボックスに、フィールド、コントロール、またはプロパティの名前を入力します。このアイテムを参照するには、<em>controlname</em> (マクロが呼び出されたフォームまたはレポートのコントロールの場合)、<strong>Forms</strong>!<em>formname</em>!<em>controlname</em> など、完全な構文を使用する必要があります。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>このアイテムの値を設定するときに Access が使用する式を指定します。式のオブジェクトを参照するには、完全な構文を使用する必要があります。たとえば、Employees フォームの Salary コントロールの値を 10% 増やすには、Forms!Employees!Salary*1.1. を使用します。この引数は省略できません。</p>

> [!NOTE]
> <P>等号 (=) を使用するべきではありません (<STRONG>=</STRONG>) この引数の式の前にします。 場合は、アクセスが式を評価し、この引数の式としてこの値を使用します。 式が文字列の場合、予期しない結果が生じる。</P>


<p>入力する場合など<strong>=&quot;文字列 1&quot; </strong> 、この引数を最初に評価され文字列 1 として表現します。 [String1 コントロールまたはフォームやレポート、マクロと呼ばれることで、文字列 1 をという名前のプロパティを検索するため、この引数の式として使用します。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>[!メモ] Access データベース (.mdb または .accdb) では、[ <STRONG>ビルド</STRONG>] をクリックし、式ビルダーを使用して、この引数のどちらかに対して式を作成します。</P>



## <a name="remarks"></a>注釈

このアクションを使用すると、フォーム、フォーム データシート、またはレポートのフィールドあるいはコントロールに対して値を設定できます。また、任意のビューのほぼすべてのコントロール、フォーム、およびレポートのプロパティに値を設定することもできます。マクロを使用して特定のプロパティを設定できるかどうか、およびどのビューでプロパティを設定できるかを確認するには、Visual Basic エディターのそのプロパティに関するヘルプ トピックを参照してください。

フィールドに連結されたコントロールがフォームに含まれていない場合でも、フォームの基になるテーブル フィールドの値を設定できます。 **フォーム**の構文を使用して、\!*フォーム*\!このようなフィールドの値を設定する**項目**] ボックスで*フィールド名*です。 **レポート**の構文を使用して、レポートの基になるテーブル内のフィールドを参照することもできます\!*レポート名*\!*フィールド名*をこのフィールドにバインドされているレポート上のコントロールが存在する必要がありますかで、フィールドを参照する必要がありますが、レポートの演算コントロールです。

フォームのコントロールの値を設定する場合、" **SetValue/値の代入** " アクションでは、コントロールのフォームレベルの入力規則はトリガーされませんが、コントロールが連結コントロールの場合は、基になるフィールドのテーブルレベルの入力規則がトリガーされます。また、" **SetValue/値の代入** " アクションでは再計算もトリガーされます。ただし、この再計算はすぐには実行されません。すぐに再描画をトリガーし、再計算が強制的に行われるようにするには、" **RepaintObject/オブジェクトの再描画** " アクションを使用します。さらに、" **SetValue/値の代入** " アクションでコントロールに設定する値には、コントロールまたは基になるフィールドの **InputMask** プロパティで設定された定型入力は適用されません。

コントロールの **AfterUpdate** イベント プロパティによって指定されたマクロで " **SetValue/値の代入** " アクションを使用すると、そのコントロールの値を変更できます。ただし、コントロールの **BeforeUpdate** イベント プロパティで指定されたマクロで " **SetValue/値の代入** " アクションでは、そのコントロールの値を変更することはできません (ただし、" **SetValue/値の代入** " アクションを使用して、他のコントロールの値を変更することはできます)。また、フォームの **BeforeUpdate** または **AfterUpdate** プロパティで指定されたマクロで " **SetValue/値の代入** " アクションを使用して、カレント レコードのコントロールの値を変更することもできます。


> [!NOTE]
> <P>"<STRONG>SetValue/値の導入</STRONG>" アクションを使用して、次のコントロールの値を設定することはできません。</P>
> <UL>
> <LI>
> <P>レポートの連結コントロールおよび演算コントロール。</P>
> <LI>
> <P>フォームの演算コントロール。</P></LI></UL>




> [!TIP]
> <P>"<STRONG>SetValue/値の代入</STRONG>" アクションを使用すると、フォーム ビューのフォームを表示または非表示にできます。[<STRONG>アイテム</STRONG>] ボックスで <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> を、[<STRONG>式</STRONG>] ボックスで <STRONG>No</STRONG> または <STRONG>Yes</STRONG> を指定します。モーダル フォームの <STRONG>Visible</STRONG> プロパティを <STRONG>No</STRONG> に設定すると、フォームは非表示およびモードレスになります。このプロパティを <STRONG>Yes</STRONG> に表示すると、フォームは表示され、再度モーダルになります。</P>



マクロで " **SetValue/値の代入** " アクションを使用してコントロールの値を変更するか新しいデータを追加した場合、ユーザー インターフェイスのこれらのコントロールのデータを変更または入力するときに発生するイベント ( **BeforeUpdate** 、 **BeforeInsert** 、 **Change** など) はトリガーされません。これらのイベントは、Visual Basic for Applications (VBA) モジュールを使用してコントロールの値を設定しても発生しません。

このアクションは VBA モジュールでは使用できません。値は Visual Basic で直接設定します。

## <a name="example"></a>例

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

