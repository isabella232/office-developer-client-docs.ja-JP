---
title: SELECT ステートメント (Microsoft Access SQL)
TOCTitle: SELECT Statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: ae7a63a3fe7647dde117db80a52e2322b9af75b9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476913"
---
# <a name="select-statement-microsoft-access-sql"></a>SELECT ステートメント (Microsoft Access SQL)

**に適用されます:** Access 2013 |Office 2013

データベースの情報をレコードのセットとして返すよう Microsoft Access データベース エンジンに指示します。

## <a name="syntax"></a>構文

選択\[*述語*\] { \*  | *テーブル*です\*。 |  \[*テーブル*です。\]*フィールド 1* \[ *alias1*と\] \[、 \[*テーブル*です。\]*フィールド 2* \[ *alias2*と\] \[、.\] \]} *Tableexpression*から\[をしています.\] \[ *Externaldatabase*内\]\[位置しています. \]\[別にグループ化しています. \]\[HAVING. \]\[を注文しています. \]\[OWNERACCESS オプションを使用して\]

SELECT 句には、次の指定項目があります。

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
<td><p><em>predicate</em></p></td>
<td><p><a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL、DISTINCT、DISTINCTROW、TOP</a> のいずれかの述語。これらの述語は、返されるレコードの数を制限するために使用します。指定がない場合は、ALL になります。  </p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>この記号を付けると、指定したテーブルのすべてのフィールドが選択されます。</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>レコードを選択するフィールドのあるテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>取得するデータのある 1 つ以上のフィールドの名前。複数のフィールドを指定した場合は、指定順に取得されます。</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>、<em>alias2</em></p></td>
<td><p>引数 <em>table</em> の元の列名の代わりに列見出しとして使用する名前。</p></td>
</tr>
<tr class="even">
<td><p><em>tableexpression</em></p></td>
<td><p>取得するデータのある 1 つ以上のテーブルの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>現在のデータベースには存在しない場合は、 <em>tableexpression</em>内のテーブルを含むデータベースの名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

Microsoft® Jet データベース エンジンは、SELECT ステートメントで指定したテーブルの検索、選択された列の抽出、抽出条件を満たす行の選択、および選択された行の指定の順序による並べ替え、またはグループ化を行います。

SELECT ステートメントは、データベース内のデータの内容を変更しません。

通常、SELECT は SQL ステートメントの先頭に記述します。ほとんどの SQL ステートメントは SELECT ステートメントまたは [SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントのいずれかになります。

SELECT ステートメントの最も簡単な構文を次に示します。

*フィールド*から*テーブル*を選択します。

アスタリスク (\*) を使用すると、テーブル内のすべてのフィールドが選択できます。次の例では、Employees テーブルにあるすべてのフィールドが選択されます。

```sql
SELECT * FROM Employees;
```

FROM 句で複数のテーブルのフィールド名が含まれている場合、は、先頭にテーブル名と、 **.** (ドット) 演算子です。 部門フィールドは次の例では、[社員] テーブルと、スーパーバイザーによるテーブルの両方で、です。 SQL ステートメントでは、スーパーバイザーのテーブルから従業員のテーブルと監修者の名前から部門を選択します。

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

**レコード セット**オブジェクトが作成されると、Microsoft Jet データベース エンジンは、 **Recordset**オブジェクト内の**フィールド**オブジェクト名としてテーブルのフィールド名を使用します。 AS を使用して、別のフィールド名を使用するフィールドを生成するために使用する式は、名前を明示しない場合、予約語です。 次の例では、結果の**Recordset**オブジェクトに返される**Field**オブジェクトの名前をタイトルの生年月日を使用します。

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

集計関数を使用する場合、またはあいまいな Field オブジェクト名や重複する Field オブジェクト名を返すクエリを使用する場合は、必ず AS 句を使用して Field オブジェクトに別の名前を付ける必要があります。次の例では、Recordset オブジェクトに返される Field オブジェクトのフィールド名は "HeadCount" になります。

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

SELECT ステートメントでは、これ以外にもさまざまな句を使用して、返されるデータを制限したり整理したりできます。詳細については、使用する句のヘルプ トピックを参照してください。

**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [SQL to VBA Formatter](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Viewing Records Within A Defined Range](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>使用例

次に示す一部の使用例では、Employees テーブルに Salary フィールドが含まれていると仮定しています。実際には、ノースウィンド データベースの Employees テーブルにこのフィールドは含まれていないので注意してください。

この例では、[社員] テーブルのすべてのレコードの [氏名] と [部署名] フィールドを選択する SQL ステートメントに基づくダイナセット タイプの**レコード セット**を作成します。 **デバッグ**ウィンドウに、**レコード セット**オブジェクトの内容を印刷する、EnumFields プロシージャを呼び出します。

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

次の使用例では、PostalCode フィールドにエントリがあるレコードの数を調べ、その値が返されるフィールドとして Tally フィールドを指定します。

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

次の使用例では、社員数と平均給与額および最高給与額を表示します。

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

**Sub** プロシージャである EnumFields には、呼び出し元のプロシージャから **Recordset** オブジェクトが渡されます。次に **Recordset** のフィールドがフォーマットされ、 **Debug** ウィンドウに出力されます。変数は、必要な出力フィールド幅を示します。一部のフィールドが表示されない場合もあります。

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




