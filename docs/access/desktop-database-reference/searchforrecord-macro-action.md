---
title: SearchForRecord マクロ アクション
TOCTitle: SearchForRecord macro action
ms:assetid: a3483c41-adb5-5923-55f4-1a3c4f60cb2f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821023(v=office.15)
ms:contentKeyID: 48546781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm118713
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d30b60680065fd3d949e64b11789e6fe6bc3b80c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572719"
---
# <a name="searchforrecord-macro-action"></a>SearchForRecord マクロ アクション


**適用先:** Access 2013、Office 2013

**SearchForRecord** アクションは、テーブル、クエリ、フォーム、またはレポート内の特定のレコードを検索するために使用します。

## <a name="setting"></a>設定

**SearchForRecord** アクションの引数は次のとおりです。

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
<td><p>検索先のデータベース オブジェクトの種類を入力または選択します。[ <strong>テーブル</strong> ]、[ <strong>クエリ</strong> ]、[ <strong>フォーム</strong> ]、[ <strong>レポート</strong> ] のいずれかを選択できます。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>検索対象のレコードが含まれている特定のオブジェクトを入力または選択します。ドロップダウン リストには、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のデータベース オブジェクトがすべて表示されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>レコード/Record</strong></p></td>
<td><p>検索の開始点と方向を指定します。</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>設定</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Previous/前のレコード</strong></p></td>
<td><p>カレント レコードから前方へ検索します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Next/次のレコード</strong></p></td>
<td><p>カレント レコードから後方へ検索します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>First/先頭のレコード</strong></p></td>
<td><p>最初のレコードから後方へ検索します。この引数の既定値です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Last/最後のレコード</strong></p></td>
<td><p>最後のレコードから前方へ検索します。</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition/Where 条件式</strong></p></td>
<td><p>WHERE 句と同じ構文を使用して検索SQLを入力します。WHERE という単語は使用 &quot; されません &quot; 。 例えば、</p>
<p>`Description = "Beverages"`</p>
<p>フォームのテキスト ボックスにある値を含む条件を作成するには、条件の最初の部分と、検索対象の値を含むテキスト ボックスの名前を連結する式を作成する必要があります。 たとえば、次の条件では、"説明" フィールドで frmCategories というフォーム上の txtDescription というテキスト ボックスに含まれる値を検索します。 式の先頭に等号 ( )、テキスト ボックス参照のどちら側でも単一引用符 <strong>=</strong> (<strong>'</strong>) を使用します。</p>
<p>`="Description = ' " & Forms![frmCategories]![txtDescription] & "'"`</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- 複数のレコードが **Where Condition/Where 条件式** 引数の条件と一致した場合は、次の要因によって、検出されるレコードが決まります。
    
  - **Record/レコード引数の設定:****Record/レコード** 引数の詳細については、「設定値」セクションの表を参照してください。
    
  - **レコードの並べ替え順序:** たとえば、**Record/レコード** 引数が [**先頭のレコード**] に設定されている場合、レコードの並べ替え順序を変更すると、検出されるレコードが変わることがあります。

- **Object Name/オブジェクト名** 引数で指定されたオブジェクトは、このアクションが実行される前に開いておく必要があります。開かれていない場合、エラーが発生します。

- **Where Condition/Where 条件式** 引数の条件と一致するレコードがなくても、エラーは発生せず、フォーカスはカレント レコードに置かれたままになります。

- 前のレコードまたは次のレコードを検索する場合、データの先頭または末尾まで検索すると、そこで終了します。条件に一致するレコードがなくても、エラーは発生せず、フォーカスはカレント レコードに置かれたままになります。条件と一致するレコードが見つかったことを確認するには、次のアクションの条件を入力し、その条件を **Where Condition/Where 条件式** 引数の条件と同じにします。

- VBA モジュールで **SearchForRecord** アクションを実行するには、 **DoCmd** オブジェクトの **SearchForRecord** メソッドを使用します。

- **SearchForRecord** アクションは、 **[FindRecord](findrecord-macro-action.md)** アクションと似ていますが、 **SearchForRecord** アクションの検索機能の方が強力です。 **FindRecord** アクションは、主に文字列の検索に使用され、その機能は [ **検索**] ダイアログ ボックスの機能と同じです。 **SearchForRecord** アクションでは、フィルターまたは SQL クエリのように機能する条件が使用されます。次の一覧は、 **SearchForRecord** アクションで実行できるいくつかの操作を示しています。
    
  - **Where Condition/Where 条件式** 引数では、次に示すような複雑な条件を使用できます。
        
    `Description = "Beverages" and CategoryID = 11`
    
  - フォームまたはレポートのレコード ソース内にあってもフォームまたはレポートには表示されないフィールドを参照できます。前の例では、フォームまたはレポートに Description も CategoryID も表示されない場合でも、条件は機能します。
    
  - 論理演算子 **\<**, **\>** (AND、OR、BETWEENなど) を使用 **できます**。 **FindRecord** アクションでは、検索対象の文字列と完全に一致する文字列、検索対象の文字列で始まる文字列、検索対象の文字列を含む文字列のみが検索されます。

## <a name="example"></a>例

次のマクロは、まず **OpenTable** アクションを使用して [商品区分] テーブルを開きます。次に、**SearchForRecord** アクションを使用して、テーブル内で [説明] フィールドが "飲料" である最初のレコードを検索します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクション</p></th>
<th><p>引数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>OpenTable</strong></p></td>
<td><p><strong>テーブル名</strong>: カテゴリ<strong>ビュー</strong>: <strong>データシートData モード</strong>: <strong>編集</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>SearchForRecord</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>TableObject 名</strong>: カテゴリ<strong>レコード</strong>: <strong>FirstWhere Condition</strong>: Description = &quot; Beverages&quot;</p></td>
</tr>
</tbody>
</table>

