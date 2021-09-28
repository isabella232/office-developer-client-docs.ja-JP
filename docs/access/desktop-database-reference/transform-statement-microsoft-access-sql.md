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
ms.localizationpriority: high
ms.openlocfilehash: 7194b383f5275daf5501f31833ec0a3f68fa58bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621732"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

クロス集計クエリを作成します。

## <a name="syntax"></a>構文

TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]

TRANSFORM ステートメントでは、次の引数を使用します。

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
<td><p><em>aggfunction</em></p></td>
<td><p>選択したデータを集計する <a href="sql-aggregate-functions-sql.md">SQL 集計関数</a>。</p></td>
</tr>
<tr class="even">
<td><p><em>selectstatement</em></p></td>
<td><p><a href="select-statement-microsoft-access-sql.md">SELECT</a> ステートメント。</p></td>
</tr>
<tr class="odd">
<td><p><em>pivotfield</em></p></td>
<td><p>クエリの結果で列見出しを作成するために使用するフィールドまたは式。</p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>, <em>value2</em></p></td>
<td><p>列見出しの作成に使用する固定値。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

クロス集計クエリを使用してデータをまとめる場合は、指定したフィールドや式の値を列見出しとして使用できます。このため、選択クエリよりも簡潔な書式でデータを表示できます。

TRANSFORM ステートメントは省略可能ですが、指定する場合は SQL 文字列の先頭に記述します。行見出しとして使用するフィールドを指定する SELECT ステートメントや、行のグループ化を指定する [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) 句よりも前に記述します。抽出条件や並べ替えを指定する [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句などの句を併用することもできます。さらに、クロス集計クエリの中でサブクエリを述語 (特に WHERE 句の中の述語) として使用することもできます。

*pivotfield* に返される値は、クエリの結果セットの列見出しとして使用されます。たとえば、クロス集計クエリで販売月別の売上高をピボットすることで 12 の列が作成されます。*pivotfield* を制限して、オプションの IN 句でリストされた固定値 (*value1*、*value2*) から見出しを作成できます。追加の列を作成するため、データが存在しない固定値を含めることもできます。

## <a name="example"></a>例

次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の数を示すクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。

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

次の使用例では、SQL TRANSFORM 句を使用して、1994 年の各四半期に各従業員が受注した注文の合計のドルの額を示す、やや複雑なクロス集計クエリを作成します。このプロシージャを実行するには、SQLTRANSFORMOutput 関数が必要です。

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
