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
ms.openlocfilehash: 1635ff8ad43af45a62cd2223be853cefb5b6e999
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870801"
---
# <a name="insert-into-statement-microsoft-access-sql"></a><span data-ttu-id="1f4f8-102">INSERT INTO ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1f4f8-102">INSERT INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1f4f8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f4f8-p101">テーブルに 1 つまたは複数のレコードを追加します。追加クエリとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p101">Adds a record or multiple records to a table. This is referred to as an append query.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f4f8-106">構文</span><span class="sxs-lookup"><span data-stu-id="1f4f8-106">Syntax</span></span>

<span data-ttu-id="1f4f8-107">**複数レコード追加クエリ**:</span><span class="sxs-lookup"><span data-stu-id="1f4f8-107">**Multiple-record append query**:</span></span>

<span data-ttu-id="1f4f8-108">INSERT INTO*ターゲット* \[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\] \[ *Externaldatabase*で\]を選択して\[*ソース*です。\]*フィールド 1*\[、*フィールド 2*\[をしています.\] *Tableexpression*から</span><span class="sxs-lookup"><span data-stu-id="1f4f8-108">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*</span></span>

<span data-ttu-id="1f4f8-109">**単一レコード追加クエリ**:</span><span class="sxs-lookup"><span data-stu-id="1f4f8-109">**Single-record append query**:</span></span>

<span data-ttu-id="1f4f8-110">INSERT INTO*ターゲット* \[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\]の値 (*値 1*\[、*値 2*\[、.\])</span><span class="sxs-lookup"><span data-stu-id="1f4f8-110">INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])</span></span>

<span data-ttu-id="1f4f8-111">INSERT INTO ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-111">The INSERT INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f4f8-112">指定項目</span><span class="sxs-lookup"><span data-stu-id="1f4f8-112">Part</span></span></p></th>
<th><p><span data-ttu-id="1f4f8-113">説明</span><span class="sxs-lookup"><span data-stu-id="1f4f8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f4f8-114"><em>target</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-114"><em>target</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-115">レコードを追加するテーブルまたはクエリの名前。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-115">The name of the table or query to append records to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f4f8-116"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-116"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-117"><em>ターゲット</em>の引数では、次の場合に、データを追加するフィールドの名前または<em>変換元</em>の引数を次の場合からのデータを取得するフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-117">Names of the fields to append data to, if following a <em>target</em> argument, or the names of fields to obtain data from, if following a <em>source</em> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f4f8-118"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-118"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-p102">外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="1f4f8-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f4f8-121"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-121"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-122">コピー元のレコードのあるテーブルまたはクエリの名前。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-122">The name of the table or query to copy records from.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f4f8-123"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-123"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-p103">挿入するレコードのある 1 つ以上のテーブルの名前。単一のテーブル名、保存されたクエリ名、または <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> のいずれかの操作の結果としてできる複合テーブルを指定します。  </span><span class="sxs-lookup"><span data-stu-id="1f4f8-p103">The name of the table or tables from which records are inserted. This argument can be a single table name or a compound resulting from an <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>, <a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>, or <a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> operation or a saved query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f4f8-126"><em>value1</em>、<em>value2</em></span><span class="sxs-lookup"><span data-stu-id="1f4f8-126"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="1f4f8-p104">新しいレコードの特定のフィールドに挿入する値。それぞれの値は、記述順にフィールドに挿入されます。つまり、引数 <em>value1</em> は新しいレコードの引数 <em>field1</em> に、引数 <em>value2</em> は引数 <em>value2</em> に挿入されます。値と値の間はコンマで区切り、テキスト フィールドの値は単一引用符 (') で囲みます。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p104">The values to insert into the specific fields of the new record. Each value is inserted into the field that corresponds to the value's position in the list: <em>value1</em> is inserted into <em>field1</em> of the new record, <em>value2</em> into <em>field2</em>, and so on. You must separate values with a comma, and enclose text fields in quotation marks (' ').</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1f4f8-130">解説</span><span class="sxs-lookup"><span data-stu-id="1f4f8-130">Remarks</span></span>

<span data-ttu-id="1f4f8-p105">INSERT INTO ステートメントで 1 つのレコードを追加するには、上記のように単一レコード追加クエリの構文を使用します。この場合は、レコードの各フィールドの名前と値を指定します。また、値を割り当てるフィールドと、そのフィールドに割り当てる値を指定します。指定していないフィールドには、既定値または **Null** 値が挿入されます。レコードはテーブルの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p105">You can use the INSERT INTO statement to add a single record to a table using the single-record append query syntax as shown above. In this case, your code specifies the name and value for each field of the record. You must specify each of the fields of the record that a value is to be assigned to and a value for that field. When you do not specify each field, the default value or **Null** is inserted for missing columns. Records are added to the end of the table.</span></span>

<span data-ttu-id="1f4f8-136">また、INSERT INTO ステートメントを使用して、別のテーブルからレコードのセットを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-136">You can also use INSERT INTO to append a set of records from another table or query by using the SELECT …</span></span> <span data-ttu-id="1f4f8-137">これには、上記の複数レコード追加クエリの構文で示したように SELECT...FROM 句によるクエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-137">FROM clause as shown above in the multiple-record append query syntax.</span></span> <span data-ttu-id="1f4f8-138">この例では、SELECT 句は、指定された*ターゲット*テーブルに追加するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-138">In this case, the SELECT clause specifies the fields to append to the specified *target* table.</span></span>

