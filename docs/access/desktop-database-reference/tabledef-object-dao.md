---
title: TableDef オブジェクト (DAO)
TOCTitle: TableDef Object
ms:assetid: 715146b6-c62a-abff-28ee-e6bbe3c08adf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195790(v=office.15)
ms:contentKeyID: 48545582
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef0a7c167321a45249fb022e0987a5f8d6364ea0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476245"
---
# <a name="tabledef-object-dao"></a><span data-ttu-id="96f66-102">TableDef オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="96f66-102">TableDef Object (DAO)</span></span>

<span data-ttu-id="96f66-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="96f66-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="96f66-104">**TableDef** オブジェクトは、ベース テーブルまたはリンク テーブルのストアド定義を表します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="96f66-104">A **TableDef** object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="96f66-105">注釈</span><span class="sxs-lookup"><span data-stu-id="96f66-105">Remarks</span></span>

<span data-ttu-id="96f66-p101">**TableDef** オブジェクトと、そのメソッドおよびプロパティを使用して、テーブル定義を操作できます。たとえば、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="96f66-p101">You manipulate a table definition using a **TableDef** object and its methods and properties. For example, you can:</span></span>

- <span data-ttu-id="96f66-108">データベースの任意のローカル テーブル、リンク テーブル、または外部キー側のテーブルのフィールドおよびインデックス構造を調べます。</span><span class="sxs-lookup"><span data-stu-id="96f66-108">Examine the field and index structure of any local, linked, or external table in a database.</span></span>

- <span data-ttu-id="96f66-109">**Connect** プロパティおよび **SourceTableName** プロパティを使用して、リンク テーブルに関する情報を設定または取得し、 **RefreshLink** メソッドを使用して、リンク テーブルへの接続を更新します。</span><span class="sxs-lookup"><span data-stu-id="96f66-109">Use the **Connect** and **SourceTableName** properties to set or return information about linked tables, and use the **RefreshLink** method to update connections to linked tables.</span></span>

- <span data-ttu-id="96f66-110">**ValidationRule** プロパティおよび **ValidationText** プロパティを使用して、入力検査の条件を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="96f66-110">Use the **ValidationRule** and **ValidationText** properties to set or return validation conditions.</span></span>

- <span data-ttu-id="96f66-111">テーブル –、ダイナセット、ダイナミック –、スナップショット タイプ、または前方のみタイプの**Recordset**オブジェクト、テーブルの定義に基づくを作成するのにには、**何らか**の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="96f66-111">Use the **OpenRecordset** method to create a table–, dynaset–, dynamic–, snapshot–, or forward–only–type **Recordset** object, based on the table definition.</span></span>

<span data-ttu-id="96f66-112">ベース テーブルの場合、 **RecordCount** プロパティには、指定したデータベース テーブルのレコード数が含まれます。</span><span class="sxs-lookup"><span data-stu-id="96f66-112">For base tables, the **RecordCount** property contains the number of records in the specified database table.</span></span> <span data-ttu-id="96f66-113">リンク テーブルは、 **RecordCount**プロパティの設定は常に値が – 1 です。</span><span class="sxs-lookup"><span data-stu-id="96f66-113">For linked tables, the **RecordCount** property setting is always –1.</span></span>

