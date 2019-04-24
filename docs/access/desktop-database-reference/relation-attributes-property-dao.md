---
title: Relation プロパティ (DAO)
TOCTitle: Attributes Property
ms:assetid: db19d2ad-5965-214c-211d-9a8eb9c3c522
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835337(v=office.15)
ms:contentKeyID: 48548098
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc6bd5ccc607854ab59de51bdb96d9ceebe1acf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309115"
---
# <a name="relationattributes-property-dao"></a><span data-ttu-id="2a6e4-102">Relation プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a6e4-102">Relation.Attributes property (DAO)</span></span>


<span data-ttu-id="2a6e4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a6e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a6e4-104">**Relation**オブジェクトの1つ以上の特性を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="2a6e4-104">Sets or returns a value that indicates one or more characteristics of a **Relation** object.</span></span> <span data-ttu-id="2a6e4-105">値の取得と設定が可能な長整数型 (**Long**) の値です。</span><span class="sxs-lookup"><span data-stu-id="2a6e4-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a6e4-106">構文</span><span class="sxs-lookup"><span data-stu-id="2a6e4-106">Syntax</span></span>

<span data-ttu-id="2a6e4-107">*式*。Attributes</span><span class="sxs-lookup"><span data-stu-id="2a6e4-107">*expression* .Attributes</span></span>

<span data-ttu-id="2a6e4-108">\*式\***Relation**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="2a6e4-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a6e4-109">注釈</span><span class="sxs-lookup"><span data-stu-id="2a6e4-109">Remarks</span></span>

<span data-ttu-id="2a6e4-110">コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="2a6e4-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="2a6e4-111">例</span><span class="sxs-lookup"><span data-stu-id="2a6e4-111">Example</span></span>

<span data-ttu-id="2a6e4-112">この例では、ノースウィンド データベースの **Field**、**Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="2a6e4-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

