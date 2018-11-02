---
title: Recordset.Index プロパティ (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b5f568889d020676be420186b49c9c50c444ee54
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926137"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="b51df-102">Recordset.Index プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="b51df-102">Recordset.Index property (DAO)</span></span>

<span data-ttu-id="b51df-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b51df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b51df-104">テーブル タイプの **[Recordset](index-object-dao.md)** オブジェクト内にある現在の **[Index](recordset-object-dao.md)** オブジェクトの名前を示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b51df-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b51df-105">構文</span><span class="sxs-lookup"><span data-stu-id="b51df-105">Syntax</span></span>

<span data-ttu-id="b51df-106">*式*です。インデックス</span><span class="sxs-lookup"><span data-stu-id="b51df-106">*expression* .Index</span></span>

<span data-ttu-id="b51df-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="b51df-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b51df-108">注釈</span><span class="sxs-lookup"><span data-stu-id="b51df-108">Remarks</span></span>

<span data-ttu-id="b51df-p101">レコードはベース テーブルに特定の順序で格納されているわけではありません。 **Index** プロパティを設定すると、データベースから取得されるレコードの順序は変わりますが、格納されているレコードの順序は変わりません。</span><span class="sxs-lookup"><span data-stu-id="b51df-p101">Records in base tables aren't stored in any particular order. Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="b51df-p102">指定する **Index** オブジェクトは前もって定義しておく必要があります。存在していない **Index** オブジェクトに **Index** プロパティを設定するか、または [**Seek**](recordset-seek-method-dao.md) メソッドを使用するときに **Index** プロパティが設定されていない場合、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b51df-p102">The specified **Index** object must already be defined. If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="b51df-113">**TableDef** オブジェクトの **Indexes** コレクションを調べ、 **TableDef** オブジェクトから作成されたテーブル タイプの **Recordset** オブジェクトに使用できる **Index** オブジェクトを特定します。</span><span class="sxs-lookup"><span data-stu-id="b51df-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="b51df-114">テーブルの新しいインデックスを作成する場合は、新しい **Index** オブジェクトを作成し、そのプロパティを設定して、基になる **TableDef** オブジェクトの **Indexes** コレクションにそのオブジェクトを追加した後、再び **Recordset** オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="b51df-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="b51df-115">テーブル タイプの **Recordset** オブジェクトは、基になる **TableDef** オブジェクトにインデックスを定義した場合にのみ、レコードを必要な順序で取得できます。</span><span class="sxs-lookup"><span data-stu-id="b51df-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="b51df-116">別の順序でレコードを並べ替えるには、ORDER BY 句を持つ SQL ステートメントを使用して、ダイナセット タイプ、スナップショット タイプまたは前方のみタイプの**Recordset**オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="b51df-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="b51df-p104">テーブルにインデックスを作成するのは必須ではありません。大きなテーブルではインデックスを持たないと、特定のレコードへのアクセスまたは **Recordset** オブジェクトの作成に長い時間がかかる場合があります。一方、インデックスを多く作成しすぎると、すべてのインデックスが自動的に更新されるため、更新、追加、および削除を実行する速度が低下します。</span><span class="sxs-lookup"><span data-stu-id="b51df-p104">You don't have to create indexes for tables. With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time. On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="b51df-120">インデックスを持たないテーブルから返されるレコードの順序は特定できません。</span><span class="sxs-lookup"><span data-stu-id="b51df-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="b51df-121">[Index](field-attributes-property-dao.md) オブジェクト内にある各 [**Field**](field-object-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="b51df-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="b51df-122">一意のインデックスを使用すると、最適な方法でレコードを検索できます。</span><span class="sxs-lookup"><span data-stu-id="b51df-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="b51df-123">インデックスを作成してもベース テーブルの物理的な順序は変更されません。インデックスによって変わるのは、特定のインデックスを選択するか、または **Recordset** オブジェクトを開いた場合に、テーブル タイプの **Recordset** オブジェクトでレコードにアクセスする方法のみです。</span><span class="sxs-lookup"><span data-stu-id="b51df-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="b51df-124">例</span><span class="sxs-lookup"><span data-stu-id="b51df-124">Example</span></span>

<span data-ttu-id="b51df-125">この例では、 **Index** プロパティを使用して、テーブル タイプの **Recordset** オブジェクトにさまざまなレコード順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="b51df-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
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

<span data-ttu-id="b51df-126">この例では、 **Seek** メソッドを使用して、ユーザーが ID 番号に基づき製品を検索できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b51df-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
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

<br/>

<span data-ttu-id="b51df-127">次の例は、 Seek メソッドを使用して、リンクしたテーブル内のレコードを見つける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b51df-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="b51df-128">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="b51df-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
