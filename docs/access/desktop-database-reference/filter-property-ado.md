---
description: ViewCtl.Filter プロパティ (Outlook ビュー コントロール)
title: Filter プロパティ (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9d3234f1d5f41fd9f07b8d98bf3df395067780ae
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734197"
---
# <a name="filter-property-ado"></a>Filter プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) のデータに対するフィルターを示します。

## <a name="settings-and-return-values"></a>設定と戻り値

次の中の 1 つを含む、バリアント型 ( **Variant** ) の値を設定または取得します。

  - **条件文字列**: **AND** 演算子または **OR** 演算子で連結された、1 つまたは複数の句で構成される文字列です。

  - **ブックマーク配列**: **Recordset** オブジェクト内のレコードを指す一意なブックマーク値の配列です。

  - [FilterGroupEnum](filtergroupenum.md) 値。

## <a name="remarks"></a>解説

**Filter** プロパティは、**Recordset** オブジェクト内のレコードを選別するために使います。フィルター処理後の **Recordset** が現在のカーソルになります。[AbsolutePosition](absoluteposition-property-ado.md)、[AbsolutePage](absolutepage-property-ado.md)、[RecordCount](recordcount-property-ado.md)、[PageCount](pagecount-property-ado.md) などの、現在のカーソルに基づいて値を返すその他のプロパティが影響を受けます。これは、**Filter** プロパティを特定の値に設定すると、カレント レコードが新しい値を満たす最初のレコードに移動するからです。

条件文字列は *、FieldName-Operator-Value* という形式の句 ("LastName = 'Smith'" など) で表されます。 複合句を作成するには、個々の句を **AND** (たとえば、"LastName = 'Smith' AND FirstName = 'John'" など) **または OR** (") と連結します。 複合句を作成するには、個々の句を **AND** (たとえば、"LastName = 'Smith' AND FirstName = 'John'" など) または **OR** ("LastName = 'Smith' OR LastName = 'Jones'" など) と連結します。 検索条件文字列を指定する際は、次の点に注意してください。

  - *FieldName* には、**Recordset** の有効なフィールド名を指定する必要があります。フィールド名にスペースを含める場合は、名前を角かっこで囲みます。

  - *演算子* は、=、LIKE \<, \> \<=, \> \<\> のいずれかを指定する **必要があります**。

  - *値* は、フィールド値を比較する値です (例: 'Smith'、8/24/95、12.345、$50.00)。 \# \# 文字列には単一引用符を使用し、日付にはポンド記号 ( \# ) を使用します。 数値の場合、小数点、ドル記号、および指数表記を使用できます。 Operator *が* **LIKE の場合***、値は* ワイルドカードを使用できます。 アスタリスク ( \* ) とパーセント記号 (%) のみワイルド カードは許可され、文字列の最後の文字である必要があります。 *Value* に Null を指定することはできません。

    > [!NOTE]
    > [!メモ] フィルターの "値" に単一引用符 (') を含めるには、2 つの単一引用符を使って 1 つの単一引用符を表します。たとえば、O'Malley にフィルターを設定するには、条件文字列は、"col1 = 'O''Malley'" とします。フィルター値の先頭と末尾に単一引用符を含めるには、シャープ記号 (#) で文字列を囲みます。たとえば、'1' にフィルターを設定するには、条件文字列を "col1 = #'1'#" とします。

-   **AND** と **OR** の間に優先順位はありません。 句はかっこでグループにまとめることができます。 ただし、次のコード スニペットのように **、OR** で結合された句をグループ化し **、AND** を使用してグループを別の句に結合することはできません。  
 `(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John'`  
  
-   この場合は、フィルターを次のように構成します。  
 `(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John')`  

  - **LIKE** 句では、パターンの先頭と末尾にワイルドカード (LastName Like 'mit ' など) を使用するか、パターンの末尾 \* \* (LastName Like 'Smit' など) のみを使用できます。 \*

フィルター定数を使うと、一括更新モードでレコード間に競合が発生した場合でも、たとえば最後の [UpdateBatch](updatebatch-method-ado.md) メソッドの呼び出しで変更されたレコードだけを表示するなどの方法で、簡単に競合を解消できます。

たとえば、レコードが他のユーザーによって既に削除されている場合など、基になるデータとの競合が原因で、 **Filter** プロパティの設定に失敗する場合があります。このような場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返しますが、プログラムの実行は停止されません。実行時エラーは、要求したすべてのレコードで競合が発生した場合にのみ発生します。競合が発生したレコードを見つけるには、 [Status](status-property-ado-recordset.md) プロパティを使用します。

**Filter** プロパティを長さ 0 の文字列 ("") に設定すると、 **adFilterNone** 定数を使った場合と同じ結果が得られます。

**Filter** プロパティを設定すると、 **Recordset** のフィルター処理済みのレコードのサブセット内で最初のレコードに現在のレコードの位置が移動します。同様に、 **Filter** プロパティを消去すると、現在のレコードの位置は **Recordset** 内で最初のレコードに移動します。

[Filter](bookmark-property-ado.md) プロパティで使用する配列を作成するときに使用するブックマーク値については、 **Bookmark** プロパティを参照してください。

条件 **文字列** の形式のフィルター (OrderDate \> '12/31/1999' など) だけが、永続化されたレコードセットの内容に影響 **します**。 **Bookmark** の配列または **FilterGroupEnum** の値を使用して作成された **Filter** は、永続化された Recordset の内容に影響しません。 これらの規則は、クライアント側カーソルまたはサーバー側カーソルで作成された **Recordset** にも当てはまります。

> [!NOTE]
> [!メモ] 単一キー テーブルのキー フィールドを基にしてフィルタリングが行われ、キー フィールド値に変更が加えられた場合、 **adFilterPendingRecords** フラグをフィルター処理および変更された **Recordset** に一括更新モードで適用すると、結果の **Recordset** は空になります。次のいずれかの条件が満たされる場合は、空ではない **Recordset** が得られます。
> - 単一キー テーブルの非キー フィールドを基にしてフィルタリングが行われた。
> - 複数キー テーブルの任意のフィールドを基にしてフィルタリングが行われた。
> - 単一キー テーブルの非キー フィールドに変更が加えられた。
> - 複数キー テーブルの任意のフィールドに変更が加えられた。

次の表に、フィルタリングと変更の条件の各組み合わせにおける **adFilterPendingRecords** の効果を示します。左側の列は変更の対象のキーを示します。変更は、任意の非キー フィールド、単一キー テーブルのキー フィールド、または複数キー テーブルの任意のキー フィールドに対して行われる可能性があります。1 行目は、フィルター条件を示します。フィルタリングは、任意の非キー フィールド、単一キー テーブルのキー フィールド、または複数キー テーブルの任意のキー フィールドに基づいて行われる可能性があります。この行と列が交差したセルが結果を示します。つまり、+ は、 **adFilterPendingRecords** を適用すると空でない **Recordset** が得られることを表します。 **-** は、空の **Recordset** が得られることを表します。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p>非キー</p></th>
<th><p>単一キー</p></th>
<th><p>複数キー</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>非キー</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>単一キー</p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p>N/A</p></td>
</tr>
<tr class="odd">
<td><p>複数キー</p></td>
<td><p>+</p></td>
<td><p>N/A</p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

