---
title: ApplyFilter マクロ アクション
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5046b0ac633f0e2811f83a2a39130d548417932d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558892"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.

> [!NOTE]
> [!メモ] このアクションは、サーバー フィルターを使用する場合のみ、SQL WHERE 句を適用するために使用します。サーバー フィルターは、保存されているプロシージャのレコード ソースには適用できません。

## <a name="setting"></a>設定

"ApplyFilter/フィルターの実行" アクションの引数は次のとおりです。

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
<td><p>Filter Name/フィルター名</p></td>
<td><p>テーブル、フォーム、またはレポートのレコードの制限または並べ替えを行うフィルターまたはクエリの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションの [ <strong>フィルター名</strong>] ボックスに、既存のクエリ、またはクエリとして保存されているフィルターの名前を入力できます。  </p><p><strong>注</strong>: このアクションを使用してサーバー フィルターを適用する場合、引数 Filter Name は空白である必要があります。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>テーブル、フォーム、またはレポートのレコードを制限するための有効な SQL WHERE 句 (WHERE という単語は除く) または式を指定します。</p>
<p><b>メモ</b>: Where Condition 引数式では、式の左側に、フォームまたはレポートの基になるテーブルまたはクエリのフィールド名が通常含まれる。 The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records. このコントロール名は、完全な名前で指定する必要があります。 たとえば、次のように指定します。</p>
<p><strong>フォーム</strong>!<em>formname</em>!<em>controlname</em> フィールド名は二重引用符で囲み、文字列リテラルは単一引用符で囲む必要があります。 Where Condition 引数の最大長は 255 文字です。 If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> 適切なデータを提供するフィルターを既に定義している場合は、引数 Filter Name を使用できます。 制限条件を直接入力する場合は、"Where Condition/Where 条件式" 引数を使用します。 両方の引数を指定すると、Microsoft Office Access 2007 では、WHERE 句がフィルターの結果に適用されます。 2 つの引数のうち少なくとも 1 つは指定する必要があります。

## <a name="remarks"></a>注釈

フィルターまたはクエリは、フォーム ビューまたはデータシート ビューで開いているフォームに適用できます。

The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.

For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.

In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.

To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).

When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.

## <a name="example"></a>例

次の例では、ApplyFilter アクションを使用し、frmFoods フォームを開くときにフィルターを適用する方法を示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



