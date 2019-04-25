---
title: Database.CreateQueryDef メソッド (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294982"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="474ac-102">Database.CreateQueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="474ac-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="474ac-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="474ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="474ac-104">新しい **[QueryDef](querydef-object-dao.md)** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="474ac-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="474ac-105">構文</span><span class="sxs-lookup"><span data-stu-id="474ac-105">Syntax</span></span>

<span data-ttu-id="474ac-106">*式* .CreateQueryDef (***Name***、***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="474ac-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="474ac-107">*式* **Database** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="474ac-107">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="474ac-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="474ac-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="474ac-109">名前</span><span class="sxs-lookup"><span data-stu-id="474ac-109">Name</span></span></p></th>
<th><p><span data-ttu-id="474ac-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="474ac-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="474ac-111">データ型</span><span class="sxs-lookup"><span data-stu-id="474ac-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="474ac-112">説明</span><span class="sxs-lookup"><span data-stu-id="474ac-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="474ac-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="474ac-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="474ac-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="474ac-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="474ac-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="474ac-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="474ac-116">新しい <strong>QueryDef</strong> の一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="474ac-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="474ac-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="474ac-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="474ac-118">省略可能</span><span class="sxs-lookup"><span data-stu-id="474ac-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="474ac-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="474ac-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="474ac-120"><strong>QueryDef</strong> を定義する SQL ステートメントである <strong>Variant</strong> (<strong>String</strong> サブタイプ)。</span><span class="sxs-lookup"><span data-stu-id="474ac-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="474ac-121">この引数を省略した場合、コレクションへの追加前または追加後に、 <a href="querydef-sql-property-dao.md"><strong>SQL</strong></a> プロパティを設定して、 <strong>QueryDef</strong> を定義できます。</span><span class="sxs-lookup"><span data-stu-id="474ac-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="474ac-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="474ac-122">Return value</span></span>

<span data-ttu-id="474ac-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="474ac-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="474ac-124">注釈</span><span class="sxs-lookup"><span data-stu-id="474ac-124">Remarks</span></span>

<span data-ttu-id="474ac-125">Microsoft Access ワークスペースでは、**QueryDef** の作成時に名前として長さ 0 の文字列以外を指定すると、作成された **QueryDef** オブジェクトが **[QueryDefs](querydefs-collection-dao.md)** コレクションに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="474ac-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="474ac-126">名前で指定されたオブジェクトが既に **QueryDefs** コレクションのメンバーである場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="474ac-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="474ac-127">**CreateQueryDef** メソッドを実行すると、名前の引数に長さ 0 の文字列を使用して一時的な **QueryDef** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="474ac-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="474ac-128">新しく作成した **QueryDef** の **[Name](querydef-name-property-dao.md)** プロパティを長さ 0 の文字列 ("") に設定することにより、これを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="474ac-128">You can also accomplish this by setting the [**Name**](querydef-name-property-dao.md) property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="474ac-129">一時的な **QueryDef** オブジェクトは、**QueryDefs** コレクション内に新しい永続的オブジェクトを作成せずに動的 SQL ステートメントを繰り返し使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="474ac-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="474ac-130">長さ 0 の文字列は永続的な **QueryDef** オブジェクトの有効な名前ではないので、一時的な **QueryDef** をコレクションに追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="474ac-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="474ac-131">新しく作成した **QueryDef** オブジェクトの **Name** プロパティと **SQL** プロパティはいつでも設定が可能であり、設定後に **QueryDef** を **QueryDefs** コレクションに追加できます。</span><span class="sxs-lookup"><span data-stu-id="474ac-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="474ac-132">
            \*\*QueryDef\*\* オブジェクトで SQL ステートメントを実行するには、**[Execute](querydef-execute-method-dao.md)\*\* メソッドまたは \*\*[OpenRecordset](database-openrecordset-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="474ac-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="474ac-133">ODBC データベースを使用して SQL パススルー クエリを実行する場合は、**QueryDef** オブジェクトの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="474ac-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="474ac-134">Microsoft Access データベース エンジンのデータベースで **QueryDefs** コレクションから **QueryDef** オブジェクトを削除するには、コレクションの **[Delete](querydefs-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="474ac-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="474ac-135">例</span><span class="sxs-lookup"><span data-stu-id="474ac-135">Example</span></span>

<span data-ttu-id="474ac-136">この例では、**CreateQueryDef** メソッドを使用して、一時的と永続的な **QueryDef** の両方を作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="474ac-136">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="474ac-137">この手順を実行するには、GetrstTemp 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="474ac-137">The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="474ac-p105">次の例では、**CreateQueryDef** メソッドと **OpenRecordset** メソッド、および **SQL** プロパティを使用して、Microsoft SQL Server サンプル データベース Pubs の題名のテーブルをクエリし、最もよく売れている本の題名と題名識別子を返します。次に、著者のテーブルをクエリし、印税の割合に基づいてそれぞれの著者にボーナス小切手を送信するようユーザーに指示します (ボーナスの合計は 1,000 ドルで、それぞれの著者はこの金額から印税の割合に応じた額を受け取ります)。</span><span class="sxs-lookup"><span data-stu-id="474ac-p105">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book. The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb 
Sub ClientServerX2() 
 
   Dim dbsCurrent As Database 
   Dim qdfBestSellers As QueryDef 
   Dim qdfBonusEarners As QueryDef 
   Dim rstTopSeller As Recordset 
   Dim rstBonusRecipients As Recordset 
   Dim strAuthorList As String 
 
   ' Open a database from which QueryDef objects can be  
   ' created. 
   Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
   ' Create a temporary QueryDef object to retrieve 
   ' data from a Microsoft SQL Server database. 
   Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
   With qdfBestSellers 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT title, title_id FROM titles " & _ 
         "ORDER BY ytd_sales DESC" 
      Set rstTopSeller = .OpenRecordset() 
      rstTopSeller.MoveFirst 
   End With 
 
   ' Create a temporary QueryDef to retrieve data from 
   ' a Microsoft SQL Server database based on the results from 
   ' the first query. 
   Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
   With qdfBonusEarners 
      ' Note: The DSN referenced below must be configured to  
      '       use Microsoft Windows NT Authentication Mode to  
      '       authorize user access to the Microsoft SQL Server. 
      .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
      .SQL = "SELECT * FROM titleauthor " & _ 
         "WHERE title_id = '" & _ 
         rstTopSeller!title_id & "'" 
      Set rstBonusRecipients = .OpenRecordset() 
   End With 
 
   ' Build the output string. 
   With rstBonusRecipients 
      Do While Not .EOF 
         strAuthorList = strAuthorList & "  " & _ 
            !au_id & ":  $" & (10 * !royaltyper) & vbCr 
         .MoveNext 
      Loop 
   End With 
 
   ' Display results. 
   MsgBox "Please send a check to the following " & _ 
      "authors in the amounts shown:" & vbCr & _ 
      strAuthorList & "for outstanding sales of " & _ 
      rstTopSeller!Title & "." 
 
   rstTopSeller.Close 
   dbsCurrent.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="474ac-140">次の例は、パラメーター クエリを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="474ac-140">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="474ac-141">Param1 および Param2 という名前の 2 つのパラメーターを使用して **myQuery** という名前のクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="474ac-141">A query named myQuery is created with two parameters, named  Param1 and  Param2.</span></span> <span data-ttu-id="474ac-142">これを行うために、クエリの SQL プロパティは、パラメータを定義する Structured Query Language (SQL) ステートメントに設定されます。</span><span class="sxs-lookup"><span data-stu-id="474ac-142">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="474ac-143">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="474ac-143">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```
