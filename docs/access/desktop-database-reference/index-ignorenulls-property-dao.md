---
title: Index.IgnoreNulls プロパティ (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6c306f76e34e24abb5065c627d9325b48c3acead
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708859"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="6780f-102">Index.IgnoreNulls プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6780f-102">Index.IgnoreNulls property (DAO)</span></span>


<span data-ttu-id="6780f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6780f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6780f-104">インデックス フィールドに Null 値を持つレコードがインデックス エントリを持つかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="6780f-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6780f-105">構文</span><span class="sxs-lookup"><span data-stu-id="6780f-105">Syntax</span></span>

<span data-ttu-id="6780f-106">*式*です。IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="6780f-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="6780f-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6780f-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6780f-108">注釈</span><span class="sxs-lookup"><span data-stu-id="6780f-108">Remarks</span></span>

<span data-ttu-id="6780f-109">このプロパティは、新しい **[Index](index-object-dao.md)** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Indexes**](indexes-collection-dao.md) コレクション内の既存の **Index** オブジェクトの場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="6780f-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="6780f-p101">レコードをより短時間で検索するために、フィールドのインデックスを定義できます。インデックス フィールドへの **null** の入力を許可し、多くの入力値が **null** になる場合、 **Index** オブジェクトの **IgnoreNulls** プロパティを **True** に設定すると、インデックスによって使用される記憶域の容量を節約できます。</span><span class="sxs-lookup"><span data-stu-id="6780f-p101">To speed up the process of searching for records, you can define an index for a field. If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="6780f-112">**IgnoreNulls** プロパティの設定および **[Required](field-required-property-dao.md)** プロパティの設定によって、インデックス値が **null** のレコードがインデックス エントリを持つかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="6780f-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6780f-113">IgnoreNulls の値</span><span class="sxs-lookup"><span data-stu-id="6780f-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="6780f-114">Required の値</span><span class="sxs-lookup"><span data-stu-id="6780f-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="6780f-115">結果</span><span class="sxs-lookup"><span data-stu-id="6780f-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6780f-116">True</span><span class="sxs-lookup"><span data-stu-id="6780f-116">True</span></span></p></td>
<td><p><span data-ttu-id="6780f-117">False</span><span class="sxs-lookup"><span data-stu-id="6780f-117">False</span></span></p></td>
<td><p><span data-ttu-id="6780f-118">インデックス フィールドへの Null 値の入力が許可されます。インデックス エントリは追加されません。</span><span class="sxs-lookup"><span data-stu-id="6780f-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6780f-119">False</span><span class="sxs-lookup"><span data-stu-id="6780f-119">False</span></span></p></td>
<td><p><span data-ttu-id="6780f-120">False</span><span class="sxs-lookup"><span data-stu-id="6780f-120">False</span></span></p></td>
<td><p><span data-ttu-id="6780f-121">インデックス フィールドへの Null 値の入力が許可されます。インデックス エントリが追加されます。</span><span class="sxs-lookup"><span data-stu-id="6780f-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6780f-122">True または False</span><span class="sxs-lookup"><span data-stu-id="6780f-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="6780f-123">True</span><span class="sxs-lookup"><span data-stu-id="6780f-123">True</span></span></p></td>
<td><p><span data-ttu-id="6780f-124">インデックス フィールドへの Null 値の入力は許可されません。インデックス エントリは追加されません。</span><span class="sxs-lookup"><span data-stu-id="6780f-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="6780f-125">例</span><span class="sxs-lookup"><span data-stu-id="6780f-125">Example</span></span>

<span data-ttu-id="6780f-126">この例では、新しい **Index** オブジェクトの **IgnoreNulls** プロパティを、ユーザーの入力に基づいて **True** または **False** に設定し、キー フィールドに **Null** 値が含まれているレコードによる **Recordset** オブジェクトへの影響を示します。</span><span class="sxs-lookup"><span data-stu-id="6780f-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
