---
title: LEFT JOIN、RIGHT JOIN 操作 (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 050226506b3dc1d00f4323ae727763f7ba6bdc66
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026114"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN、RIGHT JOIN 操作 (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句の中で使用され、ソース テーブルのレコードを結合します。

## <a name="syntax"></a>構文

*Table1 という名前*の\[左 |右\] *table1.field1* *compopr table2.field2*では、結合*テーブル 2*

LEFT JOIN 操作および RIGHT JOIN 操作には、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table1</em>、<em>table2</em></p></td>
<td><p>結合するレコードのあるテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>結合するフィールドの名前。両方のフィールドが同じデータ型で、格納されるデータが同じ種類である必要があります。ただし、同じ名前である必要はありません。</p></td>
</tr>
<tr class="odd">
<td><p><em>compopr</em></p></td>
<td><p>任意の関係比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=、&quot;または&quot; &lt; &gt;。&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

左外部結合を作成するには、LEFT JOIN 操作を使用します。左外部結合では、結合する 2 つのテーブルのうち 2 番目 (右側) のテーブルに対応するレコードがなくても、1 番目 (左側) のテーブルのレコードがすべて追加されます。

右外部結合を作成するには、RIGHT JOIN 操作を使用します。右外部結合では、結合する 2 つのテーブルのうち 1 番目 (左側) のテーブルに対応するレコードがなくても、2 番目 (右側) のテーブルのレコードがすべて追加されます。

たとえば、[部署] テーブル (左側) と [社員] テーブル (右側) がある場合に、どの部署にも所属しない社員も含めた全社員を選択するには、RIGHT JOIN 操作を使用します。反対に、社員が配属されていない部署も含めたすべての部署を選択するには、LEFT JOIN 操作を使用します。

次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合しています。このクエリでは、商品がまったくない商品区分も含めて、すべての商品区分の一覧が出力されます。

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

この例では、[区分コード] は、結合されたフィールドですが、 [SELECT](select-statement-microsoft-access-sql.md)ステートメントに含まれていないために、クエリの結果には含まれません。 結合フィールドを含むように、SELECT ステートメントでフィールド名を入力します: ここで指定してください。

> [!NOTE]
> - 結合フィールドのデータが同じレコードのみを選択するクエリを作成するには、[INNER JOIN](inner-join-operation-microsoft-access-sql.md) 操作を使用します。
> - LEFT JOIN および RIGHT JOIN は、INNER JOIN の中にネストすることができます。しかし、INNER JOIN を LEFT JOIN または RIGHT JOIN の中にネストすることはできません。結合を他の結合にネストする方法の詳細については、「INNER JOIN 操作」のネストに関する説明を参照してください。
> - ON 句は複数連結できます。詳細については、「INNER JOIN 操作」の連結に関する説明を参照してください。
> - メモ型 (Memo) または OLE オブジェクト型 (OLE Object) のデータが格納されたフィールドを結合しようとすると、エラーが発生します。

## <a name="example"></a>例

この例では:
- [社員] テーブルには、架空の部署名、部署 ID フィールドの存在を前提としています。 これらのフィールドは存在しないこと実際には Northwind データベースの Employees テーブルに注意してください。

- 従業員も含め、すべての部門を選択します。

- SELECT ステートメントの例である EnumFields プロシージャを呼び出します。


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
