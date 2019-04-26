---
title: SetValue マクロ アクション
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306819"
---
# <a name="setvalue-macro-action"></a>SetValue マクロ アクション

**適用先:** Access 2013、Office 2013

" **SetValue/値の代入** " アクションを使用すると、フォーム、フォーム データシート、またはレポートの Microsoft Access フィールド、コントロール、あるいはプロパティの値を設定できます。

> [!NOTE]
> - [!メモ] " **SetValue/値の代入** " アクションを使用して、オブジェクトを返す Access プロパティの値を設定することはできません。
> - このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"**SetValue/値の代入**" アクションの引数は次のとおりです。

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
<td><p>Access がこのアイテムの値を設定するために使う式。 式の中のオブジェクトを参照するには、常に完全な構文を使う必要があります。 たとえば、Employees フォームの Salary コントロールの値を 10% 増やすには、Forms!Employees!Salary*1.1 を使用します。 これは必須の引数です。</p><p><strong>注</strong>: この引数の式の前に等号 (=) を付けてはなりません。 等号を付けると、Access は式を評価し、その値をこの引数の式として使用します。 その式が文字列の場合、予期しない結果になる可能性があります。</p>
<p>たとえば、この引数に「<strong>=&quot;String1&quot;</strong>」と入力すると、Access は最初にこの式を "String1" と評価します。 その後、"String1" をこの引数の式として使うので、マクロを呼び出したフォームまたはレポート上の String1 という名前のコントロールまたはプロパティを検索することが予想されます。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Access データベース (.mdb または .accdb) では、これらの引数の式を作成するには、[**ビルド**] ボタンをクリックして式ビルダーを使います。

## <a name="remarks"></a>解説

このアクションを使って、フォーム、フォーム データシート、レポート上のフィールドまたはコントロールの値を設定できます。また、ビューのほぼすべてのコントロール、フォーム、レポートのプロパティの値を設定することもできます。マクロを使って特定のプロパティを設定できるかどうか、および設定できるビューについては、Visual Basic エディターでそのプロパティのヘルプ トピックを参照してください。

また、フィールドにバインドされたコントロールがフォームに含まれない場合でも、フォームの基になっているテーブルのフィールドの値を設定できます。 そのようなフィールドの値を設定するには、**[アイテム]** ボックスで **Forms**\!*formname*\!*fieldname* という構文を使用します。 また、**Reports**\!*reportname*\!*fieldname* という構文を使うことでレポートの基になっているテーブルのフィールドを参照することもできますが、このフィールドにバインドされたコントロールがレポート上に存在するか、またはレポートの演算コントロールでフィールドが参照されている必要があります。

フォームのコントロールの値を設定する場合、" **SetValue/値の代入** " アクションでは、コントロールのフォームレベルの入力規則はトリガーされませんが、コントロールが連結コントロールの場合は、基になるフィールドのテーブルレベルの入力規則がトリガーされます。また、" **SetValue/値の代入** " アクションでは再計算もトリガーされます。ただし、この再計算はすぐには実行されません。すぐに再描画をトリガーし、再計算が強制的に行われるようにするには、" **RepaintObject/オブジェクトの再描画** " アクションを使用します。さらに、" **SetValue/値の代入** " アクションでコントロールに設定する値には、コントロールまたは基になるフィールドの **InputMask** プロパティで設定された定型入力は適用されません。

コントロールの値を変更するには、コントロールの **AfterUpdate** イベント プロパティによって指定されているマクロで **"SetValue/値の代入"** アクションを使います。ただし、コントロールの **BeforeUpdate** イベント プロパティで指定されているマクロで **"SetValue/値の代入"** アクションを使って、コントロールの値を変更することはできません (ただし、**"SetValue/値の代入"** アクションを使って、他のコントロールの値を変更することはできます)。また、フォームの **BeforeUpdate** または **AfterUpdate** プロパティによって指定されたマクロで **"SetValue/値の代入"** アクションを使って、現在のレコードのコントロールの値を変更することもできます。

> [!NOTE]
> "**SetValue/値の導入**" アクションを使用して、次のコントロールの値を設定することはできません。
> - レポート上のバインドされたコントロールおよび演算コントロール
> - フォーム上の演算コントロール

> [!TIP]
> **SetValue** アクションを使用して、フォーム ビューのフォームの表示または非表示を設定できます。 **[アイテム]** ボックスで **Forms**!*formname***.Visible** を、**[式]** ボックスで **No** または **Yes** を指定します。 モーダル フォームの **Visible** プロパティを **No** に設定すると、フォームは非表示およびモードレスになります。 このプロパティを **Yes** に表示すると、フォームは表示され、再度モーダルになります。

マクロで **"SetValue/値の代入"** アクションを使って、コントロールの値を変更したり、コントロールに新しいデータを追加しても、**BeforeUpdate**、**BeforeInsert**、**Change** などのイベントはトリガーされません。これらのイベントは、ユーザー インターフェイスでこれらのコントロールのデータを変更または入力すると発生します。また、これらのイベントは、Visual Basic for Applications (VBA) モジュールを使ってコントロールの値を設定した場合も発生しません。

このアクションは、VBA モジュールでは使用できません。VBA で直接値を設定してください。

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
<td><p>[仕入先コード] コントロールに [仕入先] フォームの現在の仕入先を設定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p>"<strong>Control Name/コントロール名</strong>":商品コード</p></td>
<td><p>[商品コード] コントロールに移動します。</p></td>
</tr>
</tbody>
</table>

