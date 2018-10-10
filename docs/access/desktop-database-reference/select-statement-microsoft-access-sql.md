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
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="41ce6-102">SELECT ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="41ce6-102">SELECT Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="41ce6-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="41ce6-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="41ce6-104">データベースの情報をレコードのセットとして返すよう Microsoft Access データベース エンジンに指示します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="41ce6-105">構文</span><span class="sxs-lookup"><span data-stu-id="41ce6-105">Syntax</span></span>

<span data-ttu-id="41ce6-106">選択\[*述語*\] { \*  | *テーブル*です\*。 |  \[*テーブル*です。\]*フィールド 1* \[ *alias1*と\] \[、 \[*テーブル*です。\]*フィールド 2* \[ *alias2*と\] \[、.\] \]} *Tableexpression*から\[をしています.\] \[ *Externaldatabase*内\]\[位置しています.</span><span class="sxs-lookup"><span data-stu-id="41ce6-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="41ce6-107">\]\[別にグループ化しています.</span><span class="sxs-lookup"><span data-stu-id="41ce6-107">\] \[GROUP BY…</span></span> <span data-ttu-id="41ce6-108">\]\[HAVING.</span><span class="sxs-lookup"><span data-stu-id="41ce6-108">\] \[HAVING…</span></span> <span data-ttu-id="41ce6-109">\]\[を注文しています.</span><span class="sxs-lookup"><span data-stu-id="41ce6-109">\] \[ORDER BY…</span></span> <span data-ttu-id="41ce6-110">\]\[OWNERACCESS オプションを使用して\]</span><span class="sxs-lookup"><span data-stu-id="41ce6-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="41ce6-111">SELECT 句には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="41ce6-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41ce6-112">指定項目</span><span class="sxs-lookup"><span data-stu-id="41ce6-112">Part</span></span></p></th>
<th><p><span data-ttu-id="41ce6-113">説明</span><span class="sxs-lookup"><span data-stu-id="41ce6-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41ce6-114"><em>predicate</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-p102"><a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL、DISTINCT、DISTINCTROW、TOP</a> のいずれかの述語。これらの述語は、返されるレコードの数を制限するために使用します。指定がない場合は、ALL になります。  </span><span class="sxs-lookup"><span data-stu-id="41ce6-p102">One of the following predicates: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW, or TOP</a>. You use the predicate to restrict the number of records returned. If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="41ce6-118">この記号を付けると、指定したテーブルのすべてのフィールドが選択されます。</span><span class="sxs-lookup"><span data-stu-id="41ce6-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41ce6-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-120">レコードを選択するフィールドのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="41ce6-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41ce6-121"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-p103">取得するデータのある 1 つ以上のフィールドの名前。複数のフィールドを指定した場合は、指定順に取得されます。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p103">The names of the fields containing the data you want to retrieve. If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41ce6-124"><em>alias1</em>、<em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-125">引数 <em>table</em> の元の列名の代わりに列見出しとして使用する名前。</span><span class="sxs-lookup"><span data-stu-id="41ce6-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41ce6-126"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-127">取得するデータのある 1 つ以上のテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="41ce6-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41ce6-128"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="41ce6-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="41ce6-129">現在のデータベースには存在しない場合は、 <em>tableexpression</em>内のテーブルを含むデータベースの名前です。</span><span class="sxs-lookup"><span data-stu-id="41ce6-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="41ce6-130">解説</span><span class="sxs-lookup"><span data-stu-id="41ce6-130">Remarks</span></span>

<span data-ttu-id="41ce6-131">Microsoft® Jet データベース エンジンは、SELECT ステートメントで指定したテーブルの検索、選択された列の抽出、抽出条件を満たす行の選択、および選択された行の指定の順序による並べ替え、またはグループ化を行います。</span><span class="sxs-lookup"><span data-stu-id="41ce6-131">To perform this operation, the Microsoft® Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="41ce6-132">SELECT ステートメントは、データベース内のデータの内容を変更しません。</span><span class="sxs-lookup"><span data-stu-id="41ce6-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="41ce6-p104">通常、SELECT は SQL ステートメントの先頭に記述します。ほとんどの SQL ステートメントは SELECT ステートメントまたは [SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p104">SELECT is usually the first word in an SQL statement. Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="41ce6-135">SELECT ステートメントの最も簡単な構文を次に示します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="41ce6-136">*フィールド*から*テーブル*を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="41ce6-p105">アスタリスク (\*) を使用すると、テーブル内のすべてのフィールドが選択できます。次の例では、Employees テーブルにあるすべてのフィールドが選択されます。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p105">You can use an asterisk (\*) to select all fields in a table. The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="41ce6-139">FROM 句で複数のテーブルのフィールド名が含まれている場合、は、先頭にテーブル名と、 **.**</span><span class="sxs-lookup"><span data-stu-id="41ce6-139">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.**</span></span> <span data-ttu-id="41ce6-140">(ドット) 演算子です。</span><span class="sxs-lookup"><span data-stu-id="41ce6-140">(dot) operator.</span></span> <span data-ttu-id="41ce6-141">部門フィールドは次の例では、[社員] テーブルと、スーパーバイザーによるテーブルの両方で、です。</span><span class="sxs-lookup"><span data-stu-id="41ce6-141">In the following example, the Department field is in both the Employees table and the Supervisors table.</span></span> <span data-ttu-id="41ce6-142">SQL ステートメントでは、スーパーバイザーのテーブルから従業員のテーブルと監修者の名前から部門を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-142">The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="41ce6-143">**レコード セット**オブジェクトが作成されると、Microsoft Jet データベース エンジンは、 **Recordset**オブジェクト内の**フィールド**オブジェクト名としてテーブルのフィールド名を使用します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-143">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object.</span></span> <span data-ttu-id="41ce6-144">AS を使用して、別のフィールド名を使用するフィールドを生成するために使用する式は、名前を明示しない場合、予約語です。</span><span class="sxs-lookup"><span data-stu-id="41ce6-144">If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word.</span></span> <span data-ttu-id="41ce6-145">次の例では、結果の**Recordset**オブジェクトに返される**Field**オブジェクトの名前をタイトルの生年月日を使用します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-145">The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="41ce6-p108">集計関数を使用する場合、またはあいまいな Field オブジェクト名や重複する Field オブジェクト名を返すクエリを使用する場合は、必ず AS 句を使用して Field オブジェクトに別の名前を付ける必要があります。次の例では、Recordset オブジェクトに返される Field オブジェクトのフィールド名は "HeadCount" になります。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p108">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object. The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="41ce6-p109">SELECT ステートメントでは、これ以外にもさまざまな句を使用して、返されるデータを制限したり整理したりできます。詳細については、使用する句のヘルプ トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p109">You can use the other clauses in a SELECT statement to further restrict and organize your returned data. For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="41ce6-150">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="41ce6-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="41ce6-151">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="41ce6-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="41ce6-152">SQL to VBA Formatter</span><span class="sxs-lookup"><span data-stu-id="41ce6-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="41ce6-153">Viewing Records Within A Defined Range</span><span class="sxs-lookup"><span data-stu-id="41ce6-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="41ce6-154">使用例</span><span class="sxs-lookup"><span data-stu-id="41ce6-154">Example</span></span>

<span data-ttu-id="41ce6-p111">次に示す一部の使用例では、Employees テーブルに Salary フィールドが含まれていると仮定しています。実際には、ノースウィンド データベースの Employees テーブルにこのフィールドは含まれていないので注意してください。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p111">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table. Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="41ce6-157">この例では、[社員] テーブルのすべてのレコードの [氏名] と [部署名] フィールドを選択する SQL ステートメントに基づくダイナセット タイプの**レコード セット**を作成します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-157">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table.</span></span> <span data-ttu-id="41ce6-158">**デバッグ**ウィンドウに、**レコード セット**オブジェクトの内容を印刷する、EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-158">It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

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

<span data-ttu-id="41ce6-159">次の使用例では、PostalCode フィールドにエントリがあるレコードの数を調べ、その値が返されるフィールドとして Tally フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

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

<span data-ttu-id="41ce6-160">次の使用例では、社員数と平均給与額および最高給与額を表示します。</span><span class="sxs-lookup"><span data-stu-id="41ce6-160">This example shows the number of employees and the average and maximum salaries.</span></span>

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

<span data-ttu-id="41ce6-p113">**Sub** プロシージャである EnumFields には、呼び出し元のプロシージャから **Recordset** オブジェクトが渡されます。次に **Recordset** のフィールドがフォーマットされ、 **Debug** ウィンドウに出力されます。変数は、必要な出力フィールド幅を示します。一部のフィールドが表示されない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="41ce6-p113">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure. The procedure then formats and prints the fields of the **Recordset** to the **Debug** window. The variable is the desired printed field width. Some fields may be truncated.</span></span>

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




