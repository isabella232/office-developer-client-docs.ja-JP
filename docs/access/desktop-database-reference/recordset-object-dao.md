---
title: Recordset オブジェクト (DAO)
TOCTitle: Recordset Object
ms:assetid: 9774232c-e6da-175b-fc7f-ed2ab7908fa0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197799(v=office.15)
ms:contentKeyID: 48546469
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df3b2e8d0d5cba07a826a83098187b911f19a3a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871970"
---
# <a name="recordset-object-dao"></a><span data-ttu-id="bc72c-102">Recordset オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc72c-102">Recordset Object (DAO)</span></span>

<span data-ttu-id="bc72c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bc72c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc72c-104">**Recordset** オブジェクトは、ベース テーブルのレコード、またはクエリの実行結果のレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-104">A **Recordset** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc72c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="bc72c-105">Remarks</span></span>

<span data-ttu-id="bc72c-p101">データベースのデータをレコード レベルで操作するには、 **Recordset** オブジェクトを使用します。DAO オブジェクトを使用する場合は、 **Recordset** オブジェクトを使用してほぼすべてのデータを操作します。すべての **Recordset** オブジェクトは、レコード (行) およびフィールド (列) を使用して構成されます。次の 5 種類の **Recordset** オブジェクトがあります。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p101">You use **Recordset** objects to manipulate data in a database at the record level. When you use DAO objects, you manipulate data almost entirely using **Recordset** objects. All **Recordset** objects are constructed using records (rows) and fields (columns). There are five types of **Recordset** objects:</span></span>

