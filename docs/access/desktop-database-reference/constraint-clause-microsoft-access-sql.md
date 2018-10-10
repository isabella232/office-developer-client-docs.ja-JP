---
title: CONSTRAINT 句 (Microsoft Access SQL)
TOCTitle: CONSTRAINT Clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7b26033c8026591c87e4d0f9e077380862e39f16
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476447"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="a2c68-102">CONSTRAINT 句 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a2c68-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="a2c68-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2c68-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a2c68-104">CONSTRAINT (制約) はインデックスに似ています。インデックスと違う点は、他のテーブルとのリレーションシップも設定できることです。</span><span class="sxs-lookup"><span data-stu-id="a2c68-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="a2c68-p101">CONSTRAINT 句は、[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントおよび [CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントの中で制約を作成または削除する場合に使用します。CONSTRAINT 句には、単一フィールドの制約を作成するものと、複数フィールドの制約を作成するものの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>


> [!NOTE]
> <span data-ttu-id="a2c68-p102">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CONSTRAINT 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース以外のデータベースでは代わりに DAO の Create 系メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p102">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases. Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c68-109">構文</span><span class="sxs-lookup"><span data-stu-id="a2c68-109">Syntax</span></span>

<span data-ttu-id="a2c68-110">単一フィールド制約の場合:</span><span class="sxs-lookup"><span data-stu-id="a2c68-110">Single-field constraint:</span></span>

<span data-ttu-id="a2c68-111">制約*名*{主キー。固有 |NOT NULL。参照*外部テーブル* \[(*foreignfield1、foreignfield2*)\] \[ON UPDATE CASCADE |設定 NULL\] \[ON DELETE CASCADE |NULL 設定\]}</span><span class="sxs-lookup"><span data-stu-id="a2c68-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="a2c68-112">複数フィールド制約の場合:</span><span class="sxs-lookup"><span data-stu-id="a2c68-112">Multiple-field constraint:</span></span>

<span data-ttu-id="a2c68-113">制約*名*{0} プライマリ ・ キー (*primary1*\[、 *primary2* \[、.\]\]) |一意 (*unique 1*\[、 *unique2* \[、.\]\]) |NOT NULL (*notnull1*\[、 *notnull2* \[、.\]\]) |外部キー\[インデックスのない\](*範囲 1*\[、 *ref2* \[、.\] \]) の参照*外部テーブル* \[(*foreignfield1* \[、 *foreignfield2* \[、.\] \])\] \[ON UPDATE CASCADE |設定 NULL\] \[ON DELETE CASCADE |NULL 設定\]}</span><span class="sxs-lookup"><span data-stu-id="a2c68-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="a2c68-114">CONSTRAINT 句には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="a2c68-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2c68-115">指定項目</span><span class="sxs-lookup"><span data-stu-id="a2c68-115">Part</span></span></p></th>
<th><p><span data-ttu-id="a2c68-116">説明</span><span class="sxs-lookup"><span data-stu-id="a2c68-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2c68-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-118">作成する制約の名前。</span><span class="sxs-lookup"><span data-stu-id="a2c68-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2c68-119"><em>primary1</em>, <em>primary2</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-120">主キーに指定するフィールドの名前。複数指定もできます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2c68-121"><em>unique1</em>, <em>unique2</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-122">一意なキーに指定するフィールドの名前。複数指定もできます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2c68-123"><em>notnull1, notnull2</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-124">非 Null 値に制限されるフィールドの名前。複数指定もできます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2c68-125"><em>ref1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-126">別のテーブルにあるフィールドを参照する外部キー フィールドの名前。複数指定もできます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2c68-127"><em>foreigntable</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-128">引数 <em>foreignfield</em> で指定した 1 つ以上のフィールドのある外部キー側のテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="a2c68-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2c68-129"><em>foreignfield1</em>, <em>foreignfield2</em></span><span class="sxs-lookup"><span data-stu-id="a2c68-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="a2c68-p103">引数 <em>ref1</em>、<em>ref2</em> で指定した引数 <em>foreigntable</em> の 1 つ以上のフィールドの名前。参照されるフィールドが引数 <em>foreigntable</em> の主キーである場合は、この句を省略できます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a2c68-132">解説</span><span class="sxs-lookup"><span data-stu-id="a2c68-132">Remarks</span></span>

<span data-ttu-id="a2c68-133">単一フィールドの CONSTRAINT 構文は、ALTER TABLE ステートメントや CREATE TABLE ステートメントなどのフィールド定義句の中で、フィールド データ型の指定の直後に記述します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="a2c68-134">ALTER TABLE ステートメントや CREATE TABLE ステートメントのフィールド定義句以外の箇所で予約語 CONSTRAINT を使用する場合は、必ず複数フィールドの CONSTRAINT 構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="a2c68-135">CONSTRAINT 句を使用すると、次のいずれかの制約をフィールドに適用できます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="a2c68-p104">予約語 UNIQUE を使用すると、フィールドを一意なキーとして指定できます。この結果、テーブルでこのフィールドの値を 2 つのレコードに同時に設定することはできなくなります。どのフィールドでも一意なキーに指定することができます。数にも制限はありません。複数フィールドの制約を一意なキーとして指定した場合は、インデックス内のすべてのフィールドの値の組み合わせが重複しないようにする必要があります。1 つのフィールドのみで複数のレコードが同じ値を持っている場合も同様です。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="a2c68-p105">予約語 PRIMARY KEY を使用すると、テーブル内の 1 つ以上のフィールド セットを主キーとして指定できます。主キーの値はすべて **Null** 値以外の一意な値である必要があります。1 つのテーブルに指定できる主キーは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="a2c68-142">[!メモ] 既に主キーが設定されているテーブルには PRIMARY KEY 制約を設定しないでください。設定した場合はエラーになります。</span><span class="sxs-lookup"><span data-stu-id="a2c68-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="a2c68-p106">予約語 FOREIGN KEY を使用すると、指定したフィールドを外部キーにすることができます。外部キー側のテーブルの主キーが複数のフィールドから成る場合は、必ず複数フィールドの制約の定義を使用し、すべての参照元フィールド、外部キー側のテーブル名、および外部キー側のテーブルのすべての参照先フィールドの名前を、それぞれ指定してください。この場合は、参照先フィールドは参照元フィールドと同じ順序で指定してください。既定では、データベース エンジンは外部キー側のテーブルの主キーを参照先フィールドと見なします。このため、参照先フィールドが外部キー側のテーブルの主キーである場合は、参照先フィールドを指定する必要ありません。 外部キーの制約は、対応する主キーの値が変更されるときに行われる特定の動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="a2c68-p107">外部キー側のテーブルで行われる動作を指定することができます。この指定は、CONSTRAINT が定義されるテーブルの対応する主キーで行われる動作に基づきます。たとえば、Customers テーブルに関して次のような定義を考えます。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="a2c68-150">Orders テーブルの次のような定義を考えます。この Orders テーブルは、Customers テーブルの主キーを参照する外部キーのリレーションシップを定義しています。</span><span class="sxs-lookup"><span data-stu-id="a2c68-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="a2c68-p108">ON UPDATE CASCADE 句と ON DELETE CASCADE 句は、どちらも外部キー上に定義されます。ON UPDATE CASCADE 句は、Customers テーブルで顧客の情報 (CustId) が更新された場合、この更新が Orders テーブルをとおしてカスケードされることを意味します。各注文に含まれる、対応した顧客情報の値は、自動的に新しい値に更新されます。ON DELETE CASCADE 句は、Customers テーブルで顧客が削除された場合、Orders テーブルにある同じ顧客の顧客情報の値を含む行もすべて同様に削除されることを意味します。 CASCADE アクションの代わりに SET NULL アクションを使う、次のような Orders テーブルの異なる定義について検討します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="a2c68-p109">ON UPDATE SET NULL 句は、Customers テーブルで顧客の情報 (CustId) が更新された場合、Orders テーブルの対応する外部キーの値が自動的に NULL に設定されることを意味します。同様に、ON UPDATE SET NULL 句は、顧客が Customers テーブルから削除された場合、Orders テーブルの対応するすべての外部キーの値が、自動的に NULL に設定されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="a2c68-p110">外部キーに自動的にインデックスが作成されることを防ぐために、修飾子 NO INDEX を使用できます。この外部キーを定義する形式は、結果としてインデックスの値が頻繁に繰り返される場合に限り使用してください。外部キーのインデックスの値が頻繁に繰り返される中でインデックスを使用することは、単にテーブルのスキャンを行うよりも能率が下がります。テーブルから挿入や削除された行と一緒にこの種のインデックスを保守することは、パフォーマンスを下げるばかりで何の利益も生み出しません。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="a2c68-162">使用例</span><span class="sxs-lookup"><span data-stu-id="a2c68-162">Example</span></span>

<span data-ttu-id="a2c68-163">次の使用例では、2 つのテキスト フィールドを含む "ThisTable" という名前の新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-163">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="a2c68-164">次の使用例では、テキスト フィールド 2 つと日付/時刻型 (Date/Time) フィールド、および 3 つのフィールドすべてから作成された一意のインデックスを含む、"MyTable" というテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2c68-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="a2c68-p111">次の使用例では、2 つのテキスト フィールドおよび整数型 ( **Integer** ) フィールドを含む新しいテーブルを作成します。SSN フィールドは主キーです。</span><span class="sxs-lookup"><span data-stu-id="a2c68-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

