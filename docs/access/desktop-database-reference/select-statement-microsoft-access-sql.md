---
title: SELECT ステートメント (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
ms.localizationpriority: high
ms.openlocfilehash: 0a407c6b164f2558be46ab2804693121ba07a5c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593636"
---
# <a name="select-statement-microsoft-access-sql"></a>SELECT ステートメント (Microsoft Access SQL)

**適用先**: Access 2013 | Office 2013

Microsoft Access データベース エンジンにデータベースの情報をレコード セットとして返すように指示します。

## <a name="syntax"></a>構文

SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE… \] \[GROUP BY… \] \[HAVING… \] \[ORDER BY… \] \[WITH OWNERACCESS OPTION\]

SELECT ステートメントでは次の引数を使用します。

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
<td><p><em>predicate</em></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL、DISTINCT、DISTINCTROW、TOP</a> のいずれかの述語。これらの述語は、返されるレコードの数を制限するために使用します。指定がない場合は、ALL になります。  </p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>指定したテーブル (複数可) のすべてのフィールドを選択するよう指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>レコードを選択するフィールドを含んだテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>取得するデータを含んだフィールドの名前。 複数のフィールドを含めた場合は、リストした順序で取得されます。</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>、<em>alias2</em></p></td>
<td><p>
            <em>table</em> 内の元の列名の代わりに列見出しとして使用する名前。</p></td>
</tr>
<tr class="even">
<td><p><em>tableexpression</em></p></td>
<td><p>取得するデータを含んだテーブル (複数可) の名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>
            <em>tableexpression</em> のテーブルが現在のデータベースにない場合に、それを含むデータベースの名前。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

この操作を実行するため、Microsoft Jet データベース エンジンは指定されたテーブル (複数可) を検索して、選択した列を抽出し、条件に一致する行を選択して、結果行を指定の順序に並べ替えたり、グループ化したりします。

SELECT ステートメントはデータベース内のデータを変更することはありません。

通常、SELECT は SQL ステートメントの先頭に記述します。ほとんどの SQL ステートメントは SELECT ステートメントまたは [SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントのいずれかになります。

SELECT ステートメントの最小限の構文は次のとおりです。

SELECT *fields* FROM *table*

アスタリスク (\*) を使用すると、テーブル内のすべてのフィールドが選択できます。次の例では、Employees テーブルにあるすべてのフィールドが選択されます。

```sql
SELECT * FROM Employees;
```

FROM 句で複数のテーブルに含まれるフィールドの場合は、その前にテーブル名と **.** (ドット) 演算子を付けます。 次の例では、Department フィールドが Employees テーブルと Supervisors テーブルの両方に含まれます。 この SQL ステートメントは、Employees テーブルから部署を選択し、Supervisors テーブルから監督者名を選択します。

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object. If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word. The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

使用する集約関数やクエリで返される **Field** オブジェクト名があいまいな場合や重複する場合は、AS 句を使用して **Field** オブジェクトの代替名を指定する必要があります。 次の例では、タイトルに HeadCount を使用して、結果の **Recordset** オブジェクトで返された **Field** オブジェクトに名前を付けています。

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

SELECT ステートメントではこの他にも、返されるデータを制限して整理する句を使用できます。 詳しくは、使用する句のヘルプ トピックをご覧ください。

[UtterAccess](https://www.utteraccess.com) コミュニティで **提供されるリンク**。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [SQL to VBA Formatter](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Viewing Records Within A Defined Range](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>例

次に示す一部の使用例では、Employees テーブルに Salary フィールドが含まれていると仮定しています。実際には、ノースウィンド データベースの Employees テーブルにこのフィールドは含まれていないので注意してください。

This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table. It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.

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

<br/>

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

<br/>

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

<br/>

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




