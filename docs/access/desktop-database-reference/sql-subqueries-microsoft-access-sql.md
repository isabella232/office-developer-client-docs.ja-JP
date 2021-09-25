---
title: SQL サブクエリ (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 292522cd40fe66951d9c68671fde90449672a2f6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589072"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>SQL サブクエリ (Microsoft Access SQL)


**適用先**: Access 2013、Office 2013

サブクエリとは、[SELECT](select-statement-microsoft-access-sql.md)、[SELECT...INTO](select-into-statement-microsoft-access-sql.md)、[INSERT...INTO](insert-into-statement-microsoft-access-sql.md)、[DELETE](delete-statement-microsoft-access-sql.md)、[UPDATE](update-statement-microsoft-access-sql.md) などのステートメントおよび他のサブクエリの中にネストされた SELECT ステートメントのことです。

## <a name="syntax"></a>構文

サブクエリの作成には、次の 3 つの構文のいずれかを使用します。

*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)

*expression* \[NOT\] IN (*sqlstatement*)

\[NOT\] EXISTS (*sqlstatement*)

サブクエリには、次の指定項目があります。

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
<td><p><em>comparison</em></p></td>
<td><p>式、およびその式とサブクエリの結果とを比較する比較演算子。</p></td>
</tr>
<tr class="even">
<td><p><em>expression</em></p></td>
<td><p>サブクエリの結果の検索に使用する式。</p></td>
</tr>
<tr class="odd">
<td><p><em>sqlstatement</em></p></td>
<td><p>SELECT ステートメント。書式や規則は他の SELECT ステートメントの場合と同じです。この SELECT ステートメントはかっこで囲みます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

サブクエリは、SELECT ステートメントのフィールド リストの中で、または [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句や [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) 句の中で、式の代わりとして使用できます。サブクエリでは、SELECT ステートメントを使用して、WHERE 句および HAVING 句の式で評価に使用する 1 つまたは複数の値を取得します。

サブクエリで取得したレコードとの比較結果が真になるレコードをメイン クエリから取得するには、ANY 述語または SOME 述語 (この 2 つは同義) を使用します。次の例では、値引率 25% 以上で売られた商品よりも単価の高いすべての商品を返します。

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

サブクエリで取得したすべてのレコードとの比較結果が真になるレコードのみをメイン クエリから取得するには、[ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) 述語を使用します。前の例で ANY を ALL に変更すると、値引率 25% 以上で売られたすべての商品よりも単価の高い商品のみを返します。つまり、取得されるレコードがさらに限定されます。

サブクエリの中に同じ値を持つレコードのみをメイン クエリから取得するには、IN 述語を使用します。次の例では、値引率 25% 以上で売られたすべての商品を返します。

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

逆に、サブクエリの中に同じ値を持つレコードがないレコードのみをメイン クエリから取得するには、NOT IN 句を使用します。

EXISTS 述語 (予約語 NOT を併用することも可能) はサブクエリがレコードを返すかどうかを調べることができるので、True/False の中で使用できます。

サブクエリの中でテーブル名の別名を使用すると、サブクエリの外側にある [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句に指定したテーブルを参照することができます。次の例では、同じ役職の全社員のうち平均以上の給与を受け取っている社員の名前を返します。また、Employees テーブルに "T1" という別名を与えています。

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

この例では、予約語 AS は省略可能です。

一部のサブクエリは、クロス集計クエリの中で述語 (特に WHERE 句の中の述語) として使用できます。クロス集計クエリでは、SELECT のリストの中で出力としてサブクエリを使用することはできません。

## <a name="example"></a>例

次の使用例では、1995 年の第 2 四半期に注文を出した各得意先の名前および連絡先がリストされます。 SELECT ステートメントの使用例で見つけることができる EnumFields プロシージャを呼び出します。

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
