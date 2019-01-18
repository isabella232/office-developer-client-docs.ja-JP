---
title: ステートメント (Microsoft Access SQL) を変換します。
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9abe91d4ce6996a725e246da6922015d15a8bd39
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711960"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="ddac4-102">ステートメント (Microsoft Access SQL) を変換します。</span><span class="sxs-lookup"><span data-stu-id="ddac4-102">TRANSFORM statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ddac4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ddac4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ddac4-104">クロス集計クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="ddac4-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddac4-105">構文</span><span class="sxs-lookup"><span data-stu-id="ddac4-105">Syntax</span></span>

<span data-ttu-id="ddac4-106">*Aggfunctionselectstatement*ピボット*ピボット フィールド*の変換\[IN (*値 1*\[、 *value2*\[、.\]\])\]</span><span class="sxs-lookup"><span data-stu-id="ddac4-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="ddac4-107">TRANSFORM ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="ddac4-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddac4-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="ddac4-108">Part</span></span></p></th>
<th><p><span data-ttu-id="ddac4-109">説明</span><span class="sxs-lookup"><span data-stu-id="ddac4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddac4-110"><em>aggfunction</em></span><span class="sxs-lookup"><span data-stu-id="ddac4-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="ddac4-111">選択したデータを集計する <a href="sql-aggregate-functions-sql.md">SQL 集計関数</a>。</span><span class="sxs-lookup"><span data-stu-id="ddac4-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddac4-112"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="ddac4-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="ddac4-113"><a href="select-statement-microsoft-access-sql.md">SELECT</a> ステートメント。</span><span class="sxs-lookup"><span data-stu-id="ddac4-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddac4-114"><em>pivotfield</em></span><span class="sxs-lookup"><span data-stu-id="ddac4-114"><em>pivotfield</em></span></span></p></td>
<td><p><span data-ttu-id="ddac4-115">クエリの結果で列見出しを作成するために使用するフィールドまたは式。</span><span class="sxs-lookup"><span data-stu-id="ddac4-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddac4-116"><em>value1</em>, <em>value2</em></span><span class="sxs-lookup"><span data-stu-id="ddac4-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="ddac4-117">列見出しを作成するために使用する固定値。</span><span class="sxs-lookup"><span data-stu-id="ddac4-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="ddac4-118">解説</span><span class="sxs-lookup"><span data-stu-id="ddac4-118">Remarks</span></span>

<span data-ttu-id="ddac4-119">クロス集計クエリを使用してデータをまとめる場合は、指定したフィールドや式の値を列見出しとして使用できます。このため、選択クエリよりも簡潔な書式でデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="ddac4-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="ddac4-p101">TRANSFORM ステートメントは省略可能ですが、指定する場合は SQL 文字列の先頭に記述します。行見出しとして使用するフィールドを指定する SELECT ステートメントや、行のグループ化を指定する [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) 句よりも前に記述します。抽出条件や並べ替えを指定する [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句などの句を併用することもできます。さらに、クロス集計クエリの中でサブクエリを述語 (特に WHERE 句の中の述語) として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="ddac4-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="ddac4-p102">引数 *pivotfield* に返された値は、クエリ結果の列見出しに使用されます。たとえば、クロス集計クエリで月間の売上総額を列に指定する場合は、12 個の列を作成します。また、IN 句 (省略可能) に固定値 (引数 *value1*、*value2*) を指定して、列見出しとなる引数 *pivotfield* の値を制限することもできます。さらに、対応するデータのない固定値を指定して、列を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ddac4-p102">The values returned in *pivotfield* are used as column headings in the query's result set. For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns. You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause. You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="ddac4-128">例</span><span class="sxs-lookup"><span data-stu-id="ddac4-128">Example</span></span>

<span data-ttu-id="ddac4-p103">次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の数を示すクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="ddac4-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="ddac4-p104">次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の合計のドルの額を示す、やや複雑なクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="ddac4-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```
