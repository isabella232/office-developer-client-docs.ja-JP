---
title: INNER JOIN 操作 (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
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
ms.localizationpriority: high
ms.openlocfilehash: 098e7e1616407c1927f32db6cbedbb07b6df1283
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568909"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN 操作 (Microsoft Access SQL)


**適用先:** Access 2013、Office 2013


共通のフィールドで一致する値があるたびに、2 つのテーブルからレコードを結合します。

## <a name="syntax"></a>構文

FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*

INNER JOIN 操作には、次の指定項目があります。

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
<td><p>結合するフィールドの名前。フィールドが数値型 (Numeric) でない場合は、両方のフィールドが同じデータ型であり、両方のフィールドに格納されているデータが同じ種類である必要があります。ただし、同じ名前である必要はありません。</p></td>
</tr>
<tr class="odd">
<td><p><em>compopr</em></p></td>
<td><p>任意のリレーショナル比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=&quot;または&quot; &lt;&gt;。&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

INNER JOIN 操作は、[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句の中で使用します。INNER JOIN 操作は最も一般的な結合方法です。2 つのテーブルの共通するフィールドに同じ種類の値があった場合に、両方のテーブルのレコードを結合します。

たとえば、[部署] テーブルと [社員] テーブルで INNER JOIN 操作を行うと、各部署に所属する社員全員を選択できます。これに対して、所属する社員が 1 人もいない部署も含めすべての部署を選択したり、どの部署にも所属していない社員も含め社員全員を選択したりするには、[LEFT JOIN または RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) 操作を使用して外部結合を作成します。

メモまたは OLE オブジェクトのデータを含むフィールドを結合しようとすると、エラーが発生します。

同様の型の 2 つの数値フィールドを結合することができます。たとえば、AutoNumber フィールドと Long フィールドは同様の型なので結合できます。しかし、Single 型と Double 型のフィールドを結合することはできません。

次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合する方法を示しています。

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

前の例では、結合されるフィールドは CategoryID フィールドですが、このフィールドは [SELECT](select-statement-microsoft-access-sql.md) ステートメントで指定していないため、クエリの出力には含まれません。結合に使用したフィールドを出力するには、そのフィールド名を SELECT ステートメントで指定してください。前の例では、フィールド名は Categories.CategoryID です。

次の構文を使用して、複数の ON 句を JOIN ステートメントでリンクすることもできます。

SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;

次の構文を使用して、JOIN ステートメントを入れ子にすることもできます。

SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;

LEFT JOIN または RIGHT JOIN は、INNER JOIN の入れ子にすることができますが、INNER JOIN は LEFT JOIN または RIGHT JOIN の入れ子にすることはできません。

## <a name="example"></a>例

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
