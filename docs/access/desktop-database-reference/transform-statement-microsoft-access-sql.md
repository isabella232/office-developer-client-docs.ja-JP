---
title: TRANSFORM ステートメント (Microsoft Access SQL)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314043"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="1c7c3-102">TRANSFORM ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1c7c3-102">TRANSFORM Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1c7c3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c7c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c7c3-104">クロス集計クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="1c7c3-105">Syntax</span></span>

<span data-ttu-id="1c7c3-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span><span class="sxs-lookup"><span data-stu-id="1c7c3-106">TRANSFORM aggfunction selectstatement
    PIVOT pivotfield [IN (value1[, value2[, …]])]</span></span>

<span data-ttu-id="1c7c3-107">TRANSFORM ステートメントでは、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c7c3-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="1c7c3-108">Part</span></span></p></th>
<th><p><span data-ttu-id="1c7c3-109">説明</span><span class="sxs-lookup"><span data-stu-id="1c7c3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c7c3-110"><em>aggfunction</em></span><span class="sxs-lookup"><span data-stu-id="1c7c3-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="1c7c3-111">選択したデータを集計する <a href="sql-aggregate-functions-sql.md">SQL 集計関数</a>。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c7c3-112"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="1c7c3-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="1c7c3-113"><a href="select-statement-microsoft-access-sql.md">SELECT</a> ステートメント。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c7c3-114"><em>pivotfield</em></span><span class="sxs-lookup"><span data-stu-id="1c7c3-114"><em>PivotField</em></span></span></p></td>
<td><p><span data-ttu-id="1c7c3-115">クエリの結果で列見出しを作成するために使用するフィールドまたは式。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c7c3-116"><em>value1</em>, <em>value2</em></span><span class="sxs-lookup"><span data-stu-id="1c7c3-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="1c7c3-117">列見出しの作成に使用する固定値。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="1c7c3-118">注釈</span><span class="sxs-lookup"><span data-stu-id="1c7c3-118">Remarks</span></span>

<span data-ttu-id="1c7c3-119">クロス集計クエリを使用してデータをまとめる場合は、指定したフィールドや式の値を列見出しとして使用できます。このため、選択クエリよりも簡潔な書式でデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="1c7c3-p101">TRANSFORM ステートメントは省略可能ですが、指定する場合は SQL 文字列の先頭に記述します。行見出しとして使用するフィールドを指定する SELECT ステートメントや、行のグループ化を指定する [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) 句よりも前に記述します。抽出条件や並べ替えを指定する [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句などの句を併用することもできます。さらに、クロス集計クエリの中でサブクエリを述語 (特に WHERE 句の中の述語) として使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="1c7c3-124">*pivotfield* に返される値は、クエリの結果セットの列見出しとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-124">The values returned in  *pivotfield*  are used as column headings in the query's result set.</span></span> <span data-ttu-id="1c7c3-125">たとえば、クロス集計クエリで販売月別の売上高をピボットすることで 12 の列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-125">For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns.</span></span> <span data-ttu-id="1c7c3-126">*pivotfield* を制限して、オプションの IN 句でリストされた固定値 (*value1*、*value2*) から見出しを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-126">You can restrict  *pivotfield*  to create headings from fixed values (  *value1*  ,  *value2*  ) listed in the optional IN clause.</span></span> <span data-ttu-id="1c7c3-127">追加の列を作成するため、データが存在しない固定値を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-127">You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="1c7c3-128">例</span><span class="sxs-lookup"><span data-stu-id="1c7c3-128">Example</span></span>

<span data-ttu-id="1c7c3-p103">次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の数を示すクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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

<span data-ttu-id="1c7c3-p104">次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の合計のドルの額を示す、やや複雑なクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c7c3-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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
