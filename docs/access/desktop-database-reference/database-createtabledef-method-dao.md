---
title: Database.CreateTableDef メソッド (DAO)
TOCTitle: CreateTableDef Method
ms:assetid: d919b44e-ffae-dc4a-f1cc-d01df49987a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835094(v=office.15)
ms:contentKeyID: 48548046
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 99bccffb11dfb9813d52fed721a51b5417ef6be0
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602819"
---
# <a name="databasecreatetabledef-method-dao"></a><span data-ttu-id="18e73-102">Database.CreateTableDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="18e73-102">Database.CreateTableDef Method (DAO)</span></span>

<span data-ttu-id="18e73-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="18e73-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18e73-p101">新しい **[TableDef](tabledef-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="18e73-p101">Creates a new **[TableDef](tabledef-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="18e73-106">構文</span><span class="sxs-lookup"><span data-stu-id="18e73-106">Syntax</span></span>

<span data-ttu-id="18e73-107">*式*です。CreateTableDef (***名前***、***属性***、 ***SourceTableName***、***接続***)</span><span class="sxs-lookup"><span data-stu-id="18e73-107">*expression* .CreateTableDef(***Name***, ***Attributes***, ***SourceTableName***, ***Connect***)</span></span>

<span data-ttu-id="18e73-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="18e73-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="18e73-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18e73-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18e73-110">名前</span><span class="sxs-lookup"><span data-stu-id="18e73-110">Name</span></span></p></th>
<th><p><span data-ttu-id="18e73-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="18e73-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="18e73-112">データ型</span><span class="sxs-lookup"><span data-stu-id="18e73-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="18e73-113">説明</span><span class="sxs-lookup"><span data-stu-id="18e73-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18e73-114">名前</span><span class="sxs-lookup"><span data-stu-id="18e73-114">Name</span></span></p></td>
<td><p><span data-ttu-id="18e73-115">省略可能</span><span class="sxs-lookup"><span data-stu-id="18e73-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="18e73-116"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="18e73-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18e73-p102">新しい <strong>TableDef</strong> オブジェクトの一意の名前を表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。有効な <strong>TableDef</strong> 名の詳細については、<strong><a href="tabledef-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18e73-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18e73-119">属性</span><span class="sxs-lookup"><span data-stu-id="18e73-119">Attributes</span></span></p></td>
<td><p><span data-ttu-id="18e73-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="18e73-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="18e73-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="18e73-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18e73-p103">新しい <strong>TableDef</strong> オブジェクトの 1 つ以上の特性を示す定数 (または定数の組み合わせ)。詳細については、 <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="18e73-p103">A constant or combination of constants that indicates one or more characteristics of the new <strong>TableDef</strong> object. See the <strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18e73-124">SourceTableName</span><span class="sxs-lookup"><span data-stu-id="18e73-124">SourceTableName</span></span></p></td>
<td><p><span data-ttu-id="18e73-125">省略可能</span><span class="sxs-lookup"><span data-stu-id="18e73-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="18e73-126"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="18e73-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18e73-p104">データの元のソースである外部データベースのテーブルの名前を格納している、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。source 文字列は、新しい <strong>TableDef</strong> オブジェクトの <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> プロパティの設定値になります。</span><span class="sxs-lookup"><span data-stu-id="18e73-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) containing the name of a table in an external database that is the original source of the data. The source string becomes the <strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong> property setting of the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18e73-129">ブラウザでの</span><span class="sxs-lookup"><span data-stu-id="18e73-129">Connect</span></span></p></td>
<td><p><span data-ttu-id="18e73-130">省略可能</span><span class="sxs-lookup"><span data-stu-id="18e73-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="18e73-131"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="18e73-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="18e73-p105">開いているデータベース、パススルー クエリで使用されるデータベース、またはリンク テーブルのソースに関する情報を格納している、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。有効な接続文字列の詳細については、<strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18e73-p105">A <strong>Variant</strong> (<strong>String</strong> subtype) containing information about the source of an open database, a database used in a pass-through query, or a linked table. See the <strong><a href="tabledef-connect-property-dao.md">Connect</a></strong> property for more information about valid connection strings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18e73-134"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="18e73-134"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="18e73-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="18e73-135">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="18e73-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="18e73-136">Return value</span></span>
>>>>>>> <span data-ttu-id="18e73-137">master</span><span class="sxs-lookup"><span data-stu-id="18e73-137">master</span></span>

<span data-ttu-id="18e73-138">TableDef</span><span class="sxs-lookup"><span data-stu-id="18e73-138">TableDef</span></span>

## <a name="remarks"></a><span data-ttu-id="18e73-139">解説</span><span class="sxs-lookup"><span data-stu-id="18e73-139">Remarks</span></span>

<span data-ttu-id="18e73-p106">**CreateTableDef** メソッドの使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、一部のプロパティは変更できません。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="18e73-p106">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its properties. See the individual property topics for more details.</span></span>

