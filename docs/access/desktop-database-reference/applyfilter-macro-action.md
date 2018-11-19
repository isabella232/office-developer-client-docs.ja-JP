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
ms.openlocfilehash: f6f0511a1358e8d9b0d0ee820e83cf59d2400345
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025968"
---
# <a name="applyfilter-macro-action"></a>ApplyFilter マクロ アクション

**適用されます**Access 2013、Office 2013。

**ApplyFilter**アクションを使用すると、テーブル、フォーム、または、テーブル内のレコードまたはレコードは、基になるテーブルまたはクエリ、フォームまたはレポートの制限または並べ替えをレポートに、フィルター、クエリ、または、SQL WHERE 句を適用します。 レポート、レポートの **"開く時"** イベント プロパティで指定されたマクロでのみこの操作を使用することができます。

> [!NOTE]
> [!メモ] このアクションは、サーバー フィルターを使用する場合のみ、SQL WHERE 句を適用するために使用します。サーバー フィルターは、保存されているプロシージャのレコード ソースには適用できません。

## <a name="setting"></a>設定値

**データシート**には、次の引数があります。

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
<td><p>Filter Name</p></td>
<td><p>テーブル、フォーム、またはレポートのレコードの制限または並べ替えを行うフィルターまたはクエリの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションの [ <strong>フィルター名</strong>] ボックスに、既存のクエリ、またはクエリとして保存されているフィルターの名前を入力できます。  </p><p><strong>注</strong>: サーバー フィルターを適用するのにはこのアクションを使用する場合、[フィルター名] 引数が空白する必要があります。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>テーブル、フォーム、またはレポートのレコードを制限するための有効な SQL WHERE 句 (WHERE という単語は除く) または式を指定します。</p>
<p><b>注</b>: で、ある条件の引数の式、式の左側にあるには通常、フォームまたはレポートの基になるテーブルまたはクエリのフィールド名が含まれています。 通常、式の右側にあるには、制限するか、レコードを並べ替えるには、このフィールドに適用する条件が含まれています。 などの条件と一致する最初のフォーム内のレコードが必要な値を格納する別のフォーム上のコントロールの名前を指定できます。 コントロールの名前は、たとえば、完全修飾にする必要があります。</p>
<p><strong>フォーム</strong>です。<em>フォーム名</em>です。<em>controlname</em>フィールド名を二重引用符で囲む必要があり、文字列リテラルは単一引用符で囲む必要があります。 条件式の最大長は、255 文字です。 長い SQL WHERE 句を入力する場合はで Visual Basic for Applications (VBA) モジュールの<strong>DoCmd</strong>オブジェクトの<strong>ApplyFilter</strong>メソッドを使用します。 VBA では、SQL 句のステートメントの最大 32,768 文字を入力できます。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> 適切なデータを提供するフィルターが既に定義されている場合は、フィルター名の引数を使用できます。 制限条件を直接入力するのに条件式を使用できます。 両方の引数を指定すると、Microsoft Office Access 2007 では、WHERE 句がフィルターの結果に適用されます。 2 つの引数のうち少なくとも 1 つは指定する必要があります。

## <a name="remarks"></a>解説

フィルターまたはクエリは、フォーム ビューまたはデータシート ビューで開いているフォームに適用できます。

フィルターおよび WHERE 条件式を指定するフォームまたはレポートの**フィルター**または**フォーム**のプロパティの設定になります。

テーブルおよびフォームでは、この操作は、[**レコード**] メニューの **[フィルター/並べ替えの実行**または**サーバー フィルターの適用**] をクリックすると同様です。 メニュー コマンドは、 **ApplyFilter**アクションには、指定したフィルターまたはクエリが適用されますが、テーブルまたはフォームに最も新しく作成されたフィルターを適用します。

、Access データベースの [**レコード**] メニューの [**フィルター** ] をポイントし、[フィルター/並べ替えの編集ウィンドウに表示フィルターの条件、 **ApplyFilter**アクションを実行した後、 **[フィルター/並べ替えの編集**] をクリックしてオンにした場合にこのアクションです。

フィルターを削除し、Office Access 2007 データベース内のすべてのテーブルまたはフォームのレコードを表示、[**レコード**] メニューには、**解除**、または、[**フィルター/並べ替えの解除**] コマンドを使用できます。 Access プロジェクト (.adp) でフィルターを削除するにフォーム サーバー フィルター ウィンドウに戻るとすべてのフィルター条件を削除して、ツールバーの [**レコード**] メニューの [**サーバー フィルターの適用**] をクリックしてしたり、**フォーム サーバー フィルター**のプロパティを設定**False** (0)。

テーブルまたはフォームを保存すると、アクセス、そのオブジェクトに現在定義されているすべてのフィルターは保存されることはありませんフィルター自動的に次回オブジェクトを開いたときに自動的に、保存前にオブジェクトに適用した並べ替えに適用されます)。 フォームを最初に開いたときに自動的にフィルターを適用するには、**データシート**または**Open**イベントが発生する**DoCmd**オブジェクトの**ApplyFilter**メソッドを含むイベント プロシージャが含まれているマクロを指定します。フォームのプロパティの設定します。 **OpenForm**または**OpenReport**アクション、または、対応するメソッドを使用してフィルターを適用することもできます。 テーブルを最初に開いたときに自動的にフィルターを適用するには、**データシート**の直後、 **OpenTable**アクションを含むマクロを使用してテーブルを開くことができます。

## <a name="example"></a>使用例

次の例では、 ApplyFilter アクションを使用し、frmFoods フォームを開くときにフィルターを適用する方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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