- <span data-ttu-id="bc72c-110">テーブル タイプの Recordset: 1 つのデータベース テーブルのレコードを追加、変更、または削除できるベース テーブルのコード表示形式です (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bc72c-110">Table-type Recordset— representation in code of a base table that you can use to add, change, or delete records from a single database table (Microsoft Access workspaces only).</span></span>

- <span data-ttu-id="bc72c-p102">ダイナセット タイプの Recordset: 更新可能なレコードを持つクエリの結果です。ダイナセット タイプの **Recordset** オブジェクトは、基となっているデータベース テーブルのレコードを追加、変更、または削除できる動的なレコードセットです。ダイナセット タイプの **Recordset** オブジェクトには、データベース内の複数のテーブルのフィールドを含めることができます。このタイプは、ODBC キーセット カーソルに対応します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p102">Dynaset-type Recordset— the result of a query that can have updatable records. A dynaset-type **Recordset** object is a dynamic set of records that you can use to add, change, or delete records from an underlying database table or tables. A dynaset-type **Recordset** object can contain fields from one or more tables in a database. This type corresponds to an ODBC keyset cursor.</span></span>

- <span data-ttu-id="bc72c-p103">スナップショット タイプの Recordset: データの検索やレポートの生成に使用できるレコードセットの静的コピーです。スナップショット タイプの **Recordset** オブジェクトには、データベース内の複数のテーブルのフィールドを含めることができますが、更新はできません。このタイプは、ODBC 静的カーソルに対応します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p103">Snapshot-type Recordset— a static copy of a set of records that you can use to find data or generate reports. A snapshot-type **Recordset** object can contain fields from one or more tables in a database but can't be updated. This type corresponds to an ODBC static cursor.</span></span>

- <span data-ttu-id="bc72c-p104">前方スクロール タイプの Recordset: カーソルが提供されない点を除き、スナップショットと同じ働きをします。レコードのスクロール方向が前方向に限定されます。結果セットのスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。このタイプは、ODBC 前方スクロール カーソルに対応します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p104">Forward-only-type Recordset— identical to a snapshot except that no cursor is provided. You can only scroll forward through records. This improves performance in situations where you only need to make a single pass through a result set. This type corresponds to an ODBC forward-only cursor.</span></span>

- <span data-ttu-id="bc72c-p105">動的タイプの Recordset: 行を返すクエリからレコードを追加、変更、または削除できる 1 つまたは複数のベース テーブルからのクエリの結果セットです。さらに、他のユーザーがベース テーブルで追加、削除、または編集したレコードも **Recordset** オブジェクトに表示されます。このタイプは、ODBC 動的カーソルに対応します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p105">Dynamic-type Recordset— a query result set from one or more base tables in which you can add, change, or delete records from a row-returning query. Further, records other users add, delete, or edit in the base tables also appear in your **Recordset**. This type corresponds to an ODBC dynamic cursor (ODBCDirect workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="bc72c-p106">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="bc72c-127">**何らか**のメソッドの型引数を使用して作成する**レコード セット**オブジェクトの種類を選択できます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-127">You can choose the type of **Recordset** object you want to create using the type argument of the **OpenRecordset** method.</span></span>

<span data-ttu-id="bc72c-128">Microsoft Access ワークスペースでは、利用可能なほとんどの機能を持つ**レコード セット**の種類を作成しようと DAO の種類を指定しない場合は、テーブルで開始します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-128">In a Microsoft Access workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the most functionality available, starting with table.</span></span> <span data-ttu-id="bc72c-129">テーブル タイプが使用できない場合は、ダイナセット タイプ、スナップショット タイプ、最後に前方スクロール タイプの順で **Recordset** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-129">If this type isn't available, DAO attempts a dynaset, then a snapshot, and finally a forward-only type **Recordset** object.</span></span>

<span data-ttu-id="bc72c-130">ODBCDirect ワークスペースでは、型を指定しない場合は、DAO しようと、最も高速なクエリ応答の**レコード セット**の型を作成するのには前方から始まります。</span><span class="sxs-lookup"><span data-stu-id="bc72c-130">In an ODBCDirect workspace, if you don't specify a type, DAO attempts to create the type of **Recordset** with the fastest query response, starting with forward-only.</span></span> <span data-ttu-id="bc72c-131">前方スクロール タイプが使用できない場合は、スナップショット タイプ、ダイナセット タイプ、最後に動的タイプの順で **Recordset** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-131">If this type isn't available, DAO attempts a snapshot, then a dynaset, and finally a dynamic- type **Recordset** object.</span></span>

<span data-ttu-id="bc72c-p109">Microsoft Access ワークスペースで、リンクされていない [**TableDef**](tabledef-object-dao.md) オブジェクトを使用して **Recordset** オブジェクトを作成すると、テーブル タイプの **Recordset** オブジェクトが作成されます。リンク テーブルまたは Microsoft データベース エンジンに接続された ODBC データベースのテーブルでは、ダイナセット タイプまたはスナップショット タイプの **Recordset** オブジェクトのみを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p109">When creating a **Recordset** object using a non-linked **[TableDef](tabledef-object-dao.md)** object in a Microsoft Access workspace, table-type **Recordset** objects are created. Only dynaset-type or snapshot-type **Recordset** objects can be created with linked tables or tables in Microsoft Access database engine-connected ODBC databases.</span></span>

<span data-ttu-id="bc72c-134">新しい **Recordset** オブジェクトは、オブジェクトを開いたときに **Recordsets** コレクションに自動的に追加され、オブジェクトを閉じたときに自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-134">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the object, and is automatically removed when you close it.</span></span>

> [!NOTE]
> <span data-ttu-id="bc72c-p110">[!メモ] **Recordset** オブジェクトを表す変数、および **Recordset** オブジェクトを含む **Database** オブジェクトを使用する場合は、変数の適用範囲または有効期間が同じであることを確認してください。たとえば、 **Recordset** オブジェクトを表すパブリック変数を宣言する場合は、 **Recordset** オブジェクトを含む **Database** オブジェクトもパブリックであるか、または **Static** キーワードを使用して **Sub** または **Function** プロシージャで宣言されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p110">If you use variables to represent a **Recordset** object and the **Database** object that contains the **Recordset**, make sure the variables have the same scope, or lifetime. For example, if you declare a public variable that represents a **Recordset** object, make sure the variable that represents the **Database** containing the **Recordset** is also public, or is declared in a **Sub** or **Function** procedure using the **Static** keyword.</span></span>

<span data-ttu-id="bc72c-p111">**Recordset** オブジェクト変数は必要な数だけ作成できます。異なる **Recordset** オブジェクトでも、競合せずに同じテーブル、クエリ、およびフィールドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p111">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="bc72c-139">ダイナセット、スナップショット タイプ、および前方スクロール タイプの**Recordset**オブジェクトは、ローカル メモリに格納されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-139">Dynaset–, snapshot–, and forward–only–type **Recordset** objects are stored in local memory.</span></span> <span data-ttu-id="bc72c-140">ローカル メモリにデータを格納するための十分な空き領域がない場合、Microsoft データベース エンジンでは、追加データが TEMP ディスク領域に格納されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-140">If there isn't enough space in local memory to store the data, the Microsoft Access database engine saves the additional data to TEMP disk space.</span></span> <span data-ttu-id="bc72c-141">この領域が不足している場合は、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-141">If this space is exhausted, a trappable error occurs.</span></span>

<span data-ttu-id="bc72c-p113">**Recordset** オブジェクトの既定のコレクションは **Fields** コレクションであり、 **[Field](field-object-dao.md)** オブジェクトの既定のプロパティは **[Value](field-value-property-dao.md)** プロパティです。コードを簡略化するには、これらの既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p113">The default collection of a **Recordset** object is the **Fields** collection, and the default property of a **[Field](field-object-dao.md)** object is the **[Value](field-value-property-dao.md)** property. Use these defaults to simplify your code.</span></span>

<span data-ttu-id="bc72c-p114">**Recordset** オブジェクトを作成すると、レコードがある場合はカレント レコードが最初のレコードに配置されます。レコードがない場合は、 **RecordCount** プロパティ設定が 0 になり、 **BOF** プロパティおよび **EOF** プロパティ設定が **True** になります。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p114">When you create a **Recordset** object, the current record is positioned to the first record if there are any records. If there are no records, the **RecordCount** property setting is 0, and the **BOF** and **EOF** property settings are **True**.</span></span>

<span data-ttu-id="bc72c-p115">**MoveNext**、**MovePrevious**、**MoveFirst**、**MoveLast** の各メソッドを使用すると、カレント レコードを再配置できます。前方スクロール タイプの **Recordset** オブジェクトは、**MoveNext** メソッドのみをサポートします。Move メソッドを使用して各レコードを参照する場合 (または **Recordset** を実行する場合) は、**BOF** および **EOF** プロパティを使用して、**Recordset** オブジェクトの開始または終了を確認できます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p115">You can use the **MoveNext**, **MovePrevious**, **MoveFirst**, and **MoveLast** methods to reposition the current record. Forward–only–type **Recordset** objects support only the **MoveNext** method. When using the Move methods to visit each record (or "walk" through the **Recordset**), you can use the **BOF** and **EOF** properties to check for the beginning or end of the **Recordset** object.</span></span>

<span data-ttu-id="bc72c-p116">Microsoft Access ワークスペースで、ダイナセット タイプおよびスナップショット タイプの **Recordset** オブジェクトを使用する場合は、 FindFirst などの **Find** メソッドを使用して、基準に基づいて特定のレコードを検索することもできます。レコードが見つからない場合は、 **NoMatch** プロパティが **True** に設定されます。テーブル タイプの **Recordset** オブジェクトの場合は、 **Seek** メソッドを使用してレコードをスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p116">With dynaset- and snapshot-type **Recordset** objects in a Microsoft Access workspace, you can also use the Find methods, such as **FindFirst**, to locate a specific record based on criteria. If the record isn't found, the **NoMatch** property is set to **True**. For table-type **Recordset** objects, you can scan records using the **Seek** method.</span></span>

<span data-ttu-id="bc72c-152">**Type** プロパティは、作成される **Recordset** オブジェクトの種類を示し、 **Updatable** プロパティはオブジェクトのレコードを変更できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-152">The **Type** property indicates the type of **Recordset** object created, and the **Updatable** property indicates whether you can change the object's records.</span></span>

<span data-ttu-id="bc72c-153">各 **Field** オブジェクトおよび **Index** オブジェクトの名前およびデータ型など、ベース テーブルの構造に関する情報は、 **TableDef** オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="bc72c-153">Information about the structure of a base table, such as the names and data types of each **Field** object and any **Index** objects, is stored in a **TableDef** object.</span></span>

<span data-ttu-id="bc72c-154">コレクション内の **Recordset** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="bc72c-154">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="bc72c-155">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="bc72c-155">**Recordsets**(0)</span></span>

- <span data-ttu-id="bc72c-156">**レコード セット**("name")</span><span class="sxs-lookup"><span data-stu-id="bc72c-156">**Recordsets**("name")</span></span>

- <span data-ttu-id="bc72c-157">**レコード セット**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="bc72c-157">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="bc72c-p117">[!メモ] 同じデータ ソースまたはデータベースから **Recordset** オブジェクトを複数回開いて、 **Recordsets** コレクションに重複する名前を作成できます。 **Recordset** オブジェクトをオブジェクト変数に割り当て、変数名で参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p117">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="bc72c-160">例</span><span class="sxs-lookup"><span data-stu-id="bc72c-160">Example</span></span>

<span data-ttu-id="bc72c-161">次の使用例は、4 種類の **Recordset** オブジェクトを開き、現在の **Recordsets** オブジェクトの Recordsets コレクションを列挙して、各 **Recordsets** オブジェクトの **Database** コレクションを列挙することで、 **Properties** オブジェクトおよび **Recordset** コレクションを示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-161">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstTable As Recordset 
       Dim rstDynaset As Recordset 
       Dim rstSnapshot As Recordset 
       Dim rstForwardOnly As Recordset 
       Dim rstLoop As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
     
          ' Open one of each type of Recordset object. 
          Set rstTable = .OpenRecordset("Categories", _ 
             dbOpenTable) 
          Set rstDynaset = .OpenRecordset("Employees", _ 
             dbOpenDynaset) 
          Set rstSnapshot = .OpenRecordset("Shippers", _ 
             dbOpenSnapshot) 
          Set rstForwardOnly = .OpenRecordset _  
             ("Employees", dbOpenForwardOnly) 
     
          Debug.Print "Recordsets in Recordsets " & _ 
             "collection of dbsNorthwind" 
     
          ' Enumerate Recordsets collection. 
          For Each rstLoop In .Recordsets 
     
             With rstLoop 
                Debug.Print "  " & .Name 
     
                ' Enumerate Properties collection of each 
                ' Recordset object. Trap for any  
                ' properties whose values are invalid in  
                ' this context. 
                For Each prpLoop In .Properties 
                   On Error Resume Next 
                   If prpLoop <> "" Then Debug.Print _ 
                      "    " & prpLoop.Name & _ 
                      " = " & prpLoop 
                   On Error GoTo 0 
                Next prpLoop 
     
             End With 
     
          Next rstLoop 
     
          rstTable.Close 
          rstDynaset.Close 
          rstSnapshot.Close 
          rstForwardOnly.Close 
     
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-p118">この例では、 **OpenRecordset** メソッドを使用して、5 種類の **Recordset** オブジェクトを開き、その内容を表示します。このプロシージャを実行するには、 OpenRecordsetOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="bc72c-p118">This example uses the **OpenRecordset** method to open five different **Recordset** objects and display their contents. The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub OpenRecordsetX() 
     
       Dim wrkAcc As Workspace 
       Dim wrkODBC As Workspace 
       Dim dbsNorthwind As Database 
       Dim conPubs As Connection 
       Dim rstTemp As Recordset 
       Dim rstTemp2 As Recordset 
     
       ' Open Microsoft Access and ODBCDirect workspaces, Microsoft  
       ' Access database, and ODBCDirect connection. 
       Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
       Set wrkODBC = CreateWorkspace("", "admin", "", dbUseODBC) 
       Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
        
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       Set conPubs = wrkODBC.OpenConnection("", , , _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
     
       ' Open five different Recordset objects and display the  
       ' contents of each. 
     
       Debug.Print "Opening forward-only-type recordset " & _ 
          "where the source is a QueryDef object..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "Ten Most Expensive Products", dbOpenForwardOnly) 
       OpenRecordsetOutput rstTemp 
     
       Debug.Print "Opening read-only dynaset-type " & _ 
          "recordset where the source is an SQL statement..." 
       Set rstTemp = dbsNorthwind.OpenRecordset( _ 
          "SELECT * FROM Employees", dbOpenDynaset, dbReadOnly) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the Filter property to retrieve only certain  
       ' records with the next OpenRecordset call. 
       Debug.Print "Opening recordset from existing " & _ 
          "Recordset object to filter records..." 
       rstTemp.Filter = "LastName >= 'M'" 
       Set rstTemp2 = rstTemp.OpenRecordset() 
       OpenRecordsetOutput rstTemp2 
     
       Debug.Print "Opening dynamic-type recordset from " & _ 
          "an ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset( _ 
          "SELECT * FROM stores", dbOpenDynamic) 
       OpenRecordsetOutput rstTemp 
     
       ' Use the StillExecuting property to determine when the  
       ' Recordset is ready for manipulation. 
       Debug.Print "Opening snapshot-type recordset based " & _ 
          "on asynchronous query to ODBC connection..." 
       Set rstTemp = conPubs.OpenRecordset("publishers", _ 
          dbOpenSnapshot, dbRunAsync) 
       Do While rstTemp.StillExecuting 
          Debug.Print "  [still executing...]" 
       Loop 
       OpenRecordsetOutput rstTemp 
     
       rstTemp.Close 
       dbsNorthwind.Close 
       conPubs.Close 
       wrkAcc.Close 
       wrkODBC.Close 
     
    End Sub 
     
    Sub OpenRecordsetOutput(rstOutput As Recordset) 
     
       ' Enumerate the specified Recordset object. 
       With rstOutput 
          Do While Not .EOF 
             Debug.Print , .Fields(0), .Fields(1) 
             .MoveNext 
          Loop 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-164">この例では、動的タイプの **Recordset** オブジェクトを開き、そのレコードを列挙します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-164">This example opens a dynamic-type **Recordset** object and enumerates its records.</span></span>

```vb
    Sub dbOpenDynamicX() 
     
       Dim wrkMain As Workspace 
       Dim conMain As Connection 
       Dim qdfTemp As QueryDef 
       Dim rstTemp As Recordset 
       Dim strSQL As String 
       Dim intLoop As Integer 
     
       ' Create ODBC workspace and open connection to 
       ' SQL Server database. 
       Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
          "admin", "", dbUseODBC) 
           
       ' Note: The DSN referenced below must be configured to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server.     
       Set conMain = wrkMain.OpenConnection("Publishers", _ 
          dbDriverNoPrompt, False, _ 
          "ODBC;DATABASE=pubs;DSN=Publishers") 
           
       ' Open dynamic-type recordset. 
       Set rstTemp = _ 
          conMain.OpenRecordset("authors", _ 
          dbOpenDynamic) 
     
       With rstTemp 
          Debug.Print "Dynamic-type recordset: " & .Name 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !au_lname & ", " & _ 
                !au_fname 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       conMain.Close 
       wrkMain.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-165">この例では、ダイナセット タイプの **Recordset** を開き、フィールドをどの程度更新できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-165">This example opens a dynaset-type **Recordset** and shows the extent to which its fields are updatable.</span></span>

```vb
    Sub dbOpenDynasetX() 
     
       Dim dbsNorthwind As Database 
       Dim rstInvoices As Recordset 
       Dim fldLoop As Field 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstInvoices = _ 
          dbsNorthwind.OpenRecordset("Invoices", dbOpenDynaset) 
     
       With rstInvoices 
          Debug.Print "Dynaset-type recordset: " & .Name 
     
          If .Updatable Then 
             Debug.Print "  Updatable fields:" 
     
             ' Enumerate Fields collection of dynaset-type 
             ' Recordset object, print only updatable 
             ' fields. 
             For Each fldLoop In .Fields 
                If fldLoop.DataUpdatable Then 
                   Debug.Print "    " & fldLoop.Name 
                End If 
             Next fldLoop 
     
          End If 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-166">この例では、前方スクロール タイプの **Recordset** を開き、読み取り専用の特性を示し、 **MoveNext** メソッドを使用して **Recordset** を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-166">This example opens a forward-only-type **Recordset**, demonstrates its read-only characteristics, and steps through the **Recordset** with the **MoveNext** method.</span></span>

```vb 
Sub dbOpenForwardOnlyX() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim fldLoop As Field 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   ' Open a forward-only-type Recordset object. Only the  
   ' MoveNext and Move methods may be used to navigate  
   ' through the recordset. 
   Set rstEmployees = _ 
      dbsNorthwind.OpenRecordset("Employees", _ 
      dbOpenForwardOnly) 
 
   With rstEmployees 
      Debug.Print "Forward-only-type recordset: " & _ 
         .Name & ", Updatable = " & .Updatable 
 
      Debug.Print "  Field - DataUpdatable" 
      ' Enumerate Fields collection, printing the Name and  
      ' DataUpdatable properties of each Field object. 
      For Each fldLoop In .Fields 
         Debug.Print "    " & _ 
            fldLoop.Name & " - " & fldLoop.DataUpdatable 
      Next fldLoop 
 
      Debug.Print "  Data" 
      ' Enumerate the recordset. 
      Do While Not .EOF 
         Debug.Print "    " & !FirstName & " " & _ 
            !LastName 
         .MoveNext 
      Loop 
 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
```

<br/>

<span data-ttu-id="bc72c-167">この例では、スナップショット タイプの **Recordset** を開き、読み取り専用の特性を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-167">This example opens a snapshot-type **Recordset** and demonstrates its read-only characteristics.</span></span>

```vb
    Sub dbOpenSnapshotX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          Debug.Print "Snapshot-type recordset: " & _ 
             .Name 
     
          ' Enumerate the Properties collection of the 
          ' snapshot-type Recordset object, trapping for 
          ' any properties whose values are invalid in  
          ' this context. 
          For Each prpLoop In .Properties 
             On Error Resume Next 
             Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
             On Error Goto 0 
          Next prpLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-168">この例では、テーブル タイプの **Recordset** を開き、 **Index** プロパティを設定し、そのレコードを列挙します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-168">This example opens a table-type **Recordset**, sets its **Index** property, and enumerates its records.</span></span>

```vb
    Sub dbOpenTableX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' dbOpenTable is default. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
     
       With rstEmployees 
          Debug.Print "Table-type recordset: " & .Name 
     
          ' Use predefined index. 
          .Index = "LastName" 
          Debug.Print "  Index = " & .Index 
     
          ' Enumerate records. 
          Do While Not .EOF 
             Debug.Print "    " & !LastName & ", " & _ 
                !FirstName 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="bc72c-169">次の例は、 Seek メソッドを使用して、リンクしたテーブル内のレコードを見つける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-169">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="bc72c-170">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="bc72c-170">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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

<br/>

<span data-ttu-id="bc72c-171">次の例は、パラメーター クエリに基づく Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-171">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="bc72c-172">次の例は、テーブルまたはクエリに基づいて Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-172">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="bc72c-173">次の例は、構造化照会言語 (SQL) ステートメントに基づいて Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-173">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="bc72c-174">次の例は、 FindFirst および FindNext メソッドを使用して、 Recordset 内のレコードを見つける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-174">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="bc72c-175">次の例は、クエリの結果を新しい Microsoft Excel ブックのワークシートにコピーする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bc72c-175">The following example shows how to copy the results of a query to a worksheet in a new Microsoft Excel workbook.</span></span>

```vb
    Public Sub CopyDataFromQuery( _
        xlApp As Excel.Application, _
        strQueryName As String)
    
        ' If the xlApp object exists
        If Not xlApp Is Nothing Then
        
            ' If the Workbook exists
            If xlApp.Workbooks.Count = 1 Then
            
                ' Create Recrodset Object from the Query
                Dim rsQuery As DAO.Recordset
                Set rsQuery = Application.CurrentDb.OpenRecordset(strQueryName)
                
                ' Get the Cells object
                Dim Cells As Object
                Set Cells = xlApp.Workbooks(1).ActiveSheet.Cells
                
                ' Copy the Data from the Query into the Sheet
                Cells.CopyFromRecordset rsQuery
                
            End If
        End If
    
    End Sub
```

