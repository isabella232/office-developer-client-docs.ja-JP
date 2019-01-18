---
title: Index.Primary プロパティ (DAO)
TOCTitle: Primary property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: da0d28a5599dadc9432b38ab6155e53e884e4838
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713374"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="885bc-102">Index.Primary プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="885bc-102">Index.Primary property (DAO)</span></span>

<span data-ttu-id="885bc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="885bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="885bc-104">**[Index](index-object-dao.md)** オブジェクトがテーブルの主キー インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="885bc-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="885bc-105">構文</span><span class="sxs-lookup"><span data-stu-id="885bc-105">Syntax</span></span>

<span data-ttu-id="885bc-106">*式*です。プライマリ</span><span class="sxs-lookup"><span data-stu-id="885bc-106">*expression* .Primary</span></span>

<span data-ttu-id="885bc-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="885bc-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="885bc-108">解説</span><span class="sxs-lookup"><span data-stu-id="885bc-108">Remarks</span></span>

<span data-ttu-id="885bc-p101">**Primary** プロパティの設定は、新しい **Index** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Indexes**](indexes-collection-dao.md) コレクション内の既存の **Index** オブジェクトの場合は値の取得のみ可能です。 **Index** オブジェクトが **[TableDef](tabledef-object-dao.md)** オブジェクトに追加されていても、 **TableDef** オブジェクトが **[TableDefs](tabledefs-collection-dao.md)** コレクションに追加されていない場合、 **Index** プロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="885bc-p101">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection. If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="885bc-p102">主キー インデックスは、定義済みの順序で、テーブル内のすべてのレコードを一意に識別する 1 つ以上のフィールドで構成されます。インデックス フィールドは一意にする必要があるため、 [Index](index-unique-property-dao.md) オブジェクトの \*\*\*\*Unique\*\*\*\* プロパティを **True** に設定します。主キー インデックスが複数のフィールドで構成される場合、それぞれのフィールドには重複する値を格納できますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。主キー インデックスはテーブルのキーで構成され、通常、主キーと同じフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="885bc-p102">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order. Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**. If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique. A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>

> [!NOTE]
> <span data-ttu-id="885bc-p103">[!メモ] 必ずしもテーブルにインデックスを作成する必要はありませんが、インデックスを持たない大きなテーブルでは、特定のレコードにアクセスするのに長い時間がかかる場合があります。 [Index](field-attributes-property-dao.md) オブジェクト内にある各 [**Field**](field-object-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティによってレコードの順序が決まり、その結果、そのインデックスに対して使用するアクセス方法が決まります。データベースに新しいテーブルを作成する場合は、各レコードが一意に識別される 1 つ以上のフィールドでインデックスを作成し、 **Index** オブジェクトの **Primary** プロパティを **True** に設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="885bc-p103">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time. The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index. When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the **Primary** property of the **Index** object to **True**.</span></span>

<span data-ttu-id="885bc-118">テーブルの主キーを設定すると、その主キーがテーブルの主キー インデックスとして自動的に定義されます。</span><span class="sxs-lookup"><span data-stu-id="885bc-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="885bc-119">例</span><span class="sxs-lookup"><span data-stu-id="885bc-119">Example</span></span>

<span data-ttu-id="885bc-p104">この例では、 **Primary** プロパティを使用して、新しい **TableDef** オブジェクトの新しい **定数** オブジェクトをそのテーブルの主 **Index** オブジェクトとして指定します。 **Primary** プロパティを **True** に設定すると、 **Unique** プロパティおよび **Required** プロパティも自動的に **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="885bc-p104">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table. Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
