---
title: Container オブジェクト (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295633"
---
# <a name="container-object-dao"></a><span data-ttu-id="3d93d-102">Container オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="3d93d-102">Container object (DAO)</span></span>

<span data-ttu-id="3d93d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d93d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d93d-104">**Container** オブジェクトは、同じような種類の **Document** オブジェクトを 1 つにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="3d93d-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d93d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3d93d-105">Remarks</span></span>

<span data-ttu-id="3d93d-p101">各 **Database** オブジェクトには、組み込みの **Container** オブジェクトで構成される 1 つの **Containers** コレクションがあります。アプリケーションでは、独自のドキュメントの種類とそれに対応するコンテナーを定義できますが (Microsoft Access データベース エンジンのデータベースのみ)、これらのオブジェクトが DAO でサポートされているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="3d93d-p101">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects. Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="3d93d-p102">これらの **Container** オブジェクトには、Microsoft Access データベース エンジンで定義されているものもあれば、他のアプリケーションで定義されているものもあります。次の表では、Microsoft Access データベース エンジンで定義されている各 **Container** オブジェクトの名前と、そこに含まれる情報の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="3d93d-p102">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications. The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d93d-110">Container の名前</span><span class="sxs-lookup"><span data-stu-id="3d93d-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="3d93d-111">含まれる情報の内容</span><span class="sxs-lookup"><span data-stu-id="3d93d-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d93d-112">Databases</span><span class="sxs-lookup"><span data-stu-id="3d93d-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="3d93d-113">保存されたデータベース</span><span class="sxs-lookup"><span data-stu-id="3d93d-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d93d-114">テーブル</span><span class="sxs-lookup"><span data-stu-id="3d93d-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="3d93d-115">保存されたテーブルおよびクエリ</span><span class="sxs-lookup"><span data-stu-id="3d93d-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d93d-116">Relations</span><span class="sxs-lookup"><span data-stu-id="3d93d-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="3d93d-117">保存されたリレーションシップ</span><span class="sxs-lookup"><span data-stu-id="3d93d-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3d93d-p103">[!メモ] 上記の表の **Container** オブジェクトと、同じ名前のコレクションを混同しないでください。Databases の **Container** オブジェクトは、保存されたすべてのデータベース オブジェクトを参照しますが、 **Databases** コレクションは、特定のワークスペースで開いているデータベース オブジェクトのみを参照します。</span><span class="sxs-lookup"><span data-stu-id="3d93d-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="3d93d-p104">各 **Container** オブジェクトには、 **Container** オブジェクトで指定された組み込みのオブジェクトのインスタンスを記述する **Document** オブジェクトを含む **Documents** コレクションがあります。 **Container** オブジェクトは、通常、 **Document** オブジェクトに含まれる情報への仲介リンクとして使用します。また、 **Containers** コレクションを使用して、任意の種類のすべての **Document** オブジェクトにセキュリティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d93d-p104">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. You typically use a **Container** object as an intermediate link to the information in the **Document** object. You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="3d93d-123">既存の **Container** オブジェクトを使用すると、以下の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3d93d-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="3d93d-124">**Name** プロパティを使用して、 **Container** オブジェクトのあらかじめ定義された名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d93d-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="3d93d-p105">**Owner** プロパティを使用して、 **Container** オブジェクトの所有者を設定または取得します。 **Owner** プロパティを設定するには、 **Container** オブジェクトに対する権限が必要であり、プロパティを既存の **User** オブジェクトまたは **Group** オブジェクトの名前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d93d-p105">Use the **Owner** property to set or return the owner of the **Container** object. To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="3d93d-127">**Permissions** プロパティおよび **UserName** プロパティを使用して、 **Container** オブジェクトに対するアクセス許可を設定し、これらのアクセス許可設定が、 **Container** オブジェクトの **Documents** コレクション内に作成されるすべての **Document** オブジェクトに継承されます。</span><span class="sxs-lookup"><span data-stu-id="3d93d-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="3d93d-128">**Container** オブジェクトは組み込みのオブジェクトであるため、 **Container** オブジェクトを新規作成したり、既存のオブジェクトを削除することはできません</span><span class="sxs-lookup"><span data-stu-id="3d93d-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="3d93d-129">コレクション内の **Container** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="3d93d-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="3d93d-130">**コンテナー**.0</span><span class="sxs-lookup"><span data-stu-id="3d93d-130">**Containers**(0)</span></span>

- <span data-ttu-id="3d93d-131">**コンテナー**("*name*")</span><span class="sxs-lookup"><span data-stu-id="3d93d-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="3d93d-132">\*\*\*\*\!コンテナー\[*名*\]</span><span class="sxs-lookup"><span data-stu-id="3d93d-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="3d93d-133">例</span><span class="sxs-lookup"><span data-stu-id="3d93d-133">Example</span></span>

<span data-ttu-id="3d93d-134">次の使用例は、Northwind データベースの **Containers** コレクション、およびコレクションに含まれる各 **Container** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="3d93d-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
