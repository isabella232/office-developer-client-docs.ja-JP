---
title: TableDef.Attributes プロパティ (DAO)
TOCTitle: Attributes Property
ms:assetid: d01588c3-e94e-06bd-6568-974873411f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834701(v=office.15)
ms:contentKeyID: 48547828
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd2acd9675821dfb2b742a6cc344b34833c61ac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881784"
---
# <a name="tabledefattributes-property-dao"></a><span data-ttu-id="b0254-102">TableDef.Attributes プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0254-102">TableDef.Attributes Property (DAO)</span></span>


<span data-ttu-id="b0254-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b0254-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b0254-p101">**TableDef** オブジェクトの 1 つまたは複数の属性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0254-p101">Sets or returns a value that indicates one or more characteristics of a **TableDef** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0254-106">構文</span><span class="sxs-lookup"><span data-stu-id="b0254-106">Syntax</span></span>

<span data-ttu-id="b0254-107">*式*です。属性</span><span class="sxs-lookup"><span data-stu-id="b0254-107">*expression* .Attributes</span></span>

<span data-ttu-id="b0254-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="b0254-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0254-109">注釈</span><span class="sxs-lookup"><span data-stu-id="b0254-109">Remarks</span></span>

<span data-ttu-id="b0254-110">コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="b0254-110">For an object not yet appended to a collection, this property is read/write.</span></span>

## <a name="example"></a><span data-ttu-id="b0254-111">例</span><span class="sxs-lookup"><span data-stu-id="b0254-111">Example</span></span>

<span data-ttu-id="b0254-112">次の例では、Northwind データベースの **Field**、 **Relation**、および **TableDef** の各オブジェクトの **Attributes** プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="b0254-112">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

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

