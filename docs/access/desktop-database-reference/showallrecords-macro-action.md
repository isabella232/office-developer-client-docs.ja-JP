---
title: ShowAllRecords マクロ アクション
TOCTitle: ShowAllRecords Macro Action
ms:assetid: 6f9741ad-0440-4b8d-abea-009063c111f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195587(v=office.15)
ms:contentKeyID: 48545538
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40221ce69a03f619bd15a5a89af9018c66c52791
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479177"
---
# <a name="showallrecords-macro-action"></a>ShowAllRecords マクロ アクション


**適用されます**Access 2013 |。Office 2013


" **ShowAllRecords/全レコードの表示** " アクションを使用すると、作業中のテーブル、クエリの結果セット、またはフォームに適用されているフィルターを解除して、テーブルまたは結果セットのすべてのレコード、またはフォームの基になっているテーブルまたはクエリのすべてのレコードを表示できます。

## <a name="setting"></a>設定

" **ShowAllRecords/全レコードの表示** " アクションには、引数はありません。

## <a name="remarks"></a>注釈

このアクションを使用すると、テーブル、クエリの結果セット、またはフォームのすべてのレコード (変更されたレコードまたは新しいレコードを含む) が表示されます。このアクションにより、フォームまたはサブフォームに対してレコードの再クエリが実行されます。

また、このアクションを使用して、" **ApplyFilter/フィルターの実行** " アクション、[ **ホーム**] タブの [ **フィルター**] コマンド、または " **OpenForm/フォームを開く** " アクションの " **Filter Name/フィルター名** " または " **Where Condition/Where 条件式** " 引数で適用されたフィルターを解除することもできます。

このアクションの動作は、[ **ホーム**] タブの [ **フィルターの切り替え**] をクリックするか、フォーム ビュー、レイアウト ビュー、またはデータシート ビューでフィルターが適用されたフィールドを右クリックして [ **フィルターのクリア**] をクリックした場合と同じです。

Visual Basic for Applications (VBA) モジュールで " **ShowAllRecords/全レコードの検索** " アクションを実行するには、 **DoCmd** オブジェクトの **ShowAllRecords** メソッドを使用します。

## <a name="example"></a>例

**マクロによるフィルターの適用**

次のマクロでは、一連のアクションを使用して、"顧客電話帳" フォームの各レコードにフィルターを適用します。このマクロでは、" **ApplyFilter/フィルターの実行** " アクション、" **ShowAllRecords/全レコードの表示** " アクション、および " **GoToControl/コントロールの移動** " アクションの使い方を示します。また、フォームでオプション グループのどのトグル ボタンが選択されたかを判断するための条件の使い方も示します。アクションの各行は、レコードセットを選択するトグル ボタンに関連付けられており、たとえば、ア行、カ行、サ行などから始まるレコードや、すべてのレコードを選択します。このマクロは、[会社名フィルター] オプション グループの " **AfterUpdate/更新後処理** " イベントに設定します。

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
<td><p>[会社名フィルター] =1</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where 条件式</strong>: [会社名] と同じように&quot;[AÀÁÂÃÄ] *&quot;</p></td>
<td><p>ア行で始まる会社名を抽出します。</p></td>
</tr>
<tr class="even">
<td><p>[会社名フィルター] =2</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where 条件式</strong>: [会社名] と同じように&quot;B *&quot;</p></td>
<td><p>カ行またはガ行で始まる会社名を抽出します。</p></td>
</tr>
<tr class="odd">
<td><p>[会社名フィルター] =3</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where 条件式</strong>: [会社名] と同じように&quot;[CÇ] *&quot;</p></td>
<td><p>サ行またはザ行で始まる会社名を抽出します。</p></td>
</tr>
<tr class="even">
<td><p>タ、ダ行からワ行までのアクション行についても、ア行からサ、ザ行までと同じ形式を使用します。</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>[会社名フィルター] =26</p></td>
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Where 条件式</strong>: [会社名] と同じように&quot;[ZÆØÅ] *&quot;</p></td>
<td><p>アルファベットで始まる会社名を抽出します。</p></td>
</tr>
<tr class="even">
<td><p>[会社名フィルター] =27</p></td>
<td><p><strong>ShowAllRecords</strong></p></td>
<td><p></p></td>
<td><p>全レコードを表示します。</p></td>
</tr>
<tr class="odd">
<td><p>[RecordsetClone] です。[RecordCount]&gt;0</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: 会社名</p></td>
<td><p>選択した文字で始まるレコードが抽出されたら、[会社名] コントロールに移動します。</p></td>
</tr>
</tbody>
</table>

