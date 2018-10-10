---
title: INNER JOIN 操作 (Microsoft Access SQL)
TOCTitle: INNER JOIN Operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: da1cebb26aa7e7e8f5afcee6716cbbbbe1ebf8f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478046"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN 操作 (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013


2 つのテーブルの共通するフィールドに同じ値があった場合に、両方のテーブルのレコードを結合します。

## <a name="syntax"></a>構文

*Table1 という名前*の内部結合*table2*から*table1 という名前*にします。*フィールド 1**table2 を compopr*。*フィールド 2*

INNER JOIN 操作には、次の指定項目があります。

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
<td><p>結合するフィールドの名前。フィールドが数値型 (Numeric) でない場合は、両方のフィールドが同じデータ型であり、両方のフィールドに格納されているデータが同じ種類である必要があります。ただし、同じ名前である必要はありません。</p></td>
</tr>
<tr class="odd">
<td><p><em>compopr</em></p></td>
<td><p>任意の関係比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=、&quot;または&quot; &lt; &gt;。&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

INNER JOIN 操作は、[FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) 句の中で使用します。INNER JOIN 操作は最も一般的な結合方法です。2 つのテーブルの共通するフィールドに同じ種類の値があった場合に、両方のテーブルのレコードを結合します。

たとえば、[部署] テーブルと [社員] テーブルで INNER JOIN 操作を行うと、各部署に所属する社員全員を選択できます。これに対して、所属する社員が 1 人もいない部署も含めすべての部署を選択したり、どの部署にも所属していない社員も含め社員全員を選択したりするには、[LEFT JOIN または RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) 操作を使用して外部結合を作成します。

メモ型 (Memo) または OLE オブジェクト型 (OLE Object) のデータが格納されたフィールドを結合しようとすると、エラーが発生します。

2 つの数値型 (Numeric) フィールドのデータ型が同じであれば、それらのフィールドを結合することができます。たとえば、オートナンバ型 (AutoNumber) フィールドと長整数型 (Long) フィールドは、データ型が同じであるため結合することができます。一方、単精度浮動小数点型 (Single) フィールドと倍精度浮動小数点型 (Double) フィールドは結合できません。

次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合しています。

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

上記の例では、[区分コード] は、結合されたフィールドですが、 [SELECT](select-statement-microsoft-access-sql.md)ステートメントに含まれていないために、クエリ出力には含まれません。 結合フィールドを含めるには、そのフィールド名を SELECT ステートメントで、この例で指定してください。

次の構文を使用して、JOIN ステートメントの中で複数の ON 句を連結できます。

*フィールド*FROM *table1* INNER JOIN *table2*に*table1 という名前*を選択します。*フィールド 1**compopr**table2*。*フィールド 1**Table1 という名前*にします。*フィールド 2**compopr**table2*。*field2*)*Table1 という名前*にします。*field3**compopr**table2*。*field3*)\];

次の構文を使用して、JOIN ステートメントをネストすることができます。

INNER JOIN*フィールド*FROM *table1 という名前*を選択 (*table2*の INNER JOIN \[( \]*テーブル 3* \[INNER JOIN \[( \] *tablex* \[内部に参加しています)\] *テーブル 3*にします。*field3**compopr**tablex*。*fieldx*)\] *テーブル 2*にします。*フィールド 2**compopr**テーブル 3*です。*field3*)*Table1 という名前*にします。*フィールド 1**compopr**table2*。*フィールド 2*です。

LEFT JOIN または RIGHT JOIN は、INNER JOIN にネストできますが、INNER JOIN を LEFT JOIN または RIGHT JOIN にネストすることはできません。

## <a name="example"></a>使用例

次の使用例では、Order Details テーブルと Orders テーブルの等結合、および Orders テーブルと Employees テーブルの等結合を作成します。この結合が必要になるのは、Employees テーブルに売上データが含まれず、Order Details テーブルに社員データが含まれないためです。クエリによって、社員名と、その社員の総売上高の一覧が生成されます。

この例では、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
