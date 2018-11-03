---
title: CREATE TABLE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4beb013b09ce136d6ffa7558225e01fae80da645
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937093"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="b82d8-102">CREATE TABLE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b82d8-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b82d8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b82d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b82d8-104">新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="b82d8-105">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE TABLE 句や DDL (データ定義言語) ステートメントを使用できません。</span><span class="sxs-lookup"><span data-stu-id="b82d8-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="b82d8-106">代わりに DAO の**Create**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82d8-107">構文</span><span class="sxs-lookup"><span data-stu-id="b82d8-107">Syntax</span></span>

<span data-ttu-id="b82d8-108">作成\[一時\]テーブルの*テーブル*(*フィールド 1 種類* \[(*サイズ*)\] \[NOT NULL\] \[で圧縮。COMP と\] \[ *index1* \] \[、 *field2* *型* \[(*サイズ*)\] \[NOT NULL\] \[ *index2* \] \[、.\] \] \[、制約*multifieldindex* \[、.\]\])</span><span class="sxs-lookup"><span data-stu-id="b82d8-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="b82d8-109">CREATE TABLE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="b82d8-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b82d8-110">指定項目</span><span class="sxs-lookup"><span data-stu-id="b82d8-110">Part</span></span></p></th>
<th><p><span data-ttu-id="b82d8-111">説明</span><span class="sxs-lookup"><span data-stu-id="b82d8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b82d8-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-113">作成するテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="b82d8-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b82d8-114"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-p102">新しいテーブルに作成するフィールドの名前。少なくとも 1 つのフィールドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b82d8-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b82d8-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-118">新規テーブルの<em>フィールド</em>のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="b82d8-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b82d8-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-120">バイト数で表したフィールド サイズ。テキスト型 (Text) およびバイナリ型 (Binary) フィールドのみ指定します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b82d8-121"><em>index1</em>, <em>index2</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-122">単一フィールドを定義する CONSTRAINT 句。</span><span class="sxs-lookup"><span data-stu-id="b82d8-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="b82d8-123">このインデックスを作成する方法の詳細については、<a href="constraint-clause-microsoft-access-sql.md">制約句</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b82d8-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b82d8-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="b82d8-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="b82d8-125">複数フィールドを定義する CONSTRAINT 句。</span><span class="sxs-lookup"><span data-stu-id="b82d8-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="b82d8-126">このインデックスを作成する方法の詳細については、<a href="constraint-clause-microsoft-access-sql.md">制約句</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b82d8-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b82d8-127">解説</span><span class="sxs-lookup"><span data-stu-id="b82d8-127">Remarks</span></span>

<span data-ttu-id="b82d8-128">CREATE TABLE ステートメントを使用すると、新しいテーブルとそのフィールド、およびフィールドの制約を定義できます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="b82d8-129">しない場合は、フィールドに NULL が指定されて、新しいレコードがそのフィールドに有効なデータが存在する必要です。</span><span class="sxs-lookup"><span data-stu-id="b82d8-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="b82d8-p106">CONSTRAINT 句はフィールドに対してさまざまな制約を設定するもので、これを使用して主キーを設定することができます。また、[CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用して、既存のテーブルに主キーまたは追加のインデックスを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="b82d8-p107">NOT NULL は、単一フィールド、または名前付き CONSTRAINT 句の内部で使用できます。名前付き CONSTRAINT 句は、単一フィールドまたは複数フィールドのどちらかの名前付き CONSTRAINT 句に適用されます。ただし、NOT NULL の制約を適用できるのはフィールドに対して一度のみです。再度適用しようとした場合は実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="b82d8-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="b82d8-135">一時テーブルを作成するときは表示が作成されたセッション内でのみです。</span><span class="sxs-lookup"><span data-stu-id="b82d8-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="b82d8-136">セッションが終了すると、自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="b82d8-137">一時テーブルは、複数のユーザーからアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="b82d8-138">WITH COMPRESSION 属性には、テキスト型 (Text) であるメモ型 (Memo) や文字型 (Character) および類似のデータ型のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="b82d8-139">Unicode 文字の表示形式に変更するために、WITH COMPRESSION 属性が CHARACTER 列に追加されました。</span><span class="sxs-lookup"><span data-stu-id="b82d8-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="b82d8-140">Unicode 文字には、各文字一律に 2 バイトを必要とします。</span><span class="sxs-lookup"><span data-stu-id="b82d8-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="b82d8-141">主文字データを含む既存の Microsoft Jet データベースを Microsoft Access データベース エンジンの形式に変換するときのサイズで、データベース ・ ファイルがほぼ 2 倍はこの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b82d8-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="b82d8-142">ただし、sbcs 以前 1 バイト文字を設定 ()、多くの文字セットの Unicode 表現は簡単に 1 バイトに圧縮できます。</span><span class="sxs-lookup"><span data-stu-id="b82d8-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="b82d8-143">CHARACTER 列をこの属性で定義すると、データが格納時には自動的に圧縮され、取得時には圧縮解除されるようになります。</span><span class="sxs-lookup"><span data-stu-id="b82d8-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="b82d8-p110">MEMO 列もデータの格納を圧縮形式で定義することができます。ただし、これには制限があります。圧縮時 4096 バイト以下になる MEMO 列のインスタンスのみ圧縮されます。それ以外の MEMO 列のインスタンスは圧縮されずに残ります。これは、所定のテーブルの所定の MEMO 列で、圧縮されたデータと圧縮されていないデータが混在している可能性があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="b82d8-149">使用例</span><span class="sxs-lookup"><span data-stu-id="b82d8-149">Example</span></span>

<span data-ttu-id="b82d8-150">次の使用例では、2 つのテキスト フィールドを含む "ThisTable" という名前の新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="b82d8-151">次の使用例では、テキスト フィールド 2 つと日付/時刻型 (Date/Time) フィールド、および 3 つのフィールドすべてから作成された一意のインデックスを含む、"MyTable" というテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b82d8-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="b82d8-p111">次の使用例では、2 つのテキスト フィールドおよび整数型 ( **Integer** ) フィールドを含む新しいテーブルを作成します。SSN フィールドは主キーです。</span><span class="sxs-lookup"><span data-stu-id="b82d8-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
