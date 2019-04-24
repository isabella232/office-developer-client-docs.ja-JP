---
title: Relation プロパティ (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306994"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="0e9b0-102">Relation プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e9b0-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="0e9b0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e9b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e9b0-p101">**[Relation](relation-object-dao.md)** オブジェクトの主テーブルの名前を示します。これは、 **[TableDef](connection-name-property-dao.md)** オブジェクトまたは **[QueryDef](tabledef-object-dao.md)** オブジェクトの **[Name](querydef-object-dao.md)** プロパティの設定値と同じである必要があります (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-p101">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table. This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9b0-106">構文</span><span class="sxs-lookup"><span data-stu-id="0e9b0-106">Syntax</span></span>

<span data-ttu-id="0e9b0-107">*式*。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-107">*expression* .Table</span></span>

<span data-ttu-id="0e9b0-108">\*式\***Relation**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9b0-109">注釈</span><span class="sxs-lookup"><span data-stu-id="0e9b0-109">Remarks</span></span>

<span data-ttu-id="0e9b0-110">**Table** プロパティの設定は、コレクションにまだ追加されていない新しい **Relation** オブジェクトでは、値の取得および設定が可能で、 [**Relations**](relations-collection-dao.md) コレクションの既存の **Relation** オブジェクトでは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="0e9b0-111">2 つのテーブルまたはクエリのフィールド間のリレーションシップを表す **Relation** オブジェクトを定義するには、**Table** プロパティを **[ForeignTable](relation-foreigntable-property-dao.md)** プロパティと共に使用します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-111">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries.</span></span> <span data-ttu-id="0e9b0-112">**Table** プロパティは、主 **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値に設定し、**ForeignTable** プロパティは、外部 (参照) **TableDef** オブジェクトまたは **QueryDef** オブジェクトの **Name** プロパティの設定値に設定します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-112">Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object.</span></span> <span data-ttu-id="0e9b0-113">**[Attributes](field-attributes-property-dao.md)** プロパティは、2つのオブジェクト間のリレーションシップの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-113">The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="0e9b0-p103">たとえば、有効なパーツ コード (PartNo という名前のフィールド) の一覧が ValidParts テーブルに保存されているとき、OrderItem テーブルとの一対多リレーションシップを確立して、パーツ コードを OrderItem テーブルに入力する場合、ValidParts テーブルにもそのパーツ コードが既に存在している必要があるようにできます。パーツ コードが ValidParts テーブルに存在しておらず、 **Relation** オブジェクトの **Attributes** プロパティを **dbRelationDontEnforce** に設定していない場合は、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="0e9b0-116">この例では、ValidParts テーブルが主テーブルになるため、 **Relation** オブジェクトの **Table** プロパティが ValidParts に設定され、 **Relation** オブジェクトの **ForeignTable** プロパティが OrderItem に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-116">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="0e9b0-117">**Relation**オブジェクトの**[Fields](fields-collection-dao.md)** コレクションに含まれる**[Field](field-object-dao.md)** オブジェクトの**Name**プロパティおよび**ForeignName**プロパティは、partno に設定されています。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-117">The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="0e9b0-118">例</span><span class="sxs-lookup"><span data-stu-id="0e9b0-118">Example</span></span>

<span data-ttu-id="0e9b0-119">次の例では、 **Table**、 **ForeignTable**、および **ForeignName** の各プロパティによる 2 つのテーブル間の **Relation** の条件を定義する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0e9b0-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
