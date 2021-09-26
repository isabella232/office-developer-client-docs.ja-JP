---
title: GoToRecord マクロ アクション
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9041b1e33010f3b80be82c0e80e4a0fe86a7cf80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622229"
---
# <a name="gotorecord-macro-action"></a>GoToRecord マクロ アクション


**適用先**: Access 2013、Office 2013

"GoToRecord/レコードの移動" アクションを使用すると、開いているテーブル、フォーム、またはクエリの結果セットで、指定したレコードをカレント レコードにすることができます。

## <a name="setting"></a>設定

"**GoToRecord/レコードの移動**" アクションの引数は次のとおりです。

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
<td><p><strong>オブジェクトの種類</strong></p></td>
<td><p>カレント レコードにするレコードが含まれているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクト名</strong></p></td>
<td><p>カレント レコードにするレコードが含まれているオブジェクトの名前を指定します。[オブジェクト名] ボックスには、カレント データベースに含まれる、"Object Type/オブジェクトの種類" 引数で指定した種類のオブジェクトがすべて表示されます。"Object Type/オブジェクトの種類" 引数を指定しない場合は、この引数も指定しないでください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>カレント レコードにするレコードを指定します。[<strong>レコード</strong>] ボックスで、[<strong>前のレコード</strong>]、[<strong>次のレコード</strong>]、[<strong>先頭のレコード</strong>]、[<strong>最後のレコード</strong>]、[<strong>移動先指定</strong>]、[<strong>新しいレコード</strong>] のいずれかをクリックします。既定値は [<strong>次のレコード</strong>] です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>整数値、または結果が整数値となる式を指定します。 式の前に等号 ( ) を付けます <strong>=</strong> 。 この引数では、カレント レコードにするレコードを指定します。 この引数の使用方法は 2 とおりあります。</p>
<ul>
<li><p>引数<strong>Record</strong>が<strong></strong>Next または<strong>Previous</strong>の場合、Microsoft Office Access 2007 は Offset 引数で指定されたレコードの数を前後に<strong>移動</strong>します。</p></li>
<li><p>引数 <strong>Record が Go</strong> <strong>To の場合</strong>、Access は Offset 引数に等しい数値のレコードに <strong>移動</strong> します。 レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</p>
<p><strong>メモ</strong>: 引数<strong>Record</strong>に<strong>最初、</strong><strong>最後</strong>、または<strong>新</strong>しい設定を使用する場合、引数 Offset は無視されます。 <strong></strong> 大きすぎる <strong>Offset</strong> 引数を入力すると、エラー メッセージが表示されます。 Offset 引数に負の数値を <strong>入力</strong> できない。</p></li>
<li><p>引数<strong>Record</strong>が<strong></strong>Next または<strong>Previous</strong>の場合、Microsoft Office Access 2007 は Offset 引数で指定されたレコードの数を前後に<strong>移動</strong>します。</p></li>
<li><p>引数 <strong>Record が Go</strong> <strong>To の場合</strong>、Access は Offset 引数に等しい数値のレコードに <strong>移動</strong> します。 レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

レコードの特定のコントロールにフォーカスがある場合、このアクションを実行しても、新しいフォームの同じコントロールにフォーカスがとどまります。

You can use the **New** setting for the **Record** argument to move to the blank record at the end of a form or table so you can enter new data.

This action is similar to clicking the arrow below the **Find** button on the **Home** tab and then clicking **Go To**. The **First**, **Last**, **Next**, **Previous**, and **New Record** subcommands of the **Go To** command have the same effect on the selected object as the **First**, **Last**, **Next**, **Previous**, and **New** settings for the **Record** argument. You can also move to records by using the navigation buttons at the bottom of the window.

You can use the **GoToRecord** action to make a record on a hidden form the current record if you specify the hidden form in the **Object Type** and **Object Name** arguments.

To run the **GoToRecord** action in a Visual Basic for Applications (VBA) module, use the **GoToRecord** method of the **DoCmd** object.

