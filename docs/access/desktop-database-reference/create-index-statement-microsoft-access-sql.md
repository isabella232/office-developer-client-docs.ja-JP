---
title: CREATE INDEX ステートメント (Microsoft Access SQL)
TOCTitle: CREATE INDEX statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 46bc0a50e31555189c069e0ee09c4c84349c04c7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710952"
---
# <a name="create-index-statement-microsoft-access-sql"></a><span data-ttu-id="6aae3-102">CREATE INDEX ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6aae3-102">CREATE INDEX statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="6aae3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6aae3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6aae3-104">既存のテーブルに新しいインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-104">Creates a new index on an existing table.</span></span>

> [!NOTE]
> <span data-ttu-id="6aae3-105">Microsoft Access 以外のデータベース エンジンのデータベースを Microsoft Access データベース エンジンに以外には、ODBC のリンク テーブルに擬似インデックスを作成) のインデックスの作成またはデータ定義言語 (DDL) ステートメントのいずれかの使用はできません。</span><span class="sxs-lookup"><span data-stu-id="6aae3-105">For non-Microsoft Access database engine databases, the Microsoft Access database engine does not support the use of CREATE INDEX (except to create a pseudo index on an ODBC linked table) or any of the data definition language (DDL) statements.</span></span> <span data-ttu-id="6aae3-106">代わりに DAO の**Create**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-106">Use the DAO **Create** methods instead.</span></span> <span data-ttu-id="6aae3-107">詳細については、「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6aae3-107">For more information, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aae3-108">構文</span><span class="sxs-lookup"><span data-stu-id="6aae3-108">Syntax</span></span>

