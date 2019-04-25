---
title: INSERT INTO ステートメント (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291334"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="64e22-102">INSERT INTO ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="64e22-102">INSERT INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="64e22-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="64e22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64e22-104">1 つのテーブルに 1 つのレコードまたは複数のレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="64e22-104">Adds a record or multiple records to a table.</span></span> <span data-ttu-id="64e22-105">追加クエリとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="64e22-105">This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="64e22-106">構文</span><span class="sxs-lookup"><span data-stu-id="64e22-106">Syntax</span></span>

### <a name="multiple-record-append-query"></a><span data-ttu-id="64e22-107">複数レコード追加クエリ</span><span class="sxs-lookup"><span data-stu-id="64e22-107">Multiple-record append query:</span></span>

<span data-ttu-id="64e22-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span><span class="sxs-lookup"><span data-stu-id="64e22-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

### <a name="single-record-append-query"></a><span data-ttu-id="64e22-109">単一レコード追加クエリ:</span><span class="sxs-lookup"><span data-stu-id="64e22-109">Single-record append query:</span></span>

<span data-ttu-id="64e22-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span><span class="sxs-lookup"><span data-stu-id="64e22-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="64e22-111">INSERT INTO ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="64e22-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64e22-112">パーツ</span><span class="sxs-lookup"><span data-stu-id="64e22-112">Part</span></span></p></th>
<th><p><span data-ttu-id="64e22-113">説明</span><span class="sxs-lookup"><span data-stu-id="64e22-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64e22-114"><em>target</em></span><span class="sxs-lookup"><span data-stu-id="64e22-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-115">レコードを追加するテーブルまたはクエリの名前です。</span><span class="sxs-lookup"><span data-stu-id="64e22-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64e22-116"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="64e22-116"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-117">
            <em>target</em> 引数に続く場合、データを追加するフィールド名です。<em>source</em> 引数に続く場合、データを取得するフィールド名です。</span><span class="sxs-lookup"><span data-stu-id="64e22-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64e22-118"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="64e22-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-p102">外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="64e22-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64e22-121"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="64e22-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-122">レコードをコピーするテーブルまたはクエリの名前です。</span><span class="sxs-lookup"><span data-stu-id="64e22-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64e22-123"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="64e22-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-p103">挿入するレコードのある 1 つ以上のテーブルの名前。単一のテーブル名、保存されたクエリ名、または <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> のいずれかの操作の結果としてできる複合テーブルを指定します。  </span><span class="sxs-lookup"><span data-stu-id="64e22-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64e22-126"><em>value1</em>、<em>value2</em></span><span class="sxs-lookup"><span data-stu-id="64e22-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="64e22-p104">新しいレコードの特定のフィールドに挿入する値です。各値は、一覧内の値の位置と対応するフィールドに挿入されます。つまり、<em>value1</em> は新しいレコードの <em>field1</em> に挿入され、<em>value2</em> は <em>field2</em>に、というように挿入されます。値はコンマで区切り、テキスト フィールドは引用符 (' ') で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="64e22-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="64e22-130">注釈</span><span class="sxs-lookup"><span data-stu-id="64e22-130">Remarks</span></span>

<span data-ttu-id="64e22-p105">INSERT INTO ステートメントで 1 つのレコードを追加するには、上記のように単一レコード追加クエリの構文を使用します。この場合は、レコードの各フィールドの名前と値を指定します。また、値を割り当てるフィールドと、そのフィールドに割り当てる値を指定します。指定していないフィールドには、既定値または **Null** 値が挿入されます。レコードはテーブルの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="64e22-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="64e22-p106">また、INSERT INTO ステートメントを使用して、別のテーブルからレコードのセットを追加することもできます。これには、上記の複数レコード追加クエリの構文で示したように SELECT...FROM 句によるクエリを使用します。この場合は、引数 *target* テーブルに追加するフィールドを SELECT 句で指定します。</span><span class="sxs-lookup"><span data-stu-id="64e22-p106">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT … FROM clause as shown above in the multiple-record append query syntax. In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="64e22-p107">
            \*source* または \*target\* テーブルでは、テーブルまたはクエリを指定できます。クエリを指定すると、Microsoft Access データベース エンジンは、クエリで指定されたすべてのテーブルにレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="64e22-p107">The *source* or *target* table may specify a table or a query. If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="64e22-141">INSERT INTO ステートメントは省略可能ですが、使用する場合 [SELECT](select-statement-microsoft-access-sql.md) ステートメントよりも前に記述します。</span><span class="sxs-lookup"><span data-stu-id="64e22-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="64e22-142">レコードの追加先のテーブルに主キーがある場合、その主キー フィールドには必ず **Null** 値以外の一意な値を追加するようにしてください。この条件が満たされない場合、Microsoft Access データベース エンジンはレコードを追加しません。</span><span class="sxs-lookup"><span data-stu-id="64e22-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="64e22-p108">AutoNumber フィールドがあるレコードをテーブルに追加するときに、追加したレコードの番号を再割り当てしたい場合、クエリには AutoNumber フィールドは入れないでください。AutoNumber フィールドは、フィールドの元の値を維持したい場合のみ含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="64e22-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="64e22-145">IN 句を使用し、別のデータベースのテーブルにレコードを追加してください。</span><span class="sxs-lookup"><span data-stu-id="64e22-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="64e22-146">新しいテーブルを作成する場合は、INSERT INTO ステートメントではなく、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントを使用してテーブル作成クエリを作成してください。</span><span class="sxs-lookup"><span data-stu-id="64e22-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="64e22-147">追加クエリを実行する前にどのレコードが追加されるかをあらかじめ確認する場合は、同じ抽出条件の選択クエリを実行してその結果を確認してください。</span><span class="sxs-lookup"><span data-stu-id="64e22-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="64e22-p109">追加クエリは、1 つ以上のテーブルから別のテーブルにレコードをコピーします。追加するレコードを含むテーブルは、追加クエリの影響は受けません。</span><span class="sxs-lookup"><span data-stu-id="64e22-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="64e22-p110">別のテーブルから既存のレコードを追加する代わりに、VALUES 句を使用して 1 つの新しいレコードに各フィールドの値を指定できます。フィールド一覧を省略した場合、VALUES 句にはテーブル内のすべてのフィールドの値を含める必要があります。そうしないと、INSERT 操作は失敗します。作成するそれぞれの追加レコードには、VALUES 句がある追加の INSERT INTO ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="64e22-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="64e22-153">[UtterAccess](https://www.utteraccess.com) コミュニティで**提供されるリンク**。</span><span class="sxs-lookup"><span data-stu-id="64e22-153">**Links provided by:** Community Member Icon The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="64e22-154">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="64e22-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="64e22-155">INSERT/UPDATE ステートメントのための連続番号を生成</span><span class="sxs-lookup"><span data-stu-id="64e22-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="64e22-156">SQL から VBA のフォーマッタ</span><span class="sxs-lookup"><span data-stu-id="64e22-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="64e22-157">例</span><span class="sxs-lookup"><span data-stu-id="64e22-157">Example</span></span>

<span data-ttu-id="64e22-p112">次の例では、仮想の New Customers テーブルのすべてのレコードを選択し、それを Customers テーブルに追加します。列を個別に指定しない場合、SELECT テーブルの列名が INSERT INTO テーブルの列名と厳密に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64e22-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="64e22-160">次の使用例では、Employees テーブルに新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="64e22-160">This example creates a new record in the Employees table.</span></span>

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

