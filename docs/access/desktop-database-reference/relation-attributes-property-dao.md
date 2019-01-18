---
title: Relation.Attributes プロパティ (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc6bd5ccc607854ab59de51bdb96d9ceebe1acf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708887"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="a1ad4-102">Relation.Attributes プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1ad4-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="a1ad4-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a1ad4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1ad4-p101">**Relation** オブジェクトの 1 つまたは複数の属性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a1ad4-p101">Sets or returns a value that indicates one or more characteristics of a **Relation** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1ad4-106">構文</span><span class="sxs-lookup"><span data-stu-id="a1ad4-106">Syntax</span></span>

<span data-ttu-id="a1ad4-107">*式*です。属性</span><span class="sxs-lookup"><span data-stu-id="a1ad4-107">*expression* .Attributes</span></span>

<span data-ttu-id="a1ad4-108">\*式\***Relation**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a1ad4-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1ad4-109">注釈</span><span class="sxs-lookup"><span data-stu-id="a1ad4-109">Remarks</span></span>

<span data-ttu-id="a1ad4-110">コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="a1ad4-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="a1ad4-111">例</span><span class="sxs-lookup"><span data-stu-id="a1ad4-111">Example</span></span>

<span data-ttu-id="a1ad4-112">次の例では、Northwind データベースの **Field**、 **Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="a1ad4-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

