---
title: LEFT JOIN 操作および RIGHT JOIN 操作 (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.localizationpriority: high
ms.openlocfilehash: 01c1c1b095d37d7505524af5360b0079e6dd1c0e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602361"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN 操作および RIGHT JOIN 操作 (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句の中で使用され、ソース テーブルのレコードを結合します。

## <a name="syntax"></a>構文

FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*

LEFT JOIN 操作および RIGHT JOIN 操作には、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
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
<td><p>任意のリレーショナル比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=&quot;または&quot; &lt;&gt;。&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

左外部結合を作成するには、LEFT JOIN 操作を使用します。左外部結合では、結合する 2 つのテーブルのうち 2 番目 (右側) のテーブルに対応するレコードがなくても、1 番目 (左側) のテーブルのレコードがすべて追加されます。

右外部結合を作成するには、RIGHT JOIN 操作を使用します。右外部結合では、結合する 2 つのテーブルのうち 1 番目 (左側) のテーブルに対応するレコードがなくても、2 番目 (右側) のテーブルのレコードがすべて追加されます。

たとえば、Departments テーブル (左側) と Employees テーブル (右側) がある場合に、社員が配属されていない部署も含めたすべての部署を選択するには、LEFT JOIN 操作を使用します。どの部署にも所属しない社員も含めた全社員を選択するには、RIGHT JOIN 操作を使用します。

次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合する方法を示しています。このクエリでは、商品がまったくない商品区分も含めて、すべての商品区分の一覧が出力されます。

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

この例では、結合されるフィールドは CategoryID フィールドですが、このフィールドは [SELECT](select-statement-microsoft-access-sql.md) ステートメントで指定していないため、クエリの結果には含まれません。結合に使用したフィールドを出力するには、そのフィールド名を SELECT ステートメントで指定してください。前の例では、フィールド名は Categories.CategoryID です。

> [!NOTE]
> - 結合フィールドのデータが同じレコードのみを選択するクエリを作成するには、[INNER JOIN](inner-join-operation-microsoft-access-sql.md) 操作を使用します。
> - LEFT JOIN または RIGHT JOIN は、INNER JOIN の入れ子にすることができますが、INNER JOIN は LEFT JOIN または RIGHT JOIN の入れ子にすることはできません。結合を他の結合にネストする方法については、INNER JOIN 操作に関するページのネストの説明を参照してください
> - 複数の ON 句をリンクすることができます。詳細については、INNER JOIN 操作に関するページのリンクの説明を参照してください。
> - メモまたは OLE オブジェクトのデータを含むフィールドを結合しようとすると、エラーが発生します。

## <a name="example"></a>例

この例
- Employees テーブルに Department Name フィールドと Department ID フィールドが含まれていると仮定していますが、実際にはノースウィンド データベースの Employees テーブルにこの 2 つのフィールドは含まれていないので注意してください。

- 社員が配属されていない部署も含めてすべての部署を選択します。

- SELECT ステートメントの使用例を見つけることができるEnumFields プロシージャを呼び出します。


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
