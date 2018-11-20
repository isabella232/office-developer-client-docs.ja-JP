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
ms.openlocfilehash: 4efa4e92d7fab2dc8a4aae932ccb1ffe69c7c6c8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026100"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="45be9-102">SQL サブクエリ (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="45be9-102">SQL subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="45be9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="45be9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45be9-104">サブクエリとは、[SELECT](select-statement-microsoft-access-sql.md)、[SELECT...INTO](select-into-statement-microsoft-access-sql.md)、[INSERT...INTO](insert-into-statement-microsoft-access-sql.md)、[DELETE](delete-statement-microsoft-access-sql.md)、[UPDATE](update-statement-microsoft-access-sql.md) などのステートメントおよび他のサブクエリの中にネストされた SELECT ステートメントのことです。</span><span class="sxs-lookup"><span data-stu-id="45be9-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="45be9-105">構文</span><span class="sxs-lookup"><span data-stu-id="45be9-105">Syntax</span></span>

<span data-ttu-id="45be9-106">サブクエリの作成には、次の 3 つの構文のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="45be9-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="45be9-107">*比較*\[ANY |すべて |いくつか\](*連結*)</span><span class="sxs-lookup"><span data-stu-id="45be9-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="45be9-108">*式*\[いない\](*連結*) で</span><span class="sxs-lookup"><span data-stu-id="45be9-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="45be9-109">\[ない\]EXISTS (*連結*)</span><span class="sxs-lookup"><span data-stu-id="45be9-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="45be9-110">サブクエリには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="45be9-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45be9-111">指定項目</span><span class="sxs-lookup"><span data-stu-id="45be9-111">Part</span></span></p></th>
<th><p><span data-ttu-id="45be9-112">説明</span><span class="sxs-lookup"><span data-stu-id="45be9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45be9-113"><em>comparison</em></span><span class="sxs-lookup"><span data-stu-id="45be9-113"><em>comparison</em></span></span></p></td>
<td><p><span data-ttu-id="45be9-114">式、およびその式とサブクエリの結果とを比較する比較演算子。</span><span class="sxs-lookup"><span data-stu-id="45be9-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45be9-115"><em>expression</em></span><span class="sxs-lookup"><span data-stu-id="45be9-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="45be9-116">サブクエリの結果の検索に使用する式。</span><span class="sxs-lookup"><span data-stu-id="45be9-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45be9-117"><em>sqlstatement</em></span><span class="sxs-lookup"><span data-stu-id="45be9-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="45be9-p101">SELECT ステートメント。書式や規則は他の SELECT ステートメントの場合と同じです。この SELECT ステートメントはかっこで囲みます。</span><span class="sxs-lookup"><span data-stu-id="45be9-p101">A SELECT statement, following the same format and rules as any other SELECT statement. It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45be9-120">解説</span><span class="sxs-lookup"><span data-stu-id="45be9-120">Remarks</span></span>

<span data-ttu-id="45be9-p102">サブクエリは、SELECT ステートメントのフィールド リストの中で、または [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句や [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) 句の中で、式の代わりとして使用できます。サブクエリでは、SELECT ステートメントを使用して、WHERE 句および HAVING 句の式で評価に使用する 1 つまたは複数の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="45be9-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="45be9-p103">サブクエリで取得したレコードとの比較結果が真になるレコードをメイン クエリから取得するには、ANY 述語または SOME 述語 (この 2 つは同義) を使用します。次の例では、値引率 25% 以上で売られた商品よりも単価の高いすべての商品を返します。</span><span class="sxs-lookup"><span data-stu-id="45be9-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="45be9-p104">サブクエリで取得したすべてのレコードとの比較結果が真になるレコードのみをメイン クエリから取得するには、[ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) 述語を使用します。前の例で ANY を ALL に変更すると、値引率 25% 以上で売られたすべての商品よりも単価の高い商品のみを返します。つまり、取得されるレコードがさらに限定されます。</span><span class="sxs-lookup"><span data-stu-id="45be9-p104">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="45be9-p105">サブクエリの中に同じ値を持つレコードのみをメイン クエリから取得するには、IN 述語を使用します。次の例では、値引率 25% 以上で売られたすべての商品を返します。</span><span class="sxs-lookup"><span data-stu-id="45be9-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="45be9-130">逆に、サブクエリの中に同じ値を持つレコードがないレコードのみをメイン クエリから取得するには、NOT IN 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="45be9-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="45be9-131">EXISTS 述語 (予約語 NOT を併用することも可能) はサブクエリがレコードを返すかどうかを調べることができるので、True/False の中で使用できます。</span><span class="sxs-lookup"><span data-stu-id="45be9-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="45be9-p106">サブクエリの中でテーブル名の別名を使用すると、サブクエリの外側にある [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句に指定したテーブルを参照することができます。次の例では、同じ役職の全社員のうち平均以上の給与を受け取っている社員の名前を返します。また、Employees テーブルに "T1" という別名を与えています。</span><span class="sxs-lookup"><span data-stu-id="45be9-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="45be9-135">この例では、予約語 AS は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="45be9-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="45be9-p107">一部のサブクエリは、クロス集計クエリの中で述語 (特に WHERE 句の中の述語) として使用できます。クロス集計クエリでは、SELECT のリストの中で出力としてサブクエリを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="45be9-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="45be9-138">使用例</span><span class="sxs-lookup"><span data-stu-id="45be9-138">Example</span></span>

<span data-ttu-id="45be9-139">次の使用例では、1995 年の第 2 四半期に注文を出した各得意先の名前および連絡先がリストされます。</span><span class="sxs-lookup"><span data-stu-id="45be9-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="45be9-140">SELECT ステートメントの例で表示できる、EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="45be9-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
