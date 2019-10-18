---
title: CREATE TABLE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706174"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="6d0e5-102">CREATE TABLE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6d0e5-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="6d0e5-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d0e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d0e5-104">新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="6d0e5-105">Microsoft Access データベース エンジンでは、Microsoft Access データベース エンジン以外のデータベースで CREATE TABLE やその他の DDL ステートメントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="6d0e5-106">代わりに、DAO の **Create** メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0e5-107">構文</span><span class="sxs-lookup"><span data-stu-id="6d0e5-107">Syntax</span></span>

<span data-ttu-id="6d0e5-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="6d0e5-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="6d0e5-109">CREATE TABLE ステートメントでは、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d0e5-110">パーツ</span><span class="sxs-lookup"><span data-stu-id="6d0e5-110">Part</span></span></p></th>
<th><p><span data-ttu-id="6d0e5-111">説明</span><span class="sxs-lookup"><span data-stu-id="6d0e5-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d0e5-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-113">作成されるテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d0e5-114"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-p102">新しいテーブルを作成するフィールドの名前です。1 つ以上のフィールドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d0e5-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-118">新しいテーブルの<em>フィールド</em>のデータ型。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d0e5-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-120">文字数単位のフィールド サイズです (テキスト型とバイナリ型のフィールドのみ)。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d0e5-121"><em>index1</em>、<em>index2</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-122">単一フィールド インデックスを定義する CONSTRAINT 句です。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="6d0e5-123">このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d0e5-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="6d0e5-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="6d0e5-125">複数フィールド インデックスを定義する CONSTRAINT 句です。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="6d0e5-126">このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6d0e5-127">注釈</span><span class="sxs-lookup"><span data-stu-id="6d0e5-127">Remarks</span></span>

<span data-ttu-id="6d0e5-128">CREATE TABLE ステートメントを使用して、新しいテーブル、フィールド、およびフィールドの制約を定義します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="6d0e5-129">フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="6d0e5-p106">CONSTRAINT 句はフィールドに対してさまざまな制約を設定するもので、これを使用して主キーを設定することができます。また、[CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用して、既存のテーブルに主キーまたは追加のインデックスを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="6d0e5-p107">NOT NULL を 1 つのフィールドまたは名前付きの CONSTRAINT 句内で使用し、CONSTRAINT という名前の 1 つのフィールドまたは複数のフィールドに適用することができます。ただし、フィールドに NOT NULL 制限を 1 回だけ適用することができます。この制限を複数回実行しようすると、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="6d0e5-135">TEMPORARY テーブルが作成される場合、作成されたセッションの中でのみ見ることができます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="6d0e5-136">セッションの終了時に自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="6d0e5-137">一時テーブルは、複数のユーザーによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="6d0e5-138">WITH COMPRESSION 属性は、CHARACTER および MEMO (TEXT とも呼ばれます) データ型およびそれらの類義語でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="6d0e5-139">Unicode 文字表現形式の変更のために、WITH COMPRESSION 属性が、CHARACTER 列に追加されました。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="6d0e5-140">Unicode 文字では、各文字を格納するのにそれぞれ 2 バイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="6d0e5-141">これは、主に文字データを含む既存の Microsoft Jet データベースを Microsoft Access データベース エンジンの形式に変換すると、ファイル サイズが約 2 倍になることを意味します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="6d0e5-142">しかし、Unicode 表示形式の文字セットの多くは、以前 1 バイトの文字セット (SBCS) であり、簡単に 1 バイトに圧縮することが可能です。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="6d0e5-143">この属性を使用して CHARACTER 型の列を定義すると、列への格納時のデータ圧縮と列からの取得時のデータ圧縮解除が自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="6d0e5-p110">MEMO 型の列を定義すると、圧縮形式でデータを格納することもできます。ただし、これには制限があります。MEMO 型の列のインスタンスが、圧縮されるときには、4096 バイト以内のみが圧縮されます。MEMO 型の列の他のすべてのインスタンスは圧縮されません。これは、特定のテーブル内の MEMO 型の列で、データの一部が圧縮され、一部のデータが圧縮されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="6d0e5-149">例</span><span class="sxs-lookup"><span data-stu-id="6d0e5-149">Example</span></span>

<span data-ttu-id="6d0e5-150">次の使用例では、2 つのテキスト フィールドを含む "ThisTable" という名前の新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-150">This example creates a new table called ThisTable with two text fields.</span></span>

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="6d0e5-151">次の使用例では、テキスト フィールド 2 つと日付/時刻型 (Date/Time) フィールド、および 3 つのフィールドすべてから作成された一意のインデックスを含む、"MyTable" というテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="6d0e5-p111">次の使用例では、2 つのテキスト フィールドおよび整数型 ( **Integer** ) フィールドを含む新しいテーブルを作成します。SSN フィールドは主キーです。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="6d0e5-154">次の使用例では、すべての異なるフィールドとインデックスの種類を示す`~~Kitsch'n Sync`という新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-154">This example creates a new table called `~~Kitsch'n Sync` that demonstrates all the different field and index types.</span></span> <span data-ttu-id="6d0e5-155">AutoNumber フィールドが主キーです。</span><span class="sxs-lookup"><span data-stu-id="6d0e5-155">The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
