---
title: ALTER TABLE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 07a83c16368caa6e5c05c7554300c5589a437067
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734183"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="821e3-102">ALTER TABLE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="821e3-102">ALTER TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="821e3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="821e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="821e3-104">[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントで作成されたテーブルのデザインを変更します。</span><span class="sxs-lookup"><span data-stu-id="821e3-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="821e3-105">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース以外のデータベースの ALTER TABLE または DDL (データ定義言語) ステートメントをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="821e3-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="821e3-106">代わりに、DAO の **Create** メソッドをご使用ください。</span><span class="sxs-lookup"><span data-stu-id="821e3-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="821e3-107">構文</span><span class="sxs-lookup"><span data-stu-id="821e3-107">Syntax</span></span>

<span data-ttu-id="821e3-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span><span class="sxs-lookup"><span data-stu-id="821e3-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="821e3-109">ALTER TABLE ステートメントでは、次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="821e3-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="821e3-110">パーツ</span><span class="sxs-lookup"><span data-stu-id="821e3-110">Part</span></span></p></th>
<th><p><span data-ttu-id="821e3-111">説明</span><span class="sxs-lookup"><span data-stu-id="821e3-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="821e3-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="821e3-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-113">変更されるテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="821e3-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="821e3-114"><em>field</em></span><span class="sxs-lookup"><span data-stu-id="821e3-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-115"><em>table</em> に対して追加または削除されるフィールドの名前です。</span><span class="sxs-lookup"><span data-stu-id="821e3-115">The name of the field to be added to or deleted from <em>table</em>.</span></span> <span data-ttu-id="821e3-116">または、<em>table</em> で変更されるフィールドの名前です。</span><span class="sxs-lookup"><span data-stu-id="821e3-116">Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="821e3-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="821e3-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-118">
            <em>field</em> のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="821e3-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="821e3-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="821e3-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-120">文字数単位のフィールド サイズです (テキスト型とバイナリ型のフィールドのみ)。</span><span class="sxs-lookup"><span data-stu-id="821e3-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="821e3-121"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="821e3-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-122"><em>field</em> のインデックスです。</span><span class="sxs-lookup"><span data-stu-id="821e3-122">The index for <em>field</em>.</span></span> <span data-ttu-id="821e3-123">このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="821e3-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="821e3-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="821e3-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-125"><em>table</em> に追加される複数フィールド インデックス定義です。</span><span class="sxs-lookup"><span data-stu-id="821e3-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="821e3-126">このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="821e3-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="821e3-127"><em>indexname</em></span><span class="sxs-lookup"><span data-stu-id="821e3-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="821e3-128">削除される複数フィールド インデックスの名前です。</span><span class="sxs-lookup"><span data-stu-id="821e3-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="821e3-129">注釈</span><span class="sxs-lookup"><span data-stu-id="821e3-129">Remarks</span></span>

<span data-ttu-id="821e3-130">ALTER TABLE ステートメントを使用すると、いくつかの方法で既存のテーブルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="821e3-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="821e3-131">以下のことが実行できます。</span><span class="sxs-lookup"><span data-stu-id="821e3-131">You can:</span></span>

- <span data-ttu-id="821e3-p106">ADD COLUMN を使用して新しいフィールドをテーブルに追加します。フィールド名、データ型、および (テキスト型とバイナリ型のフィールドの場合) 省略可能なサイズを指定します。たとえば、次のステートメントでは、Notes という 25 文字のテキスト型フィールドを Employees テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="821e3-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="821e3-135">そのフィールドにインデックスを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="821e3-135">You can also define an index on that field.</span></span> <span data-ttu-id="821e3-136">単一フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="821e3-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="821e3-137">フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。</span><span class="sxs-lookup"><span data-stu-id="821e3-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="821e3-p108">既存のフィールドのデータ型を変更するには、ALTER COLUMN を使用します。フィールド名、新しいデータ型、および (テキスト型とバイナリ型のフィールドの場合) 省略可能なサイズを指定します。たとえば、次のステートメントでは、Employees テーブルの ZipCode というフィールドの (元は整数として定義されていた) データ型を 10 文字のテキスト型フィールドに変更しています。</span><span class="sxs-lookup"><span data-stu-id="821e3-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="821e3-141">複数フィールド インデックスを追加するには、ADD CONSTRAINT を使用します。</span><span class="sxs-lookup"><span data-stu-id="821e3-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="821e3-142">複数フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="821e3-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="821e3-p110">フィールドを削除するには、DROP COLUMN を使用します。フィールドの名前のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="821e3-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="821e3-p111">複数フィールド インデックスを削除するには、DROP CONSTRAINT を使用します。予約語の CONSTRAINT に続けて、インデックス名のみを指定します。</span><span class="sxs-lookup"><span data-stu-id="821e3-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="821e3-147">同時に複数のフィールドまたはインデックスを追加または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="821e3-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="821e3-148">[CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用すると、単一フィールド インデックスまたは複数フィールド インデックスをテーブルに追加できます。また、ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは [DROP](drop-statement-microsoft-access-sql.md) ステートメントを使用して削除できます。</span><span class="sxs-lookup"><span data-stu-id="821e3-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="821e3-149">NOT NULL を 1 つのフィールドまたは名前付きの CONSTRAINT 句内で使用し、CONSTRAINT という名前の 1 つのフィールドまたは複数のフィールドに適用することができます。</span><span class="sxs-lookup"><span data-stu-id="821e3-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="821e3-150">ただし、フィールドに NOT NULL 制限を 1 回だけ適用することができます。</span><span class="sxs-lookup"><span data-stu-id="821e3-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="821e3-151">この制限を複数回実行しようすると、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="821e3-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="821e3-152">例</span><span class="sxs-lookup"><span data-stu-id="821e3-152">Example</span></span>

<span data-ttu-id="821e3-153">次の使用例では、データ型が通貨型 ( **Money** ) である Salary フィールドを Employees テーブルに追加します。</span><span class="sxs-lookup"><span data-stu-id="821e3-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="821e3-154">次の使用例では、Salary フィールドのデータ型を通貨型 ( **Money** ) から文字型 ( **Char** ) に変更します。</span><span class="sxs-lookup"><span data-stu-id="821e3-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Modify the existing Salary field of the Employees table  
        ' by changing it to a CHAR data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="821e3-155">次の使用例では、Salary フィールドを Employees テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="821e3-155">This example removes the Salary field from the Employees table.</span></span>

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="821e3-p113">次の使用例では、外部キーを Orders テーブルに追加します。外部キーは、EmployeeID フィールドに基づき、Employees テーブルの EmployeeID フィールドを参照します。この例では、REFERENCES 句の Employees テーブルの後に EmployeeID フィールドをリストする必要はありません。EmployeeID が Employees テーブルの主キーだからです。</span><span class="sxs-lookup"><span data-stu-id="821e3-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="821e3-159">次の使用例では、外部キーを Orders テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="821e3-159">This example removes the foreign key from the Orders table.</span></span>

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
