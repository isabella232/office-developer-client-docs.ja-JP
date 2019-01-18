---
title: Field2.ForeignName プロパティ (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a8368165f73fc52c51cf1503da9c2cc02e969bf4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708369"
---
# <a name="field2foreignname-property-dao"></a><span data-ttu-id="b3f7e-102">Field2.ForeignName プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="b3f7e-102">Field2.ForeignName property (DAO)</span></span>


<span data-ttu-id="b3f7e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3f7e-104">あるリレーションシップにおいて、主テーブルのフィールドに対応する外部キー側のテーブルの **Field2** オブジェクトの名前を指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-104">Sets or returns a value that specifies the name of the **Field2** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f7e-105">構文</span><span class="sxs-lookup"><span data-stu-id="b3f7e-105">Syntax</span></span>

<span data-ttu-id="b3f7e-106">*式*です。ForeignName</span><span class="sxs-lookup"><span data-stu-id="b3f7e-106">*expression* .ForeignName</span></span>

<span data-ttu-id="b3f7e-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f7e-108">注釈</span><span class="sxs-lookup"><span data-stu-id="b3f7e-108">Remarks</span></span>

<span data-ttu-id="b3f7e-p101">**[Relation](relation-object-dao.md)** オブジェクトが **[Database](database-object-dao.md)** に追加されていない状態で、 **Field2** オブジェクトを **Relation** オブジェクトに追加する場合は、 **ForeignName** プロパティは値の取得および設定が可能です。 **Relation** オブジェクトがデータベースに追加されると、 **ForeignName** プロパティは値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field2** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="b3f7e-111">**ForeignName** プロパティをサポートできるのは、 **Relation** オブジェクトの **Fields** コレクションに属している **Field2** オブジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-111">Only a **Field2** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="b3f7e-p102">[Field2](connection-name-property-dao.md) オブジェクトの \*\*\*\*Name\*\*\*\* プロパティおよび **ForeignName** プロパティの設定値は、リレーションシップの主テーブルおよび外部キー側のテーブルの対応するフィールドの名前を指定します。 [Relation](relation-table-property-dao.md) オブジェクトの [**Table**](relation-foreigntable-property-dao.md) プロパティおよび \*\*\*\*ForeignTable\*\*\*\* プロパティの設定値は、リレーションシップの主テーブルおよび外部キー側のテーブルを識別します。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field2** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="b3f7e-p103">たとえば、ValidParts テーブルに有効な部品コード (PartNo という名前のフィールド) の一覧が格納されている場合、OrderItem テーブルに部品コードが入力されるときには、その部品コードが ValidParts テーブルに既に存在している必要があるという、OrderItem テーブルとのリレーションシップを設定できます。部品コードが ValidParts テーブルに存在せず、 [Relation](field-attributes-property-dao.md) オブジェクトの \*\*\*\*Attributes\*\*\*\* プロパティを **dbRelationDontEnforce** に設定していない場合は、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="b3f7e-p104">この場合は、ValidParts テーブルが外部キー側のテーブルであるため、 **Relation** オブジェクトの **ForeignTable** プロパティは ValidParts に設定され、 **Relation** オブジェクトの **Table** プロパティは OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクションに含まれる **Field2** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field2** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="b3f7e-118">例</span><span class="sxs-lookup"><span data-stu-id="b3f7e-118">Example</span></span>

<span data-ttu-id="b3f7e-119">次の例では、 **Table**、 **ForeignTable**、および **ForeignName** の各プロパティによる 2 つのテーブル間の **Relation** の条件を定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b3f7e-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
