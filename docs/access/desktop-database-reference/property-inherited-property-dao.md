---
title: プロパティ継承プロパティ (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf3aef6d04c7d7cc573ec1d6efaca7d5238f5125
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302927"
---
# <a name="propertyinherited-property-dao"></a><span data-ttu-id="6c29b-102">プロパティ継承プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c29b-102">Property.Inherited property (DAO)</span></span>


<span data-ttu-id="6c29b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c29b-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="6c29b-104">基になるオブジェクトから **[Property](property-object-dao.md)** オブジェクトが継承されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6c29b-104">Returns a value that indicates whether a **[Property](property-object-dao.md)** object is inherited from an underlying object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c29b-105">構文</span><span class="sxs-lookup"><span data-stu-id="6c29b-105">Syntax</span></span>

<span data-ttu-id="6c29b-106">*式*。引き継が</span><span class="sxs-lookup"><span data-stu-id="6c29b-106">*expression* .Inherited</span></span>

<span data-ttu-id="6c29b-107">\*式\***Property**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6c29b-107">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c29b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="6c29b-108">Remarks</span></span>

<span data-ttu-id="6c29b-109">定義済みのプロパティを表す組み込みの **Property** オブジェクトの場合、可能な戻り値は **False** のみです。</span><span class="sxs-lookup"><span data-stu-id="6c29b-109">For built-in **Property** objects that represent predefined properties, the only possible return value is **False**.</span></span>

<span data-ttu-id="6c29b-110">**Inherited** プロパティを使用すると、対象のオブジェクトに対してユーザー定義の **Property** オブジェクトが作成されたかどうか、または別のオブジェクトから **Property** オブジェクトが継承されたかどうかを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="6c29b-110">You can use the **Inherited** property to determine whether a user-defined **Property** was created for the object it applies to, or whether the **Property** was inherited from another object.</span></span> <span data-ttu-id="6c29b-111">たとえば、**[QueryDef](querydef-object-dao.md)** オブジェクトに対して新しい **Property** オブジェクトを作成し、**QueryDef** オブジェクトから **[Recordset](recordset-object-dao.md)** オブジェクトを開くとします。</span><span class="sxs-lookup"><span data-stu-id="6c29b-111">For example, suppose you create a new **Property** for a **[QueryDef](querydef-object-dao.md)** object and then open a **[Recordset](recordset-object-dao.md)** object from the **QueryDef** object.</span></span> <span data-ttu-id="6c29b-112">この新しい **Property** オブジェクトは **Recordset** オブジェクトの **[Properties](properties-collection-dao.md)** コレクションの一部となりますが、Property オブジェクトは **Recordset** オブジェクトではなく **QueryDef** オブジェクトに対して作成されたため、**Inherited** プロパティは **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6c29b-112">This new **Property** will be part of the **Recordset** object's **[Properties](properties-collection-dao.md)** collection, and its **Inherited** property will be set to **True** because the property was created for the **QueryDef** object, not the **Recordset** object.</span></span>

## <a name="example"></a><span data-ttu-id="6c29b-113">例</span><span class="sxs-lookup"><span data-stu-id="6c29b-113">Example</span></span>

<span data-ttu-id="6c29b-114">この例では、 **Inherited** プロパティを使用して、ユーザー定義の **Property** オブジェクトが、 **Recordset** オブジェクトに対して作成されたか、または別の基となるオブジェクトに対して作成されたかを調べます。</span><span class="sxs-lookup"><span data-stu-id="6c29b-114">This example use the **Inherited** property to determine if a user-defined **Property** object was created for a **Recordset** object or for some underlying object.</span></span>

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