<span data-ttu-id="6aae3-109">作成\[独自の\]*インデックス*の*テーブル*のインデックス (*フィールド* \[ASC |DESC\]\[、*フィールド* \[ASC |DESC\]をしています.\]) \[WITH {主 |NULL を許可しません。NULL を無視します。\]</span><span class="sxs-lookup"><span data-stu-id="6aae3-109">CREATE \[ UNIQUE \] INDEX *index* ON *table* (*field* \[ASC|DESC\]\[, *field* \[ASC|DESC\], …\]) \[WITH { PRIMARY | DISALLOW NULL | IGNORE NULL }\]</span></span>

<span data-ttu-id="6aae3-110">CREATE INDEX ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="6aae3-110">The CREATE INDEX statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6aae3-111">指定項目</span><span class="sxs-lookup"><span data-stu-id="6aae3-111">Part</span></span></p></th>
<th><p><span data-ttu-id="6aae3-112">説明</span><span class="sxs-lookup"><span data-stu-id="6aae3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6aae3-113"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="6aae3-113"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="6aae3-114">作成するインデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="6aae3-114">The name of the index to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6aae3-115"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="6aae3-115"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="6aae3-116">インデックスを作成する既存のテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6aae3-116">The name of the existing table that will contain the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6aae3-117"><em>field</em></span><span class="sxs-lookup"><span data-stu-id="6aae3-117"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="6aae3-p102">インデックスを付けるフィールドの名前。単一フィールド インデックスを作成するには、テーブル名の後にフィールド名をかっこで囲んで指定します。複数フィールド インデックスを作成するには、インデックスを設定するフィールドの名前をすべて列挙します。また、降順のインデックスを作成するには、予約語 DESC を使用します。DESC による指定がなければ昇順と見なされます。</span><span class="sxs-lookup"><span data-stu-id="6aae3-p102">The name of the field or fields to be indexed. To create a single-field index, list the field name in parentheses following the table name. To create a multiple-field index, list the name of each field to be included in the index. To create descending indexes, use the DESC reserved word; otherwise, indexes are assumed to be ascending.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6aae3-122">解説</span><span class="sxs-lookup"><span data-stu-id="6aae3-122">Remarks</span></span>

<span data-ttu-id="6aae3-123">インデックス フィールドの値がレコード間で重複しないようにするには、予約語 UNIQUE を使用します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-123">To prohibit duplicate values in the indexed field or fields of different records, use the UNIQUE reserved word.</span></span>

<span data-ttu-id="6aae3-124">省略可能な句を使用して、データの入力規則を適用できます。</span><span class="sxs-lookup"><span data-stu-id="6aae3-124">In the optional WITH clause, you can enforce data validation rules.</span></span> <span data-ttu-id="6aae3-125">次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6aae3-125">You can:</span></span>

- <span data-ttu-id="6aae3-126">DISALLOW NULL オプションを使用すると、新しいレコードのインデックス フィールドに Null 値を入力できなくなります。</span><span class="sxs-lookup"><span data-stu-id="6aae3-126">Prohibit Null entries in the indexed field or fields of new records by using the DISALLOW NULL option.</span></span>

- <span data-ttu-id="6aae3-127">IGNORE NULL オプションを使用すると、インデックス フィールドに **Null** 値が格納されているレコードを、インデックスに入れることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="6aae3-127">Prevent records with **Null** values in the indexed field or fields from being included in the index by using the IGNORE NULL option.</span></span>

- <span data-ttu-id="6aae3-p104">予約語 PRIMARY を使用すると、インデックス フィールドを主キーとして指定します。これによりキーが一意な値になるため、予約語 UNIQUE は省略できます。</span><span class="sxs-lookup"><span data-stu-id="6aae3-p104">Designate the indexed field or fields as the primary key by using the PRIMARY reserved word. This implies that the key is unique, so you can omit the UNIQUE reserved word.</span></span>

<span data-ttu-id="6aae3-130">インデックスの作成を使用すると、インデックスがない、Microsoft SQL Server などの ODBC データ ソースにリンクされているテーブルに擬似インデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-130">You can use CREATE INDEX to create a pseudo index on a linked table in an ODBC data source, such as Microsoft SQL Server, that does not already have an index.</span></span> <span data-ttu-id="6aae3-131">、擬似インデックスを作成するには、アクセス許可またはリモート サーバーにアクセスする必要はありませんし、リモート ・ データベースを認識しないと、擬似インデックスによって影響を受けていないのです。</span><span class="sxs-lookup"><span data-stu-id="6aae3-131">You do not need permission or access to the remote server to create a pseudo index, and the remote database is unaware of and unaffected by the pseudo index.</span></span> <span data-ttu-id="6aae3-132">リンクとネイティブの両方のテーブルには、同じ構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-132">You use the same syntax for both linked and native tables.</span></span> <span data-ttu-id="6aae3-133">擬似インデックスを作成するには通常は読み取り専用テーブルには、特に便利です。</span><span class="sxs-lookup"><span data-stu-id="6aae3-133">Creating a pseudo-index on a table that would ordinarily be read-only can be especially useful.</span></span>

<span data-ttu-id="6aae3-134">[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントを使用して、テーブルに単一フィールド インデックスまたは複数フィールド インデックスを追加することもできます。ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは [DROP](drop-statement-microsoft-access-sql.md) ステートメントを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="6aae3-134">You can also use the [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use the ALTER TABLE statement or the [DROP](drop-statement-microsoft-access-sql.md) statement to remove an index created with ALTER TABLE or CREATE INDEX.</span></span>

> [!NOTE]
> <span data-ttu-id="6aae3-135">[!メモ] 既に主キーが設定されているテーブルに新しいインデックスを作成する場合は、予約語 PRIMARY は使用しないでください。使用した場合はエラーになります。</span><span class="sxs-lookup"><span data-stu-id="6aae3-135">Do not use the PRIMARY reserved word when you create a new index on a table that already has a primary key; if you do, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="6aae3-136">使用例</span><span class="sxs-lookup"><span data-stu-id="6aae3-136">Example</span></span>

<span data-ttu-id="6aae3-137">次の使用例では、Employees テーブルの "Home Phone" および "Extension" というフィールドで構成されたインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6aae3-137">This example creates an index consisting of the fields Home Phone and Extension in the Employees table.</span></span>

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="6aae3-p106">次の使用例では、CustomerID フィールドを使用して Customers テーブルにインデックスを作成します。CustomerID フィールドの 2 つのレコードに同じデータを入れることはできません。また、Null 値も入力できません。</span><span class="sxs-lookup"><span data-stu-id="6aae3-p106">This example creates an index on the Customers table using the CustomerID field. No two records can have the same data in the CustomerID field, and no Null values are allowed.</span></span>

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
