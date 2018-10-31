---
title: Document オブジェクト (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35d9d80ba9299049eb55ee4ae83ac00d57c22293
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861958"
---
# <a name="document-object-dao"></a><span data-ttu-id="c12ae-102">Document オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="c12ae-102">Document Object (DAO)</span></span>


<span data-ttu-id="c12ae-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c12ae-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c12ae-p101">**Document** オブジェクトには、オブジェクトの 1 つのインスタンスの情報があります。オブジェクトは、データベース、保存されたテーブル、クエリ、またはリレーションシップのいずれかです (Microsoft Access データベース エンジン データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p101">A **Document** object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="c12ae-106">注釈</span><span class="sxs-lookup"><span data-stu-id="c12ae-106">Remarks</span></span>

<span data-ttu-id="c12ae-p102">各 **Container** オブジェクトには、 **Container** オブジェクトで指定された組み込みのオブジェクトのインスタンスを記述する **Document** オブジェクトを含む **Documents** コレクションがあります。次の表に、各 **Document** オブジェクトが記述するオブジェクトの種類、その **Container** オブジェクトの名前、および **Document** オブジェクトに格納されている情報の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p102">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c12ae-109">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c12ae-109">Document</span></span></p></th>
<th><p><span data-ttu-id="c12ae-110">コンテナー</span><span class="sxs-lookup"><span data-stu-id="c12ae-110">Container</span></span></p></th>
<th><p><span data-ttu-id="c12ae-111">格納されている情報</span><span class="sxs-lookup"><span data-stu-id="c12ae-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c12ae-112">データベース</span><span class="sxs-lookup"><span data-stu-id="c12ae-112">Database</span></span></p></td>
<td><p><span data-ttu-id="c12ae-113">Databases</span><span class="sxs-lookup"><span data-stu-id="c12ae-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="c12ae-114">保存されたデータベース</span><span class="sxs-lookup"><span data-stu-id="c12ae-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c12ae-115">テーブルまたはクエリ</span><span class="sxs-lookup"><span data-stu-id="c12ae-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="c12ae-116">Tables</span><span class="sxs-lookup"><span data-stu-id="c12ae-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="c12ae-117">保存されたテーブルまたはクエリ</span><span class="sxs-lookup"><span data-stu-id="c12ae-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c12ae-118">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="c12ae-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="c12ae-119">Relations</span><span class="sxs-lookup"><span data-stu-id="c12ae-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="c12ae-120">保存されたリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="c12ae-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c12ae-p103">[!メモ] 上記の表の **Container** オブジェクトと、同じ名前のコレクションを混同しないでください。Databases の **Container** オブジェクトは、保存されたすべてのデータベース オブジェクトを参照しますが、 **Databases** コレクションは、特定のワークスペースで開いているデータベース オブジェクトのみを参照します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>



<span data-ttu-id="c12ae-123">**Document** オブジェクトを使用すると、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c12ae-123">With a **Document** object, you can:</span></span>

  - <span data-ttu-id="c12ae-124">**Name** プロパティを使用して、ユーザーまたは Microsoft Access データベース エンジンがオブジェクトの作成時に付けた名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

  - <span data-ttu-id="c12ae-125">**Container** プロパティを使用して、 **Document** オブジェクトを含む **Container** オブジェクトの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

  - <span data-ttu-id="c12ae-p104">**Owner** プロパティを使用して、オブジェクトの所有者を設定または取得します。 **Owner** プロパティを設定するには、 **Document** オブジェクトに対する書き込み権限が必要であり、プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p104">Use the **Owner** property to set or return the owner of the object. To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="c12ae-p105">**UserName** プロパティまたは **Permissions** プロパティを使用して、オブジェクトのユーザーまたはグループのアクセス権限を設定または取得します。これらのプロパティを設定するには、 **Document** オブジェクトへの書き込み権限が必要であり、 **UserName** プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p105">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object. To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

  - <span data-ttu-id="c12ae-130">**DateCreated** プロパティを使用して、 **Document** オブジェクトが作成された日時を取得し、 **LastUpdated** プロパティを使用して、最後に変更された日時を取得します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="c12ae-p106">各 **Document** オブジェクトは、既存のオブジェクトに対応しているため、 **Document** オブジェクトを新規作成したり、既存のオブジェクトを削除することはできません。コレクション内の **Document** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="c12ae-p106">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones. To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="c12ae-133">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="c12ae-133">**Documents**(0)</span></span>

  - <span data-ttu-id="c12ae-134">**ドキュメント**(以下「*名前*」)</span><span class="sxs-lookup"><span data-stu-id="c12ae-134">**Documents**("*name*")</span></span>

  - <span data-ttu-id="c12ae-135">**ドキュメント**\!\[*名*\]</span><span class="sxs-lookup"><span data-stu-id="c12ae-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="c12ae-136">例</span><span class="sxs-lookup"><span data-stu-id="c12ae-136">Example</span></span>

<span data-ttu-id="c12ae-137">この例では、Tables コンテナーの **Documents** コレクションを列挙し、次にコレクションの最初の **Document** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<span data-ttu-id="c12ae-138">次の使用例は、 **Owner** プロパティおよび **SystemDB** プロパティを使用して、さまざまな **Document** オブジェクトの所有者を表示します。</span><span class="sxs-lookup"><span data-stu-id="c12ae-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

