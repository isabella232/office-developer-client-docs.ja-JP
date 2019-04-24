---
title: ForeignTable プロパティ (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307048"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="5cb5e-102">ForeignTable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="5cb5e-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="5cb5e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cb5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cb5e-104">リレーションシップに含まれる外部キー側のテーブルの名前を設定または取得します (Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-104">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5cb5e-105">.</span><span class="sxs-lookup"><span data-stu-id="5cb5e-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="5cb5e-106">構文</span><span class="sxs-lookup"><span data-stu-id="5cb5e-106">Syntax</span></span>

<span data-ttu-id="5cb5e-107">*式*。ForeignTable</span><span class="sxs-lookup"><span data-stu-id="5cb5e-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="5cb5e-108">\*式\***Relation**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb5e-109">注釈</span><span class="sxs-lookup"><span data-stu-id="5cb5e-109">Remarks</span></span>

<span data-ttu-id="5cb5e-110">このプロパティは、新しい **[Relation](relation-object-dao.md)** オブジェクトがコレクションに追加されていない場合は値の取得および設定が可能で、 [**Relations**](relations-collection-dao.md) コレクション内の既存の **Relation** オブジェクトの場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="5cb5e-111">**Relation** オブジェクトの **ForeignTable** プロパティの設定値は、外部テーブルまたはクエリを表す **[TableDef](connection-name-property-dao.md)** オブジェクトまたは **[QueryDef](tabledef-object-dao.md)** オブジェクトの **[Name](querydef-object-dao.md)** プロパティの設定値で、 **[Table](relation-table-property-dao.md)** プロパティの設定値は、主テーブルまたはクエリを表す **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値です。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="5cb5e-112">たとえば、ValidParts テーブルに格納された有効な部品コード (フィールド名 PartNo 内) のリストがあり、OrderItem テーブルに部品コードが入力された場合に OrderItem テーブルとのリレーションシップを確立するには、ValidParts テーブルにその部品コードが既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-112">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table.</span></span> <span data-ttu-id="5cb5e-113">このパーツコードが validparts テーブルに存在せず、 **Relation**オブジェクトの**[Attributes](field-attributes-property-dao.md)** プロパティを**dbRelationDontEnforce**に設定していない場合は、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-113">If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="5cb5e-p103">この例では、ValidParts テーブルが主テーブルになるため、 **Relation** オブジェクトの **Table** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **ForeignTable** プロパティが OrderItem に設定されます。 **Relation** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **Name** プロパティおよび **ForeignName** プロパティは、PartNo に設定されます。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-p103">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="5cb5e-116">例</span><span class="sxs-lookup"><span data-stu-id="5cb5e-116">Example</span></span>

<span data-ttu-id="5cb5e-117">次の例では、 **Table**、 **ForeignTable**、および **ForeignName** の各プロパティによる 2 つのテーブル間の **Relation** の条件を定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5cb5e-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