<span data-ttu-id="18e73-143">名が既にコレクションのメンバーであるオブジェクトを参照を追加する**tabledef オブジェクト**または**[Field](field-object-dao.md)** オブジェクトに無効なプロパティを指定する場合、 **[Append](tabledefs-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="18e73-143">If name refers to an object that is already a member of the collection, or you specify an invalid property in the **TableDef** or **[Field](field-object-dao.md)** object you're appending, a run-time error occurs when you use the **[Append](tabledefs-append-method-dao.md)** method.</span></span> <span data-ttu-id="18e73-144">また、 **TableDef** オブジェクトの **Field** を少なくとも 1 つ定義しないと、 **TableDef** オブジェクトを **TableDefs** コレクションに追加できません。</span><span class="sxs-lookup"><span data-stu-id="18e73-144">Also, you can't append a **TableDef** object to the **TableDefs** collection until you define at least one **Field** for the **TableDef** object.</span></span>

<span data-ttu-id="18e73-145">[**TableDefs**](tabledefs-collection-dao.md) コレクションから **TableDef** オブジェクトを削除するには、コレクションの **[Delete](tabledefs-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="18e73-145">To remove a **TableDef** object from the **[TableDefs](tabledefs-collection-dao.md)** collection, use the **[Delete](tabledefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="18e73-146">例</span><span class="sxs-lookup"><span data-stu-id="18e73-146">Example</span></span>

<span data-ttu-id="18e73-147">この例では、Northwind データベースで新しい **TableDef** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="18e73-147">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb
    Sub CreateTableDefX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create a new TableDef object. 
     Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
     
     With tdfNew 
     ' Create fields and append them to the new TableDef 
     ' object. This must be done before appending the 
     ' TableDef object to the TableDefs collection of the 
     ' Northwind database. 
     .Fields.Append .CreateField("FirstName", dbText) 
     .Fields.Append .CreateField("LastName", dbText) 
     .Fields.Append .CreateField("Phone", dbText) 
     .Fields.Append .CreateField("Notes", dbMemo) 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "before appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     ' Append the new TableDef object to the Northwind 
     ' database. 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new TableDef object " & _ 
     "after appending to collection:" 
     
     ' Enumerate Properties collection of new TableDef 
     ' object. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     ' Delete new TableDef object since this is a 
     ' demonstration. 
     dbsNorthwind.TableDefs.Delete "Contacts" 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="18e73-p108">この例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize** 、 **CacheStart** 、 **SourceTableName** の各プロパティを使用して、リンクされたテーブルのレコードを 2 回列挙します。その後、50 レコードのキャッシュを使用してレコードを 2 回列挙します。さらに、リンクされたテーブルの処理にキャッシュを使用しなかった場合と使用した場合のパフォーマンスの統計を表示します。</span><span class="sxs-lookup"><span data-stu-id="18e73-p108">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

```vb
    Sub ClientServerX3() 
     
     Dim dbsCurrent As Database 
     Dim tdfRoyalties As TableDef 
     Dim rstRemote As Recordset 
     Dim sngStart As Single 
     Dim sngEnd As Single 
     Dim sngNoCache As Single 
     Dim sngCache As Single 
     Dim intLoop As Integer 
     Dim strTemp As String 
     Dim intRecords As Integer 
     
     ' Open a database to which a linked table can be 
     ' appended. 
     Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
     ' Create a linked table that connects to a Microsoft SQL 
     ' Server database. 
     Set tdfRoyalties = _ 
     dbsCurrent.CreateTableDef("Royalties") 
     ' Note: The DSN referenced below must be set to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     tdfRoyalties.Connect = _ 
     "ODBC;DATABASE=pubs;DSN=Publishers" 
     tdfRoyalties.SourceTableName = "roysched" 
     dbsCurrent.TableDefs.Append tdfRoyalties 
     Set rstRemote = _ 
     dbsCurrent.OpenRecordset("Royalties") 
     
     With rstRemote 
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     sngStart = Timer 
     
     For intLoop = 1 To 2 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     .MoveNext 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngNoCache = sngEnd - sngStart 
     
     ' Cache the first 50 records. 
     .MoveFirst 
     .CacheSize = 50 
     .FillCache 
     sngStart = Timer 
     
     ' Enumerate the Recordset object twice and record 
     ' the elapsed time. 
     For intLoop = 1 To 2 
     intRecords = 0 
     .MoveFirst 
     Do While Not .EOF 
     ' Execute a simple operation for the 
     ' performance test. 
     strTemp = !title_id 
     ' Count the records. If the end of the 
     ' cache is reached, reset the cache to the 
     ' next 50 records. 
     intRecords = intRecords + 1 
     .MoveNext 
     If intRecords Mod 50 = 0 Then 
     .CacheStart = .Bookmark 
     .FillCache 
     End If 
     Loop 
     Next intLoop 
     
     sngEnd = Timer 
     sngCache = sngEnd - sngStart 
     
     ' Display performance results. 
     MsgBox "Caching Performance Results:" & vbCr & _ 
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