<span data-ttu-id="1f4f8-139">*ソース*または*ターゲット*テーブルには、テーブルまたはクエリを指定できます。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-139">The *source* or *target* table may specify a table or a query.</span></span> <span data-ttu-id="1f4f8-140">クエリを指定した場合、Microsoft Access データベース エンジンは、クエリで指定したすべてのテーブルにレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-140">If a query is specified, the Microsoft Access database engine appends records to any and all tables specified by the query.</span></span>

<span data-ttu-id="1f4f8-141">INSERT INTO ステートメントは省略可能ですが、使用する場合 [SELECT](select-statement-microsoft-access-sql.md) ステートメントよりも前に記述します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-141">INSERT INTO is optional but when included, precedes the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="1f4f8-142">レコードの追加先のテーブルに主キーがある場合、その主キー フィールドには必ず **Null** 値以外の一意な値を追加するようにしてください。この条件が満たされない場合、Microsoft Access データベース エンジンはレコードを追加しません。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-142">If your destination table contains a primary key, make sure you append unique, non-**Null** values to the primary key field or fields; if you do not, the Microsoft Access database engine will not append the records.</span></span>

<span data-ttu-id="1f4f8-p108">オートナンバ型 (AutoNumber) フィールドのあるテーブルにレコードを追加する場合、追加したレコードに新しく番号を割り当てる場合は、クエリにオートナンバ型 (AutoNumber) フィールドを含めないでください。既にこのフィールドに割り当てられている値をそのまま使用する場合は、クエリにオートナンバ型 (AutoNumber) フィールドを含めてください。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p108">If you append records to a table with an AutoNumber field and you want to renumber the appended records, do not include the AutoNumber field in your query. Do include the AutoNumber field in the query if you want to retain the original values from the field.</span></span>

<span data-ttu-id="1f4f8-145">別のデータベースにあるテーブルにレコードを追加するには、IN 句を使用します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-145">Use the IN clause to append records to a table in another database.</span></span>

<span data-ttu-id="1f4f8-146">新しいテーブルを作成する場合は、INSERT INTO ステートメントではなく、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントを使用してテーブル作成クエリを作成してください。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-146">To create a new table, use the [SELECT… INTO](select-into-statement-microsoft-access-sql.md) statement instead to create a make-table query.</span></span>

<span data-ttu-id="1f4f8-147">追加クエリを実行する前にどのレコードが追加されるかをあらかじめ確認する場合は、同じ抽出条件の選択クエリを実行してその結果を確認してください。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-147">To find out which records will be appended before you run the append query, first execute and view the results of a select query that uses the same selection criteria.</span></span>

<span data-ttu-id="1f4f8-p109">追加クエリを実行すると、1 つまたは複数のテーブルから他のテーブルにレコードがコピーされます。追加クエリを実行しても、レコードのコピー元のテーブルは変更されません。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p109">An append query copies records from one or more tables to another. The tables that contain the records you append are not affected by the append query.</span></span>

<span data-ttu-id="1f4f8-p110">別のテーブルからの既存のレコードを追加する代わりに、VALUES 句を使用して、各フィールドの値を指定した単一の新規レコードを追加することもできます。フィールド リストを省略する場合は、VALUES 句にはテーブルにあるすべてのフィールドの値を指定してください。すべてのフィールドの値を指定しないと、INSERT 操作は失敗します。VALUES 句を使用する INSERT INTO ステートメントは、追加するレコードの数だけ記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p110">Instead of appending existing records from another table, you can specify the value for each field in a single new record using the VALUES clause. If you omit the field list, the VALUES clause must include a value for every field in the table; otherwise, the INSERT operation will fail. Use an additional INSERT INTO statement with a VALUES clause for each additional record you want to create.</span></span>

<span data-ttu-id="1f4f8-153">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-153">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="1f4f8-154">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-154">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="1f4f8-155">INSERT/UPDATE ステートメントのための連続番号を生成</span><span class="sxs-lookup"><span data-stu-id="1f4f8-155">Generating sequential numbers for INSERT/UPDATE statements</span></span>](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [<span data-ttu-id="1f4f8-156">SQL から VBA のフォーマッタ</span><span class="sxs-lookup"><span data-stu-id="1f4f8-156">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a><span data-ttu-id="1f4f8-157">使用例</span><span class="sxs-lookup"><span data-stu-id="1f4f8-157">Example</span></span>

<span data-ttu-id="1f4f8-p112">次の例では、仮想の New Customers テーブルのすべてのレコードを選択し、それを Customers テーブルに追加します。列を個別に指定しない場合、SELECT テーブルの列名が INSERT INTO テーブルの列名と厳密に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-p112">This example selects all records in a hypothetical New Customers table and adds them to the Customers table. When individual columns are not designated, the SELECT table column names must match exactly those in the INSERT INTO table.</span></span>

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

<span data-ttu-id="1f4f8-160">次の使用例では、Employees テーブルに新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="1f4f8-160">This example creates a new record in the Employees table.</span></span>

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

