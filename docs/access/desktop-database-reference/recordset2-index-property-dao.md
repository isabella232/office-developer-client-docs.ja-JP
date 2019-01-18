---
title: Recordset2.Index プロパティ (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716769"
---
# <a name="recordset2index-property-dao"></a><span data-ttu-id="44f5c-102">Recordset2.Index プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="44f5c-102">Recordset2.Index property (DAO)</span></span>

<span data-ttu-id="44f5c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="44f5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44f5c-104">テーブル タイプの **[Recordset](index-object-dao.md)** オブジェクト内にある現在の **[Index](recordset-object-dao.md)** オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="44f5c-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="44f5c-105">構文</span><span class="sxs-lookup"><span data-stu-id="44f5c-105">Syntax</span></span>

<span data-ttu-id="44f5c-106">*式*です。インデックス</span><span class="sxs-lookup"><span data-stu-id="44f5c-106">*expression* .Index</span></span>

<span data-ttu-id="44f5c-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="44f5c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f5c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="44f5c-108">Remarks</span></span>

<span data-ttu-id="44f5c-p101">レコードはベース テーブルに特定の順序で格納されているわけではありません。 **Index** プロパティを設定すると、データベースから取得されるレコードの順序は変わりますが、格納されているレコードの順序は変わりません。</span><span class="sxs-lookup"><span data-stu-id="44f5c-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="44f5c-p102">指定する **Index** オブジェクトは前もって定義しておく必要があります。存在していない **Index** オブジェクトに **Index** プロパティを設定するか、または [**Seek**](recordset2-seek-method-dao.md) メソッドを使用するときに **Index** プロパティが設定されていない場合、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="44f5c-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="44f5c-113">**TableDef** オブジェクトの **Indexes** コレクションを調べ、 **TableDef** オブジェクトから作成されたテーブル タイプの **Recordset** オブジェクトに使用できる **Index** オブジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="44f5c-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="44f5c-114">テーブルの新しいインデックスを作成する場合は、新しい **Index** オブジェクトを作成し、そのプロパティを設定して、基になる **TableDef** オブジェクトの **Indexes** コレクションにそのオブジェクトを追加した後、再び **Recordset** オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="44f5c-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="44f5c-115">テーブル タイプの **Recordset** オブジェクトは、基になる **TableDef** オブジェクトにインデックスを定義した場合にのみ、レコードを必要な順序で取得できます。</span><span class="sxs-lookup"><span data-stu-id="44f5c-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="44f5c-116">別の順序でレコードを並べ替えるには、ORDER BY 句を持つ SQL ステートメントを使用して、ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="44f5c-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="44f5c-p104">テーブルにインデックスを作成するのは必須ではありません。大きなテーブルではインデックスを持たないと、特定のレコードへのアクセスまたは **Recordset** オブジェクトの作成に長い時間がかかる場合があります。一方、インデックスを多く作成しすぎると、すべてのインデックスが自動的に更新されるため、更新、追加、および削除を実行する速度が低下します。</span><span class="sxs-lookup"><span data-stu-id="44f5c-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="44f5c-120">インデックスを持たないテーブルから返されるレコードの順序は特定できません。</span><span class="sxs-lookup"><span data-stu-id="44f5c-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="44f5c-121">[Index](field-attributes-property-dao.md) オブジェクト内にある各 [**Field**](field-object-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="44f5c-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="44f5c-122">一意のインデックスを使用すると、最適な方法でレコードを検索できます。</span><span class="sxs-lookup"><span data-stu-id="44f5c-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="44f5c-123">インデックスは、ベース テーブルの物理的な順序には影響を与えません。特定のインデックスを選択するか、 **Recordset** オブジェクトを開く際の、テーブル タイプの **Recordset** オブジェクトによるレコードへのアクセス方法にのみ影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="44f5c-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>

## <a name="example"></a><span data-ttu-id="44f5c-124">例</span><span class="sxs-lookup"><span data-stu-id="44f5c-124">Example</span></span>

<span data-ttu-id="44f5c-125">この例では、 **Index** プロパティを使用して、テーブル タイプの **Recordset** オブジェクトにさまざまなレコード順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="44f5c-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="44f5c-126">この例では、 **Seek** メソッドを使用して、ユーザーが ID 番号に基づき製品を検索できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="44f5c-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
