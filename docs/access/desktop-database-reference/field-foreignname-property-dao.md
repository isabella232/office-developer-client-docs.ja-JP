---
title: Field.ForeignName プロパティ (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708467"
---
# <a name="fieldforeignname-property-dao"></a><span data-ttu-id="e9266-102">Field.ForeignName プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9266-102">Field.ForeignName property (DAO)</span></span>


<span data-ttu-id="e9266-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e9266-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9266-104">リレーションシップの主テーブルのフィールドに対応する、外部キー側のテーブルの **[Field](field-object-dao.md)** オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e9266-104">Sets or returns a value that specifies the name of the **[Field](field-object-dao.md)** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9266-105">構文</span><span class="sxs-lookup"><span data-stu-id="e9266-105">Syntax</span></span>

<span data-ttu-id="e9266-106">*式*です。ForeignName</span><span class="sxs-lookup"><span data-stu-id="e9266-106">*expression* .ForeignName</span></span>

<span data-ttu-id="e9266-107">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e9266-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9266-108">注釈</span><span class="sxs-lookup"><span data-stu-id="e9266-108">Remarks</span></span>

<span data-ttu-id="e9266-p101">**[Database](relation-object-dao.md)** オブジェクトに **[Relation](database-object-dao.md)** オブジェクトが追加されておらず、 **Relation** オブジェクトに **Field** オブジェクトが追加されている場合、 **ForeignName** プロパティは値の取得および設定が可能です。データベースに **Relation** オブジェクトを追加すると、 **ForeignName** プロパティは値の取得のみ可能になります。</span><span class="sxs-lookup"><span data-stu-id="e9266-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="e9266-111">**Relation** オブジェクトの **Fields** コレクションに属する **Field** オブジェクトのみが、 **ForeignName** プロパティをサポートできます。</span><span class="sxs-lookup"><span data-stu-id="e9266-111">Only a **Field** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="e9266-p102">[Field](connection-name-property-dao.md) オブジェクトの \*\*\*\*Name\*\*\*\* プロパティおよび **ForeignName** プロパティの設定値によって、リレーションシップの主テーブルと外部キー側のテーブル内にある対応するフィールドの名前が指定されます。 [Relation](relation-table-property-dao.md) オブジェクトの [**Table**](relation-foreigntable-property-dao.md) プロパティおよび \*\*\*\*ForeignTable\*\*\*\* プロパティの設定値によって、リレーションシップの主テーブルと外部キー側のテーブルが決まります。</span><span class="sxs-lookup"><span data-stu-id="e9266-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="e9266-p103">たとえば、ValidParts テーブルに格納された有効な部品コード (フィールド名 PartNo 内) のリストがあり、OrderItem テーブルに部品コードが入力された場合に OrderItem テーブルとのリレーションシップを確立するには、ValidParts テーブルにその部品コードが既に存在している必要があります。ValidParts テーブルに部品コードがなく、 [Relation](field-attributes-property-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティが **dbRelationDontEnforce** に設定されていない場合、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e9266-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="e9266-p104">この例では、ValidParts テーブルが外部キー側のテーブルになるため、 **Relation** オブジェクトの **ForeignTable** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **Table** プロパティが OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e9266-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="e9266-118">例</span><span class="sxs-lookup"><span data-stu-id="e9266-118">Example</span></span>

<span data-ttu-id="e9266-119">次の例では、 **Table**、 **ForeignTable**、および **ForeignName** の各プロパティによる 2 つのテーブル間の **Relation** の条件を定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e9266-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
