---
title: TRANSFORM ステートメント (Microsoft Access SQL)
TOCTitle: TRANSFORM Statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d05f278e38cc8cf132cf06605703dfa99eb8728
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478638"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

クロス集計クエリを作成します。

## <a name="syntax"></a>構文

*Aggfunctionselectstatement*ピボット*ピボット フィールド*の変換\[IN (*値 1*\[、 *value2*\[、.\]\])\]

TRANSFORM ステートメントには、次の指定項目があります。

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
<td><p><em>value1</em>、<em>value2</em></p></td>
<td><p>列見出しを作成するために使用する固定値。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>解説

クロス集計クエリを使用してデータをまとめる場合は、指定したフィールドや式の値を列見出しとして使用できます。このため、選択クエリよりも簡潔な書式でデータを表示できます。

TRANSFORM ステートメントは省略可能ですが、指定する場合は SQL 文字列の先頭に記述します。行見出しとして使用するフィールドを指定する SELECT ステートメントや、行のグループ化を指定する [GROUP BY](https://msdn.microsoft.com/library/ff837271\(v=office.15\)) 句よりも前に記述します。抽出条件や並べ替えを指定する [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) 句などの句を併用することもできます。さらに、クロス集計クエリの中でサブクエリを述語 (特に WHERE 句の中の述語) として使用することもできます。

引数 *pivotfield* に返された値は、クエリ結果の列見出しに使用されます。たとえば、クロス集計クエリで月間の売上総額を列に指定する場合は、12 個の列を作成します。また、IN 句 (省略可能) に固定値 (引数 *value1*、*value2*) を指定して、列見出しとなる引数 *pivotfield* の値を制限することもできます。さらに、対応するデータのない固定値を指定して、列を追加することもできます。

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