<span data-ttu-id="96f66-114">新しい **TableDef** オブジェクトを作成するには、 **[CreateTableDef](database-createtabledef-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="96f66-114">To create a new **TableDef** object, use the **[CreateTableDef](database-createtabledef-method-dao.md)** method.</span></span>

### <a name="to-add-a-field-to-a-table"></a><span data-ttu-id="96f66-115">テーブルにフィールドを追加するには</span><span class="sxs-lookup"><span data-stu-id="96f66-115">To add a field to a table</span></span>

1.  <span data-ttu-id="96f66-116">テーブルに基づいた **[Recordset](recordset-object-dao.md)** オブジェクトがすべて閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="96f66-116">Make sure any **[Recordset](recordset-object-dao.md)** objects based on the table are all closed.</span></span>

2.  <span data-ttu-id="96f66-117">**CreateField** メソッドを使用して、 **Field** オブジェクト変数を作成し、そのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="96f66-117">Use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

3.  <span data-ttu-id="96f66-118">**Append** メソッドを使用して、 **Field** オブジェクトを **TableDef** オブジェクトの **Fields** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="96f66-118">Use the **Append** method to add the **Field** object to the **Fields** collection of the **TableDef** object.</span></span>

<span data-ttu-id="96f66-119">インデックスが割り当てられていない場合、 **TableDefs** コレクションから **Field** オブジェクトを削除できますが、フィールドのデータが失われます。</span><span class="sxs-lookup"><span data-stu-id="96f66-119">You can delete a **Field** object from a **TableDefs** collection if it doesn't have any indexes assigned to it, but you will lose the field's data.</span></span>

### <a name="to-create-a-table-that-is-ready-for-new-records-in-a-database"></a><span data-ttu-id="96f66-120">データベースの新しいレコードを格納するテーブルを作成するには</span><span class="sxs-lookup"><span data-stu-id="96f66-120">To create a table that is ready for new records in a database</span></span>

1.  <span data-ttu-id="96f66-121">**CreateTableDef** メソッドを使用して、 **TableDef** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="96f66-121">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="96f66-122">そのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="96f66-122">Set its properties.</span></span>

3.  <span data-ttu-id="96f66-123">テーブルのフィールドごとに、 **CreateField** メソッドを使用して、 **Field** オブジェクト変数を作成し、そのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="96f66-123">For each field in the table, use the **CreateField** method to create a **Field** object variable and set its properties.</span></span>

4.  <span data-ttu-id="96f66-124">**Append** メソッドを使用して、フィールドを **TableDef** オブジェクトの **Fields** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="96f66-124">Use the **Append** method to add the fields to the **Fields** collection of the **TableDef** object.</span></span>

5.  <span data-ttu-id="96f66-125">**Append** メソッドを使用して、新しい **TableDef** オブジェクトを **Database** オブジェクトの **TableDefs** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="96f66-125">Use the **Append** method to add the new **TableDef** object to the **TableDefs** collection of the **Database** object.</span></span>

<span data-ttu-id="96f66-126">リンク テーブルは、 **TableDef** オブジェクトの **SourceTableName** プロパティおよび **Connect** プロパティによってデータベースに接続されます。</span><span class="sxs-lookup"><span data-stu-id="96f66-126">A linked table is connected to the database by the **SourceTableName** and **Connect** properties of the **TableDef** object.</span></span>

### <a name="to-link-a-table-to-a-database"></a><span data-ttu-id="96f66-127">テーブルをデータベースにリンクするには</span><span class="sxs-lookup"><span data-stu-id="96f66-127">To link a table to a database</span></span>

1.  <span data-ttu-id="96f66-128">**CreateTableDef** メソッドを使用して、 **TableDef** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="96f66-128">Use the **CreateTableDef** method to create a **TableDef** object.</span></span>

2.  <span data-ttu-id="96f66-129">その **Connect** プロパティおよび **SourceTableName** プロパティ、さらにオプションで **Attributes** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="96f66-129">Set its **Connect** and **SourceTableName** properties (and optionally, its **Attributes** property).</span></span>

3.  <span data-ttu-id="96f66-130">**Append** メソッドを使用して、 **Database** の **TableDefs** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="96f66-130">Use the **Append** method to add it to the **TableDefs** collection of a **Database**.</span></span>

<span data-ttu-id="96f66-131">コレクション内の **TableDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="96f66-131">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="96f66-132">**テーブル定義**(0)</span><span class="sxs-lookup"><span data-stu-id="96f66-132">**TableDefs**(0)</span></span>

<span data-ttu-id="96f66-133">**テーブル定義**("name")</span><span class="sxs-lookup"><span data-stu-id="96f66-133">**TableDefs**("name")</span></span>

<span data-ttu-id="96f66-134">**テーブル**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="96f66-134">**TableDefs**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="96f66-135">例</span><span class="sxs-lookup"><span data-stu-id="96f66-135">Example</span></span>

<span data-ttu-id="96f66-p103">この例では、新しい **TableDef** オブジェクトを作成し、Northwind Database オブジェクトの **TableDefs** コレクションに追加します。次に、 **TableDefs** コレクションおよび新しい **TableDef** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="96f66-p103">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="96f66-138">この例では、Northwind データベースで新しい **TableDef** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="96f66-138">This example creates a new **TableDef** object in the Northwind database.</span></span>

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
         If prpLoop <> "" Then Debug.Print "  " & _ 
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
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
```

<br/>

<span data-ttu-id="96f66-p104">次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。</span><span class="sxs-lookup"><span data-stu-id="96f66-p104">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="96f66-142">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="96f66-142">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```
