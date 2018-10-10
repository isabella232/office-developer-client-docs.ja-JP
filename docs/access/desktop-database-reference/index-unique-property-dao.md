---
title: Index.Unique プロパティ (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf2bbd8e1bf5c7c51d93e0669becbfd093e29994
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478908"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="caa36-102">Index.Unique プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="caa36-102">Index.Unique Property (DAO)</span></span>

<span data-ttu-id="caa36-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="caa36-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="caa36-104">**[Index](index-object-dao.md)** オブジェクトがテーブルの固有 (キー) インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="caa36-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="caa36-105">構文</span><span class="sxs-lookup"><span data-stu-id="caa36-105">Syntax</span></span>

<span data-ttu-id="caa36-106">*式*です。一意</span><span class="sxs-lookup"><span data-stu-id="caa36-106">*expression* .Unique</span></span>

<span data-ttu-id="caa36-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="caa36-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa36-108">注釈</span><span class="sxs-lookup"><span data-stu-id="caa36-108">Remarks</span></span>

<span data-ttu-id="caa36-109">このプロパティの設定は、オブジェクトがコレクションに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="caa36-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="caa36-p101">固有インデックスは、固有の定義済み順序で、テーブル内のすべてのレコードを論理的に配列する 1 つ以上のフィールドで構成されます。固有インデックスが 1 つのフィールドで構成される場合は、そのフィールド内の値はテーブル全体で一意である必要があります。固有インデックスが複数のフィールドで構成される場合は、各フィールドでは値の重複が許されますが、インデックスが設定されたすべてのフィールドの値を組み合わせた結果は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="caa36-p101">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order. If the index consists of one field, values in that field must be unique for the entire table. If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="caa36-p102">**Index** オブジェクトの [Unique](index-primary-property-dao.md) プロパティと \*\*\*\*Primary\*\*\*\* プロパティの両方が **True** に設定されている場合、そのインデックスは、固有の主インデックスとなり、定義済みの論理的な順序でテーブル内のすべてのレコードを一意に識別します。 **Primary** プロパティが **False** に設定されている場合、2 次インデックスとなります。2 次インデックス (キーと非キーの両方) は、テーブル内のレコードの識別子としては機能せずに、定義済み順序でレコードを論理的に配列します。</span><span class="sxs-lookup"><span data-stu-id="caa36-p102">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order. If the **Primary** property is set to **False**, the index is a secondary index. Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="caa36-116">テーブルにインデックスを作成する必要はありませんが、テーブルが大きくてインデックスが設定されていない場合、特定のレコードへのアクセス時間が長くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="caa36-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span></P>
> <LI>
> <P><span data-ttu-id="caa36-117">インデックスのないテーブルからレコードを取得する場合、特定の順序でレコードを取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="caa36-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="caa36-118"><A href="field-attributes-property-dao.md">Index</A> オブジェクト内の各 <A href="field-object-dao.md"><STRONG>Field</STRONG></A> オブジェクトの <STRONG><STRONG>Attributes</STRONG></STRONG> プロパティによって、レコードの順序が決まり、したがって該当する <STRONG>Index</STRONG> オブジェクトに使用するアクセス手法が決まります。</span><span class="sxs-lookup"><span data-stu-id="caa36-118">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that <STRONG>Index</STRONG> object.</span></span></P>
> <LI>
> <P><span data-ttu-id="caa36-119">固有インデックスは、レコードの検索を最適化するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="caa36-119">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="caa36-120">インデックスは、ベース テーブルの物理的順序には影響を与えません。特定のインデックスを選択するか、Microsoft Access データベース エンジンで <A href="recordset-object-dao.md">Recordset</A> オブジェクトを作成する際に、テーブル タイプの <STRONG><STRONG>Recordset</STRONG></STRONG> オブジェクトによるレコードへのアクセス方法にのみ影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="caa36-120">Indexes don't affect the physical order of a base table indexes affect only how the records are accessed by the table-type <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> object when a particular index is chosen or when the Microsoft Access database engine creates <STRONG>Recordset</STRONG> objects.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="caa36-121">例</span><span class="sxs-lookup"><span data-stu-id="caa36-121">Example</span></span>

<span data-ttu-id="caa36-p103">次の例では、新しい **Index** オブジェクトの **Unique** プロパティを **True** に設定し、Index オブジェクトを Employees テーブルの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの **Indexes** コレクションと各 **Index** オブジェクトの **Properties** コレクションを列挙します。新しい **Index** オブジェクトでは、 **TableDef** オブジェクトの Country、LastName、FirstName の特定の組み合わせを持つレコードが 1 つのみ許可されます。</span><span class="sxs-lookup"><span data-stu-id="caa36-p103">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table. It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**. The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
